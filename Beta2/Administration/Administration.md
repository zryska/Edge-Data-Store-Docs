---
uid: edgeSystemAdministration
---

# Edge System Administration

The Edge System provides a number administration level functions.

## Resetting the Edge System

The Edge System provides a method by which a user may perform a complete reset of the product. When performed, all event data and configuration related to the Edge System will be deleted, and the product will be restarted.

Note - All configuration and stored data will be lost as a result of performing this action.

To reset the Edge System

Use any REST client and make a request using the following:
```
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/System/Reset
Header: Content-Type application/json
```

Example using cURL:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/System/Reset
```

HTTP status 204 indicates success.

## Resetting the Edge Storage Component

The Edge System provides a method by which a user may delete and reset all event data and configuration related to the Edge Data Store component, after which the product will be restarted

To reset the Storage component

Use any REST client and make a request using the following:

```
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/Storage/Reset
Header: Content-Type application/json
```

Example using cURL:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/Storage/Reset
```

HTTP status 204 indicates success..

## Stopping and Starting an Edge Connectivity Component

The Edge System provides the ability to stop and start connectivity components. By default, when the Edge System starts, all connectivity components currently configured are started and remain running until the product shuts down.

### Stopping a Connectivity Component

To stop an individual connectivity component:

Use any REST client and make a request using the following:

```
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/ConnectivityId/Stop
Header: Content-Type application/json
```

Example using cURL:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/ConnectivityId/Stop
```

Note - Replace ```ConnectivityId``` with the id of the connectivity component you wish to stop.

HTTP status 204 indicates success.

### Starting a Connectivity Component

To start an individual connectivity component:

Use any REST client and make a request using the following:

```
Method: POST
Endpoint: http://localhost:5590/api/v1/administration/ConnectivityId/Start
Header: Content-Type application/json
```

Example using cURL:

```bash
curl -v -d "" -X POST http://localhost:5590/api/v1/Administration/ConnectivityId/Start
```

Note - Replace ```ConnectivityId``` with the id of the connectivity component you wish to start.

HTTP status 204 indicates success.
