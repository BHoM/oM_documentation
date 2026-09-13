---
title: IEnergyMaterialOpaque
---

# <small>BH.oM.LadybugTools.</small>**IEnergyMaterialOpaque**

An interface for opaque energy materials.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The IEnergyMaterialOpaque is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.LadybugTools.[ILadybugTools](/api/oM/Adapter/LadybugTools/ILadybugTools)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)


### Classes implementing this interface

???+ bhom "The following classes are implementing this interface:"

    - BH.oM.LadybugTools.[EnergyMaterial](/api/oM/Adapter/LadybugTools/Constructions/EnergyMaterial)
    - BH.oM.LadybugTools.[EnergyMaterialVegetation](/api/oM/Adapter/LadybugTools/Constructions/EnergyMaterialVegetation)


## Properties



### Defining properties

The following properties are defined on the interface

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Identifier | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Unique identifier for this material. | - |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface IEnergyMaterialOpaque : BH.oM.LadybugTools.ILadybugTools, BH.oM.Base.IBHoMObject, BH.oM.Base.IObject
```

Assembly: LadybugTools_oM.dll

The C# interface definition is available on github:

- [IEnergyMaterialOpaque.cs](https://github.com/BHoM/LadybugTools_Toolkit/blob/develop/LadybugTools_oM/Constructions\IEnergyMaterialOpaque.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/LadybugTools_oM/IEnergyMaterialOpaque.json"
}
```

The JSON Schema is available on github here:

- [IEnergyMaterialOpaque.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/LadybugTools_oM/IEnergyMaterialOpaque.json)
