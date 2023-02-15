---
id: "BeeDebug"
title: "Class: BeeDebug"
sidebar_label: "BeeDebug"
sidebar_position: 0
custom_edit_url: null
---

## Constructors

### constructor

• **new BeeDebug**(`url`, `options?`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `url` | `string` |
| `options?` | [`BeeOptions`](../interfaces/BeeOptions.md) |

#### Defined in

[bee-js/src/bee-debug.ts:79](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L79)

## Properties

### url

• `Readonly` **url**: `string`

URL on which is the Debug API of Bee node exposed

#### Defined in

[bee-js/src/bee-debug.ts:71](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L71)

## Methods

### cancelPendingTransaction

▸ **cancelPendingTransaction**(`transactionHash`, `gasPrice?`, `options?`): `Promise`<[`TransactionHash`](../types/TransactionHash.md)\>

Cancel currently pending transaction

#### Parameters

| Name | Type |
| :------ | :------ |
| `transactionHash` | `string` \| [`TransactionHash`](../types/TransactionHash.md) |
| `gasPrice?` | [`NumberString`](../types/NumberString.md) |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`TransactionHash`](../types/TransactionHash.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:673](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L673)

___

### cashoutLastCheque

▸ **cashoutLastCheque**(`address`, `options?`): `Promise`<`string`\>

Cashout the last cheque for the peer

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `address` | `string` \| [`Address`](../types/Address.md) | Swarm address of peer |
| `options?` | [`CashoutOptions`](../interfaces/CashoutOptions.md) |  |

#### Returns

`Promise`<`string`\>

#### Defined in

[bee-js/src/bee-debug.ts:293](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L293)

___

### createPostageBatch

▸ **createPostageBatch**(`amount`, `depth`, `options?`): `Promise`<[`BatchId`](../types/BatchId.md)\>

Creates new postage batch from the funds that the node has available in its Ethereum account.

For better understanding what each parameter means and what are the optimal values please see
[Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive).

**WARNING: THIS CREATES TRANSACTIONS THAT SPENDS MONEY**

**`throws`** BeeArgumentError when negative amount or depth is specified

