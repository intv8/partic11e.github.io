```ts
interface IInternalExceptionBase {
  name: string;
  message: string;
  cause?: Error | IInternalExceptionBase;
  code: number;
  helpUrl: string;
  data?: IInternalExceptionInit
}
```

* **name**: `string` - The exception name.
* **message**: `string` - The exception message.
* **cause**: `Error` | [`IInternalExceptionBase`](interface?id=iinternalexceptionbase) - The inner exception, or cause, of the exception.
* **code**: `number` - The exception code.
* **helpUrl**: `string` - Any additional data to be included in the exception.
* **data**: [`IInternalExceptionInit`](interface?id=iinternalexceptioninit) - The URL for the exception explainer.