---
id: "SOCReader"
title: "Interface: SOCReader"
sidebar_label: "SOCReader"
sidebar_position: 0
custom_edit_url: null
---

Interface for downloading single owner chunks

## Hierarchy

- **`SOCReader`**

  ↳ [`SOCWriter`](SOCWriter.md)

## Properties

### owner

• `Readonly` **owner**: `HexEthAddress`

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

#### Defined in

[bee-js/src/types/index.ts:460](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L460)
