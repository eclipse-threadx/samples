# Azure RTOS - Additional samples

This repository hosts additional samples for Azure RTOS.

## Embedded IDE samples

You can find Embedded IDE (IAR Workbench and semi's IDE) sample projects in addition to the content in the [getting-started repository](https://github.com/azure-rtos/getting-started). Each board-specific sample project contains a series of projects that cover Azure RTOS components (ThreadX, NetX Duo, GUIX, FileX and USBX) as well as connecting to Azure IoT samples using Azure IoT Middleware for Azure RTOS depending on the actual capability of the board.

The following ZIP files can be downloaded from the [release](https://github.com/azure-rtos/samples/releases) associated with this repository or the direct links:

|Company|Devkit|Samples|
|-|-|-|
|Microchip|ATSAME54-XPRO    |[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_ATSAME54-XPRO_IAR_Samples_2021_11_03.zip) / [MPLAB](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_ATSAME54-XPRO_MPLab_Samples_2021_11_03.zip)|
|NXP|MIMXRT1060-EVK|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_MIMXRT1060_IAR_Samples_2021_11_03.zip) / [MCUXpresso](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_MIMXRT1060_MCUXpresso_Samples_2021_11_03.zip)|
|STMicroelectronics|STM32F746G DISCO|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_STM32F746G-DISCO_IAR_Samples_2021_11_03.zip) / [STM32CubeIDE](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_STM32F746G-DISCO_STM32CubeIDE_Samples_2021_11_03.zip)|
|STMicroelectronics|B-L4S5I-IOT01A|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_STM32L4+-DISCO_IAR_Samples_2021_11_03.zip) / [STM32CubeIDE](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_STM32L4+-DISCO_STM32CubeIDE_Samples_2021_11_03.zip)|
|STMicroelectronics|B-U585I-IOT02A|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_B-U585I-IOT02A_IAR_Samples_Beta_2021_10_01.zip)|
|Renesas|RX65N Cloud Kit|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX65N_Cloud_Kit_IAR_Samples_2022_05_25.zip) / [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX65N_Cloud_Kit_E2Studio_CCRX_Samples_2022_05_25.zip) / [e² studio GNURX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX65N_Cloud_Kit_E2Studio_GNURX_Samples_2022_05_25.zip)|
|Renesas|RZA1 RSK|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RZA1_RSK_IAR_Samples_2021_04_28.zip) / [e² studio](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RZA1_RSK_E2Studio_2021_01_08.zip)|
|Renesas|RX130 Target Board|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX130_Target_Board_IAR_Samples_2021_09_16.zip) / [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX130_Target_Board_e2studio_ccrx_Samples_2021_09_16.zip) / [e² studio GNURX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX130_Target_Board_e2studio_gnurx_Samples_2021_09_16.zip)|
|Renesas|RX65N RSK|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RX65N_RSK_2MB_IAR_Sample_2021_11_19.zip) / [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RX65N_RSK_2MB_e2studio_CCRX_Sample_2021_11_19.zip) / [e² studio GNURX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RX65N_RSK_2MB_e2studio_gnurx_Sample_2021_11_19.zip)|
|Renesas|RSK RX66T|[e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RSK_RX66T_E2Studio_CCRX_Samples_2021_09_07.zip) / [e² studio GNURX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RSK_RX66T_E2Studio_GNURX_Samples_2021_09_07.zip)|
|Renesas|RX671 RSK|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RX671_RSK_IAR_Samples_2021_09_30.zip) / [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RX671_RSK_e2studio_ccrx_Samples_2021_09_30.zip) / [e² studio GNURX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_Renesas_RX671_RSK_e2studio_gnurx_Samples_2021_09_30.zip)|
|Renesas|RX72N Envision Kit Ethernet|[IAR](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX72N_Envision_Kit_Ethernet_IAR_Samples_2021_08_18.zip) / [e² studio CCRX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX72N_Envision_Kit_Ethernet_e2studio_ccrx_Samples_2021_08_18.zip) / [e² studio GNURX](https://github.com/azure-rtos/samples/releases/download/v6.1_rel/Azure_RTOS_6.1_RX72N_Envision_Kit_Ethernet_e2studio_gnurx_Samples_2021_08_18.zip)|

> NOTE: These zip files are completely self-contained and include appropriate code from the other Azure RTOS repositories. Please refer to the LICENSE.txt file in each ZIP file for licensing requirements.

The [MXChip AZ3166 IoT DevKit](https://aka.ms/iot-devkit) is currently supported by the [getting-started](https://github.com/azure-rtos/getting-started/tree/master/MXChip/AZ3166) guide.

## Microsoft Learning samples

Samples for Microsoft Learning courses can be built and run on GitHub Codespaces or Windows using Visual Studio:

https://github.com/Azure-Samples/azure-rtos-learn-samples

## Azure RTOS with Azure Sphere samples

The Azure RTOS and Azure Sphere better together sample can be found at:

https://github.com/Azure-Samples/Azure-RTOS-on-Azure-Sphere-Mediatek-MT3620

This sample demonstrates how Azure Sphere and Azure RTOS are able to run together on the MediaTek MT3620 Development Kit.
