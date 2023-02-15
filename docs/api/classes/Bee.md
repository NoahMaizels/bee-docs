---
id: "Bee"
title: "Class: Bee"
sidebar_label: "Bee"
sidebar_position: 0
custom_edit_url: null
---

The main component that abstracts operations available on the main Bee API.

Not all methods are always available as it depends in what mode is Bee node launched in.
For example gateway mode and light node mode has only limited set of endpoints enabled.

## Constructors

### constructor

• **new Bee**(`url`, `options?`)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `url` | `string` | URL on which is the main API of Bee node exposed |
| `options?` | [`BeeOptions`](../interfaces/BeeOptions.md) |  |

#### Defined in

[bee-js/src/bee.ts:114](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L114)

## Properties

### signer

• `Optional` `Readonly` **signer**: [`Signer`](../types/Signer.md)

Default Signer object used for signing operations, mainly Feeds.

#### Defined in

[bee-js/src/bee.ts:102](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L102)

___

### url

• `Readonly` **url**: `string`

URL on which is the main API of Bee node exposed

#### Defined in

[bee-js/src/bee.ts:97](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L97)

## Methods

### checkConnection

▸ **checkConnection**(`options?`): `Promise`<`void`\>

Ping the Bee node to see if there is a live Bee node on the given URL.

**`throws`** If connection was not successful throw error

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee.ts:1101](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L1101)

___

### createFeedManifest

▸ **createFeedManifest**(`postageBatchId`, `type`, `topic`, `owner`, `options?`): `Promise`<[`Reference`](../types/Reference.md)\>

Create feed manifest chunk and return the reference to it.

Feed manifest chunk allows for a feed to be able to be resolved through `/bzz` endpoint.

