## Interface IInternalExceptionInit

> Interface describing the base exception initialization data. Used during
> exception construction to provide additional data to the exception.

### Info

* Defined in `./src/types/interfaces.ts`
* Exported in:
  * **https://denopkg.com/partic11e/internal/mod.ts**
  * https://denopkg.com/partic11e/internal/src/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/interfaces.ts

### Hierarchy
  * **IInternalExceptionInit**

### Definition

```ts
interface IInternalExceptionInit {
  [key: string]: unknown;
}
```

### Properties

| Name | Type | Description |
|------|------|-------------|
| `[key: string]` | `unknown` | `string`-indexed keys with value of `unknown` type providing additional initialization data to the exception. |
