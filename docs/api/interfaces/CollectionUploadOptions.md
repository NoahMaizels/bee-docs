---
id: "CollectionUploadOptions"
title: "Interface: CollectionUploadOptions"
sidebar_label: "CollectionUploadOptions"
sidebar_position: 0
custom_edit_url: null
---

## Hierarchy

- [`UploadOptions`](UploadOptions.md)

  ↳ **`CollectionUploadOptions`**

## Properties

### deferred

• `Optional` **deferred**: `boolean`

Determines if the uploaded data should be sent to the network immediately (eq. deferred=false) or in a deferred fashion (eq. deferred=true).

With deferred style client uploads all the data to Bee node first and only then Bee node starts push the data to network itself. The progress of this upload can be tracked with tags.
With non-deferred style client uploads the data to Bee which immediately starts pushing the data to network. The request is only finished once all the data was pushed through the Bee node to the network.

In future there will be move to the non-deferred style and even the support for deferred upload will be removed from Bee itself.

**`default`** true

#### Inherited from

[UploadOptions](UploadOptions.md).[deferred](UploadOptions.md#deferred)

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

#### Inherited from

[UploadOptions](UploadOptions.md).[encrypt](UploadOptions.md#encrypt)

#### Defined in

[bee-js/src/types/index.ts:195](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L195)

___

### errorDocument

• `Optional` **errorDocument**: `string`

Configure custom error document to be returned when a specified path can not be found in collection.

**`see`** [Bee docs - Upload a directory](https://docs.ethswarm.org/docs/access-the-swarm/upload-a-directory)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/File)

#### Defined in

[bee-js/src/types/index.ts:250](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L250)

___

### fetch

• `Optional` **fetch**: `Fetch`

User defined Fetch compatible function

#### Inherited from

[UploadOptions](UploadOptions.md).[fetch](UploadOptions.md#fetch)

#### Defined in

[bee-js/src/types/index.ts:128](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L128)

___

### indexDocument

• `Optional` **indexDocument**: `string`

Default file to be returned when the root hash of collection is accessed.

**`see`** [Bee docs - Upload a directory](https://docs.ethswarm.org/docs/access-the-swarm/upload-a-directory)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/File)

#### Defined in

[bee-js/src/types/index.ts:242](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L242)

___

### pin

• `Optional` **pin**: `boolean`

Will pin the data locally in the Bee node as well.

Locally pinned data is possible to reupload to network if it disappear.

**Warning! Not allowed when node is in Gateway mode!**

**`see`** [Bee docs - Pinning](https://docs.ethswarm.org/docs/access-the-swarm/pinning)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz/post)

#### Inherited from

[UploadOptions](UploadOptions.md).[pin](UploadOptions.md#pin)

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

[UploadOptions](UploadOptions.md).[retry](UploadOptions.md#retry)

#### Defined in

[bee-js/src/types/index.ts:123](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L123)

___

### tag

• `Optional` **tag**: `number`

Tags keep track of syncing the data with network. This option allows attach existing Tag UUID to the uploaded data.

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz/post)

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`link`** Tag

#### Inherited from

[UploadOptions](UploadOptions.md).[tag](UploadOptions.md#tag)

#### Defined in

[bee-js/src/types/index.ts:204](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L204)

___

### timeout

• `Optional` **timeout**: `number`

Timeout of requests in milliseconds

#### Inherited from

[UploadOptions](UploadOptions.md).[timeout](UploadOptions.md#timeout)

#### Defined in

[bee-js/src/types/index.ts:115](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L115)
