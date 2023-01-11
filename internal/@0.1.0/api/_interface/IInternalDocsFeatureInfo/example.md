```ts
import {
  getDocsUrl,
  IInternalDocsFeatureInfo,
} from "https://denopkg.com/partic11e/internal/mod.ts";

const info: IInternalDocsFeatureInfo = {
  package: "internal",
  version: "0.1.0",
  featureType: InternalDocsFeatureType.Function,
  feature: "getDocsUrl",
};

const url = getDocsUrl(info);

console.log(url);
//  https://partic11e.docs.integer11.org/#/internal/@0.1.0/function?id=getdocsurl
```
