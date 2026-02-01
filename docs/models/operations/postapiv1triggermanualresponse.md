# PostApiV1TriggerManualResponse

Executes a workflow on-demand using client credentials and an optional payload.

## Example Usage

```typescript
import { PostApiV1TriggerManualResponse } from "@linkage-open/sdk/models/operations";

let value: PostApiV1TriggerManualResponse = {
  success: true,
  message: "Workflow execution started successfully",
};
```

## Fields

| Field                                   | Type                                    | Required                                | Description                             | Example                                 |
| --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- | --------------------------------------- |
| `success`                               | *boolean*                               | :heavy_minus_sign:                      | N/A                                     | true                                    |
| `executionId`                           | *any*                                   | :heavy_minus_sign:                      | Unknown type                            |                                         |
| `triggerExecutionId`                    | *any*                                   | :heavy_minus_sign:                      | Unknown type                            |                                         |
| `message`                               | *string*                                | :heavy_minus_sign:                      | N/A                                     | Workflow execution started successfully |