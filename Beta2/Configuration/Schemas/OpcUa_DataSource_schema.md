---
uid: opcUa_DataSelection_Schema
---

# Opc Ua Data Source Configuration Schema

```

```

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                                   |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------------------------------------ |
| Can be instantiated | Yes        | Experimental | No           | Forbidden         | Forbidden             | [OpcUa_DataSource_schema.json](OpcUa_DataSource_schema.json) |

# DataSourceConfiguration Properties

| Property                                    | Type      | Required | Nullable | Defined by                            |
| ------------------------------------------- | --------- | -------- | -------- | ------------------------------------- |
| [EndpointUrl](#endpointurl)                 | `string`  | Optional | Yes      | DataSourceConfiguration (this schema) |
| [IncomingTimestamp](#incomingtimestamp)     | reference | Optional | No       | DataSourceConfiguration (this schema) |
| [Password](#password)                       | `string`  | Optional | Yes      | DataSourceConfiguration (this schema) |
| [RootNodeIds](#rootnodeids)                 | `string`  | Optional | Yes      | DataSourceConfiguration (this schema) |
| [StreamIdPrefix](#streamidprefix)           | `string`  | Optional | Yes      | DataSourceConfiguration (this schema) |
| [UseSecureConnection](#usesecureconnection) | `boolean` | Optional | No       | DataSourceConfiguration (this schema) |
| [UserName](#username)                       | `string`  | Optional | Yes      | DataSourceConfiguration (this schema) |

## EndpointUrl

`EndpointUrl`

- is optional
- type: `string`
- defined in this schema

### EndpointUrl Type

`string`, nullable

## IncomingTimestamp

`IncomingTimestamp`

- is optional
- type: reference
- defined in this schema

### IncomingTimestamp Type

- []() – `#/definitions/IncomingTimestampType`

## Password

`Password`

- is optional
- type: `string`
- defined in this schema

### Password Type

`string`, nullable

## RootNodeIds

`RootNodeIds`

- is optional
- type: `string`
- defined in this schema

### RootNodeIds Type

`string`, nullable

## StreamIdPrefix

`StreamIdPrefix`

- is optional
- type: `string`
- defined in this schema

### StreamIdPrefix Type

`string`, nullable

## UseSecureConnection

`UseSecureConnection`

- is optional
- type: `boolean`
- defined in this schema

### UseSecureConnection Type

`boolean`

## UserName

`UserName`

- is optional
- type: `string`
- defined in this schema

### UserName Type

`string`, nullable

**All** of the following _requirements_ need to be fulfilled.

#### Requirement 1

- []() – `#/definitions/EdgeConfigurationBase`

#### Requirement 2

`object` with following properties:

| Property              | Type    | Required |
| --------------------- | ------- | -------- |
| `EndpointUrl`         | string  | Optional |
| `IncomingTimestamp`   |         | Optional |
| `Password`            | string  | Optional |
| `RootNodeIds`         | string  | Optional |
| `StreamIdPrefix`      | string  | Optional |
| `UseSecureConnection` | boolean | Optional |
| `UserName`            | string  | Optional |

#### EndpointUrl

`EndpointUrl`

- is optional
- type: `string`

##### EndpointUrl Type

`string`, nullable

#### IncomingTimestamp

`IncomingTimestamp`

- is optional
- type: reference

##### IncomingTimestamp Type

- []() – `#/definitions/IncomingTimestampType`

#### Password

`Password`

- is optional
- type: `string`

##### Password Type

`string`, nullable

#### RootNodeIds

`RootNodeIds`

- is optional
- type: `string`

##### RootNodeIds Type

`string`, nullable

#### StreamIdPrefix

`StreamIdPrefix`

- is optional
- type: `string`

##### StreamIdPrefix Type

`string`, nullable

#### UseSecureConnection

`UseSecureConnection`

- is optional
- type: `boolean`

##### UseSecureConnection Type

`boolean`

#### UserName

`UserName`

- is optional
- type: `string`

##### UserName Type

`string`, nullable
