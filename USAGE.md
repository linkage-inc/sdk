<!-- Start SDK Example Usage [usage] -->
```typescript
import { Linkage } from "@linkage-open/sdk";

const linkage = new Linkage();

async function run() {
  const result = await linkage.workflows.create();

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->