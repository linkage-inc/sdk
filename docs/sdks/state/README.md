# State

## Overview

### Available Operations

* [options](#options) - use to set the summary
* [get](#get) - use to set the summary
* [update](#update) - use to set the summary

## options

use jsdoc tag to set the description

### Example Usage

<!-- UsageSnippet language="typescript" operationID="options_/api/v1/state" method="options" path="/api/v1/state" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  await linkage.state.options();


}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { stateOptions } from "@linkage-open/sdk/funcs/stateOptions.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await stateOptions(linkage);
  if (res.ok) {
    const { value: result } = res;
    
  } else {
    console.log("stateOptions failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<void\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.LinkageDefaultError | 4XX, 5XX                   | \*/\*                      |

## get

use jsdoc tag to set the description

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/api/v1/state" method="get" path="/api/v1/state" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.state.get();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { stateGet } from "@linkage-open/sdk/funcs/stateGet.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await stateGet(linkage);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("stateGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetApiV1StateResponse](../../models/operations/getapiv1stateresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.LinkageDefaultError | 4XX, 5XX                   | \*/\*                      |

## update

use jsdoc tag to set the description

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/api/v1/state" method="post" path="/api/v1/state" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.state.update();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { stateUpdate } from "@linkage-open/sdk/funcs/stateUpdate.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await stateUpdate(linkage);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("stateUpdate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostApiV1StateResponse](../../models/operations/postapiv1stateresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.LinkageDefaultError | 4XX, 5XX                   | \*/\*                      |