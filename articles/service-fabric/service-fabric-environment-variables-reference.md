---
title: Azure Service Fabric environment variables 
description: Learn about environment variables in Azure Service Fabric. Contains a reference of a full list of variables and their uses.
ms.topic: reference
ms.author: tomcassidy
author: tomvcassidy
ms.service: azure-service-fabric
services: service-fabric
ms.date: 07/14/2022
# Customer intent: "As a developer using Azure Service Fabric, I want to understand the environment variables available for my service instances, so that I can effectively configure and troubleshoot my applications."
---

# Service Fabric environment variables

Service Fabric has built-in environment variables set for each service instance. The full list of environment variables is below:

| Environment Variable                         | Description                                                            | Example                                                              |
|----------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------|
| Fabric_ApplicationName                       | The fabric uri name of the application                                 | fabric:/MyApplication                                                |
| Fabric_CodePackageName                       | The name of the code package to which the process belongs              | Code                                                                 |
| Fabric_Endpoint\_IPOrFQDN\_*ServiceEndpointName*     | The ip address or FQDN of the endpoint                                 | 10.0.0.1                                                     |
| Fabric\_Endpoint\_*ServiceEndpointName*              | Port number for the endpoint                                  | 8234                                                                 |
| Fabric_Folder_App_Log                        | Log folder                                                             | C:\\\\Data\\\\_App\\\\_Node_0\\\\MyApplicationType_App12\\\\log      |
| Fabric_Folder_App_Temp                       | Temp folder                                                            | C:\\\\Data\\\\_App\\\\_Node_0\\\\MyApplicationType_App12\\\\temp     |
| Fabric_Folder_App_Work                       | Work folder                                                            | C:\\\\Data\\\\_App\\\\_Node_0\\\\MyApplicationType_App12\\\\work     |
| Fabric_Folder_Application                    | The applications home folder                                           | C:\\\\Data\\\\_App\\\\_Node_0\\\\MyApplicationType_App12             |
| Fabric_IsContainerHost                       | A bool specifying whether the process is a container                   | false                                                                |
| Fabric_NodeId                                | The node ID of the node running the process                            | bf865279ba277deb864a976fbf4c200e                                     |
| Fabric_NodeIPOrFQDN                          | The IP or FQDN of the node, as specified in the cluster manifest file. | localhost or 10.0.0.1                                                |
| Fabric_NodeName                              | The node name of the node running the process                          | _Node_0                                                              |
| Fabric_ServiceName                           | The fabric uri name of the service, if service is hosted in ExclusiveProcess mode. This variable value is only available if you create the service with ServicePackageActivationMode ExclusiveProcess.  | fabric:/MyApplication/MyService                                               |
| Fabric_ServicePackageActivationId            | The ServicePackageActivationId                                         | A GUID                                                               |
| Fabric_ServicePackageName                    | Name of the service package the process is part of                     | Web1Pkg                                                              |

Internal Environment Variables Used by Service Fabric Runtime:

- Fabric_ApplicationHostId
- Fabric_ApplicationHostType
- Fabric_ApplicationId
- Fabric_CodePackageInstanceId
- Fabric_CodePackageInstanceSeqNum
- Fabric_InstanceId
- Fabric_ReplicaId
- Fabric_RuntimeConnectionAddress
- Fabric_ServicePackageActivationGuid
- Fabric_ServicePackageInstanceId
- Fabric_ServicePackageInstanceSeqNum
- Fabric_ServicePackageVersionInstance
- FabricActivatorAddress
- FabricPackageFileName
- HostedServiceName
