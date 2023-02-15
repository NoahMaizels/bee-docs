---
id: "Utils.readableWebToNode"
title: "Function: readableWebToNode"
sidebar_label: "readableWebToNode"
custom_edit_url: null
---

[Utils](../namespaces/Utils.md).readableWebToNode

▸ **readableWebToNode**(`webStream`, `options?`): `NodeReadableNative`

Function that converts WHATWG ReadableStream into Node's Readable

Taken over from https://github.com/gwicke/node-web-streams/blob/master/lib/conversions.js
Because it uses forked web-streams-polyfill that is outdated.

**Warning!**
If you want to use this function in browser you have to polyfill `stream` package with your bundler.

**`author`** https://github.com/gwicke

**`licence`** Apache License 2.0 https://github.com/gwicke/node-web-streams/blob/master/LICENSE

#### Parameters

| Name | Type |
| :------ | :------ |
| `webStream` | `ReadableStream`<`unknown`\> |
| `options?` | `ReadableOptions` |

#### Returns

`NodeReadableNative`

#### Defined in

[bee-js/src/utils/stream.ts:143](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/utils/stream.ts#L143)
