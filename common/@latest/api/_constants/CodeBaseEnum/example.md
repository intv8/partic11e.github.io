```ts
import { CodeBaseEnum } from "https://denopkg.com/partic11e/common/mod.ts";

const isExtensible = (codebase: CodeBaseEnum) => {
  switch (codebase) {
    case CodeBaseEnum.Extension:
    case CodeBaseEnum.Plugin:
    case CodeBaseEnum.Adapter:
      return true;
    default:
      return false;
  }
};

console.log(isExtensible(CodeBaseEnum.Module));
//  false;
console.log(isExtensible(CodeBaseEnum.Plugin));
//  true;
```
