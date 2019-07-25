---
uid: security
---
# Edge System Security Overview

## Connectivity
### REST APIs
The Edge System supports REST APIs for configuration, data reading (via SDS), and data writing (via OMF and SDS). 

The Edge System is built to provide only localhost access to REST APIs - any code that reads or writes to the REST APIs must reside on the computer or device that the Edge System is running on. 

REST access is via HTTP; the default port is 5590. The Port number can be changed at install time or by configuration after installation. URLs must be of the form "http://localhost:{port}/" or "http://127.0.0.1:{port}/" - do not use the host's name or IP Address in the URL.

Note for Docker users: You must use the "host" networking mode for the container. See the section pertaining to [Docker containers](xref:edgeDocker) for an example of running a container using this mode.

### Data egress
Writing data to OSIsoft Cloud Services or OSIsoft PI Web API is not limited to the local machine and data can be written to either of these destinations using HTTPS.

### Adapters
Modbus and Opc Ua are not limited to the local machine; both are enabled to access remote data sources via binary protocols.

## Secure Storage
Sensitive information, such as passwords and client secrets, are saved in configuration files in an encrypted form; only the Edge System runtime can properly store and retrieve these protected data items. Do not manually edit configuration files; altering encrypted values will cause failures.

The only time unencrypted values for sensitive information are available is when the user is providing them to the system via the REST API, e.g. for initial configuration or update. From that point forward, the unencrypted values are not available, either in the configuration file(s) or via the REST API. The REST API will only return a placeholder string (e.g. "****") for such values.

Care should be taken when submitting sensitive data items; for example, a temporary file used to submit configuration to the REST API containing unencrypted credentials should be removed from the system.

## Service and File System Security

The installer creates a specific user account that the Edge System service runs under. This account can only be used for running the service, e.g. it cannot be used for interactive sessions etc. 

This service account is typically not user configurable -- modifying the service configuration in this respect could cause system failure.

The Edge System binary files, configuration files, and data files are configured by the installer and runtime to allow appropriate access by the service account. Normally, the user does not need to modify the permission and ownership assignments for these files, and should not as failures could occur.
 





