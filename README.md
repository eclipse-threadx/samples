# Azure RTOS - Additional samples

This repository hosts additional samples for Azure RTOS.

For this branch, it contains samples for [Device Update for IoT Hub](https://docs.microsoft.com/azure/iot-hub-device-update/understand-device-update) (public preview refresh). For all other samples you can go to the [main](https://github.com/azure-rtos/samples) branch.

To learn more about the Device Update agent within Azure RTOS NetX Duo, it can be found on the [feature/adu](https://aka.ms/azrtos-device-update-preview) branch.

## Embedded IDE samples

You can find Embedded IDE (IAR Workbench and semi's IDE) sample projects in addition to the content in the [getting-started repository](https://github.com/azure-rtos/getting-started). Each board-specific sample project contains the code and docs about using Device Update for IoT Hub on it.

The following ZIP files can be downloaded from the [release](https://github.com/azure-rtos/samples/releases) associated with this repository or the direct links:

|Company|Devkit|Samples|
|-|-|-|
| Microchip | ATSAME54-XPRO | [IAR](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta_refresh/Azure_RTOS_6.1_ADU_ATSAME54-XPRO_IAR_Sample_2022_04_10.zip) / [MPLAB](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta_refresh/Azure_RTOS_6.1_ADU_ATSAME54-XPRO_MPLab_Sample_2022_04_10.zip)|
| NXP | MIMXRT1060-EVK| [IAR](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta_refresh/Azure_RTOS_6.1_ADU_MIMXRT1060_IAR_Sample_2022_04_10.zip) / [MCUXpresso](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta_refresh/Azure_RTOS_6.1_ADU_MIMXRT1060_MCUXpresso_Sample_2022_04_10.zip) |
| STMicroelectronics | B-L4S5I-IOT01A | [IAR](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta_refresh/Azure_RTOS_6.1_ADU_STM32L4+-DISCO_IAR_Sample_2022_04_10.zip) / [STM32CubeIDE](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta_refresh/Azure_RTOS_6.1_ADU_STM32L4+-DISCO_STM32CubeIDE_Sample_2022_04_10.zip) |
| Renesas | RX65N RSK 2MB | [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta_refresh/Azure_RTOS_6.1_ADU_Renesas_RX65N_RSK_2MB_e2studio_CCRX_Sample_2022_04_10.zip) |
| Renesas | RX671 RSK | [IAR](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta/Azure_RTOS_6.1_ADU_Renesas_RX671_RSK_IAR_Samples_2022_03_17.zip) / [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta/Azure_RTOS_6.1_ADU_Renesas_RX671_RSK_e2studio_ccrx_Samples_2022_03_17.zip) / [e² studio GNURX](https://github.com/azure-rtos/samples/releases/download/rel_6.1_adu_beta/Azure_RTOS_6.1_ADU_Renesas_RX671_RSK_e2studio_gnurx_Sample_2022_03_17.zip)| 

> NOTE: These zip files are completely self-contained and include appropriate code from the other Azure RTOS repositories. All samples are currently using `v6.1.10` code base. Please refer to the LICENSE.txt file in each ZIP file for licensing requirements.
