---
id: "FeedReader"
title: "Interface: FeedReader"
sidebar_label: "FeedReader"
sidebar_position: 0
custom_edit_url: null
---

FeedReader is an interface for downloading feed updates

## Hierarchy

- **`FeedReader`**

  ↳ [`FeedWriter`](FeedWriter.md)

## Properties

### owner

• `Readonly` **owner**: `HexEthAddress`

#### Defined in

[bee-js/src/types/index.ts:406](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L406)

___

### topic

• `Readonly` **topic**: [`Topic`](../types/Topic.md)

#### Defined in

[bee-js/src/types/index.ts:407](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L407)

___

### type

• `Readonly` **type**: ``"sequence"`` \| ``"epoch"``

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

#### Defined in

[bee-js/src/types/index.ts:411](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L411)
