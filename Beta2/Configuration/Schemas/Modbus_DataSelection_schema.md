---
uid: modbus_DataSelection_schema
---

# Modbus DataSelectionConfiguration Schema

```

```

| Abstract            | Extensible | Status       | Identifiable | Custom Properties | Additional Properties | Defined In                                                           |
| ------------------- | ---------- | ------------ | ------------ | ----------------- | --------------------- | -------------------------------------------------------------------- |
| Can be instantiated | Yes        | Experimental | No           | Forbidden         | Forbidden             | [Modbus_DataSelection_schema.json](Modbus_DataSelection_schema.json) |

# DataSelectionConfiguration Properties

| Property                              | Type      | Required | Nullable | Defined by                               |
| ------------------------------------- | --------- | -------- | -------- | ---------------------------------------- |
| [BitMap](#bitmap)                     | `string`  | Optional | Yes      | DataSelectionConfiguration (this schema) |
| [ConversionFactor](#conversionfactor) | `number`  | Optional | Yes      | DataSelectionConfiguration (this schema) |
| [ConversionOffset](#conversionoffset) | `number`  | Optional | Yes      | DataSelectionConfiguration (this schema) |
| [DataTypeCode](#datatypecode)         | `integer` | Optional | No       | DataSelectionConfiguration (this schema) |
| [Name](#name)                         | `string`  | Optional | Yes      | DataSelectionConfiguration (this schema) |
| [RegisterOffset](#registeroffset)     | `integer` | Optional | No       | DataSelectionConfiguration (this schema) |
| [RegisterType](#registertype)         | reference | Optional | No       | DataSelectionConfiguration (this schema) |
| [ScanRate](#scanrate)                 | `integer` | Optional | No       | DataSelectionConfiguration (this schema) |
| [Selected](#selected)                 | `boolean` | Optional | No       | DataSelectionConfiguration (this schema) |
| [StreamId](#streamid)                 | `string`  | Optional | Yes      | DataSelectionConfiguration (this schema) |
| [UnitId](#unitid)                     | `integer` | Optional | No       | DataSelectionConfiguration (this schema) |

## BitMap

`BitMap`

- is optional
- type: `string`
- defined in this schema

### BitMap Type

`string`, nullable

## ConversionFactor

`ConversionFactor`

- is optional
- type: `number`
- defined in this schema

### ConversionFactor Type

`number`, nullable

## ConversionOffset

`ConversionOffset`

- is optional
- type: `number`
- defined in this schema

### ConversionOffset Type

`number`, nullable

## DataTypeCode

`DataTypeCode`

- is optional
- type: `integer`
- defined in this schema

### DataTypeCode Type

`integer`

## Name

`Name`

- is optional
- type: `string`
- defined in this schema

### Name Type

`string`, nullable

## RegisterOffset

`RegisterOffset`

- is optional
- type: `integer`
- defined in this schema

### RegisterOffset Type

`integer`

## RegisterType

`RegisterType`

- is optional
- type: reference
- defined in this schema

### RegisterType Type

- []() – `#/definitions/ModbusRegisterType`

## ScanRate

`ScanRate`

- is optional
- type: `integer`
- defined in this schema

### ScanRate Type

`integer`

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

## UnitId

`UnitId`

- is optional
- type: `integer`
- defined in this schema

### UnitId Type

`integer`

**All** of the following _requirements_ need to be fulfilled.

#### Requirement 1

- []() – `#/definitions/EdgeConfigurationBase`

#### Requirement 2

`object` with following properties:

| Property           | Type    | Required |
| ------------------ | ------- | -------- |
| `BitMap`           | string  | Optional |
| `ConversionFactor` | number  | Optional |
| `ConversionOffset` | number  | Optional |
| `DataTypeCode`     | integer | Optional |
| `Name`             | string  | Optional |
| `RegisterOffset`   | integer | Optional |
| `RegisterType`     |         | Optional |
| `ScanRate`         | integer | Optional |
| `Selected`         | boolean | Optional |
| `StreamId`         | string  | Optional |
| `UnitId`           | integer | Optional |

#### BitMap

`BitMap`

- is optional
- type: `string`

##### BitMap Type

`string`, nullable

#### ConversionFactor

`ConversionFactor`

- is optional
- type: `number`

##### ConversionFactor Type

`number`, nullable

#### ConversionOffset

`ConversionOffset`

- is optional
- type: `number`

##### ConversionOffset Type

`number`, nullable

#### DataTypeCode

`DataTypeCode`

- is optional
- type: `integer`

##### DataTypeCode Type

`integer`

#### Name

`Name`

- is optional
- type: `string`

##### Name Type

`string`, nullable

#### RegisterOffset

`RegisterOffset`

- is optional
- type: `integer`

##### RegisterOffset Type

`integer`

#### RegisterType

`RegisterType`

- is optional
- type: reference

##### RegisterType Type

- []() – `#/definitions/ModbusRegisterType`

#### ScanRate

`ScanRate`

- is optional
- type: `integer`

##### ScanRate Type

`integer`

#### Selected

`Selected`

- is optional
- type: `boolean`

##### Selected Type

`boolean`

#### StreamId

`StreamId`

- is optional
- type: `string`

##### StreamId Type

`string`, nullable

#### UnitId

`UnitId`

- is optional
- type: `integer`

##### UnitId Type

`integer`
