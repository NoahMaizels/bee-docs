---
id: "JsonFeedOptions"
title: "Interface: JsonFeedOptions"
sidebar_label: "JsonFeedOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`RequestOptions`](RequestOptions.md)

  ↳ **`JsonFeedOptions`**

## Properties

### address

• `Optional` **address**: `string` \| `Uint8Array` \| [`EthAddress`](../types/Utils.EthAddress.md)

Valid only for `get` action, where either this `address` or `signer` has
to be specified.

#### Defined in

[bee-js/src/types/index.ts:419](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L419)

___

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Inherited from

[RequestOptions](RequestOptions.md).[fetch](RequestOptions.md#fetch)

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

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

### signer

• `Optional` **signer**: `string` \| `Uint8Array` \| [`Signer`](../types/Signer.md)

Custom Signer object or private key in either binary or hex form.
This required for `set` action, and optional for `get` although
if not specified for `get` then `address` option has to be specified.

#### Defined in

[bee-js/src/types/index.ts:426](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L426)

___

### timeout

• `Optional` **timeout**: `number`

Timeout of requests in milliseconds

#### Inherited from

[RequestOptions](RequestOptions.md).[timeout](RequestOptions.md#timeout)

#### Defined in

[bee-js/src/types/index.ts:115](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L115)

___

### type

• `Optional` **type**: ``"sequence"`` \| ``"epoch"``

#### Defined in

[bee-js/src/types/index.ts:427](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L427)
