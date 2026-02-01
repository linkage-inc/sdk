# PostApiV1RunsResponse

Creates a new run for the specified workflow and returns the run metadata.

## Example Usage

```typescript
import { PostApiV1RunsResponse } from "@linkage-open/sdk/models/operations";

let value: PostApiV1RunsResponse = {};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `runId`            | *any*              | :heavy_minus_sign: | N/A                |
| `workflowId`       | *any*              | :heavy_minus_sign: | Circular type      |
| `status`           | *any*              | :heavy_minus_sign: | Circular type      |
| `nodeStatuses`     | *any*              | :heavy_minus_sign: | Circular type      |
| `startedAt`        | *any*              | :heavy_minus_sign: | Circular type      |
| `finishedAt`       | *any*              | :heavy_minus_sign: | Circular type      |
| `metadata`         | *any*              | :heavy_minus_sign: | Circular type      |
| `lastEventId`      | *any*              | :heavy_minus_sign: | Circular type      |