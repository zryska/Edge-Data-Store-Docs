---
uid: edgeSystemConfiguration
---

# Edge System configuration
You use JSON files stored in a protected directory on Linux or Windows to configure Edge System. While the files are accessible to view, it is recommended that you use REST for any changes you make to the files. As part of making Edge System as secure as possible, any passwords or secrets that are configured will be stored in encrypted form (with cryptographic key material stored separately in a secure location.) If the files are edited directly, the system may not work as expected. Configuration of the system can also be accomplished using the command line if desired, but since REST is the primary means of interacting with Edge Storage functionality, REST is the recommended technique for configuring the system.

**Note:** It is possible to edit any single component or facet of the system using REST, but it is also possible to configure the system as a whole with a single REST call.

## Configuring the Edge System

The Edge System hosts other components. While the initial release of the Edge System includes Modbus, Opc Ua, and Storage components, they are only active if the system is configured to use them. The System itself has a relatively small configuration surface area - the list of components and the HTTP Port used for REST calls.

### System_Port.json

System_Port.json specifies the port on which the System is listening for REST API calls. The same port is used for configuration and for writing data to OMF and SDS. The default configuration port is 5590. The default System_Port.json file installed is:

```json
{
  "Port": 5590
}
```

Allowable ports are in the range of 1024-65535. Before you change the default, ensure that no other service or application on the computer running the EdgeSystem is using that port - only one application or service can use a port. The Edge System must be restarted if the port number changes through the REST API or the command line.

### System_Components.json

The minimum System_Components.json file for the System is below. The Storage component is required for this initial release for the System to run. With later releases of the Edge System, the storage component may not be required.

```json
[
  {
    "ComponentId": "Storage",
    "ComponentType": "EDS.Component"
  }
]
```

The default System_Components.json for Beta 2 is given below. It includes three components - Storage, a single Modbus adapter (Modbus1), a single Opc Ua Adapter (OpcUa1), and a Storage component (EDS.Component).

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

 Additional Modbus and Opc Ua components can be added if desired, but only a single Storage component is supported. In Beta 2 the system must be restarted if a component is added or deleted using the REST API or the command line.

## Configuring entire system

The following JSON file represents minimal configuration of an Edge System. There are no Modbus or Opc Ua components, and the Storage component configurations are set to the default. If a system were configured with this JSON file, any existing Modbus or Opc Ua components would be disabled and removed. No storage data would be deleted or modified, and OMF and SDS data access would not be impacted.

```json
{
    "Storage": {
        "Runtime": {
            "streamStorageLimitMb": 2,
            "streamStorageTargetMb": 1,
            "ingressDebugExpiration": "0001-01-01T00:00:00"
        },
        "Logging": {
            "logLevel": "Information",
            "logFileSizeLimitBytes": 34636833,
            "logFileCountLimit": 31
        },
        "PeriodicEgressEndpoints": []
    },
    "System": {
        "Logging": {
            "logLevel": "Information",
            "logFileSizeLimitBytes": 34636833,
            "logFileCountLimit": 31
        },
        "Components": [
             {
                "componentId": "Storage",
                "componentType": "EDS.Component"
            }
        ],
        "HealthEndpoints": [],
        "Port": {
            "port": 5590
        }
    }
}
```

When the following curl command is run, this will be set as the configuration of a running Edge System:

```bash
curl -i -d "@EdgeMinimumConfiguration.json" -H "Content-Type: application/json" -X PUT http://localhost:5590/api/v1/configuration
```

The configuration takes effect immediately after the command completes.

Full JSON definition of configuration parameters:
[Edge System Configuration](xref:edge_system_schema)
