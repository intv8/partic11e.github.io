**Specified version**

```ts
import { getExceptionsHelpUrl } from "https://denopkg.com/partic11e/common/mod.ts";

const url = getExceptionsHelpUrl("Exception", "1.1.2");
console.log(url);
//  http://p11-docs.integer11.com/#/ex-plain/Exception/@1.1.2
```

**No specified version**

```ts
const url = getExceptionsHelpUrl();
console.log(url);
//  http://p11-docs.integer11.com/#/ex-plain/Exception/@latest
```
