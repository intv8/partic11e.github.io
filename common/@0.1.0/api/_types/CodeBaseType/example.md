```ts
import { CodeBaseEnum } from "https://denopkg.com/partic11e/common/mod.ts";
import type { CodeBaseType } from "https://denopkg.com/partic11e/common/mod.ts";

const isExtensible = (codebase: CodeBaseType) => {
  switch (codebase) {
    case CodeBaseEnum.Extension:
    case CodeBaseEnum.Plugin:
    case CodeBaseEnum.Adapter:
      return true;
    default:
      return false;
  }
};

console.log(isExtensible("module"));
//  false;
console.log(isExtensible("plugin"));
//  true;
```
