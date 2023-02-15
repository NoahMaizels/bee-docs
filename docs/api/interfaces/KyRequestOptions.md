---
id: "KyRequestOptions"
title: "Interface: KyRequestOptions"
sidebar_label: "KyRequestOptions"
sidebar_position: 0
custom_edit_url: null
---

Internal interface that represents configuration for creating a request with Ky

## Hierarchy

- `Omit`<`KyOptions`, ``"searchParams"``\>

  ↳ **`KyRequestOptions`**

## Properties

### body

• `Optional` **body**: ``null`` \| `BodyInit`

A BodyInit object or null to set request's body.

#### Inherited from

Omit.body

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1498

___

### cache

• `Optional` **cache**: `RequestCache`

A string indicating how the request will interact with the browser's cache to set request's cache.

#### Inherited from

Omit.cache

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1500

___

### credentials

• `Optional` **credentials**: `RequestCredentials`

A string indicating whether credentials will be sent with the request always, never, or only when sent to a same-origin URL. Sets request's credentials.

#### Inherited from

Omit.credentials

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1502

___

### headers

• `Optional` **headers**: `KyHeadersInit`

HTTP headers used to make the request.

You can pass a `Headers` instance or a plain object.

You can remove a header with `.extend()` by passing the header with an `undefined` value.

**`example`**
```
import ky from 'ky';

const url = 'https://sindresorhus.com';

const original = ky.create({
headers: {
rainbow: 'rainbow',
unicorn: 'unicorn'
}
});

const extended = original.extend({
headers: {
rainbow: undefined
}
});

const response = await extended(url).json();

console.log('rainbow' in response);
//=> false

console.log('unicorn' in response);
//=> true
```

#### Inherited from

Omit.headers

#### Defined in

[bee-js/src/types/ky-options.ts:76](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L76)

___

### hooks

• `Optional` **hooks**: `Hooks`

Hooks allow modifications during the request lifecycle. Hook functions may be async and are run serially.

#### Inherited from

Omit.hooks

#### Defined in

[bee-js/src/types/ky-options.ts:165](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L165)

___

### integrity

• `Optional` **integrity**: `string`

A cryptographic hash of the resource to be fetched by request. Sets request's integrity.

#### Inherited from

Omit.integrity

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1506

___

### json

• `Optional` **json**: `unknown`

Shortcut for sending JSON. Use this instead of the `body` option.

Accepts any plain object or value, which will be `JSON.stringify()`'d and sent in the body with the correct header set.

#### Inherited from

Omit.json

#### Defined in

[bee-js/src/types/ky-options.ts:82](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L82)

___

### keepalive

• `Optional` **keepalive**: `boolean`

A boolean to set request's keepalive.

#### Inherited from

Omit.keepalive

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1508

___

### method

• `Optional` **method**: `LiteralUnion`<`HTTPMethod`, `string`\>

HTTP method used to make the request.

Internally, the standard methods (`GET`, `POST`, `PUT`, `PATCH`, `HEAD` and `DELETE`) are uppercased in order to avoid server errors due to case sensitivity.

#### Inherited from

Omit.method

#### Defined in

[bee-js/src/types/ky-options.ts:40](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L40)

___

### mode

• `Optional` **mode**: `RequestMode`

A string to indicate whether the request will use CORS, or will be restricted to same-origin URLs. Sets request's mode.

#### Inherited from

Omit.mode

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1512

___

### path

• **path**: `string`

#### Defined in

[bee-js/src/types/index.ts:102](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L102)

___

### prefixUrl

• `Optional` **prefixUrl**: `string` \| `URL`

A prefix to prepend to the `input` URL when making the request. It can be any valid URL, either relative or absolute. A trailing slash `/` is optional and will be added automatically, if needed, when it is joined with `input`. Only takes effect when `input` is a string. The `input` argument cannot start with a slash `/` when using this option.

Useful when used with `ky.extend()` to create niche-specific Ky-instances.

