---
id: "BeeNotAJsonError"
title: "Class: BeeNotAJsonError"
sidebar_label: "BeeNotAJsonError"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`BeeError`](BeeError.md)

  ↳ **`BeeNotAJsonError`**

## Constructors

### constructor

• **new BeeNotAJsonError**()

#### Overrides

[BeeError](BeeError.md).[constructor](BeeError.md#constructor)

#### Defined in

[bee-js/src/utils/error.ts:45](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/error.ts#L45)

## Properties

### message

• **message**: `string`

#### Inherited from

[BeeError](BeeError.md).[message](BeeError.md#message)

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:1023

___

### name

• **name**: `string`

#### Inherited from

[BeeError](BeeError.md).[name](BeeError.md#name)

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:1022

___

### stack

• `Optional` **stack**: `string`

#### Inherited from

[BeeError](BeeError.md).[stack](BeeError.md#stack)

#### Defined in

node_modules/typescript/lib/lib.es5.d.ts:1024

___

### stackTraceLimit

▪ `Static` **stackTraceLimit**: `number`

#### Inherited from

[BeeError](BeeError.md).[stackTraceLimit](BeeError.md#stacktracelimit)

#### Defined in

bee-js/node_modules/@types/node/globals.d.ts:13

## Methods

### captureStackTrace

▸ `Static` **captureStackTrace**(`targetObject`, `constructorOpt?`): `void`

Create .stack property on a target object

#### Parameters

| Name | Type |
| :------ | :------ |
| `targetObject` | `object` |
| `constructorOpt?` | `Function` |

#### Returns

`void`

#### Inherited from

[BeeError](BeeError.md).[captureStackTrace](BeeError.md#capturestacktrace)

#### Defined in

bee-js/node_modules/@types/node/globals.d.ts:4

___

### prepareStackTrace

▸ `Static` `Optional` **prepareStackTrace**(`err`, `stackTraces`): `any`

Optional override for formatting stack traces

**`see`** https://v8.dev/docs/stack-trace-api#customizing-stack-traces

#### Parameters

| Name | Type |
| :------ | :------ |
| `err` | `Error` |
| `stackTraces` | `CallSite`[] |

#### Returns

`any`

#### Inherited from

[BeeError](BeeError.md).[prepareStackTrace](BeeError.md#preparestacktrace)

#### Defined in

bee-js/node_modules/@types/node/globals.d.ts:11
