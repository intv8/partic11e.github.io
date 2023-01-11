```ts
import {
  getDocsUrl,
  InternalDocsFeatureType,
} from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl({
  package: "internal",
  version: "0.1.0",
  featureType: InternalDocsFeatureType.Class,
  feature: "getDocsUrl"
});

console.log(url);
//  https://partic11e.docs.integer11.org/#/internal/@0.1.0/api/class?id=getdocsurl
```
