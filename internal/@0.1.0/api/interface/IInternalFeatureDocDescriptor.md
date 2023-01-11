## Interface IInternalFeatureDocDescriptor

> Interface describing a documentation descriptor for a package.

### Info

* Defined in `./src/types/interfaces.ts`
* Exported in:
  * **https://denopkg.com/partic11e/internal/mod.ts**
  * https://denopkg.com/partic11e/internal/src/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/mod.ts
  * https://denopkg.com/partic11e/internal/src/types/interfaces.ts

### Hierarchy
  * [IInternalPackageDocDescriptor](IInternalPackageDocDescriptor)
    * **IInternalFeatureDocDescriptor**

### Definition

```ts
interface IInternalPackageDocDescriptor extends IInternalPackageDocDescriptor {
  featureType: InternalDocsFeatureType;
  feature: string;
}
```

### Properties

| Name | Type | Description |
|------|------|-------------|
| `package`<sup>1</sup> | `string` | The name of the package. |
| `version`<sup>1</sup> | `string` | The optional version of the package. Defaults to `"latest"` |
| `featureType` | [`InternalDocsFeatureType`](../enum/InternalDocsFeatureType) | The type of feature. |
| `feature` | `string` | The name of the feature. |

<small>**Note**</small>  
<small>1. Property inherited from [IInternalPackageDocDescriptor](IInternalPackageDocDescriptor)</small>
