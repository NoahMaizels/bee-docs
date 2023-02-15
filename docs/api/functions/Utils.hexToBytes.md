---
id: "Utils.hexToBytes"
title: "Function: hexToBytes"
sidebar_label: "hexToBytes"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).hexToBytes

▸ **hexToBytes**<`Length`, `LengthHex`\>(`hex`): [`Bytes`](../interfaces/Utils.Bytes.md)<`Length`\>

Converts a hex string to Uint8Array

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Length` | extends `number` |
| `LengthHex` | extends `number` = `number` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `hex` | [`HexString`](../types/Utils.HexString.md)<`LengthHex`\> | string input without 0x prefix! |

#### Returns

[`Bytes`](../interfaces/Utils.Bytes.md)<`Length`\>

#### Defined in

[bee-js/src/utils/hex.ts:69](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/hex.ts#L69)
