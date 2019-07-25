---
uid: modbus_DataSource_schema
---

# Modbus Data Source Configuration Schema

```

```

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                                     |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | -------------------------------------------------------------- |
| Can be instantiated | Yes        | Experimental | No           | Forbidden         | Forbidden             | [Modbus_DataSource_schema.json](Modbus_DataSource_schema.json) |

# DataSourceConfiguration Properties

| Property                                        | Type      | Required | Nullable | Defined by                            |
| ----------------------------------------------- | --------- | -------- | -------- | ------------------------------------- |
| [ConnectTimeout](#connecttimeout)               | `integer` | Optional | No       | DataSourceConfiguration (this schema) |
| [DelayBetweenRequests](#delaybetweenrequests)   | `integer` | Optional | No       | DataSourceConfiguration (this schema) |
| [IpAddress](#ipaddress)                         | `string`  | Optional | Yes      | DataSourceConfiguration (this schema) |
| [MaxResponseDataLength](#maxresponsedatalength) | `integer` | Optional | No       | DataSourceConfiguration (this schema) |
| [Port](#port)                                   | `integer` | Optional | No       | DataSourceConfiguration (this schema) |
| [ReconnectInterval](#reconnectinterval)         | `integer` | Optional | No       | DataSourceConfiguration (this schema) |
| [RequestTimeout](#requesttimeout)               | `integer` | Optional | No       | DataSourceConfiguration (this schema) |
| [StreamIdPrefix](#streamidprefix)               | `string`  | Optional | Yes      | DataSourceConfiguration (this schema) |

## ConnectTimeout

`ConnectTimeout`

- is optional
- type: `integer`
- defined in this schema

### ConnectTimeout Type

`integer`

## DelayBetweenRequests

`DelayBetweenRequests`

- is optional
- type: `integer`
- defined in this schema

### DelayBetweenRequests Type

`integer`

## IpAddress

`IpAddress`

- is optional
- type: `string`
- defined in this schema

### IpAddress Type

`string`, nullable

## MaxResponseDataLength

`MaxResponseDataLength`

- is optional
- type: `integer`
- defined in this schema

### MaxResponseDataLength Type

`integer`

## Port

`Port`

- is optional
- type: `integer`
- defined in this schema

### Port Type

`integer`

## ReconnectInterval

`ReconnectInterval`

- is optional
- type: `integer`
- defined in this schema

### ReconnectInterval Type

`integer`

## RequestTimeout

`RequestTimeout`

- is optional
- type: `integer`
- defined in this schema

### RequestTimeout Type

`integer`

## StreamIdPrefix

`StreamIdPrefix`

- is optional
- type: `string`
- defined in this schema

### StreamIdPrefix Type

`string`, nullable

**All** of the following _requirements_ need to be fulfilled.

#### Requirement 1

- []() – `#/definitions/EdgeConfigurationBase`

#### Requirement 2

`object` with following properties:

| Property                | Type    | Required |
| ----------------------- | ------- | -------- |
| `ConnectTimeout`        | integer | Optional |
| `DelayBetweenRequests`  | integer | Optional |
| `IpAddress`             | string  | Optional |
| `MaxResponseDataLength` | integer | Optional |
| `Port`                  | integer | Optional |
| `ReconnectInterval`     | integer | Optional |
| `RequestTimeout`        | integer | Optional |
| `StreamIdPrefix`        | string  | Optional |

#### ConnectTimeout

`ConnectTimeout`

- is optional
- type: `integer`

##### ConnectTimeout Type

`integer`

#### DelayBetweenRequests

`DelayBetweenRequests`

- is optional
- type: `integer`

##### DelayBetweenRequests Type

`integer`

#### IpAddress

`IpAddress`

- is optional
- type: `string`

##### IpAddress Type

`string`, nullable

#### MaxResponseDataLength

`MaxResponseDataLength`

- is optional
- type: `integer`

##### MaxResponseDataLength Type

`integer`

#### Port

`Port`

- is optional
- type: `integer`

##### Port Type

`integer`

#### ReconnectInterval

`ReconnectInterval`

- is optional
- type: `integer`

##### ReconnectInterval Type

`integer`

#### RequestTimeout

`RequestTimeout`

- is optional
- type: `integer`

##### RequestTimeout Type

`integer`

#### StreamIdPrefix

`StreamIdPrefix`

- is optional
- type: `string`

##### StreamIdPrefix Type

`string`, nullable
