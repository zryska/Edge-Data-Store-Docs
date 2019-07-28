---
uid: opcUa_DataSelection_schema
---

# OPC UA data collection item schema


| Abstract            | Extensible | Status       | Identifiable | Custom properties | Additional properties | Defined In                                                         |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------------------------------------------ |
| Can be instantiated | Yes        | Experimental | No           | Forbidden         | Forbidden             | [OpcUa_DataSelection_schema.json](OpcUa_DataSelection_schema.json) |

# DataCollectionItem properties

| Property              | Type      | Required | Nullable | Defined by                       |
| --------------------- | --------- | -------- | -------- | -------------------------------- |
| [Name](#name)         | `string`  | Optional | Yes      | DataCollectionItem (this schema) |
| [NodeId](#nodeid)     | `string`  | Optional | Yes      | DataCollectionItem (this schema) |
| [Selected](#selected) | `boolean` | Optional | No       | DataCollectionItem (this schema) |
| [StreamId](#streamid) | `string`  | Optional | Yes      | DataCollectionItem (this schema) |

## Name

`Name`

- is optional
- type: `string`
- defined in this schema

### Name type

`string`, nullable

## NodeId

`NodeId`

- is optional
- type: `string`
- defined in this schema

### NodeId Type

`string`, nullable

## Selected

`Selected`

- is optional
- type: `boolean`
- defined in this schema

### Selected Type

`boolean`

## StreamId

`StreamId`

- is optional
- type: `string`
- defined in this schema

### StreamId Type

`string`, nullable

**All** of the following _requirements_ need to be fulfilled.

#### Requirement 1

- []() – `#/definitions/EdgeConfigurationBase`

#### Requirement 2

`object` with following properties:

| Property   | Type    | Required |
| ---------- | ------- | -------- |
| `Name`     | string  | Optional |
| `NodeId`   | string  | Optional |
| `Selected` | boolean | Optional |
| `StreamId` | string  | Optional |

#### Name

`Name`

- is optional
- type: `string`

##### Name type

`string`, nullable

#### NodeId

`NodeId`

- is optional
- type: `string`

##### NodeId type

`string`, nullable

#### Selected

`Selected`

- is optional
- type: `boolean`

##### Selected type

`boolean`

#### StreamId

`StreamId`

- is optional
- type: `string`

##### StreamId type

`string`, nullable
