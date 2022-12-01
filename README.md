# Azure RTOS - Additional samples

This repository hosts additional samples for Azure RTOS v6.2.0. For samples based previous releases, you can find them in the [v6.1 branch](https://github.com/azure-rtos/samples/tree/v6.1).

## Embedded IDE samples

You can find Embedded IDE (IAR Workbench and semi's IDE) sample projects in addition to the content in the [Getting Started Guides](https://github.com/azure-rtos/getting-started). Each board-specific sample project contains a series of projects that cover Azure RTOS components (ThreadX, NetX Duo, GUIX, FileX and USBX) as well as samples for connecting to [Azure IoT Hub](https://learn.microsoft.com/azure/iot-hub/), and enable OTA for the device using [Device Update for IoT Hub](https://learn.microsoft.com/azure/iot-hub-device-update/) service. Detailed guide is inlcuded in the file of each devkit.

The following ZIP files can be downloaded from the [release](https://github.com/azure-rtos/samples/releases) associated with this repository or the direct links:

|Company|Devkit|Samples|
|-|-|-|
| Microchip          | [ATSAME54-XPRO](https://www.microchip.com/en-us/development-tool/atsame54-xpro)               | [IAR](https://github.com/azure-rtos/samples/releases/download/v6.2_rel/Azure_RTOS_6.2_ATSAME54-XPRO_IAR_Samples_2021_11_30.zip) / [MPLAB](https://github.com/azure-rtos/samples/releases/download/v6.2_rel/Azure_RTOS_6.2_ATSAME54-XPRO_MPLab_Samples_2022_11_30.zip)                                                                                                                                                                                                                     |
| NXP                | [MIMXRT1060-EVK](https://www.nxp.com/design/development-boards/i-mx-evaluation-and-development-boards/i-mx-rt1060-evaluation-kit:MIMXRT1060-EVKB)              | [IAR](https://github.com/azure-rtos/samples/releases/download/v6.2_rel/Azure_RTOS_6.2_MIMXRT1060_IAR_Samples_2022_11_30.zip) / [MCUXpresso](https://github.com/azure-rtos/samples/releases/download/v6.2_rel/Azure_RTOS_6.2_MIMXRT1060_MCUXpresso_Samples_2022_11_30.zip)                                                                                                                                                                                                                 |                                                                                                                                                                                               |
| STMicroelectronics | [B-L4S5I-IOT01A](https://www.st.com/en/evaluation-tools/b-l4s5i-iot01a.html)              | [IAR](https://github.com/azure-rtos/samples/releases/download/v6.2_rel/Azure_RTOS_6.2_STM32L4+-DISCO_IAR_Samples_2022_11_30.zip) / [STM32CubeIDE](https://github.com/azure-rtos/samples/releases/download/v6.2_rel/Azure_RTOS_6.2_STM32L4+-DISCO_STM32CubeIDE_Samples_2022_11_30.zip)                                                                                                                                                                                                     |
| Renesas | [RX65N RSK]([https://www.st.com/en/evaluation-tools/b-l4s5i-iot01a.html](https://www.renesas.com/us/en/products/microcontrollers-microprocessors/rx-32-bit-performance-efficiency-mcus/rx65n-2mb-starter-kit-plus-renesas-starter-kit-rx65n-2mb))              | [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/v6.2_rel/Azure_RTOS_6.2_Renesas_RX65N_RSK_2MB_e2studio_CCRX_Sample_2022_11_30.zip)                                                                                                                                                                                                |

> NOTE: These zip files are completely self-contained and include appropriate code from the other Azure RTOS repositories. Please refer to the LICENSE.txt file in each ZIP file for licensing requirements.

### User-defined Crypto Ciphersuite

This [guide](./user-defined-ciphersuite.md) demonstrates how to implement user-defined crypto ciphersuite and integrate it with Azure IoT Sample.

## Microsoft Learning samples

Samples for Microsoft Learning courses can be built and run on GitHub Codespaces or Windows using Visual Studio:

https://github.com/Azure-Samples/azure-rtos-learn-samples

## Azure RTOS with Azure Sphere samples

The Azure RTOS and Azure Sphere better together sample can be found at:

https://github.com/Azure-Samples/Azure-RTOS-on-Azure-Sphere-Mediatek-MT3620

This sample demonstrates how Azure Sphere and Azure RTOS are able to run together on the MediaTek MT3620 Development Kit.



