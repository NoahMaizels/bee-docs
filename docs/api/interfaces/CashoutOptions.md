---
id: "CashoutOptions"
title: "Interface: CashoutOptions"
sidebar_label: "CashoutOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`RequestOptions`](RequestOptions.md)

  ↳ **`CashoutOptions`**

## Properties

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Inherited from

[RequestOptions](RequestOptions.md).[fetch](RequestOptions.md#fetch)

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

___

### gasLimit

• `Optional` **gasLimit**: [`NumberString`](../types/NumberString.md)

Gas limit for the cashout transaction in WEI

#### Defined in

[bee-js/src/types/debug.ts:98](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/debug.ts#L98)

___

### gasPrice

• `Optional` **gasPrice**: [`NumberString`](../types/NumberString.md)

Gas price for the cashout transaction in WEI

#### Defined in

[bee-js/src/types/debug.ts:93](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/debug.ts#L93)

___

### retry

• `Optional` **retry**: `number`

Configure backoff mechanism for requests retries.
Specifies how many retries will be performed before failing a request.
Retries are performed for GET, PUT, HEAD, DELETE, OPTIONS and TRACE requests.
Default is 2.

#### Inherited from

[RequestOptions](RequestOptions.md).[retry](RequestOptions.md#retry)

#### Defined in

[bee-js/src/types/index.ts:123](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L123)

___

### timeout

• `Optional` **timeout**: `number`

Timeout of requests in milliseconds

#### Inherited from

[RequestOptions](RequestOptions.md).[timeout](RequestOptions.md#timeout)

#### Defined in

[bee-js/src/types/index.ts:115](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L115)
