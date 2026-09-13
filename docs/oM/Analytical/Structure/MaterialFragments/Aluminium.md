---
title: Aluminium
---

# <small>BH.oM.Structure.MaterialFragments.</small>**Aluminium**

Structural aluminium material to be used on structural elements and properties or as a fragment of the physical material.

## Class structure

### Implemented interfaces and base types

???+ bhom "The Aluminium is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Structure.MaterialFragments.[IIsotropic](/api/oM/Analytical/Structure/MaterialFragments/IIsotropic)
    -  BH.oM.Structure.MaterialFragments.[IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment)
    -  BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)
    -  BH.oM.Physical.Materials.[IMaterialProperties](/api/oM/Physical/Physical/Materials/IMaterialProperties)
    -  BH.oM.Structure.[IProperty](/api/oM/Analytical/Structure/IProperty)
    -  BH.oM.Physical.Materials.[IDensityProvider](/api/oM/Physical/Physical/Materials/IDensityProvider)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Name | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Unique Names are required for some structural packages to create and identify the object. | - |
| Density | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | - | [Density](/api/oM/Dimensional/Quantities/Attributes/Density) [kg/m³] |
| DampingRatio | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Dynamic damping ratio, expressed as a ratio between actual damping and critical damping. For structures, typically taken as 0.02 (i.e. 2%). | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| PoissonsRatio | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Ratio between axial and transverse strain. Used together with YoungsModulus to derive the ShearModulus for isotropic materials. | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| ThermalExpansionCoeff | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The strain induced in the material per unit change of temperature. | [ThermalExpansionCoefficient](/api/oM/Dimensional/Quantities/Attributes/ThermalExpansionCoefficient) [1/K] |
| YoungsModulus | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Modulus of elasticity of the material. Ratio between axial stress and axial strain. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |


### Inherited properties
The following properties are inherited from the base class of the object

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| BHoM_Guid | [Guid](https://learn.microsoft.com/en-us/dotnet/api/System.Guid?view=netstandard-2.0) | - | - |
| Fragments | [FragmentSet](/api/oM/Framework/Base/FragmentSet) | - | - |
| Tags | [HashSet](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.HashSet-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | - | - |
| CustomData | [Dictionary](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.Dictionary-2?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0), [object](https://learn.microsoft.com/en-us/dotnet/api/System.Object?view=netstandard-2.0)&gt; | - | - |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| Description | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the material based on its properties. | - | Structure_Engine |
| DescriptionOrName | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Gets the name from a IProperty. If null or empty, a default description name is provided instead. | - | Structure_Engine |
| IDescription | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the IProperty, based on its properties. | - | Structure_Engine |
| IMaterialType | [MaterialType](/api/oM/Analytical/Structure/MaterialFragments/Enums/MaterialType) | Gets the material type from the MaterialFragment. | - | Structure_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a MaterialFragment is null and outputs relevant error message. | - | Structure_Engine |
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |
| MaterialType | [MaterialType](/api/oM/Analytical/Structure/MaterialFragments/Enums/MaterialType) | Gets the material type from the MaterialFragment. For a Aluminium material this will always return type Aluminium. | - | Structure_Engine |
| ShearModulus | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Shear modulus of the isotropic material fragment. Evaluated based on YoungsModulus and PoissonsRatio as G = E/2(1+ν). | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class Aluminium : BH.oM.Base.BHoMObject,
BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Structure.MaterialFragments.IIsotropic,
BH.oM.Structure.MaterialFragments.IMaterialFragment,
BH.oM.Base.IFragment,
BH.oM.Physical.Materials.IMaterialProperties,
BH.oM.Structure.IProperty,
BH.oM.Physical.Materials.IDensityProvider
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [Aluminium.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/MaterialFragments\Aluminium.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/MaterialFragments/Aluminium.json"
}
```

The JSON Schema is available on github here:

- [Aluminium.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/MaterialFragments/Aluminium.json)