**`throws`** TypeError if non-integer value is passed to amount or depth

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee Debug API reference - `POST /stamps`](https://docs.ethswarm.org/debug-api/#tag/Postage-Stamps/paths/~1stamps~1{amount}~1{depth}/post)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amount` | [`NumberString`](../types/NumberString.md) | Amount that represents the value per chunk, has to be greater or equal zero. |
| `depth` | `number` | Logarithm of the number of chunks that can be stamped with the batch. |
| `options?` | [`PostageBatchOptions`](../interfaces/PostageBatchOptions.md) | Options for creation of postage batch |

#### Returns

`Promise`<[`BatchId`](../types/BatchId.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:515](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L515)

___

### depositTokens

▸ **depositTokens**(`amount`, `gasPrice?`, `options?`): `Promise`<`string`\>

Deposit tokens from overlay address into chequebook

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amount` | `number` \| [`NumberString`](../types/NumberString.md) | Amount of tokens to deposit (must be positive integer) |
| `gasPrice?` | [`NumberString`](../types/NumberString.md) | Gas Price in WEI for the transaction call |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<`string`\>

string  Hash of the transaction

#### Defined in

[bee-js/src/bee-debug.ts:307](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L307)

___

### diluteBatch

▸ **diluteBatch**(`postageBatchId`, `depth`, `options?`): `Promise`<`void`\>

Dilute given Postage Batch with new depth (that has to be bigger then the original depth), which allows
the Postage Batch to be used for more chunks.

For better understanding what each parameter means and what are the optimal values please see
[Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive).

**WARNING: THIS CREATES TRANSACTIONS THAT SPENDS MONEY**

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee Debug API reference - `PATCH /stamps/topup/${id}/${amount}`](https://docs.ethswarm.org/debug-api/#tag/Postage-Stamps/paths/~1stamps~1topup~1{id}~1{amount}/patch)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Batch ID |
| `depth` | `number` | Amount to be added to the batch |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Request options |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee-debug.ts:576](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L576)

___

### getAllBalances

▸ **getAllBalances**(`options?`): `Promise`<[`BalanceResponse`](../interfaces/BalanceResponse.md)\>

Get the balances with all known peers including prepaid services

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`BalanceResponse`](../interfaces/BalanceResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:185](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L185)

___

### getAllPendingTransactions

▸ **getAllPendingTransactions**(`options?`): `Promise`<[`TransactionInfo`](../interfaces/TransactionInfo.md)[]\>

Return lists of all current pending transactions that the Bee made

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`TransactionInfo`](../interfaces/TransactionInfo.md)[]\>

#### Defined in

[bee-js/src/bee-debug.ts:632](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L632)

___

### getAllPostageBatch

▸ **getAllPostageBatch**(`options?`): `Promise`<[`PostageBatch`](../interfaces/PostageBatch.md)[]\>

Return all postage batches that has the node available.

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee Debug API reference - `GET /stamps`](https://docs.ethswarm.org/debug-api/#tag/Postage-Stamps/paths/~1stamps/get)

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`PostageBatch`](../interfaces/PostageBatch.md)[]\>

#### Defined in

[bee-js/src/bee-debug.ts:623](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L623)

___

### getAllSettlements

▸ **getAllSettlements**(`options?`): `Promise`<[`AllSettlements`](../interfaces/AllSettlements.md)\>

Get settlements with all known peers and total amount sent or received

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`AllSettlements`](../interfaces/AllSettlements.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:363](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L363)

___

### getBlocklist

▸ **getBlocklist**(`options?`): `Promise`<[`Peer`](../interfaces/Peer.md)[]\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`Peer`](../interfaces/Peer.md)[]\>

#### Defined in

[bee-js/src/bee-debug.ts:119](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L119)

___

### getChainState

▸ **getChainState**(`options?`): `Promise`<[`ChainState`](../interfaces/ChainState.md)\>

Get chain state

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`ChainState`](../interfaces/ChainState.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:481](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L481)

___

### getChequebookAddress

▸ **getChequebookAddress**(`options?`): `Promise`<[`ChequebookAddressResponse`](../interfaces/ChequebookAddressResponse.md)\>

Get the address of the chequebook contract used.

**Warning:** The address is returned with 0x prefix unlike all other calls.
https://github.com/ethersphere/bee/issues/1443

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`ChequebookAddressResponse`](../interfaces/ChequebookAddressResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:234](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L234)

___

### getChequebookBalance

▸ **getChequebookBalance**(`options?`): `Promise`<[`ChequebookBalanceResponse`](../interfaces/ChequebookBalanceResponse.md)\>

Get the balance of the chequebook

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`ChequebookBalanceResponse`](../interfaces/ChequebookBalanceResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:243](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L243)

___

### getHealth

▸ **getHealth**(`options?`): `Promise`<[`Health`](../interfaces/Health.md)\>

Get health of node

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`Health`](../interfaces/Health.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:372](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L372)

___

### getLastCashoutAction

▸ **getLastCashoutAction**(`address`, `options?`): `Promise`<[`LastCashoutActionResponse`](../interfaces/LastCashoutActionResponse.md)\>

Get last cashout action for the peer

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `address` | `string` \| [`Address`](../types/Address.md) | Swarm address of peer |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`LastCashoutActionResponse`](../interfaces/LastCashoutActionResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:278](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L278)

___

### getLastCheques

▸ **getLastCheques**(`options?`): `Promise`<[`LastChequesResponse`](../interfaces/LastChequesResponse.md)\>

Get last cheques for all peers

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`LastChequesResponse`](../interfaces/LastChequesResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:252](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L252)

___

### getLastChequesForPeer

▸ **getLastChequesForPeer**(`address`, `options?`): `Promise`<[`LastChequesForPeerResponse`](../interfaces/LastChequesForPeerResponse.md)\>

Get last cheques for the peer

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `address` | `string` \| [`Address`](../types/Address.md) | Swarm address of peer |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`LastChequesForPeerResponse`](../interfaces/LastChequesForPeerResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:263](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L263)

___

### getNodeAddresses

▸ **getNodeAddresses**(`options?`): `Promise`<[`NodeAddresses`](../interfaces/NodeAddresses.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`NodeAddresses`](../interfaces/NodeAddresses.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:113](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L113)

___

### getNodeInfo

▸ **getNodeInfo**(`options?`): `Promise`<[`NodeInfo`](../interfaces/NodeInfo.md)\>

Get mode information of node

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`NodeInfo`](../interfaces/NodeInfo.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:381](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L381)

___

### getPastDueConsumptionBalances

▸ **getPastDueConsumptionBalances**(`options?`): `Promise`<[`BalanceResponse`](../interfaces/BalanceResponse.md)\>

Get the past due consumption balances with all known peers

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`BalanceResponse`](../interfaces/BalanceResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:206](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L206)

___

### getPastDueConsumptionPeerBalance

▸ **getPastDueConsumptionPeerBalance**(`address`, `options?`): `Promise`<[`PeerBalance`](../interfaces/PeerBalance.md)\>

Get the past due consumption balance with a specific peer

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `address` | `string` \| [`Address`](../types/Address.md) | Swarm address of peer |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`PeerBalance`](../interfaces/PeerBalance.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:217](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L217)

___

### getPeerBalance

▸ **getPeerBalance**(`address`, `options?`): `Promise`<[`PeerBalance`](../interfaces/PeerBalance.md)\>

Get the balances with a specific peer including prepaid services

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `address` | `string` \| [`Address`](../types/Address.md) | Swarm address of peer |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`PeerBalance`](../interfaces/PeerBalance.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:196](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L196)

___

### getPeers

▸ **getPeers**(`options?`): `Promise`<[`Peer`](../interfaces/Peer.md)[]\>

Get list of peers for this node

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`Peer`](../interfaces/Peer.md)[]\>

#### Defined in

[bee-js/src/bee-debug.ts:152](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L152)

___

### getPendingTransaction

▸ **getPendingTransaction**(`transactionHash`, `options?`): `Promise`<[`TransactionInfo`](../interfaces/TransactionInfo.md)\>

Return transaction information for specific transaction

#### Parameters

| Name | Type |
| :------ | :------ |
| `transactionHash` | `string` \| [`TransactionHash`](../types/TransactionHash.md) |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`TransactionInfo`](../interfaces/TransactionInfo.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:642](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L642)

___

### getPostageBatch

▸ **getPostageBatch**(`postageBatchId`, `options?`): `Promise`<[`PostageBatch`](../interfaces/PostageBatch.md)\>

Return details for specific postage batch.

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee Debug API reference - `GET /stamps/${id}`](https://docs.ethswarm.org/debug-api/#tag/Postage-Stamps/paths/~1stamps~1{id}/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Batch ID |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`PostageBatch`](../interfaces/PostageBatch.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:592](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L592)

___

### getPostageBatchBuckets

▸ **getPostageBatchBuckets**(`postageBatchId`, `options?`): `Promise`<[`PostageBatchBuckets`](../interfaces/PostageBatchBuckets.md)\>

Return detailed information related to buckets for specific postage batch.

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee Debug API reference - `GET /stamps/${id}/buckets`](https://docs.ethswarm.org/debug-api/#tag/Postage-Stamps/paths/~1stamps~1{id}~1buckets/get)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Batch ID |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`PostageBatchBuckets`](../interfaces/PostageBatchBuckets.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:607](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L607)

___

### getReserveState

▸ **getReserveState**(`options?`): `Promise`<[`ReserveState`](../interfaces/ReserveState.md)\>

Get reserve state

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`ReserveState`](../interfaces/ReserveState.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:472](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L472)

___

### getSettlements

▸ **getSettlements**(`address`, `options?`): `Promise`<[`Settlements`](../interfaces/Settlements.md)\>

Get amount of sent and received from settlements with a peer

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `address` | `string` \| [`Address`](../types/Address.md) | Swarm address of peer |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`Settlements`](../interfaces/Settlements.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:353](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L353)

___

### getTopology

▸ **getTopology**(`options?`): `Promise`<[`Topology`](../interfaces/Topology.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`Topology`](../interfaces/Topology.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:165](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L165)

___

### getVersions

▸ **getVersions**(`options?`): `Promise`<[`BeeVersions`](../interfaces/BeeVersions.md)\>

Returns object with all versions specified by the connected Bee node (properties prefixed with `bee*`)
and versions that bee-js supports (properties prefixed with `supported*`).

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`BeeVersions`](../interfaces/BeeVersions.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:463](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L463)

___

### getWalletBalance

▸ **getWalletBalance**(`options?`): `Promise`<[`WalletBalance`](../interfaces/WalletBalance.md)\>

Get wallet balances for xDai and BZZ of the Bee node

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`WalletBalance`](../interfaces/WalletBalance.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:492](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L492)

___

### isSupportedApiVersion

▸ **isSupportedApiVersion**(`options?`): `Promise`<`boolean`\>

Connects to a node and checks if its Main and Debug API versions matches with the one that bee-js supports.

This should be the main way how to check compatibility for your app and Bee node.

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[bee-js/src/bee-debug.ts:451](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L451)

___

### isSupportedDebugApiVersion

▸ **isSupportedDebugApiVersion**(`options?`): `Promise`<`boolean`\>

Connects to a node and checks if its Debug API version matches with the one that bee-js supports.

This is useful if you are not using `Bee` class in your application and want to make sure
about compatibility.

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[bee-js/src/bee-debug.ts:437](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L437)

___

### isSupportedExactVersion

▸ **isSupportedExactVersion**(`options?`): `Promise`<`boolean`\>

Connects to a node and checks if its version matches with the one that bee-js supports.

Be aware that this is the most strict version check and most probably
you will want to use more relaxed API-versions based checks like
`BeeDebug.isSupportedApiVersion()`, `BeeDebug.isSupportedMainApiVersion()` or `BeeDebug.isSupportedDebugApiVersion()`
based on your use-case.

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[bee-js/src/bee-debug.ts:409](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L409)

___

### isSupportedMainApiVersion

▸ **isSupportedMainApiVersion**(`options?`): `Promise`<`boolean`\>

Connects to a node and checks if its main's API version matches with the one that bee-js supports.

This is useful if you are not using `BeeDebug` class (for anything else then this check)
and want to make sure about compatibility.

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<`boolean`\>

#### Defined in

[bee-js/src/bee-debug.ts:423](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L423)

___

### isSupportedVersion

▸ **isSupportedVersion**(`options?`): `Promise`<`boolean`\>

Connnects to a node and checks if it is a supported Bee version by the bee-js

**`deprecated`** Use `BeeDebug.isSupportedExactVersion()` instead

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<`boolean`\>

true if the Bee node version is supported

#### Defined in

[bee-js/src/bee-debug.ts:393](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L393)

___

### pingPeer

▸ **pingPeer**(`peer`, `options?`): `Promise`<[`PingResponse`](../interfaces/PingResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `peer` | `string` \| [`Address`](../types/Address.md) |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`PingResponse`](../interfaces/PingResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:171](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L171)

___

### rebroadcastPendingTransaction

▸ **rebroadcastPendingTransaction**(`transactionHash`, `options?`): `Promise`<[`TransactionHash`](../types/TransactionHash.md)\>

Rebroadcast already created transaction.
This is mainly needed when your transaction fall off mempool from other reason is not incorporated into block.

#### Parameters

| Name | Type |
| :------ | :------ |
| `transactionHash` | `string` \| [`TransactionHash`](../types/TransactionHash.md) |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`TransactionHash`](../types/TransactionHash.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:658](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L658)

___

### removePeer

▸ **removePeer**(`peer`, `options?`): `Promise`<[`RemovePeerResponse`](../interfaces/RemovePeerResponse.md)\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `peer` | `string` \| [`Address`](../types/Address.md) |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) |

#### Returns

`Promise`<[`RemovePeerResponse`](../interfaces/RemovePeerResponse.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:158](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L158)

___

### retrieveExtendedTag

▸ **retrieveExtendedTag**(`tagUid`, `options?`): `Promise`<[`ExtendedTag`](../interfaces/ExtendedTag.md)\>

Retrieve tag extended information from Bee node

**`throws`** TypeError if tagUid is in not correct format

**`see`** [Bee docs - Syncing / Tags](https://docs.ethswarm.org/docs/access-the-swarm/syncing)

**`see`** [Bee API reference - `GET /tags/{uid}`](https://docs.ethswarm.org/debug-api/#tag/Tag)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tagUid` | `number` \| [`Tag`](../interfaces/Tag.md) | UID or tag object to be retrieved |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<[`ExtendedTag`](../interfaces/ExtendedTag.md)\>

#### Defined in

[bee-js/src/bee-debug.ts:135](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L135)

___

### topUpBatch

▸ **topUpBatch**(`postageBatchId`, `amount`, `options?`): `Promise`<`void`\>

Topup a fresh amount of BZZ to given Postage Batch.

For better understanding what each parameter means and what are the optimal values please see
[Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive).

**WARNING: THIS CREATES TRANSACTIONS THAT SPENDS MONEY**

**`see`** [Bee docs - Keep your data alive / Postage stamps](https://docs.ethswarm.org/docs/access-the-swarm/keep-your-data-alive)

**`see`** [Bee Debug API reference - `PATCH /stamps/topup/${id}/${amount}`](https://docs.ethswarm.org/debug-api/#tag/Postage-Stamps/paths/~1stamps~1topup~1{id}~1{amount}/patch)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `postageBatchId` | `string` \| [`BatchId`](../types/BatchId.md) | Batch ID |
| `amount` | [`NumberString`](../types/NumberString.md) | Amount to be added to the batch |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | Request options |

#### Returns

`Promise`<`void`\>

#### Defined in

[bee-js/src/bee-debug.ts:552](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L552)

___

### withdrawTokens

▸ **withdrawTokens**(`amount`, `gasPrice?`, `options?`): `Promise`<`string`\>

Withdraw tokens from the chequebook to the overlay address

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amount` | `number` \| [`NumberString`](../types/NumberString.md) | Amount of tokens to withdraw (must be positive integer) |
| `gasPrice?` | [`NumberString`](../types/NumberString.md) | Gas Price in WEI for the transaction call |
| `options?` | [`RequestOptions`](../interfaces/RequestOptions.md) | - |

#### Returns

`Promise`<`string`\>

string  Hash of the transaction

#### Defined in

[bee-js/src/bee-debug.ts:329](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/bee-debug.ts#L329)
