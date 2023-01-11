## Interface IInternalExceptionBase

> Interface describing the features of a partic11e exception.

### Info

* Defined in `./src/types/interfaces.ts`
* Exported in:
  * **https://denopkg.com/partic11e/internal/mod.ts**
  * https://denopkg.com/partic11e/internal/src/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/interfaces.ts

### Hierarchy
  * **IInternalExceptionBase**

### Definition

```ts
interface IInternalExceptionBase {
  name: string;
  message: string;
  code: number;
  helpUrl: string;
  cause?: Error | IInternalExceptionBase;
  data?: IInternalExceptionInit;
}
```

### Properties

| Name | Type | Description |
|------|------|-------------|
| `name` | `string` | The name of the exception. |
| `message` | `string` | A brief message describing the exception. |
| `code` | `number` | The exception code for the exception. |
| `helpUrl` | `string` | The URL referencing the exception explanation of the exception. |
| `cause` | `Error` \| `IInternalExceptionBase` | The optional inner cause of the exception. |
| `data` | [`IInternalExceptionInit`](iinternalexceptioninit) | The optional additional initialization data for the exception. |
