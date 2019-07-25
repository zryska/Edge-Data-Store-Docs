---
uid: troubleShooting
---

# Edge System Troubleshooting

If errors are encountered while using or developing against the Edge System, there are both local and remote means of diagnosing issues.

The Edge System supports a diagnostics namespace that is used to store streams containing diagnostic information from the Edge System itself. As with any other stream data stored in the Edge Storage component, this can be egressed to either PI Web API or OSIsoft Cloud Services to monitor the state of a system remotely.

In addition, all components in the Edge System support OMF Health messages that can be configured using the Health Endpoint configuration so that OMF Health messages are sent to remote PI Web API or OSIsoft Cloud Service endpoints to support remote monitoring of devices.

## Egress

### Egress Logging

Log messages related to egress can be found in the Storage logs. Setting the log level temporarily to Verbose will output the most information for troubleshooting.

### Egress Debugging

In order to troubleshoot problems between the Edge System and the destination, enable debugging. Setting an appropriate value for the *DebugExpiration* property in an egress configuration will enable debugging for that destination, and result in HTTP request and response content being stored to disk for review. The property represents the date and time that debugging should no longer be enabled. Setting the the value to *null* will also disable debugging.

Examples of valid strings representing date and time:

    Utc: “yyyy-mm-ddThh:mm:ssZ”

    Local: “mm-dd-yyyy hh:mm:ss”

The content length of each request/response, as well as the overall number of requests/responses, can be quite large. As a result debug inforamtion is stored to disk in a separate location then the typical log messages. Debug folders/files will be created under the Edge System data folder. The debug folder/file structure is:

    Windows: %programdata%\OSIsoft\EdgeSystem\Storage\egressdump\{tenantId}\{namespaceId}\{egressId}\{omfType}\{Ticks}-{Guid}-{Req/Res}.txt

    Linux: /usr/share/OSIsoft/EdgeSystem/Storage/egressdump/{tenantId}/{namespaceId}/{egressId}/{omfType}/{Ticks}-{Guid}-{Req/Res}.txt

where *omfType* represents Type/Container/Data; *Ticks* represents the tick count for the Utc DateTime when it was decided that the message would be written to disk; *Guid* represents a unique Guid for each request/response pair; *Req/Res* whether it was the HTTP request or response.
