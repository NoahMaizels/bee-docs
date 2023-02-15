---
id: "AllTagsOptions"
title: "Interface: AllTagsOptions"
sidebar_label: "AllTagsOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`RequestOptions`](RequestOptions.md)

  ↳ **`AllTagsOptions`**

## Properties

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Inherited from

[RequestOptions](RequestOptions.md).[fetch](RequestOptions.md#fetch)

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

___

### limit

• `Optional` **limit**: `number`

#### Defined in

[bee-js/src/types/index.ts:293](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L293)

___

### offset

• `Optional` **offset**: `number`

#### Defined in

[bee-js/src/types/index.ts:294](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L294)

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
