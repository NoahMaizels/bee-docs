---
id: "Utils.makeHexString"
title: "Function: makeHexString"
sidebar_label: "makeHexString"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).makeHexString

▸ **makeHexString**<`L`\>(`input`, `len?`): [`HexString`](../types/Utils.HexString.md)<`L`\>

Creates unprefixed hex string from wide range of data.

TODO: Make Length mandatory: https://github.com/ethersphere/bee-js/issues/208

#### Type parameters

| Name | Type |
| :------ | :------ |
| `L` | extends `number` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `input` | `unknown` |  |
| `len?` | `L` | of the resulting HexString WITHOUT prefix! |

#### Returns

[`HexString`](../types/Utils.HexString.md)<`L`\>

#### Defined in

[bee-js/src/utils/hex.ts:33](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/hex.ts#L33)
