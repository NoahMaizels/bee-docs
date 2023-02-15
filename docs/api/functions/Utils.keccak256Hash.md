---
id: "Utils.keccak256Hash"
title: "Function: keccak256Hash"
sidebar_label: "keccak256Hash"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).keccak256Hash

▸ **keccak256Hash**(...`messages`): [`Bytes`](../interfaces/Utils.Bytes.md)<``32``\>

Helper function for calculating the keccak256 hash with
correct types.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `...messages` | `Message`[] | Any number of messages (strings, byte arrays etc.) |

#### Returns

[`Bytes`](../interfaces/Utils.Bytes.md)<``32``\>

#### Defined in

[bee-js/src/utils/hash.ts:13](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/hash.ts#L13)
