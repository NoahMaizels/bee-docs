---
id: "Utils.getStampUsage"
title: "Function: getStampUsage"
sidebar_label: "getStampUsage"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).getStampUsage

▸ **getStampUsage**(`__namedParameters`): `number`

Utility function that calculates usage of postage batch based on its utilization, depth and bucket depth.

Be aware for small depths (17, 18) this does not provide that much information as the provided set of distinct values
is small.

#### Parameters

| Name | Type |
| :------ | :------ |
| `__namedParameters` | [`PostageBatch`](../interfaces/PostageBatch.md) |

#### Returns

`number`

#### Defined in

[bee-js/src/utils/stamps.ts:13](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/stamps.ts#L13)
