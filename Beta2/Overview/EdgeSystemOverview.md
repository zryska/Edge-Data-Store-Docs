---
uid: edgeSystemOverview
---

# Edge System overview

Edge System is a cross-platform component based application framework that is designed to host connectivity components (adapters such as Modbus TCP and OPC UA), and other components such as Storage. In the future, the same framework will be used to host other adapters.

## Configuring Edge System

Edge System hosts other components. While the initial release of Edge System includes Modbus TCP, OPC UA, and Storage components, they are only active if the system is configured to use them. The system itself has a relatively small configuration surface area - the list of components and the HTTP Port used for REST calls.

Edge System is a cross-platform component based application framework that is designed to host connectivity components (adapters such as Modbus TCP and OPC UA), and other components such as Storage. In the future the same framework will be used to host other adapters.

## Installation of the Edge System

The Edge System can be installed on both Linux and Windows: [Edge System Installation Overview](xref:installationOverview).

## Data Ingress to the Edge System

The Edge System can store (ingress) data in a number of ways. There are two built-in adapters - [Modbus](xref:modbusQuickStart) and [OPC UA](xref:opcUaQuickStart). In addition data can be ingressed using OSIsoft Message Format [(OMF)](xref:omfQuickStart) and the Sequential Data Store [SDS](xref:sdsWritingData) REST APIs.

The Modbus and OPC UA adapters require additional configuration of data source and data selection before they will collect data in the Edge System. For OMF data ingress, once the Edge System is installed OMF ingress can be started with no further configuration steps.

Allowable ports are in the range of 1024-65535. Before you change the default, ensure that no other service or application on the computer running Edge System is using that port - only one application or service can use a port. You must restart Edge System if you change the port number through the REST API or the command line.

The Edge System is composed of components and is designed to allow the addition at a later date of additional adapters. Edge System Beta 2 comes pre-configured with one Modbus and one OPC UA adapter. This behavior will change in the final release.

## Local Data Read and Write Access

Following is the minimum System_Components.json file for the System. The Storage component is required for this initial release for the System to run. With later releases of Edge System, the storage component may not be required.  

All data in the Edge System storage can be accessed using the Sequential Data Store [SDS](xref:sdsQuickStart) REST API.

## Data Egress from the Edge System

The default System_Components.json for Beta 2 is given below. It includes three components - Storage, a single Modbus TCP adapter (Modbus1), a single OPC UA adapter (OpcUa1), and a Storage component (EDS.Component).

 ```json
[
  {
    "ComponentId": "OpcUa1",
    "ComponentType": "OpcUa"
  },
  {
    "ComponentId": "Modbus1",
    "ComponentType": "Modbus"
  },
  {
    "ComponentId": "Storage",
    "ComponentType": "EDS.Component"
  }
]
 ```

You can add additional Modbus TCP and OPC UA components if you want, but only a single Storage component is supported. In Beta 2, you must restart the system if you add or delete a component using the REST API or the command line.

The Edge System can send data on to both the PI Data Archive (using [PI Web API](xref:piEgressQuickStart)) and OSIsoft Cloud Services ([OCS](xref:ocsEgressQuickStart)).

Additional configuration is necessary to send data to both OCS and PI Web API after the Edge System is installed.