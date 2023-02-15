---
id: "Utils.makeEthereumWalletSigner"
title: "Function: makeEthereumWalletSigner"
sidebar_label: "makeEthereumWalletSigner"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).makeEthereumWalletSigner

▸ **makeEthereumWalletSigner**(`provider`, `ethAddress?`): `Promise`<[`Signer`](../types/Signer.md)\>

Function that takes Ethereum EIP-1193 compatible provider and create an Signer instance that
uses `personal_sign` method to sign requested data.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `provider` | `JsonRPC` | Injected web3 provider like window.ethereum or other compatible with EIP-1193 |
| `ethAddress?` | `string` \| `HexEthAddress` \| [`HexString`](../types/Utils.HexString.md)<`number`\> | Optional address of the account which the data should be signed with. If not specified `eth_requestAccounts` request is used to get the account address. |

#### Returns

`Promise`<[`Signer`](../types/Signer.md)\>

#### Defined in

[bee-js/src/utils/eth.ts:195](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/eth.ts#L195)
