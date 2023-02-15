---
id: "RequestOptions"
title: "Interface: RequestOptions"
sidebar_label: "RequestOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- **`RequestOptions`**

  ↳ [`BeeOptions`](BeeOptions.md)

  ↳ [`UploadOptions`](UploadOptions.md)

  ↳ [`AllTagsOptions`](AllTagsOptions.md)

  ↳ [`JsonFeedOptions`](JsonFeedOptions.md)

  ↳ [`PostageBatchOptions`](PostageBatchOptions.md)

  ↳ [`CashoutOptions`](CashoutOptions.md)

## Properties

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

___

### retry

• `Optional` **retry**: `number`

Configure backoff mechanism for requests retries.
Specifies how many retries will be performed before failing a request.
Retries are performed for GET, PUT, HEAD, DELETE, OPTIONS and TRACE requests.
Default is 2.

#### Defined in

[bee-js/src/types/index.ts:123](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L123)

___

### timeout

• `Optional` **timeout**: `number`

Timeout of requests in milliseconds

#### Defined in

[bee-js/src/types/index.ts:115](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L115)
