---
id: "BeeOptions"
title: "Interface: BeeOptions"
sidebar_label: "BeeOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`RequestOptions`](RequestOptions.md)

  ↳ **`BeeOptions`**

## Properties

### defaultHeaders

• `Optional` **defaultHeaders**: `Record`<`string`, `string`\>

Object that contains default headers that will be present
in all outgoing bee-js requests for instance of Bee class.

#### Defined in

[bee-js/src/types/index.ts:141](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L141)

___

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Inherited from

[RequestOptions](RequestOptions.md).[fetch](RequestOptions.md#fetch)

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

___

### onRequest

• `Optional` **onRequest**: [`HookCallback`](../types/HookCallback.md)<[`BeeRequest`](BeeRequest.md)\>

Function that registers listener callback for all outgoing HTTP requests that Bee instance makes.

#### Defined in

[bee-js/src/types/index.ts:146](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L146)

___

### onResponse

• `Optional` **onResponse**: [`HookCallback`](../types/HookCallback.md)<[`BeeResponse`](BeeResponse.md)\>

Function that registers listener callback for all incoming HTTP responses that Bee instance made.

#### Defined in

[bee-js/src/types/index.ts:151](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L151)

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

Signer object or private key of the Signer in form of either hex string or Uint8Array that will be default signer for the instance.

#### Defined in

[bee-js/src/types/index.ts:135](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L135)

___

### timeout

• `Optional` **timeout**: `number`

Timeout of requests in milliseconds

#### Inherited from

[RequestOptions](RequestOptions.md).[timeout](RequestOptions.md#timeout)

#### Defined in

[bee-js/src/types/index.ts:115](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L115)
