---
id: "Reference"
title: "Type alias: Reference"
sidebar_label: "Reference"
sidebar_position: 0
custom_edit_url: null
---

Ƭ **Reference**: [`HexString`](Utils.HexString.md)<typeof [`REFERENCE_HEX_LENGTH`](../variables/REFERENCE_HEX_LENGTH.md)\> \| [`HexString`](Utils.HexString.md)<typeof [`ENCRYPTED_REFERENCE_HEX_LENGTH`](../variables/ENCRYPTED_REFERENCE_HEX_LENGTH.md)\>

Generic reference that can be either non-encrypted reference which is a hex string of length 64 or encrypted
reference which is a hex string of length 128.

Encrypted reference consists of two parts. The reference address itself (like non-encrypted reference) and decryption key.

**`see`** [Bee docs - Store with Encryption](https://docs.ethswarm.org/docs/access-the-swarm/store-with-encryption)

#### Defined in

[bee-js/src/types/index.ts:61](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L61)
