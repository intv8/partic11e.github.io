## Interface IInternalPackageDocDescriptor

> Interface describing a documentation descriptor for a package.

### Info

* Defined in `./src/types/interfaces.ts`
* Exported in:
  * **https://denopkg.com/partic11e/internal/mod.ts**
  * https://denopkg.com/partic11e/internal/src/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/interfaces.ts

### Hierarchy  
  * **IInternalPackageDocDescriptor**
    * [IInternalFeatureDocDescriptor](IInternalFeatureDocDescriptor)

### Definition

```ts
interface IInternalPackageDocDescriptor {
  package: string;
  version?: string;
}
```

### Properties

| Name | Type | Description |
|------|------|-------------|
| `package` | `string` | The name of the package. |
| `version` | `string` | The optional version of the package. Defaults to `"latest"`. |
