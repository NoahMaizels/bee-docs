---
id: "Utils.toLittleEndian"
title: "Function: toLittleEndian"
sidebar_label: "toLittleEndian"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).toLittleEndian

▸ **toLittleEndian**(`bigEndian`, `pad?`): [`HexString`](../types/Utils.HexString.md) \| `never`

Convert big-endian hex or number to little-endian.
Note: Before conversion it is automatically padded to even length hexstring

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `bigEndian` | `string` \| `number` \| [`HexString`](../types/Utils.HexString.md)<`number`\> | `undefined` | Big-endian hex string or number to convert |
| `pad` | `number` | `2` | Length to which the string should be padded before conversion (defaul: 2) |

#### Returns

[`HexString`](../types/Utils.HexString.md) \| `never`

little-endian encoded hexstring

#### Defined in

[bee-js/src/utils/eth.ts:109](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/eth.ts#L109)
