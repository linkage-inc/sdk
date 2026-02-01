# Workflows

## Overview

### Available Operations

* [create](#create) - Create a workflow

## create

Creates a workflow for a project with the provided nodes and edges.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="post_/api/v1/create" method="post" path="/api/v1/create" -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.workflows.create();

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { LinkageCore } from "@linkage-open/sdk/core.js";
import { workflowsCreate } from "@linkage-open/sdk/funcs/workflowsCreate.js";

// Use `LinkageCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const linkage = new LinkageCore();

async function run() {
  const res = await workflowsCreate(linkage);
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("workflowsCreate failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.PostApiV1CreateRequest](../../models/operations/postapiv1createrequest.md)                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.PostApiV1CreateResponse](../../models/operations/postapiv1createresponse.md)\>**

### Errors

| Error Type                                | Status Code                               | Content Type                              |
| ----------------------------------------- | ----------------------------------------- | ----------------------------------------- |
| errors.PostApiV1CreateBadRequestError     | 400                                       | application/json                          |
| errors.PostApiV1CreateNotFoundError       | 404                                       | application/json                          |
| errors.PostApiV1CreateInternalServerError | 500                                       | application/json                          |
| errors.LinkageDefaultError                | 4XX, 5XX                                  | \*/\*                                     |