---
id: "UploadOptions"
title: "Interface: UploadOptions"
sidebar_label: "UploadOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`RequestOptions`](RequestOptions.md)

  ↳ **`UploadOptions`**

  ↳↳ [`FileUploadOptions`](FileUploadOptions.md)

  ↳↳ [`CollectionUploadOptions`](CollectionUploadOptions.md)

## Properties

### deferred

• `Optional` **deferred**: `boolean`

Determines if the uploaded data should be sent to the network immediately (eq. deferred=false) or in a deferred fashion (eq. deferred=true).

With deferred style client uploads all the data to Bee node first and only then Bee node starts push the data to network itself. The progress of this upload can be tracked with tags.
With non-deferred style client uploads the data to Bee which immediately starts pushing the data to network. The request is only finished once all the data was pushed through the Bee node to the network.

In future there will be move to the non-deferred style and even the support for deferred upload will be removed from Bee itself.

**`default`** true

#### Defined in

[bee-js/src/types/index.ts:216](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L216)

___

### encrypt

• `Optional` **encrypt**: `boolean`

Will encrypt the uploaded data and return longer hash which also includes the decryption key.

**Warning! Not allowed when node is in Gateway mode!**

**`see`** [Bee docs - Store with Encryption](https://docs.ethswarm.org/docs/access-the-swarm/store-with-encryption)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz/post)

**`see`** Reference

#### Defined in

[bee-js/src/types/index.ts:195](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L195)

___

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Inherited from

[RequestOptions](RequestOptions.md).[fetch](RequestOptions.md#fetch)

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

___

### pin

• `Optional` **pin**: `boolean`

Will pin the data locally in the Bee node as well.

Locally pinned data is possible to reupload to network if it disappear.

**Warning! Not allowed when node is in Gateway mode!**

**`see`** [Bee docs - Pinning](https://docs.ethswarm.org/docs/access-the-swarm/pinning)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz/post)

#### Defined in

[bee-js/src/types/index.ts:184](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L184)

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

### tag

• `Optional` **tag**: `number`

Tags keep track of syncing the data with network. This option allows attach existing Tag UUID to the uploaded data.

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz/post)

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`link`** Tag

#### Defined in

[bee-js/src/types/index.ts:204](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L204)

___

### timeout

• `Optional` **timeout**: `number`

Timeout of requests in milliseconds

#### Inherited from

[RequestOptions](RequestOptions.md).[timeout](RequestOptions.md#timeout)

#### Defined in

[bee-js/src/types/index.ts:115](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L115)
