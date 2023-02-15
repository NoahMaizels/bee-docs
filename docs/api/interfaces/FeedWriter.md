---
id: "FeedWriter"
title: "Interface: FeedWriter"
sidebar_label: "FeedWriter"
sidebar_position: 0
custom_edit_url: null
---

FeedWriter is an interface for updating feeds

## Hierarchy

- [`FeedReader`](FeedReader.md)

  ↳ **`FeedWriter`**

## Properties

### owner

• `Readonly` **owner**: `HexEthAddress`

#### Inherited from

[FeedReader](FeedReader.md).[owner](FeedReader.md#owner)

#### Defined in

[bee-js/src/types/index.ts:406](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L406)

___

### topic

• `Readonly` **topic**: [`Topic`](../types/Topic.md)

#### Inherited from

[FeedReader](FeedReader.md).[topic](FeedReader.md#topic)

#### Defined in

[bee-js/src/types/index.ts:407](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L407)

___

### type

• `Readonly` **type**: ``"sequence"`` \| ``"epoch"``

#### Inherited from

[FeedReader](FeedReader.md).[type](FeedReader.md#type)

#### Defined in

[bee-js/src/types/index.ts:405](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L405)

## Methods

### download

▸ **download**(`options?`): `Promise`<`FetchFeedUpdateResponse`\>

Download the latest feed update

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | `FeedUpdateOptions` |

#### Returns

`Promise`<`FetchFeedUpdateResponse`\>

#### Inherited from

[FeedReader](FeedReader.md).[download](FeedReader.md#download)

#### Defined in

[bee-js/src/types/index.ts:411](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L411)

___

### upload

▸ **upload**(`postageBatchId`, `reference`, `options?`): `Promise`<[`Reference`](../types/Reference.md)\>

Upload a new feed update

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Postage BatchId to be used to upload the data with |
| `reference` | [`Reference`](../types/Reference.md) \| [`BytesReference`](../types/BytesReference.md) | The reference to be stored in the new update |
| `options?` | `FeedUploadOptions` | Additional options like `at` |

#### Returns

`Promise`<[`Reference`](../types/Reference.md)\>

Reference that points at Single Owner Chunk that contains the new update and pointer to the updated chunk reference.

#### Defined in

[bee-js/src/types/index.ts:443](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L443)