Notes:
- After `prefixUrl` and `input` are joined, the result is resolved against the [base URL](https://developer.mozilla.org/en-US/docs/Web/API/Node/baseURI) of the page (if any).
- Leading slashes in `input` are disallowed when using this option to enforce consistency and avoid confusion about how the `input` URL is handled, given that `input` will not follow the normal URL resolution rules when `prefixUrl` is being used, which changes the meaning of a leading slash.

**`example`**
```
import ky from 'ky';

// On https://example.com

const response = await ky('unicorn', {prefixUrl: '/api'});
//=> 'https://example.com/api/unicorn'

const response = await ky('unicorn', {prefixUrl: 'https://cats.com'});
//=> 'https://cats.com/unicorn'
```

#### Inherited from

Omit.prefixUrl

#### Defined in

[bee-js/src/types/ky-options.ts:131](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L131)

___

### redirect

• `Optional` **redirect**: `RequestRedirect`

A string indicating whether request follows redirects, results in an error upon encountering a redirect, or returns the redirect (in an opaque fashion). Sets request's redirect.

#### Inherited from

Omit.redirect

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1514

___

### referrer

• `Optional` **referrer**: `string`

A string whose value is a same-origin URL, "about:client", or the empty string, to set request's referrer.

#### Inherited from

Omit.referrer

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1516

___

### referrerPolicy

• `Optional` **referrerPolicy**: `ReferrerPolicy`

A referrer policy to set request's referrerPolicy.

#### Inherited from

Omit.referrerPolicy

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1518

___

### responseType

• `Optional` **responseType**: ``"json"`` \| ``"arraybuffer"`` \| ``"stream"``

#### Defined in

[bee-js/src/types/index.ts:103](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L103)

___

### retry

• `Optional` **retry**: `number` \| `RetryOptions`

An object representing `limit`, `methods`, `statusCodes` and `maxRetryAfter` fields for maximum retry count, allowed methods, allowed status codes and maximum [`Retry-After`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Retry-After) time.

If `retry` is a number, it will be used as `limit` and other defaults will remain in place.

If `maxRetryAfter` is set to `undefined`, it will use `options.timeout`. If [`Retry-After`](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Retry-After) header is greater than `maxRetryAfter`, it will cancel the request.

Delays between retries is calculated with the function `0.3 * (2 ** (retry - 1)) * 1000`, where `retry` is the attempt number (starts from 1).

**`example`**
```
import ky from 'ky';

const json = await ky('https://example.com', {
retry: {
limit: 10,
methods: ['get'],
statusCodes: [413]
}
}).json();
```

#### Inherited from

Omit.retry

#### Defined in

[bee-js/src/types/ky-options.ts:154](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L154)

___

### searchParams

• `Optional` **searchParams**: `Record`<`string`, `undefined` \| `string` \| `number` \| `boolean`\>

Overridden parameter that allows undefined as a value.

#### Defined in

[bee-js/src/types/index.ts:108](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/index.ts#L108)

___

### signal

• `Optional` **signal**: ``null`` \| `AbortSignal`

An AbortSignal to set request's signal.

#### Inherited from

Omit.signal

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1520

___

### throwHttpErrors

• `Optional` **throwHttpErrors**: `boolean`

Throw an `HTTPError` when, after following redirects, the response has a non-2xx status code. To also throw for redirects instead of following them, set the [`redirect`](https://developer.mozilla.org/en-US/docs/Web/API/WindowOrWorkerGlobalScope/fetch#Parameters) option to `'manual'`.

Setting this to `false` may be useful if you are checking for resource availability and are expecting error responses.

**`default`** true

#### Inherited from

Omit.throwHttpErrors

#### Defined in

[bee-js/src/types/ky-options.ts:173](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L173)

___

### timeout

• `Optional` **timeout**: `number` \| ``false``

Timeout in milliseconds for getting a response. Can not be greater than 2147483647.
If set to `false`, there will be no timeout.

**`default`** 10000

#### Inherited from

Omit.timeout

#### Defined in

[bee-js/src/types/ky-options.ts:161](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L161)

___

### window

• `Optional` **window**: ``null``

Can only be null. Used to disassociate request from any Window.

#### Inherited from

Omit.window

#### Defined in

node_modules/typescript/lib/lib.dom.d.ts:1522

## Methods

### fetch

▸ `Optional` **fetch**(`input`, `init?`): `Promise`<`Response`\>

User-defined `fetch` function.
Has to be fully compatible with the [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) standard.

Use-cases:
1. Use custom `fetch` implementations like [`isomorphic-unfetch`](https://www.npmjs.com/package/isomorphic-unfetch).
2. Use the `fetch` wrapper function provided by some frameworks that use server-side rendering (SSR).

**`default`** fetch

**`example`**
```
import ky from 'ky';
import fetch from 'isomorphic-unfetch';

const json = await ky('https://example.com', {fetch}).json();
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `input` | `RequestInfo` |
| `init?` | `RequestInit` |

#### Returns

`Promise`<`Response`\>

#### Inherited from

Omit.fetch

#### Defined in

[bee-js/src/types/ky-options.ts:212](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L212)

___

### onDownloadProgress

▸ `Optional` **onDownloadProgress**(`progress`, `chunk`): `void`

Download progress event handler.

**`example`**
```
import ky from 'ky';

const response = await ky('https://example.com', {
onDownloadProgress: (progress, chunk) => {
// Example output:
// `0% - 0 of 1271 bytes`
// `100% - 1271 of 1271 bytes`
console.log(`${progress.percent * 100}% - ${progress.transferredBytes} of ${progress.totalBytes} bytes`);
}
});
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `progress` | `DownloadProgress` | - |
| `chunk` | `Uint8Array` | Note: It's empty for the first call. |

#### Returns

`void`

#### Inherited from

Omit.onDownloadProgress

#### Defined in

[bee-js/src/types/ky-options.ts:193](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L193)

___

### parseJson

▸ `Optional` **parseJson**(`text`): `unknown`

User-defined JSON-parsing function.

Use-cases:
1. Parse JSON via the [`bourne` package](https://github.com/hapijs/bourne) to protect from prototype pollution.
2. Parse JSON with [`reviver` option of `JSON.parse()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse).

**`default`** JSON.parse()

**`example`**
```
import ky from 'ky';
import bourne from '@hapijs/bourne';

const json = await ky('https://example.com', {
parseJson: text => bourne(text)
}).json();
```

#### Parameters

| Name | Type |
| :------ | :------ |
| `text` | `string` |

#### Returns

`unknown`

#### Inherited from

Omit.parseJson

#### Defined in

[bee-js/src/types/ky-options.ts:102](https://github.com/ethersphere/bee-js/blob/2c8b9d1/src/types/ky-options.ts#L102)
