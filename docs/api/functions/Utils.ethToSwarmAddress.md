---
id: "Utils.ethToSwarmAddress"
title: "Function: ethToSwarmAddress"
sidebar_label: "ethToSwarmAddress"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).ethToSwarmAddress

▸ **ethToSwarmAddress**(`ethAddress`, `networkId?`): `OverlayAddress`

Get swarm overlay address from public ethereum address and swarm network id

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `ethAddress` | `string` \| `HexEthAddress` \| [`HexString`](../types/Utils.HexString.md)<`number`\> | `undefined` | Public ethereum address |
| `networkId` | `number` | `1` | Swarm network id |

#### Returns

`OverlayAddress`

Swarm overlay address

#### Defined in

[bee-js/src/utils/eth.ts:165](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/eth.ts#L165)
