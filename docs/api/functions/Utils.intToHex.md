---
id: "Utils.intToHex"
title: "Function: intToHex"
sidebar_label: "intToHex"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).intToHex

▸ **intToHex**<`Length`\>(`int`, `len?`): [`HexString`](../types/Utils.HexString.md)<`Length`\>

Converts integer number to hex string.

Optionally provides '0x' prefix or padding

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Length` | extends `number` = `number` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `int` | `number` | The positive integer to be converted |
| `len?` | `Length` | The length of the non prefixed HexString |

#### Returns

[`HexString`](../types/Utils.HexString.md)<`Length`\>

#### Defined in

[bee-js/src/utils/hex.ts:109](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/hex.ts#L109)
