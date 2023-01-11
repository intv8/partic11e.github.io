```ts
import { OperationEnum } from "https://denopkg.com/partic11e/common/mod.ts";
import type { OperationType } from "https://denopkg.com/partic11e/common/mod.ts";

const isUserActivated = (operation: OperationType) => {
  switch (operation) {
    case OperationEnum.Build:
    case OperationEnum.Action:
    case OperationEnum.Operation:
      return true;
    default:
      return false;
  }
};

console.log(isUserActivated("workflow"));
//  false;
console.log(isUserActivated("build"));
//  true;
```
