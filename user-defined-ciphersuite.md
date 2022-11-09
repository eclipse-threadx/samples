# User-defined Crypto Ciphersuite Used by Azure IoT Sample

## Introduction

[Azure RTOS NetX Crypto](https://learn.microsoft.com/azure/rtos/netx/netx-crypto/chapter1) is the default crypto ciphersuite used by [Azure RTOS NetX Secure](https://learn.microsoft.com/azure/rtos/netx-duo/netx-secure-tls/chapter1) TLS stack in [Azure IoT Sample](https://github.com/azure-rtos/samples). If clients want to use different crypto algorithm implementation, such as hardware security engine, TF-M PSA, or PKCS#11 based crypto methods, this user guide will show how to implement user-defined crypto ciphersuite and integrate it with Azure IoT Sample.

## General Process

There are four steps to implement and utilize a user-defined crypto ciphersuite.

1. Declare a [NX_CRYPTO_METHOD](https://github.com/azure-rtos/netxduo/blob/master/crypto_libraries/inc/nx_crypto.h#L320) struct for your crypto algorithm, which contains initialization, cleanup and crypto operations function pointers for the crypto method in use.

2. Define initialization, cleanup and crypto operation functions for this crypto method.
   
3. Define a struct to save meta data such as scrtch buffer, algotithm id, etc, which will be passed into above functions as as input parameter.

4. Add this newly defined `NX_CRYPTO_METHOD` into tls crypto array `_nx_azure_iot_tls_supported_crypto[]`, which will be automatically initialized during tls session creation and then utilized by NetX Secure TLS stack.

## Example

[The STMicroelectronics B-U585I-IOT02A sample project](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_B-U585I-IOT02A_IAR_Samples_Beta_2021_10_01.zip) implements [TF-M PSA](https://www.trustedfirmware.org/projects/tf-m/) based ECDSA crypto ciphersuite for TLS device authentication. We will use it an an example to demonstrate the above process.

All the changed files are under the path *B-U585I-IOT02A\Projects\B-U585I-IOT02A\Applications\TFM\TFM_Appli\NonSecure\Projects\B-U585I-IOT02A\Applications\TFM\TFM_Appli\NonSecure*.

1. In *psa_crypto_ciphersuites/nx_crypto_psa_crypto_ciphersuites.c*, declare NX_CRYPTO_METHOD struct `crypto_method_ecdsa_psa_crypto` for PSA based ECDSA crypto method.

```c
NX_CRYPTO_METHOD crypto_method_ecdsa_psa_crypto =
{
    NX_CRYPTO_DIGITAL_SIGNATURE_ECDSA,           /* ECDSA crypto algorithm   name     */
    0,                                           /* Key size in bits                       */
    0,                                           /* IV size in bits                        */
    0,                                           /* ICV size in bits, not used             */
    0,                                           /* Block size in bytes                    */
    sizeof(NX_CRYPTO_ECDSA_PSA_CRYPTO),                 /* Metadata size in bytes                 */
    _nx_crypto_method_ecdsa_psa_crypto_init,            /* ECDSA initialization routine           */
    _nx_crypto_method_ecdsa_psa_crypto_cleanup,         /* ECDSA cleanup routine                  */
    _nx_crypto_method_ecdsa_psa_crypto_operation,       /* ECDSA operation                        */
};
```

2. In *psa_crypto_ciphersuites/nx_crypto_ecdsa_psa_crypto.c*, define initialization, cleanup and crypto operations for this crypto method.
- `_nx_crypto_method_ecdsa_psa_crypto_init()` for parameter check and metadata initialization;
- `_nx_crypto_method_ecdsa_psa_crypto_cleanup()` for metadata clean up;
- `_nx_crypto_method_ecdsa_psa_crypto_operation()` to perform ECDSA operations, including ECDSA signature, verify, EC curve setting, with [PSA crypto APIs](https://armmbed.github.io/mbed-crypto/html/index.html).

3. In *psa_crypto_ciphersuites/nx_crypto_ecdsa_psa_crypto.h*, define a struct `NX_CRYPTO_ECDSA_PSA_CRYPTO` to save metadata used by crypto functions, such as scrtch buffer, psa key handle, etc.

4. In *Src/nx_azure_iot_ciphersuites.c*, add this newly defined NX_CRYPTO_METHOD `crypto_method_ecdsa_psa_crypto` into `_nx_azure_iot_tls_supported_crypto[]`.

```c
const NX_CRYPTO_METHOD *_nx_azure_iot_tls_supported_crypto[] =
{
    &crypto_method_hmac,
    &crypto_method_hmac_sha256,
    &crypto_method_tls_prf_sha256,
    &crypto_method_sha256,
    &crypto_method_aes_cbc_128,
    &crypto_method_rsa,
#ifdef NX_SECURE_ENABLE_ECC_CIPHERSUITE
#ifdef ENABLE_PSA_CRYPTO_CIPHERSUITES
    &crypto_method_ecdsa_psa_crypto,    /* PSA based ECDSA crypto method */
#else
    &crypto_method_ecdsa,
#endif
    &crypto_method_ecdhe,
    &crypto_method_ec_secp384,
    &crypto_method_ec_secp256,
#endif /* NX_SECURE_ENABLE_ECC_CIPHERSUITE */
};
```

With these changes, the user-defined PSA based ECDSA crypto method will be used by NX secure TLS stack in Azure IoT Sample.
