# Features

## Overview

### Available Operations

* [get](#get) - Get project features

## get

Returns enabled feature flags for the project, including billing-gated features.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/api/v1/features" method="get" path="/api/v1/features" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.features.get();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { featuresGet } from "@linkage-open/sdk/funcs/featuresGet.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await featuresGet(linkage);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("featuresGet failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetApiV1FeaturesRequest](../../models/operations/getapiv1featuresrequest.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetApiV1FeaturesResponse](../../models/operations/getapiv1featuresresponse.md)\>**

### Errors

| Error Type                                 | Status Code                                | Content Type                               |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| errors.GetApiV1FeaturesUnauthorizedError   | 401                                        | application/json                           |
| errors.GetApiV1FeaturesInternalServerError | 500                                        | application/json                           |
| errors.LinkageDefaultError                 | 4XX, 5XX                                   | \*/\*                                      |