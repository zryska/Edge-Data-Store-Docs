---
uid: sdsQuickStart
---

# Edge Storage SDS Quick Start

This document is a quick tour of getting data into the Edge Storage component using the Sequential Data Store (SDS) REST API. This tour assumes the Edge System has been installed, and is accessible via a REST API using the default installed port (5590). This tour will use curl, a commonly available tool on both Windows and Linux, and use command line commands. The same operations can be used with any programming language or tool that supports making REST calls. In addition data retrieval steps (GET commands) can be accomplished using a browser if one is available on the device.

## Create an SDS Type

The first step in SDS data ingress is to create an SDS type that describes the format of the data to be stored in a container. In our example the data to be written is a timestamp and a numeric value, so the JSON describing the type is:

```json
{
    "Id": "Simple",
    "Name": "Simple",
    "SdsTypeCode": 1,
    "Properties": [
        {
            "Id": "Time",
            "Name": "Time",
            "IsKey": true,
            "SdsType": {
                "SdsTypeCode": 16
            }
        },
        {
            "Id": "Measurement",
            "Name": "Measurement",
            "SdsType": {
                "SdsTypeCode": 14
            }
        }
    ]
}
```

The value is indexed by a timestamp and the numeric value that will be stored is a 64 bit floating point value. In order to create the SDS type in the Edge Storage, the JSON should be stored as a file with the name SDSCreateType.json and run the following curl script:

```bash
curl -i -d "@SDSCreateType.json" -H "Content-Type: application/json"  -X POST http://localhost:5590/api/v1/tenants/default/namespaces/default/types/Simple
```

When this command completes successfully, an SDS type with the same name will have been created on the server. Any number of containers can be created from the type, as long as they use a timestamp as an index and a 32 bit floating point value. Type creation only needs to be done the first time you send using a custom application, but it does not cause an error if you resend the same definition at a later time.

## Create an SDS Stream

The next step in writing SDS data is to create a stream. As with an SDS Type, this only needs to be done once before sending data events, and resending the same definition repeatedly does not cause an error.

```json
{
    "Id": "Simple",
    "Name": "Simple",
    "TypeId": "Simple"
}
```

This stream references the type that was created in the last step, and an error will occur if the type does not exist when the stream is created. In order to create the SDS stream in the Edge Storage, the JSON should be stored as a file with the name SDSCreateStream.json and the following curl script run:

```bash
curl -i -d "@SDSCreateStream.json" -H "Content-Type: application/json"  -X POST http://localhost:5590/api/v1/tenants/default/namespaces/default/streams/Simple
```

When this command completes successfully, an SDS stream will have been created to store data defined by the type.

## Write Data Events to the SDS stream

Now that the type and container have been created, we can write data using SDS:

```json
[{
    "Time": "2017-11-23T17:00:00Z",
    "Measurement": 50.0
},
{
    "Time": "2017-11-23T18:00:00Z",
    "Measurement": 60.0
}]
```

This example includes two data events that will be stored in the SDS Stream that was created in the previous steps. It is generally a best practice to batch SDS values when writing them for the best performance. In order to write the data for the purpose of this example, the JSON should be stored as a file with the name SDSWriteData.json and run the following curl script:

```bash
curl -i -d "@SDSWriteData.json" -H "Content-Type: application/json"  -X POST http://localhost:5590/api/v1/tenants/default/namespaces/default/streams/Simple/Data
```

When this command completes successfully, two values will have been written to the SDS stream.

## Read Last Data written using SDS

In order to read the data back from the server that has been written, you can use the SDS REST API. Here is an example curl script that reads back the last value entered:

```bash
curl http://localhost:5590/api/v1/tenants/default/namespaces/default/streams/MyCustomContainer/Data/Last
```

When run this GET command returns the last value written:

```json
{"Timestamp":"2019-07-16T15:18:25.9870136Z","Value":12346.6787}
```

## Read a range of data events written using SDS

In order to read the data back from the server that has been written, you can use the SDS REST API. Here is an example curl script that reads back a time range of values that have been written:

```bash
curl "http://localhost:5590/api/v1/tenants/default/namespaces/default/streams/MyCustomContainer/Data?startIndex=2019-07-08T13:00:00Z&count=100"
```

```json
[{"Timestamp":"2019-07-16T15:18:24.9870136Z","Value":12345.6787},{"Timestamp":"2019-07-16T15:18:25.9870136Z","Value":12346.6787}]
```

Both values that were entered were returned - up to 100 values after the specified timestamp would be returned.

For more information on SDS APIs see the SDS section of this documentation.
