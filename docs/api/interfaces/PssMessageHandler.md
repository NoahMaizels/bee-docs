---
id: "PssMessageHandler"
title: "Interface: PssMessageHandler"
sidebar_label: "PssMessageHandler"
sidebar_position: 0
custom_edit_url: null
---

## Methods

### onError

▸ **onError**(`error`, `subscription`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `error` | [`BeeError`](../classes/BeeError.md) |
| `subscription` | [`PssSubscription`](PssSubscription.md) |

#### Returns

`void`

#### Defined in

[bee-js/src/types/index.ts:359](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L359)

___

### onMessage

▸ **onMessage**(`message`, `subscription`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `message` | [`Data`](Data.md) |
| `subscription` | [`PssSubscription`](PssSubscription.md) |

#### Returns

`void`

#### Defined in

[bee-js/src/types/index.ts:358](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L358)
