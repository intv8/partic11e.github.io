```ts
import {
  getDocsUrl,
  IInternalDocsBaseInfo,
} from "https://denopkg.com/partic11e/internal/mod.ts";

const info: IInternalDocsBaseInfo = {
  package: "internal",
  version: "0.1.0",
};

const url = getDocsUrl(info);

console.log(url);
//  https://partic11e.docs.integer11.org/#/internal/@0.1.0
```
