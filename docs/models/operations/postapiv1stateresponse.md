# PostApiV1StateResponse

Persists workflow nodes/edges when the payload hash changes.

## Example Usage

```typescript
import { PostApiV1StateResponse } from "@linkage-open/sdk/models/operations";

let value: PostApiV1StateResponse = {};
```

## Fields

| Field                                                    | Type                                                     | Required                                                 | Description                                              |
| -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- | -------------------------------------------------------- |
| `nodesHash`                                              | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `edgesHash`                                              | *string*                                                 | :heavy_minus_sign:                                       | N/A                                                      |
| `updated`                                                | [operations.Updated](../../models/operations/updated.md) | :heavy_minus_sign:                                       | N/A                                                      |