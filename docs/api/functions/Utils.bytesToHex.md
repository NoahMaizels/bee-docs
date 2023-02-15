---
id: "Utils.bytesToHex"
title: "Function: bytesToHex"
sidebar_label: "bytesToHex"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).bytesToHex

▸ **bytesToHex**<`Length`\>(`bytes`, `len?`): [`HexString`](../types/Utils.HexString.md)<`Length`\>

Converts array of number or Uint8Array to HexString without prefix.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Length` | extends `number` = `number` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bytes` | `Uint8Array` | The input array |
| `len?` | `Length` | The length of the non prefixed HexString |

#### Returns

[`HexString`](../types/Utils.HexString.md)<`Length`\>

#### Defined in

[bee-js/src/utils/hex.ts:89](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/hex.ts#L89)
