---
uid: system_Components_schema
---

# Edge System Components Schema

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                                     |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | -------------------------------------------------------------- |
| Can be instantiated | Yes        | Experimental | No           | Forbidden         | Forbidden             | [System_Components_schema.json](System_Components_schema.json) |

# EdgeSystemConfig Definitions

| Property                        | Type     | Group                               |
| ------------------------------- | -------- | ----------------------------------- |
| [ComponentId](#componentid)     | `string` | `#/definitions/EdgeComponentConfig` |
| [ComponentType](#componenttype) | `string` | `#/definitions/EdgeComponentConfig` |

## ComponentId

`ComponentId`

- is optional
- type: `string`
- defined in this schema

### ComponentId Type

`string`, nullable

## ComponentType

`ComponentType`

- is optional
- type: `string`
- defined in this schema

### ComponentType Type

`string`, nullable

# EdgeSystemConfig Properties

| Property                                            | Type      | Required | Nullable | Defined by                     |
| --------------------------------------------------- | --------- | -------- | -------- | ------------------------------ |
| [ComponentConfigurations](#componentconfigurations) | reference | Optional | Yes      | EdgeSystemConfig (this schema) |

## ComponentConfigurations

`ComponentConfigurations`

- is optional
- type: reference
- defined in this schema

### ComponentConfigurations Type

Array type: reference

All items must be of the type:

- []() – `#/definitions/EdgeComponentConfig`

**All** of the following _requirements_ need to be fulfilled.

#### Requirement 1

- []() – `#/definitions/EdgeConfigurationBase`

#### Requirement 2

`object` with following properties:

| Property                  | Type  | Required |
| ------------------------- | ----- | -------- |
| `ComponentConfigurations` | array | Optional |

#### ComponentConfigurations

`ComponentConfigurations`

- is optional
- type: reference

##### ComponentConfigurations Type

Array type: reference

All items must be of the type:

- []() – `#/definitions/EdgeComponentConfig`