**`see`** [Bee docs - Feeds](https://docs.ethswarm.org/docs/dapps-on-swarm/feeds)

**`see`** [Bee API reference - `POST /feeds`](https://docs.ethswarm.org/api/#tag/Feed/paths/~1feeds~1{owner}~1{topic}/post)
TODO: Once breaking add support for Feed CID

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to create the Feed Manifest |
| `type` | ``"sequence"`` \| ``"epoch"`` | The type of the feed, can be 'epoch' or 'sequence' |
| `topic` | `string` \| `Uint8Array` \| [`Topic`](../types/Topic.md) | Topic in hex or bytes |
| `owner` | `string` \| `Uint8Array` \| [`EthAddress`](../types/Utils.EthAddress.md) | Owner's ethereum address in hex or bytes |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Reference`](../types/Reference.md)\>

#### Defined in

[bee-js/src/bee.ts:897](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L897)

___

### createTag

▸ **createTag**(`options?`): `Promise`<[`Tag`](../interfaces/Tag.md)\>

Create a new Tag which is meant for tracking progres of syncing data across network.

**Warning! Not allowed when node is in Gateway mode!**

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`see`** [Bee API reference - `POST /tags`](https://docs.ethswarm.org/api/#tag/Tag/paths/~1tags/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Tag`](../interfaces/Tag.md)\>

#### Defined in

[bee-js/src/bee.ts:462](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L462)

___

### deleteTag

▸ **deleteTag**(`tagUid`, `options?`): `Promise`<`void`\>

Delete Tag

**Warning! Not allowed when node is in Gateway mode!**

**`throws`** TypeError if tagUid is in not correct format

**`throws`** BeeResponse error if something went wrong on the Bee node side while deleting the tag.

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`see`** [Bee API reference - `DELETE /tags/{uid}`](https://docs.ethswarm.org/api/#tag/Tag/paths/~1tags~1{uid}/delete)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tagUid` | `number` \| [`Tag`](../interfaces/Tag.md) | UID or tag object to be retrieved |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee.ts:523](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L523)

___

### downloadChunk

▸ **downloadChunk**(`reference`, `options?`): `Promise`<[`Data`](../interfaces/Data.md)\>

Download chunk as a byte array

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `GET /chunks`](https://docs.ethswarm.org/api/#tag/Chunk/paths/~1chunks~1{reference}/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | [`ReferenceOrEns`](../types/ReferenceOrEns.md) | Bee chunk reference in hex string (either 64 or 128 chars long) or ENS domain. |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Data`](../interfaces/Data.md)\>

#### Defined in

[bee-js/src/bee.ts:254](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L254)

___

### downloadData

▸ **downloadData**(`reference`, `options?`): `Promise`<[`Data`](../interfaces/Data.md)\>

Download data as a byte array

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `GET /bytes`](https://docs.ethswarm.org/api/#tag/Bytes/paths/~1bytes~1{reference}/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | [`ReferenceOrEns`](../types/ReferenceOrEns.md) | Bee data reference in hex string (either 64 or 128 chars long) or ENS domain. |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Data`](../interfaces/Data.md)\>

#### Defined in

[bee-js/src/bee.ts:186](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L186)

___

### downloadFile

▸ **downloadFile**(`reference`, `path?`, `options?`): `Promise`<[`FileData`](../interfaces/FileData.md)<[`Data`](../interfaces/Data.md)\>\>

Download single file.

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** Data

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `GET /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz~1{reference}~1{path}/get)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `reference` | [`ReferenceCidOrEns`](../types/ReferenceCidOrEns.md) | `undefined` | Bee file reference in hex string (either 64 or 128 chars long), ENS domain or Swarm CID. |
| `path` | `string` | `''` | If reference points to manifest, then this parameter defines path to the file |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | `undefined` | Options that affects the request behavior |

#### Returns

`Promise`<[`FileData`](../interfaces/FileData.md)<[`Data`](../interfaces/Data.md)\>\>

#### Defined in

[bee-js/src/bee.ts:328](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L328)

___

### downloadReadableData

▸ **downloadReadableData**(`reference`, `options?`): `Promise`<`ReadableStream`<`Uint8Array`\>\>

Download data as a Readable stream

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `GET /bytes`](https://docs.ethswarm.org/api/#tag/Bytes/paths/~1bytes~1{reference}/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | [`ReferenceOrEns`](../types/ReferenceOrEns.md) | Bee data reference in hex string (either 64 or 128 chars long) or ENS domain. |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`ReadableStream`<`Uint8Array`\>\>

#### Defined in

[bee-js/src/bee.ts:203](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L203)

___

### downloadReadableFile

▸ **downloadReadableFile**(`reference`, `path?`, `options?`): `Promise`<[`FileData`](../interfaces/FileData.md)<`ReadableStream`<`Uint8Array`\>\>\>

Download single file as a readable stream

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `GET /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz~1{reference}~1{path}/get)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `reference` | [`ReferenceCidOrEns`](../types/ReferenceCidOrEns.md) | `undefined` | Bee file reference in hex string (either 64 or 128 chars long), ENS domain or Swarm CID. |
| `path` | `string` | `''` | If reference points to manifest / collections, then this parameter defines path to the file |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | `undefined` | Options that affects the request behavior |

#### Returns

`Promise`<[`FileData`](../interfaces/FileData.md)<`ReadableStream`<`Uint8Array`\>\>\>

#### Defined in

[bee-js/src/bee.ts:351](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L351)

___

### getAllPins

▸ **getAllPins**(`options?`): `Promise`<[`Reference`](../types/Reference.md)[]\>

Get list of all locally pinned references

**Warning! Not allowed when node is in Gateway mode!**

**`see`** [Bee docs - Pinning](https://docs.ethswarm.org/docs/access-the-swarm/pinning)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Reference`](../types/Reference.md)[]\>

#### Defined in

[bee-js/src/bee.ts:601](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L601)

___

### getAllTags

▸ **getAllTags**(`options?`): `Promise`<[`Tag`](../interfaces/Tag.md)[]\>

Fetches all tags.

The listing is limited by options.limit. So you have to iterate using options.offset to get all tags.

**Warning! Not allowed when node is in Gateway mode!**

**`throws`** TypeError if limit or offset are not numbers or undefined

**`throws`** BeeArgumentError if limit or offset have invalid options

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`see`** [Bee API reference - `GET /tags`](https://docs.ethswarm.org/api/#tag/Tag/paths/~1tags/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options?` | [`AllTagsOptions`](../interfaces/AllTagsOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Tag`](../interfaces/Tag.md)[]\>

#### Defined in

[bee-js/src/bee.ts:482](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L482)

___

### getJsonFeed

▸ **getJsonFeed**<`T`\>(`topic`, `options?`): `Promise`<`T`\>

High-level function that allows you to easily get data from feed.
Returned data are parsed using JSON.parse().

This method also supports specification of `signer` object passed to constructor. The order of evaluation is:
 - `options.address`
 - `options.signer`
 - `this.signer`

At least one of these has to be specified!

**`see`** [Bee docs - Feeds](https://docs.ethswarm.org/docs/dapps-on-swarm/feeds)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`AnyJson`](../types/AnyJson.md) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `topic` | `string` | Human readable string, that is internally hashed so there are no constrains there. |
| `options?` | [`JsonFeedOptions`](../interfaces/JsonFeedOptions.md) |  |

#### Returns

`Promise`<`T`\>

#### Defined in

[bee-js/src/bee.ts:1017](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L1017)

___

### getPin

▸ **getPin**(`reference`, `options?`): `Promise`<[`Pin`](../interfaces/Pin.md)\>

Get pinning status of chunk with given reference

**Warning! Not allowed when node is in Gateway mode!**

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** [Bee docs - Pinning](https://docs.ethswarm.org/docs/access-the-swarm/pinning)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | `string` \| [`Reference`](../types/Reference.md) | Bee data reference in hex string (either 64 or 128 chars long) or ENS domain. |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Pin`](../interfaces/Pin.md)\>

#### Defined in

[bee-js/src/bee.ts:619](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L619)

___

### isConnected

▸ **isConnected**(`options?`): `Promise`<`boolean`\>

Ping the Bee node to see if there is a live Bee node on the given URL.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`boolean`\>

true if successful, false on error

#### Defined in

[bee-js/src/bee.ts:1113](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L1113)

___

### isFeedRetrievable

▸ **isFeedRetrievable**(`type`, `owner`, `topic`, `index?`, `options?`): `Promise`<`boolean`\>

Functions that validates if feed is retrievable in the network.

If no index is passed then it check for "latest" update, which is a weaker guarantee as nobody can be really
sure what is the "latest" update.

If index is passed then it validates all previous sequence index chunks if they are available as they are required
to correctly resolve the feed upto the given index update.

#### Parameters

| Name | Type |
| :------ | :------ |
| `type` | ``"sequence"`` \| ``"epoch"`` |
| `owner` | `string` \| `Uint8Array` \| [`EthAddress`](../types/Utils.EthAddress.md) |
| `topic` | `string` \| `Uint8Array` \| [`Topic`](../types/Topic.md) |
| `index?` | `Index` |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[bee-js/src/bee.ts:676](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L676)

___

### isReferenceRetrievable

▸ **isReferenceRetrievable**(`reference`, `options?`): `Promise`<`boolean`\>

Checks if content specified by reference is retrievable from the network.

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** [Bee API reference - `GET /stewardship`](https://docs.ethswarm.org/api/#tag/Stewardship/paths/~1stewardship~1{reference}/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | [`ReferenceOrEns`](../types/ReferenceOrEns.md) | Bee data reference to be checked in hex string (either 64 or 128 chars long) or ENS domain. |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[bee-js/src/bee.ts:654](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L654)

___

### makeFeedReader

▸ **makeFeedReader**(`type`, `topic`, `owner`, `options?`): [`FeedReader`](../interfaces/FeedReader.md)

Make a new feed reader for downloading feed updates.

**`see`** [Bee docs - Feeds](https://docs.ethswarm.org/docs/dapps-on-swarm/feeds)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | ``"sequence"`` \| ``"epoch"`` | The type of the feed, can be 'epoch' or 'sequence' |
| `topic` | `string` \| `Uint8Array` \| [`Topic`](../types/Topic.md) | Topic in hex or bytes |
| `owner` | `string` \| `Uint8Array` \| [`EthAddress`](../types/Utils.EthAddress.md) | Owner's ethereum address in hex or bytes |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

[`FeedReader`](../interfaces/FeedReader.md)

#### Defined in

[bee-js/src/bee.ts:924](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L924)

___

### makeFeedTopic

▸ **makeFeedTopic**(`topic`): [`Topic`](../types/Topic.md)

Make a new feed topic from a string

Because the topic has to be 32 bytes long this function
hashes the input string to create a topic string of arbitrary length.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `topic` | `string` | The input string |

#### Returns

[`Topic`](../types/Topic.md)

#### Defined in

[bee-js/src/bee.ts:1056](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L1056)

___

### makeFeedWriter

▸ **makeFeedWriter**(`type`, `topic`, `signer?`, `options?`): [`FeedWriter`](../interfaces/FeedWriter.md)

Make a new feed writer for updating feeds

**`see`** [Bee docs - Feeds](https://docs.ethswarm.org/docs/dapps-on-swarm/feeds)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `type` | ``"sequence"`` \| ``"epoch"`` | The type of the feed, can be 'epoch' or 'sequence' |
| `topic` | `string` \| `Uint8Array` \| [`Topic`](../types/Topic.md) | Topic in hex or bytes |
| `signer?` | `string` \| `Uint8Array` \| [`Signer`](../types/Signer.md) | The signer's private key or a Signer instance that can sign data |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

[`FeedWriter`](../interfaces/FeedWriter.md)

#### Defined in

[bee-js/src/bee.ts:949](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L949)

___

### makeSOCReader

▸ **makeSOCReader**(`ownerAddress`, `options?`): [`SOCReader`](../interfaces/SOCReader.md)

Returns an object for reading single owner chunks

**`see`** [Bee docs - Chunk Types](https://docs.ethswarm.org/docs/dapps-on-swarm/chunk-types#single-owner-chunks)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `ownerAddress` | `string` \| `Uint8Array` \| [`EthAddress`](../types/Utils.EthAddress.md) | The ethereum address of the owner |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

[`SOCReader`](../interfaces/SOCReader.md)

#### Defined in

[bee-js/src/bee.ts:1067](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L1067)

___

### makeSOCWriter

▸ **makeSOCWriter**(`signer?`, `options?`): [`SOCWriter`](../interfaces/SOCWriter.md)

Returns an object for reading and writing single owner chunks

**`see`** [Bee docs - Chunk Types](https://docs.ethswarm.org/docs/dapps-on-swarm/chunk-types#single-owner-chunks)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `signer?` | `string` \| `Uint8Array` \| [`Signer`](../types/Signer.md) | The signer's private key or a Signer instance that can sign data |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

[`SOCWriter`](../interfaces/SOCWriter.md)

#### Defined in

[bee-js/src/bee.ts:1084](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L1084)

___

### pin

▸ **pin**(`reference`, `options?`): `Promise`<`void`\>

Pin local data with given reference

**Warning! Not allowed when node is in Gateway mode!**

**`throws`** TypeError if reference is in not correct format

**`see`** [Bee docs - Pinning](https://docs.ethswarm.org/docs/access-the-swarm/pinning)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | `string` \| [`Reference`](../types/Reference.md) | Data reference |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee.ts:568](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L568)

___

### pssReceive

▸ **pssReceive**(`topic`, `timeoutMsec?`): `Promise`<[`Data`](../interfaces/Data.md)\>

Receive message with Postal Service for Swarm

Because sending a PSS message is slow and CPU intensive,
it is not supposed to be used for general messaging but
most likely for setting up an encrypted communication
channel by sending an one-off message.

This is a helper function to wait for exactly one message to
arrive and then cancel the subscription. Additionally a
timeout can be provided for the message to arrive or else
an error will be thrown.

**Warning! Not allowed when node is in Gateway mode!**

**Warning! If connected Bee node is a light node, then he will never receive any message!**
This is because light nodes does not fully participate in the data exchange in Swarm network and hence the message won't arrive to them.

**`see`** [Bee docs - PSS](https://docs.ethswarm.org/docs/dapps-on-swarm/pss)

**`see`** [Bee API reference - `GET /pss`](https://docs.ethswarm.org/api/#tag/Postal-Service-for-Swarm/paths/~1pss~1subscribe~1{topic}/get)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `topic` | `string` | `undefined` | Topic name |
| `timeoutMsec` | `number` | `0` | Timeout in milliseconds |

#### Returns

`Promise`<[`Data`](../interfaces/Data.md)\>

Message in byte array

#### Defined in

[bee-js/src/bee.ts:847](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L847)

___

### pssSend

▸ **pssSend**(`postageBatchId`, `topic`, `target`, `data`, `recipient?`, `options?`): `Promise`<`void`\>

Send data to recipient or target with Postal Service for Swarm.

Because sending a PSS message is slow and CPU intensive,
it is not supposed to be used for general messaging but
most likely for setting up an encrypted communication
channel by sending an one-off message.

**Warning! Not allowed when node is in Gateway mode!**

**Warning! If the recipient Bee node is a light node, then he will never receive the message!**
This is because light nodes does not fully participate in the data exchange in Swarm network and hence the message won't arrive to them.

**`throws`** TypeError if `data`, `batchId`, `target` or `recipient` are in invalid format

**`see`** [Bee docs - PSS](https://docs.ethswarm.org/docs/dapps-on-swarm/pss)

**`see`** [Bee API reference - `POST /pss`](https://docs.ethswarm.org/api/#tag/Postal-Service-for-Swarm/paths/~1pss~1send~1{topic}~1{targets}/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId that will be assigned to sent message |
| `topic` | `string` | Topic name |
| `target` | [`AddressPrefix`](../types/AddressPrefix.md) | Target message address prefix. Has a limit on length. Recommend to use `Utils.Pss.makeMaxTarget()` to get the most specific target that Bee node will accept. |
| `data` | `string` \| `Uint8Array` | Message to be sent |
| `recipient?` | `string` \| [`PublicKey`](../types/PublicKey.md) | Recipient public key |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee.ts:734](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L734)

___

### pssSubscribe

▸ **pssSubscribe**(`topic`, `handler`): [`PssSubscription`](../interfaces/PssSubscription.md)

Subscribe to messages for given topic with Postal Service for Swarm

**Warning! Not allowed when node is in Gateway mode!**

**Warning! If connected Bee node is a light node, then he will never receive any message!**
This is because light nodes does not fully participate in the data exchange in Swarm network and hence the message won't arrive to them.

**`see`** [Bee docs - PSS](https://docs.ethswarm.org/docs/dapps-on-swarm/pss)

**`see`** [Bee API reference - `GET /pss`](https://docs.ethswarm.org/api/#tag/Postal-Service-for-Swarm/paths/~1pss~1subscribe~1{topic}/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `topic` | `string` | Topic name |
| `handler` | [`PssMessageHandler`](../interfaces/PssMessageHandler.md) | Message handler interface |

#### Returns

[`PssSubscription`](../interfaces/PssSubscription.md)

Subscription to a given topic

#### Defined in

[bee-js/src/bee.ts:776](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L776)

___

### retrieveTag

▸ **retrieveTag**(`tagUid`, `options?`): `Promise`<[`Tag`](../interfaces/Tag.md)\>

Retrieve tag information from Bee node

**Warning! Not allowed when node is in Gateway mode!**

**`throws`** TypeError if tagUid is in not correct format

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`see`** [Bee API reference - `GET /tags/{uid}`](https://docs.ethswarm.org/api/#tag/Tag/paths/~1tags~1{uid}/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tagUid` | `number` \| [`Tag`](../interfaces/Tag.md) | UID or tag object to be retrieved |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<[`Tag`](../interfaces/Tag.md)\>

#### Defined in

[bee-js/src/bee.ts:502](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L502)

___

### reuploadPinnedData

▸ **reuploadPinnedData**(`reference`, `options?`): `Promise`<`void`\>

Instructs the Bee node to reupload a locally pinned data into the network.

**`throws`** BeeArgumentError if the reference is not locally pinned

**`throws`** TypeError if some of the input parameters is not expected type

**`throws`** BeeArgumentError if there is passed ENS domain with invalid unicode characters

**`see`** [Bee API reference - `PUT /stewardship`](https://docs.ethswarm.org/api/#tag/Stewardship/paths/~1stewardship~1{reference}/put)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | [`ReferenceOrEns`](../types/ReferenceOrEns.md) | Bee data reference to be re-uploaded in hex string (either 64 or 128 chars long) or ENS domain. |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee.ts:637](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L637)

___

### setJsonFeed

▸ **setJsonFeed**<`T`\>(`postageBatchId`, `topic`, `data`, `options?`): `Promise`<[`Reference`](../types/Reference.md)\>

High-level function that allows you to easily set JSON data to feed.
JSON-like data types are supported.

The default Signer of Bee instance is used if `options.signer` is not specified.
If none of those two is set error is thrown.

**`throws`** BeeError if `options.signer` is not specified nor the default Signer on Bee's instance is specified.

**`see`** [Bee docs - Feeds](https://docs.ethswarm.org/docs/dapps-on-swarm/feeds)

#### Type parameters

| Name | Type |
| :------ | :------ |
| `T` | extends [`AnyJson`](../types/AnyJson.md) |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to upload the data with |
| `topic` | `string` | Human readable string, that is internally hashed so there are no constrains there. |
| `data` | `T` | JSON compatible data |
| `options?` | [`JsonFeedOptions`](../interfaces/JsonFeedOptions.md) |  |

#### Returns

`Promise`<[`Reference`](../types/Reference.md)\>

#### Defined in

[bee-js/src/bee.ts:982](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L982)

___

### unpin

▸ **unpin**(`reference`, `options?`): `Promise`<`void`\>

Unpin local data with given reference

**Warning! Not allowed when node is in Gateway mode!**

**`throws`** TypeError if reference is in not correct format

**`see`** [Bee docs - Pinning](https://docs.ethswarm.org/docs/access-the-swarm/pinning)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reference` | `string` \| [`Reference`](../types/Reference.md) | Data reference |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee.ts:586](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L586)

___

### updateTag

▸ **updateTag**(`tagUid`, `reference`, `options?`): `Promise`<`void`\>

Update tag's total chunks count.

This is important if you are uploading individual chunks with a tag. Then upon finishing the final root chunk,
you can use this method to update the total chunks count for the tag.

**Warning! Not allowed when node is in Gateway mode!**

**`throws`** TypeError if tagUid is in not correct format

**`throws`** BeeResponse error if something went wrong on the Bee node side while deleting the tag.

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`see`** [Bee API reference - `PATCH /tags/{uid}`](https://docs.ethswarm.org/api/#tag/Tag/paths/~1tags~1{uid}/patch)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tagUid` | `number` \| [`Tag`](../interfaces/Tag.md) | UID or tag object to be retrieved |
| `reference` | `string` \| [`Reference`](../types/Reference.md) | The root reference that contains all the chunks to be counted |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Options that affects the request behavior |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee.ts:548](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L548)

___

### uploadChunk

▸ **uploadChunk**(`postageBatchId`, `data`, `options?`): `Promise`<[`Reference`](../types/Reference.md)\>

Upload chunk to a Bee node

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `POST /chunks`](https://docs.ethswarm.org/api/#tag/Chunk/paths/~1chunks/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to upload the chunk with |
| `data` | `Uint8Array` | Raw chunk to be uploaded |
| `options?` | [`UploadOptions`](../interfaces/UploadOptions.md) | Additional options like tag, encryption, pinning, content-type and request options |

#### Returns

`Promise`<[`Reference`](../types/Reference.md)\>

reference is a content hash of the data

#### Defined in

[bee-js/src/bee.ts:224](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L224)

___

### uploadCollection

▸ **uploadCollection**(`postageBatchId`, `collection`, `options?`): `Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

Upload Collection that you can assembly yourself.

The returned `UploadResult.tag` might be undefined if called in CORS-enabled environment.
This will be fixed upon next Bee release. https://github.com/ethersphere/bee-js/issues/406

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) |  |
| `collection` | [`Collection`](../types/Collection.md)<`Uint8Array` \| [`Readable`](../types/Readable.md)\> |  |
| `options?` | [`CollectionUploadOptions`](../interfaces/CollectionUploadOptions.md) | Collections and request options |

#### Returns

`Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

#### Defined in

[bee-js/src/bee.ts:405](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L405)

___

### uploadData

▸ **uploadData**(`postageBatchId`, `data`, `options?`): `Promise`<[`UploadResult`](../interfaces/UploadResult.md)\>

Upload data to a Bee node

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `POST /bytes`](https://docs.ethswarm.org/api/#tag/Bytes/paths/~1bytes/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to upload the data with |
| `data` | `string` \| `Uint8Array` | Data to be uploaded |
| `options?` | [`UploadOptions`](../interfaces/UploadOptions.md) | Additional options like tag, encryption, pinning, content-type and request options |

#### Returns

`Promise`<[`UploadResult`](../interfaces/UploadResult.md)\>

reference is a content hash of the data

#### Defined in

[bee-js/src/bee.ts:163](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L163)

___

### uploadFile

▸ **uploadFile**(`postageBatchId`, `data`, `name?`, `options?`): `Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

Upload single file to a Bee node.

**To make sure that you won't loose critical data it is highly recommended to also
locally pin the data with `options.pin = true`**

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee docs - Upload and download](https://docs.ethswarm.org/docs/access-the-swarm/upload-and-download)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/File/paths/~1bzz/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to upload the data with |
| `data` | `string` \| `File` \| `Uint8Array` \| [`Readable`](../types/Readable.md) | Data or file to be uploaded |
| `name?` | `string` | Optional name of the uploaded file |
| `options?` | [`FileUploadOptions`](../interfaces/FileUploadOptions.md) | Additional options like tag, encryption, pinning, content-type and request options |

#### Returns

`Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

reference is a content hash of the file

#### Defined in

[bee-js/src/bee.ts:277](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L277)

___

### uploadFiles

▸ **uploadFiles**(`postageBatchId`, `fileList`, `options?`): `Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

Upload collection of files to a Bee node

Uses the FileList API from the browser.

The returned `UploadResult.tag` might be undefined if called in CORS-enabled environment.
This will be fixed upon next Bee release. https://github.com/ethersphere/bee-js/issues/406

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee docs - Upload directory](https://docs.ethswarm.org/docs/access-the-swarm/upload-a-directory/)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to upload the data with |
| `fileList` | `FileList` \| `File`[] | list of files to be uploaded |
| `options?` | [`CollectionUploadOptions`](../interfaces/CollectionUploadOptions.md) | Additional options like tag, encryption, pinning and request options |

#### Returns

`Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

#### Defined in

[bee-js/src/bee.ts:378](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L378)

___

### uploadFilesFromDirectory

▸ **uploadFilesFromDirectory**(`postageBatchId`, `dir`, `options?`): `Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

Upload collection of files.

Available only in Node.js as it uses the `fs` module.

The returned `UploadResult.tag` might be undefined if called in CORS-enabled environment.
This will be fixed upon next Bee release. https://github.com/ethersphere/bee-js/issues/406

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee docs - Upload directory](https://docs.ethswarm.org/docs/access-the-swarm/upload-a-directory/)

**`see`** [Bee API reference - `POST /bzz`](https://docs.ethswarm.org/api/#tag/Collection/paths/~1bzz/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to upload the data with |
| `dir` | `string` | the path of the files to be uploaded |
| `options?` | [`CollectionUploadOptions`](../interfaces/CollectionUploadOptions.md) | Additional options like tag, encryption, pinning and request options |

#### Returns

`Promise`<[`UploadResultWithCid`](../interfaces/UploadResultWithCid.md)\>

#### Defined in

[bee-js/src/bee.ts:437](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee.ts#L437)
