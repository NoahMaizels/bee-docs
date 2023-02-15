---
id: "Utils.PrefixedHexString"
title: "Type alias: PrefixedHexString"
sidebar_label: "PrefixedHexString"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).PrefixedHexString

Ƭ **PrefixedHexString**: [`BrandedType`](BrandedType.md)<`string`, ``"PrefixedHexString"``\>

Type for HexString with prefix.
The main hex type used internally should be non-prefixed HexString
and therefore this type should be used as least as possible.
Because of that it does not contain the Length property as the variables
should be validated and converted to HexString ASAP.

#### Defined in

[bee-js/src/utils/hex.ts:23](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/hex.ts#L23)
