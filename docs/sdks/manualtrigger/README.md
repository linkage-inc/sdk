# ManualTrigger

## Overview

### Available Operations

* [execute](#execute) - Execute a manual trigger

## execute

Executes a workflow on-demand using client credentials and an optional payload.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/api/v1/trigger/manual" method="post" path="/api/v1/trigger/manual" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.manualTrigger.execute();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { manualTriggerExecute } from "@linkage-open/sdk/funcs/manualTriggerExecute.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await manualTriggerExecute(linkage);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("manualTriggerExecute failed:", res.error);
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

**Promise\<[operations.PostApiV1TriggerManualResponse](../../models/operations/postapiv1triggermanualresponse.md)\>**

### Errors

| Error Type                                          | Status Code                                         | Content Type                                        |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| errors.PostApiV1TriggerManualBadRequestError        | 400                                                 | application/json                                    |
| errors.PostApiV1TriggerManualUnauthorizedError      | 401                                                 | application/json                                    |
| errors.ForbiddenError                               | 403                                                 | application/json                                    |
| errors.PostApiV1TriggerTriggerIdNotFoundError       | 404                                                 | application/json                                    |
| errors.PostApiV1TriggerTriggerIdInternalServerError | 500                                                 | application/json                                    |
| errors.LinkageDefaultError                          | 4XX, 5XX                                            | \*/\*                                               |