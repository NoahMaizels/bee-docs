---
id: "SOCWriter"
title: "Interface: SOCWriter"
sidebar_label: "SOCWriter"
sidebar_position: 0
custom_edit_url: null
---

Interface for downloading and uploading single owner chunks

## Hierarchy

- [`SOCReader`](SOCReader.md)

  ↳ **`SOCWriter`**

## Properties

### owner

• `Readonly` **owner**: `HexEthAddress`

#### Inherited from

[SOCReader](SOCReader.md).[owner](SOCReader.md#owner)

#### Defined in

[bee-js/src/types/index.ts:454](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L454)

## Methods

### download

▸ **download**(`identifier`): `Promise`<`SingleOwnerChunk`\>

Downloads a single owner chunk

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `identifier` | `Identifier` | The identifier of the chunk |

#### Returns

`Promise`<`SingleOwnerChunk`\>

#### Inherited from

[SOCReader](SOCReader.md).[download](SOCReader.md#download)

#### Defined in

[bee-js/src/types/index.ts:460](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L460)

___

### upload

▸ **upload**(`postageBatchId`, `identifier`, `data`, `options?`): `Promise`<[`Reference`](../types/Reference.md)\>

Uploads a single owner chunk

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | - |
| `identifier` | `Identifier` | The identifier of the chunk |
| `data` | `Uint8Array` | The chunk payload data |
| `options?` | [`UploadOptions`](UploadOptions.md) | Upload options |

#### Returns

`Promise`<[`Reference`](../types/Reference.md)\>

#### Defined in

[bee-js/src/types/index.ts:474](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L474)
