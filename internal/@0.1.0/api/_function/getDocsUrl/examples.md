**No specified version**

```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl("internal");

console.log(url);
//  https://partic11e.docs.integer11.org/#/internal/@latest/
```

**Specified version**

```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl("internal", "0.1.0");

console.log(url);
//  https://partic11e.docs.integer11.org/#/internal/@0.1.0/
```

**Using `InternalDocsInfo`**

```ts
import { getDocsUrl, InternalDocsFeatureType } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl({
  package: "internal",
  version: "0.1.0",
  featureType: InternalDocsFeatureType.Function,
  feature: "getDocsUrl"
});

console.log(url);
//  https://partic11e.docs.integer11.org/#/internal/@0.1.0/function?id=getdocsurl
```
