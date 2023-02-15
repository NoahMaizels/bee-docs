---
id: "Tag"
title: "Interface: Tag"
sidebar_label: "Tag"
sidebar_position: 0
custom_edit_url: null
---

Object that contains infromation about progress of upload of data to network.

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

## Properties

### processed

• **processed**: `number`

Number of chunks that is locally stored in the Bee node.

#### Defined in

[bee-js/src/types/index.ts:274](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L274)

___

### startedAt

• **startedAt**: `string`

When the upload process started

#### Defined in

[bee-js/src/types/index.ts:289](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L289)

___

### synced

• **synced**: `number`

Number of chunks that arrived to their designated destination in the network

#### Defined in

[bee-js/src/types/index.ts:279](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L279)

___

### total

• **total**: `number`

Number of all chunks that the data will be split into.

#### Defined in

[bee-js/src/types/index.ts:269](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L269)

___

### uid

• **uid**: `number`

Unique identifier

#### Defined in

[bee-js/src/types/index.ts:284](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L284)
