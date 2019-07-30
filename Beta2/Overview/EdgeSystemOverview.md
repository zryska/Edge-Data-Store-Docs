---
uid: edgeSystemOverview
---

# Edge System overview

Edge System is a cross-platform component based application framework that is designed to host connectivity components (adapters such as Modbus TCP and OPC UA), and other components such as Storage. In the future, the same framework will be used to host other adapters.

## Configuring Edge System

Edge System hosts other components. While the initial release of Edge System includes Modbus TCP, OPC UA, and Storage components, they are only active if the system is configured to use them. The System itself has a relatively small configuration surface area - the list of components and the HTTP Port used for REST calls.

### System_Port.json

System_Port.json specifies the port on which the System is listening for REST API calls. The same port is used for configuration and for writing data to OMF and SDS. The default configuration port is 5590. The default System_Port.json file installed is:

```json
{
  "Port": 5590
}
```

Allowable ports are in the range of 1024-65535. Before you change the default, ensure that no other service or application on the computer running Edge System is using that port - only one application or service can use a port. You must restart Edge System if you change the port number through the REST API or the command line.

### System_Components.json

Following is the minimum System_Components.json file for the System. The Storage component is required for this initial release for the System to run. With later releases of Edge System, the storage component may not be required.

```json
[
  {
    "ComponentId": "Storage",
    "ComponentType": "EDS.Component"
  }
]
```

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

You can add additional Modbus TCP and OPC UA components if you want, but only a single Storage component is supported. In Beta 2, you must restart the system must if you add or delete a component using the REST API or the command line.
