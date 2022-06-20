```ts
import { OperationEnum } from "https://denopkg.com/partic11e/common/mod.ts";

const isUserActivated = (operation: OperationEnum) => {
  switch (operation) {
    case OperationEnum.Build:
    case OperationEnum.Action:
    case OperationEnum.Operation:
      return true;
    default:
      return false;
  }
};

console.log(isUserActivated(OperationEnum.Workflow));
//  false;
console.log(isUserActivated(OperationEnum.Build));
//  true;
```
