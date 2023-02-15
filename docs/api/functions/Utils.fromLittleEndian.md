---
id: "Utils.fromLittleEndian"
title: "Function: fromLittleEndian"
sidebar_label: "fromLittleEndian"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).fromLittleEndian

▸ **fromLittleEndian**(`littleEndian`, `pad?`): [`HexString`](../types/Utils.HexString.md) \| `never`

Convert little-endian hex or number to big-endian
Note: Before conversion it is automatically padded to even length hexstring

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `littleEndian` | `string` \| `number` \| [`HexString`](../types/Utils.HexString.md)<`number`\> | `undefined` | Little-endian hex string or number to convert |
| `pad` | `number` | `2` | Length to which the string should be padded before conversion (defaul: 2) |

#### Returns

[`HexString`](../types/Utils.HexString.md) \| `never`

big-endian encoded hexstring

#### Defined in

[bee-js/src/utils/eth.ts:142](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/eth.ts#L142)
