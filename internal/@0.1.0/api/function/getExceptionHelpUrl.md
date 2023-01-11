## Function getExceptionHelpUrl

> Function accepting a partic11e exception returning the URL to the help page
> and exception explaination for that exception.

### Info

* Defined in `./src/get_exception_help_url.ts`
* Exported in:
  * **https://denopkg.com/partic11e/internal/mod.ts**
  * https://denopkg.com/partic11e/internal/src/mod.ts
  * https://denopkg.com/partic11e/internal/src/get_exception_help_url.ts

### Definition

```ts
getExceptionHelpUrl(data: IInternalExceptionBase): string;
```

### getExceptionHelpUrl(data: IInternalExceptionBase): string

Accepts a partic11e exception and returns the URL to the help page and exception explaination for that exception.

#### Arguments

| Name | Type | Description |
|------|------|-------------|
| `data` | [`IInternalExceptionBase`](../interface/iinternalexceptionbase) | The partic11e exception to get the URL to the help page and exception explaination for. |

#### Returns

A `string` containing the URL to the help page and exception explaination for the exception.

### Examples

<!-- tabs:start -->
## **Simple exception**
```ts
import { getExceptionHelpUrl, IInternalExceptionBase } from "https://denopkg.com/partic11e/internal/mod.ts";

const exception: IInternalExceptionBase = {
  name: "InternalException",
  message: "This is an exception.",
  code: 25,
  helpUrl: "https://example.com",
};
const url = getExceptionHelpUrl(exception);

console.log(url);
// https://docs.integer11.org/ee/p11/0x019?m=This%20is%20an%exception.
// m=This is an exception
```

## **Exception with native Error cause**
```ts
import { getExceptionHelpUrl, IInternalExceptionBase } from "https://denopkg.com/partic11e/internal/mod.ts";

const exception: IInternalExceptionBase = {
  name: "InternalException",
  message: "This is an exception.",
  code: 25,
  helpUrl: "https://example.com",
  cause: new Error("Inner exception"),
};
const url = getExceptionHelpUrl(exception);

console.log(url);
// https://docs.integer11.org/ee/p11/0x019?m=This%20is%20an%20internal%20exception.&c=%7B%22n%22%3A%22Error%22%2C%22m%22%3A%22This%20is%20an%20exception.%22%2C%22l%22%3A%22%22%7D
// m=This is an exception
// c={"n":"Error","m":"This is an exception.","l":""}
```

## **Exception with partic11e exception cause**
```ts
import { getExceptionHelpUrl, IInternalExceptionBase } from "https://denopkg.com/partic11e/internal/mod.ts";

const exception: IInternalExceptionBase = {
  name: "InternalException",
  message: "This is an exception.",
  code: 25,
  helpUrl: "https://example.com",  
  cause: {
    name: "Exception",
    message: "Inner Exception",
    code: 26,
    helpUrl: "https://example.com/baz",
  },
};
const url = getExceptionHelpUrl(exception);

console.log(url);
// https://docs.integer11.org/ee/p11/0x019?m=This%20is%20an%20internal%20exception.&c=%7B%22n%22%3A%22Exception%22%2C%22m%22%3A%22Inner%20Exception%22%2C%22l%22%3A%22https%3A%2F%2Fexample.com%2Fbaz%22%7D
// m=This is an exception
// c={"n":"Exception","m":"Inner Exception","l":"https://example.com/baz"}
```

<!-- tabs:end -->