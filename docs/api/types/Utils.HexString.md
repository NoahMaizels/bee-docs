---
id: "Utils.HexString"
title: "Type alias: HexString<Length>"
sidebar_label: "HexString"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).HexString

Ƭ **HexString**<`Length`\>: [`FlavoredType`](FlavoredType.md)<`string` & { `length`: `Length`  }, ``"HexString"``\>

Nominal type to represent hex strings WITHOUT '0x' prefix.
For example for 32 bytes hex representation you have to use 64 length.
TODO: Make Length mandatory: https://github.com/ethersphere/bee-js/issues/208

#### Type parameters

| Name | Type |
| :------ | :------ |
| `Length` | extends `number` = `number` |

#### Defined in

[bee-js/src/utils/hex.ts:9](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/hex.ts#L9)
