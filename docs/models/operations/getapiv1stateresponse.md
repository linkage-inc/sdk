# GetApiV1StateResponse

Fetches workflow nodes/edges and hashes for a workflow.

## Example Usage

```typescript
import { GetApiV1StateResponse } from "@linkage-open/sdk/models/operations";

let value: GetApiV1StateResponse = {};
```

## Fields

| Field              | Type               | Required           | Description        |
| ------------------ | ------------------ | ------------------ | ------------------ |
| `nodes`            | *any*              | :heavy_minus_sign: | N/A                |
| `edges`            | *any*              | :heavy_minus_sign: | Circular type      |
| `nodesById`        | *any*              | :heavy_minus_sign: | Circular type      |
| `edgesById`        | *any*              | :heavy_minus_sign: | Circular type      |
| `nodesHash`        | *string*           | :heavy_minus_sign: | N/A                |
| `edgesHash`        | *any*              | :heavy_minus_sign: | Circular type      |