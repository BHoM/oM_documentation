---
title: IEnvironmentMaterial
---

# <small>BH.oM.Environment.MaterialFragments.</small>**IEnvironmentMaterial**



## Interface structure

### Implemented interfaces and base types

???+ bhom "The IEnvironmentMaterial is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Physical.Materials.[IMaterialProperties](/api/oM/Physical/Physical/Materials/IMaterialProperties)
    -  BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)
    -  BH.oM.Physical.Materials.[IDensityProvider](/api/oM/Physical/Physical/Materials/IDensityProvider)


### Classes implementing this interface

???+ bhom "The following classes are implementing this interface:"

    - BH.oM.Environment.MaterialFragments.[GasMaterial](/api/oM/Analytical/Environment/MaterialFragments/GasMaterial)
    - BH.oM.Environment.MaterialFragments.[SolidMaterial](/api/oM/Analytical/Environment/MaterialFragments/SolidMaterial)


## Properties



### Defining properties

The following properties are defined on the interface

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Conductivity | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | - | - |
| SpecificHeat | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | - | - |
| VapourResistivity | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | - | - |
| Description | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | - | - |
| Roughness | [Roughness](/api/oM/Analytical/Environment/MaterialFragments/Enums/Roughness) | Required for some calculations, such as determining the convective heat transfer coefficient. Use Roughness enum | - |
| Refraction | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | - | - |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface IEnvironmentMaterial : BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Physical.Materials.IMaterialProperties,
BH.oM.Base.IFragment,
BH.oM.Physical.Materials.IDensityProvider
```

Assembly: Environment_oM.dll

The C# interface definition is available on github:

- [IEnvironmentMaterial.cs](https://github.com/BHoM/BHoM/blob/develop/Environment_oM/MaterialFragments\IEnvironmentMaterial.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Environment_oM/MaterialFragments/IEnvironmentMaterial.json"
}
```

The JSON Schema is available on github here:

- [IEnvironmentMaterial.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Environment_oM/MaterialFragments/IEnvironmentMaterial.json)
