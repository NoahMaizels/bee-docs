---
id: "Utils.readableNodeToWeb"
title: "Function: readableNodeToWeb"
sidebar_label: "readableNodeToWeb"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).readableNodeToWeb

▸ **readableNodeToWeb**(`nodeStream`): `ReadableStream`<`Uint8Array`\>

Function that converts Node's Readable into WHATWG ReadableStream

Taken over from https://github.com/gwicke/node-web-streams/blob/master/lib/conversions.js
Because it uses forked web-streams-polyfill that are outdated.

**`author`** https://github.com/gwicke

**`licence`** Apache License 2.0 https://github.com/gwicke/node-web-streams/blob/master/LICENSE

#### Parameters

| Name | Type |
| :------ | :------ |
| `nodeStream` | `Readable` |

#### Returns

`ReadableStream`<`Uint8Array`\>

#### Defined in

[bee-js/src/utils/stream.ts:63](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/stream.ts#L63)
