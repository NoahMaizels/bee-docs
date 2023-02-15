---
id: "NodeInfo"
title: "Interface: NodeInfo"
sidebar_label: "NodeInfo"
sidebar_position: 0
custom_edit_url: null
---

Information about Bee node and its configuration

## Properties

### beeMode

• **beeMode**: [`BeeModes`](../enums/BeeModes.md)

Indicates in what mode Bee is running.

#### Defined in

[bee-js/src/types/debug.ts:180](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/debug.ts#L180)

___

### chequebookEnabled

• **chequebookEnabled**: `boolean`

Indicates whether the Bee node has its own deployed chequebook.

**`see`** [Bee docs - Chequebook](https://docs.ethswarm.org/docs/introduction/terminology#cheques--chequebook)

#### Defined in

[bee-js/src/types/debug.ts:187](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/debug.ts#L187)

___

### gatewayMode

• **gatewayMode**: `boolean`

Indicates whether the node is in a Gateway mode.
Gateway mode is a restricted mode where some features are not available.

#### Defined in

[bee-js/src/types/debug.ts:175](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/debug.ts#L175)

___

### swapEnabled

• **swapEnabled**: `boolean`

Indicates whether SWAP is enabled for the Bee node.

**`see`** [Bee docs - SWAP](https://docs.ethswarm.org/docs/introduction/terminology#swap)

#### Defined in

[bee-js/src/types/debug.ts:194](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/debug.ts#L194)
