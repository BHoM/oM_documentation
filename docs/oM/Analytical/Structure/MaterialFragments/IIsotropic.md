---
title: IIsotropic
---

# <small>BH.oM.Structure.MaterialFragments.</small>**IIsotropic**

Base interface for isotropic structural materials.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The IIsotropic is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Structure.MaterialFragments.[IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment)
    -  BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Physical.Materials.[IMaterialProperties](/api/oM/Physical/Physical/Materials/IMaterialProperties)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Structure.[IProperty](/api/oM/Analytical/Structure/IProperty)
    -  BH.oM.Physical.Materials.[IDensityProvider](/api/oM/Physical/Physical/Materials/IDensityProvider)


### Classes implementing this interface

???+ bhom "The following classes are implementing this interface:"

    - BH.oM.Structure.MaterialFragments.[Aluminium](/api/oM/Analytical/Structure/MaterialFragments/Aluminium)
    - BH.oM.Structure.MaterialFragments.[Concrete](/api/oM/Analytical/Structure/MaterialFragments/Concrete)
    - BH.oM.Structure.MaterialFragments.[GenericIsotropicMaterial](/api/oM/Analytical/Structure/MaterialFragments/GenericIsotropicMaterial)
    - BH.oM.Structure.MaterialFragments.[Steel](/api/oM/Analytical/Structure/MaterialFragments/Steel)


## Properties



### Defining properties

The following properties are defined on the interface

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| YoungsModulus | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Modulus of elasticity of the material. Ratio between axial stress and axial strain. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| PoissonsRatio | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Ratio between axial and transverse strain. Used together with YoungsModulus to derive the ShearModulus for isotropic materials. | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| ThermalExpansionCoeff | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The strain induced in the material per unit change of temperature. | [ThermalExpansionCoefficient](/api/oM/Dimensional/Quantities/Attributes/ThermalExpansionCoefficient) [1/K] |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| DescriptionOrName | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Gets the name from a IProperty. If null or empty, a default description name is provided instead. | - | Structure_Engine |
| IDescription | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the IProperty, based on its properties. | - | Structure_Engine |
| IMaterialType | [MaterialType](/api/oM/Analytical/Structure/MaterialFragments/Enums/MaterialType) | Gets the material type from the MaterialFragment. | - | Structure_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a MaterialFragment is null and outputs relevant error message. | - | Structure_Engine |
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |
| ShearModulus | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Shear modulus of the isotropic material fragment. Evaluated based on YoungsModulus and PoissonsRatio as G = E/2(1+ν). | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface IIsotropic : BH.oM.Structure.MaterialFragments.IMaterialFragment,
BH.oM.Base.IFragment,
BH.oM.Base.IObject,
BH.oM.Physical.Materials.IMaterialProperties,
BH.oM.Base.IBHoMObject,
BH.oM.Structure.IProperty,
BH.oM.Physical.Materials.IDensityProvider
```

Assembly: Structure_oM.dll

The C# interface definition is available on github:

- [IIsotropic.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/MaterialFragments\IIsotropic.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/MaterialFragments/IIsotropic.json"
}
```

The JSON Schema is available on github here:

- [IIsotropic.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/MaterialFragments/IIsotropic.json)
