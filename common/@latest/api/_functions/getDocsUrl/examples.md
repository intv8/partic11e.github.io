**Specified version**

```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/common/mod.ts";

const url = getDocsUrl("common", "1.1.2");
console.log(url);
//  http://p11-docs.integer11.com/#/common/@1.1.2/
```

**No specified version**

```ts
const url = getDocsUrl();
console.log(url);
//  http://p11-docs.integer11.com/#/common/@latest/
```
