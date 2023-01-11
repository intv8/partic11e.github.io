```ts
import { DecoratorEnum } from "https://denopkg.com/partic11e/common/mod.ts";

const GetDecorator = (decorator: DecoratorEnum) => {
  if (decorator === DecoratorEnum.Accessor) {
    return ((target: any, key: string, descriptor: PropertyDescriptor) => {
      descriptor.get = () => "Hello, world!";
    }) as PropertyDecorator;
  }

  if (decorator === DecoratorEnum.Method) {
    return ((target: any, key: string, descriptor: PropertyDescriptor) => {
      descriptor.value = function () {
        return (this as any).myProp;
      };
    }) as MethodDecorator;
  }

  throw new Error(`Cannot apply this decorator to type ${decorator}.`);
};

class Example {
  @GetDecorator(DecoratorEnum.Method)
  public test() {
    return "Hello";
  }

  @GetDecorator(DecoratorEnum.Accessor)
  public get myProp() {
    return "Test";
  }
}

const ex = new Example();

console.log(ex.test());
//  Hello, world!
```
