---
uid: omfOverview
---

# OSIsoft Message Format (OMF) Ingress with Edge Storage

The Edge Storage component supports both OMF version 1.0 and OMF version 1.1 for data ingress. The OMF ingress functionality is the same technology that is used in OSIsoft Cloud Services (OCS), so writing an OMF application to run on EDS is very similar to writing an OMF application to write data to OCS. No authentication is necessary for writing to Edge System, as long as the application is running on the same computer or device as the Edge System. Remote access to OMF data ingress is not currently supported.

## OMF Specification

The OMF specification may be found here: <http://omf-docs.osisoft.com>

## OMF Endpoint

The route to the OMF endpoint provided by the Edge Storage component is:

```
Method: POST
Endpoint: http://localhost:5590/api/v1/tenants/default/namespaces/default/omf
```

## Supported functionality

The OMF endpoint for the Edge Storage component supports both OMF version 1.0 and OMF version 1.1 for data ingress.

The OMF endpoint for the Edge Storage component does not support the update action.
