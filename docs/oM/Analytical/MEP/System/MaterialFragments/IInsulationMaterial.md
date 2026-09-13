---
title: IInsulationMaterial
---

# <small>BH.oM.MEP.System.MaterialFragments.</small>**IInsulationMaterial**

Insulation is the material surrounding a duct, pipe or wire which mitigates the loss of the internal conditions of the fluid within the object.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The IInsulationMaterial is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Physical.Materials.[IMaterialProperties](/api/oM/Physical/Physical/Materials/IMaterialProperties)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)


### Classes implementing this interface

???+ bhom "The following classes are implementing this interface:"

    - BH.oM.MEP.System.MaterialFragments.[InsulationMaterial](/api/oM/Analytical/MEP/System/MaterialFragments/InsulationMaterial)
    - BH.oM.MEP.System.MaterialFragments.[LiningMaterial](/api/oM/Analytical/MEP/System/MaterialFragments/LiningMaterial)


## Properties



### Defining properties

The following properties are defined on the interface

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| RValue | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | RValue is the measure of the resistance of conductive heat loss by the insulation material. | - |
| KValue | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | KValue is the measure of the insulation material's ability to conduct heat (W/m*K), the lower the KValue the better the ability to conduct heat. | - |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface IInsulationMaterial : BH.oM.Base.IFragment, BH.oM.Base.IObject, BH.oM.Physical.Materials.IMaterialProperties, BH.oM.Base.IBHoMObject
```

Assembly: MEP_oM.dll

The C# interface definition is available on github:

- [IInsulationMaterial.cs](https://github.com/BHoM/BHoM/blob/develop/MEP_oM/System\MaterialFragments\IInsulationMaterial.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/MEP_oM/System/MaterialFragments/IInsulationMaterial.json"
}
```

The JSON Schema is available on github here:

- [IInsulationMaterial.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/MEP_oM/System/MaterialFragments/IInsulationMaterial.json)
