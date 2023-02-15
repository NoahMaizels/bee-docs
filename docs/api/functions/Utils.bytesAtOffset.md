---
id: "Utils.bytesAtOffset"
title: "Function: bytesAtOffset"
sidebar_label: "bytesAtOffset"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).bytesAtOffset

▸ **bytesAtOffset**<`Length`\>(`data`, `offset`, `length`): [`Bytes`](../interfaces/Utils.Bytes.md)<`Length`\>

Return `length` bytes starting from `offset`

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Length` | extends `number` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `data` | `Uint8Array` | The original data |
| `offset` | `number` | The offset to start from |
| `length` | `Length` | The length of data to be returned |

#### Returns

[`Bytes`](../interfaces/Utils.Bytes.md)<`Length`\>

#### Defined in

[bee-js/src/utils/bytes.ts:107](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/bytes.ts#L107)
