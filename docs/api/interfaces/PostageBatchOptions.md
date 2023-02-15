---
id: "PostageBatchOptions"
title: "Interface: PostageBatchOptions"
sidebar_label: "PostageBatchOptions"
sidebar_position: 0
custom_edit_url: null
---

Options for creation of postage batch

## Hierarchy

- [`RequestOptions`](RequestOptions.md)

  ↳ **`PostageBatchOptions`**

## Properties

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Inherited from

[RequestOptions](RequestOptions.md).[fetch](RequestOptions.md#fetch)

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

___

### gasPrice

• `Optional` **gasPrice**: [`NumberString`](../types/NumberString.md)

Sets gas price in Wei for the transaction that creates the postage batch

#### Defined in

[bee-js/src/types/index.ts:546](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L546)

___

### immutableFlag

• `Optional` **immutableFlag**: `boolean`

#### Defined in

[bee-js/src/types/index.ts:547](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L547)

___

### label

• `Optional` **label**: `string`

Sets label for the postage batch

#### Defined in

[bee-js/src/types/index.ts:541](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L541)

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

___

### waitForUsable

• `Optional` **waitForUsable**: `boolean`

The returned Promise will await until the purchased Postage Batch is usable.
In other word, it has to have enough block confirmations that Bee pronounce it usable.
If turned on, this significantly prolong the creation of postage batch!
If you plan to use the stamp right away for some action with Bee (like uploading using this stamp) it is
highly recommended to use this option, otherwise you might get errors "stamp not usable" from Bee.

In next breaking release this option will be turned on by default.

**`default`** false

#### Defined in

[bee-js/src/types/index.ts:559](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L559)

___

### waitForUsableTimeout

• `Optional` **waitForUsableTimeout**: `number`

When waiting for the postage stamp to become usable, this specify the timeout for the waiting.
Default: 120s

#### Defined in

[bee-js/src/types/index.ts:565](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L565)
