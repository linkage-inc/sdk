# Trigger

## Overview

### Available Operations

* [execute](#execute) - Execute a webhook trigger
* [getDetails](#getdetails) - Get trigger details

## execute

Validates the webhook trigger and starts a workflow execution.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/api/v1/trigger/{triggerId}" method="post" path="/api/v1/trigger/{triggerId}" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.trigger.execute({
    triggerId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { triggerExecute } from "@linkage-open/sdk/funcs/triggerExecute.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await triggerExecute(linkage, {
    triggerId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("triggerExecute failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostApiV1TriggerTriggerIdRequest](../../models/operations/postapiv1triggertriggeridrequest.md)                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostApiV1TriggerTriggerIdResponse](../../models/operations/postapiv1triggertriggeridresponse.md)\>**

### Errors

| Error Type                                          | Status Code                                         | Content Type                                        |
| --------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------- |
| errors.PostApiV1TriggerTriggerIdBadRequestError     | 400                                                 | application/json                                    |
| errors.PostApiV1TriggerTriggerIdUnauthorizedError   | 401                                                 | application/json                                    |
| errors.ForbiddenError                               | 403                                                 | application/json                                    |
| errors.PostApiV1TriggerTriggerIdNotFoundError       | 404                                                 | application/json                                    |
| errors.PostApiV1TriggerTriggerIdInternalServerError | 500                                                 | application/json                                    |
| errors.LinkageDefaultError                          | 4XX, 5XX                                            | \*/\*                                               |

## getDetails

Returns metadata about a trigger for testing or debugging.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="get_/api/v1/trigger/{triggerId}" method="get" path="/api/v1/trigger/{triggerId}" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.trigger.getDetails({
    triggerId: "<id>",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { triggerGetDetails } from "@linkage-open/sdk/funcs/triggerGetDetails.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await triggerGetDetails(linkage, {
    triggerId: "<id>",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("triggerGetDetails failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.GetApiV1TriggerTriggerIdRequest](../../models/operations/getapiv1triggertriggeridrequest.md)                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.GetApiV1TriggerTriggerIdResponse](../../models/operations/getapiv1triggertriggeridresponse.md)\>**

### Errors

| Error Type                                     | Status Code                                    | Content Type                                   |
| ---------------------------------------------- | ---------------------------------------------- | ---------------------------------------------- |
| errors.GetApiV1TriggerTriggerIdBadRequestError | 400                                            | application/json                               |
| errors.GetApiV1TriggerTriggerIdNotFoundError   | 404                                            | application/json                               |
| errors.LinkageDefaultError                     | 4XX, 5XX                                       | \*/\*                                          |