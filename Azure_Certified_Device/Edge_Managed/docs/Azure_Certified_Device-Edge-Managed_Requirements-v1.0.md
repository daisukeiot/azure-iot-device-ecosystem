# Azure Certification Edge Managed 

This document outlines the device specific capabilities that will be represented in the Azure Certified Device catalog. A capability is singular device attribute that may that describes the device. 

## Program Purpose

Edge Managed certification, an incremental certification beyond the seline Azure Certified Device certification, focuses on device management standards for Azure connected devices and for IoT devices running Windows, Linux, or RTOS. Today, this program certification focuses on Edge runtime compatibility for module deployment and management though will continue to grow in the future with additional customer manageability needs. (Previously, this program was identified as the IoT Edge certification program.) 

Edge Managed certification validates IoT Edge runtime compatibility for module deployment and management. This program provides confidence in the management of Azure connected IoT devices.

## Requirements

The Edge Managed certification requires that all requirements from the Azure Certified Device baseline program.  See <https://aka.ms/AzureCertifiedDevice> for more information.

**DPS:  The purpose of test is to check the device implements and supports IoT Hub Device Provisioning Service with one of the three attestation methods**

| **Name**                | AzureReady.DPS                                               |
| ----------------------- | ------------------------------------------------------------ |
| **Target Availability** | Ignite (in preview)                                                |
| **Applies To**          | Any device                                      |
| **OS**                  | Agnostic                                                     |
| **Validation Type**     | Automated                                                    |
| **Validation**          | AICS validates the device code support DPS. **1.** User has to select one of the attestation methods (X.509, TPM and SAS key). **2.** Depending on the attestation method, user needs to take corresponding action such as **a)** Upload X.509 cert to AICS managed DPS scope **b)** Implement SAS key or endorsement key into the device. **3.** Subsequently, user will hit ‘Connect’ button to connect to AICS managed IoT Hub via DPS                                                    |
| **Resources**           |                                                      |
| **Azure Recommended:**     | N/A                                                    |

## IoT Edge

**Edge runtime exists:  The purpose of test is to make sure devices that contains IoT Edge runtime ($edgehub and $edgeagent) are functioning correctly.**

| **Name**                | EdgeManaged.EdgeRT                                               |
| ----------------------- | ------------------------------------------------------------ |
| **Target Availability** | Available now                                                          |
| **Applies To**          | IoT Edge device                                                   |
| **OS**                  | [Tier1 and Tier2 OS](https://docs.microsoft.com/en-us/azure/iot-edge/support)                                                     |
| **Validation Type**     | Automated                                                    |
| **Validation**          | AICS validates the deploy-ability of the installed IoT Edge RT. **1.** User needs to specify specific OS (OS not on the list of Tier1/2 are not accepted) **2.** AICS generates its config.yaml and deploy canonical [simulated temp sensor edge module](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/azure-iot.simulated-temperature-sensor?tab=Overview) **3.** AICS validates that docker compatible container subsystem (Moby) is installed on the device **4.** Test result is determined based on successful deployment of the simulated temp sensor edge module and functionality of docker compatible container subsystem                                                    |
| **Resources**           | **a)** [AICS blog](https://azure.microsoft.com/en-in/blog/expanding-azure-iot-certification-service-to-support-azure-iot-edge-device-certification/), **b)** [Certification steps](https://aka.ms/IoTCertificationsBasics) (has all the additional resources), **c)** [Requirements](https://aka.ms/certfaq) |
| **Azure Recommended:**     | N/A                                                    |

**Edge runtime exists:  The purpose of test is to make sure devices that contains IoT Edge runtime ($edgehub and $edgeagent) are functioning correctly.**                                                              

| **Name**                | EdgeManaged.EdgeRT                                                  |
| ----------------------- | ------------------------------------------------------------ |
| **Target Availability** | Available now                                            |
| **Applies To**          | IoT Edge device                                                   |
| **OS**                  | [Tier1 and Tier2 OS](https://docs.microsoft.com/en-us/azure/iot-edge/support)                                                     |
| **Validation Type**     | Automated                                                    |
| **Validation**          | AICS validates the deploy-ability of the installed IoT Edge RT. **1.** User needs to specify specific OS (OS not on the list of Tier1/2 are not accepted) **2.** AICS generates its config.yaml and deploy canonical [simulated temp sensor edge module](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/azure-iot.simulated-temperature-sensor?tab=Overview) **3.** AICS validates that docker compatible container subsystem (Moby) is installed on the device **4.** Test result is determined based on successful deployment of the simulated temp sensor edge module and functionality of docker compatible container subsystem                                                    |
| **Resources**           | **a)** [AICS blog](https://azure.microsoft.com/en-in/blog/expanding-azure-iot-certification-service-to-support-azure-iot-edge-device-certification/), **b)** [Certification steps](https://aka.ms/IoTCertificationsBasics) (has all the additional resources), **c)** [Requirements](https://aka.ms/certfaq) |
| **Azure Recommended:**     | N/A                                                    |

### Capability Template:

**IoT Edge easy setup:  The purpose of test is to make sure IoT Edge device is easy to set up and preinstalls IoT EdgeRT through physical device validation**

| **Name**                | EdgeManaged.PhysicalDevice                                             |
| ----------------------- | ------------------------------------------------------------ |
| **Target Availability** | Available now (this is currently on halt due to COVID-19)                                            |
| **Applies To**          | IoT Edge device                                                   |
| **OS**                  | [Tier1 and Tier2 OS](https://docs.microsoft.com/en-us/azure/iot-edge/support)                                                     |
| **Validation Type**     | Manual / Lab Verified                                                    |
| **Validation**          | OEM must ship the physical device to IoT administration (HCL). HCL performs manual validation on the physical device to check: **1.** EdgeRT is using Moby subsystem (allowed redist version). Not docker **2.** Pick the latest edge module to re-validate edge module deploy-ability                                                    |
| **Resources**           | **a)** [AICS blog](https://azure.microsoft.com/en-in/blog/expanding-azure-iot-certification-service-to-support-azure-iot-edge-device-certification/), **b)** [Certification steps](https://aka.ms/IoTCertificationsBasics) (has all the additional resources), **c)** [Requirements](https://aka.ms/certfaq) |
| **Azure Recommended:**     | N/A                                                    |

**IoT Edge easy setup:  The purpose of test is to make sure IoT Edge device is easy to set up and preinstalls IoT EdgeRT through physical device validation**

| **Name**                | EdgeManaged.PhysicalDevice                                             |
| ----------------------- | ------------------------------------------------------------ |
| **Target Availability** | Available now (this is currently on halt due to COVID-19)                                            |
| **Applies To**          | IoT Edge device                                                   |
| **OS**                  | [Tier1 and Tier2 OS](https://docs.microsoft.com/en-us/azure/iot-edge/support)                                                     |
| **Validation Type**     | Manual / Lab Verified                                                    |
| **Validation**          | OEM must ship the physical device to IoT administration (HCL). HCL performs manual validation on the physical device to check: **1.** EdgeRT is using Moby subsystem (allowed redist version). Not docker **2.** Pick the latest edge module to re-validate edge module deploy-ability                                                    |
| **Resources**           | **a)** [AICS blog](https://azure.microsoft.com/en-in/blog/expanding-azure-iot-certification-service-to-support-azure-iot-edge-device-certification/), **b)** [Certification steps](https://aka.ms/IoTCertificationsBasics) (has all the additional resources), **c)** [Requirements](https://aka.ms/certfaq) |
| **Azure Recommended:**     | N/A                                                    |