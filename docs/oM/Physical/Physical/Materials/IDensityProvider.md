---
title: IDensityProvider
---

# <small>BH.oM.Physical.Materials.</small>**IDensityProvider**

Interface to be added to IMaterialProperties the specifies the density of the Material the proeprty is attached to.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The IDensityProvider is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Physical.Materials.[IMaterialProperties](/api/oM/Physical/Physical/Materials/IMaterialProperties)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)


### Interfaces implementing this interface

???+ bhom "The following interfaces are implementing this interface:"

    - BH.oM.Environment.MaterialFragments.[IEnvironmentMaterial](/api/oM/Analytical/Environment/MaterialFragments/IEnvironmentMaterial)
    - BH.oM.Structure.MaterialFragments.[IIsotropic](/api/oM/Analytical/Structure/MaterialFragments/IIsotropic)
    - BH.oM.Structure.MaterialFragments.[IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment)
    - BH.oM.Structure.MaterialFragments.[IOrthotropic](/api/oM/Analytical/Structure/MaterialFragments/IOrthotropic)
    - BH.oM.Structure.MaterialFragments.[ITimber](/api/oM/Analytical/Structure/MaterialFragments/ITimber)


### Classes implementing this interface

???+ bhom "The following classes are implementing this interface:"

    - BH.oM.Environment.MaterialFragments.[GasMaterial](/api/oM/Analytical/Environment/MaterialFragments/GasMaterial)
    - BH.oM.Environment.MaterialFragments.[SolidMaterial](/api/oM/Analytical/Environment/MaterialFragments/SolidMaterial)
    - BH.oM.Adapters.GSA.MaterialFragments.[Fabric](/api/oM/Adapter/Adapters/GSA/MaterialFragments/Fabric)
    - BH.oM.Structure.MaterialFragments.[Aluminium](/api/oM/Analytical/Structure/MaterialFragments/Aluminium)
    - BH.oM.Structure.MaterialFragments.[Concrete](/api/oM/Analytical/Structure/MaterialFragments/Concrete)
    - BH.oM.Structure.MaterialFragments.[GenericIsotropicMaterial](/api/oM/Analytical/Structure/MaterialFragments/GenericIsotropicMaterial)
    - BH.oM.Structure.MaterialFragments.[GenericOrthotropicMaterial](/api/oM/Analytical/Structure/MaterialFragments/GenericOrthotropicMaterial)
    - BH.oM.Structure.MaterialFragments.[Glulam](/api/oM/Analytical/Structure/MaterialFragments/Glulam)
    - BH.oM.Structure.MaterialFragments.[LaminatedVeneerLumberCrossbands](/api/oM/Analytical/Structure/MaterialFragments/LaminatedVeneerLumberCrossbands)
    - BH.oM.Structure.MaterialFragments.[LaminatedVeneerLumberParallel](/api/oM/Analytical/Structure/MaterialFragments/LaminatedVeneerLumberParallel)
    - BH.oM.Structure.MaterialFragments.[SawnTimber](/api/oM/Analytical/Structure/MaterialFragments/SawnTimber)
    - BH.oM.Structure.MaterialFragments.[Steel](/api/oM/Analytical/Structure/MaterialFragments/Steel)
    - BH.oM.Structure.MaterialFragments.[Timber](/api/oM/Analytical/Structure/MaterialFragments/Timber)


## Properties



### Defining properties

The following properties are defined on the interface

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Density | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | - | [Density](/api/oM/Dimensional/Quantities/Attributes/Density) [kg/m³] |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface IDensityProvider : BH.oM.Physical.Materials.IMaterialProperties, BH.oM.Base.IBHoMObject, BH.oM.Base.IObject
```

Assembly: Physical_oM.dll

The C# interface definition is available on github:

- [IDensityProvider.cs](https://github.com/BHoM/BHoM/blob/develop/Physical_oM/Materials\IDensityProvider.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Physical_oM/Materials/IDensityProvider.json"
}
```

The JSON Schema is available on github here:

- [IDensityProvider.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Physical_oM/Materials/IDensityProvider.json)
