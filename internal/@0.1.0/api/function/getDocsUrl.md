## Function getDocsUrl

> Function accepting a document descriptor for a package or feature returning the URL to the documentation for that package or feature.

### Info

* Defined in `./src/get_docs_url.ts`
* Exported in:
  * **https://denopkg.com/partic11e/internal/mod.ts**
  * https://denopkg.com/partic11e/internal/src/mod.ts
  * https://denopkg.com/partic11e/internal/src/get_docs_url.ts

### Definition

```ts
getDocsUrl(data: InternalDocDescriptor): string;
getDocsUrl(packageName: string, version?: string): string;
```

### Signatures

<!-- tabs:start -->

## **Package only**

### getDocsUrl(packageName: string, version?: string): string

Accepts a package name and an optional version and returns the URL to the
documentation for that package.

#### Arguments

| Name | Type | Description |
|------|------|-------------|
| `packageName` | `string` | The name of the package. |
| `version` | `string` | The optional version of the package. Defaults to `"latest"` |

#### Returns

A `string` containing the URL to the documentation for the package.

## **Package or feature**

### getDocsUrl(data: InternalDocDescriptor): string

Accepts a document descriptor for a package or feature and returns the URL to the documentation for that package or feature.

#### Arguments

| Name | Type | Description |
|------|------|-------------|
| `data` | [`InternalDocDescriptor`](../type/InternalDocDescriptor) | The document descriptor for the package or feature. |

#### Returns

A `string` containing the URL to the documentation for the package or feature.

<!-- tabs:end -->

### Examples

<!-- tabs:start -->
## **Package only**

**Latest package version**
```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl("internal");

console.log(url);
// https://partic11e.docs.integer11.org/#/internal/@latest
```

**Specific package version**
```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl("internal", "0.1.0");

console.log(url);
// https://partic11e.docs.integer11.org/#/internal/@0.1.0
```

## **Package or feature**

**Latest package version**
```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl({ package: "internal" });

console.log(url);
// https://partic11e.docs.integer11.org/#/internal/@latest
```

**Specific package version**
```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl({
  package: "internal",
  version: "0.1.0",
});

console.log(url);
// https://partic11e.docs.integer11.org/#/internal/@0.1.0
```

**Latest version feature**

```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl({
  package: "internal",
  featureType: "function",
  feature: "getDocsUrl",
});

console.log(url);
// https://partic11e.docs.integer11.org/#/internal/@latest/function/getdocsurl
```

**Specific version feature**

```ts
import { getDocsUrl } from "https://denopkg.com/partic11e/internal/mod.ts";

const url = getDocsUrl({
  package: "internal",
  version: "0.1.0",
  featureType: "function",
  feature: "getDocsUrl",
});

console.log(url);
// https://partic11e.docs.integer11.org/#/internal/@0.1.0/function/getdocsurl
```

<!-- tabs:end -->