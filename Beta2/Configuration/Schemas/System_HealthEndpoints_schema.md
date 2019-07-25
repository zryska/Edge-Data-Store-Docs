---
uid: system_HealthEndpoints_schema
---

# Omf Health Endpoint Configuration Schema

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                                               |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | ------------------------------------------------------------------------ |
| Can be instantiated | Yes        | Experimental | No           | Forbidden         | Forbidden             | [System_HealthEndpoints_schema.json](System_HealthEndpoints_schema.json) |

# OmfHealthEndpointConfiguration Properties

| Property                                                    | Type      | Required | Nullable | Defined by                                   |
| ----------------------------------------------------------- | --------- | -------- | -------- | -------------------------------------------- |
| [Buffering](#buffering)                                     | reference | Optional | No       | OmfHealthEndpointConfiguration (this schema) |
| [ClientId](#clientid)                                       | `string`  | Optional | Yes      | OmfHealthEndpointConfiguration (this schema) |
| [ClientSecret](#clientsecret)                               | `string`  | Optional | Yes      | OmfHealthEndpointConfiguration (this schema) |
| [Endpoint](#endpoint)                                       | `string`  | Optional | Yes      | OmfHealthEndpointConfiguration (this schema) |
| [Id](#id)                                                   | `string`  | Optional | Yes      | OmfHealthEndpointConfiguration (this schema) |
| [MaxBufferSizeMB](#maxbuffersizemb)                         | `integer` | Optional | No       | OmfHealthEndpointConfiguration (this schema) |
| [Password](#password)                                       | `string`  | Optional | Yes      | OmfHealthEndpointConfiguration (this schema) |
| [UserName](#username)                                       | `string`  | Optional | Yes      | OmfHealthEndpointConfiguration (this schema) |
| [ValidateEndpointCertificate](#validateendpointcertificate) | `boolean` | Optional | No       | OmfHealthEndpointConfiguration (this schema) |

## Buffering

`Buffering`

- is optional
- type: reference
- defined in this schema

### Buffering Type

- []() – `#/definitions/BufferType`

## ClientId

`ClientId`

- is optional
- type: `string`
- defined in this schema

### ClientId Type

`string`, nullable

## ClientSecret

`ClientSecret`

- is optional
- type: `string`
- defined in this schema

### ClientSecret Type

`string`, nullable

## Endpoint

`Endpoint`

- is optional
- type: `string`
- defined in this schema

### Endpoint Type

`string`, nullable

## Id

`Id`

- is optional
- type: `string`
- defined in this schema

### Id Type

`string`, nullable

## MaxBufferSizeMB

`MaxBufferSizeMB`

- is optional
- type: `integer`
- defined in this schema

### MaxBufferSizeMB Type

`integer`

## Password

`Password`

- is optional
- type: `string`
- defined in this schema

### Password Type

`string`, nullable

## UserName

`UserName`

- is optional
- type: `string`
- defined in this schema

### UserName Type

`string`, nullable

## ValidateEndpointCertificate

`ValidateEndpointCertificate`

- is optional
- type: `boolean`
- defined in this schema

### ValidateEndpointCertificate Type

`boolean`

**All** of the following _requirements_ need to be fulfilled.

#### Requirement 1

- []() – `#/definitions/EdgeConfigurationBase`

#### Requirement 2

`object` with following properties:

| Property                      | Type    | Required |
| ----------------------------- | ------- | -------- |
| `Buffering`                   |         | Optional |
| `ClientId`                    | string  | Optional |
| `ClientSecret`                | string  | Optional |
| `Endpoint`                    | string  | Optional |
| `Id`                          | string  | Optional |
| `MaxBufferSizeMB`             | integer | Optional |
| `Password`                    | string  | Optional |
| `UserName`                    | string  | Optional |
| `ValidateEndpointCertificate` | boolean | Optional |

#### Buffering

`Buffering`

- is optional
- type: reference

##### Buffering Type

- []() – `#/definitions/BufferType`

#### ClientId

`ClientId`

- is optional
- type: `string`

##### ClientId Type

`string`, nullable

#### ClientSecret

`ClientSecret`

- is optional
- type: `string`

##### ClientSecret Type

`string`, nullable

#### Endpoint

`Endpoint`

- is optional
- type: `string`

##### Endpoint Type

`string`, nullable

#### Id

`Id`

- is optional
- type: `string`

##### Id Type

`string`, nullable

#### MaxBufferSizeMB

`MaxBufferSizeMB`

- is optional
- type: `integer`

##### MaxBufferSizeMB Type

`integer`

#### Password

`Password`

- is optional
- type: `string`

##### Password Type

`string`, nullable

#### UserName

`UserName`

- is optional
- type: `string`

##### UserName Type

`string`, nullable

#### ValidateEndpointCertificate

`ValidateEndpointCertificate`

- is optional
- type: `boolean`

##### ValidateEndpointCertificate Type

`boolean`
