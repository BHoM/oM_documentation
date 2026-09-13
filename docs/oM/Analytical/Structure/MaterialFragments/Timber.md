---
title: Timber
---

# <small>BH.oM.Structure.MaterialFragments.</small>**Timber**

Structural timber material to be used on structural elements and properties or as a fragment of the physical material.

## Class structure

### Implemented interfaces and base types

???+ bhom "The Timber is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Structure.MaterialFragments.[ITimber](/api/oM/Analytical/Structure/MaterialFragments/ITimber)
    -  BH.oM.Structure.MaterialFragments.[IOrthotropic](/api/oM/Analytical/Structure/MaterialFragments/IOrthotropic)
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
| Name | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Name. A unique name is required for some structural packages to create and identify the object. | - |
| DensityCharacteristic | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Density. Used to calculate other mechanical properties (not mass). Called G (specific gravity) in American codes, p_k in Eurocode. | [Density](/api/oM/Dimensional/Quantities/Attributes/Density) [kg/m³] |
| Density | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean Density. Used to calculate mass. Called p_mean in Eurocode. | [Density](/api/oM/Dimensional/Quantities/Attributes/Density) [kg/m³] |
| DampingRatio | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Dynamic Damping Ratio. Ratio between actual damping and critical damping. | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| YoungsModulus | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Characteristic Modulus Of Elasticity of the material. Ratio between stress and strain in all directions. Vector components made up of: X - Parallel, E_0,k in Eurocode; Y - Perpendicular, E_90,k in Eurocode; Z - Perpendicular, E_90,k in Eurocode. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| YoungsModulusMean | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Mean Modulus Of Elasticity of the material. Ratio between stress and strain in all directions. Vector components made up of: X - Parallel, E_0,mean in Eurocode; Y - Perpendicular, E_90,mean in Eurocode; Z - Perpendicular, E_90,mean in Eurocode. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| PoissonsRatio | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Poisson's Ratio. Ratio between axial and transverse strain. Typically take as 0.4 in all directions, though value varies depending on timber species. Vector components made up of: X - Parallel; Y - Perpendicular; Z - Perpendicular. | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| ThermalExpansionCoeff | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Thermal Expansion Coefficeint. Strain induced in the material per unit change of temperature. Typically take as 5x10^-6 in all directions, though value varies depending on timber species. Vector components made up of: X - Parallel; Y - Perpendicular; Z - Perpendicular. | [ThermalExpansionCoefficient](/api/oM/Dimensional/Quantities/Attributes/ThermalExpansionCoefficient) [1/K] |
| ShearModulus | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Characterstic Shear Modulus or Modulus of Rigidity. Ratio between shear stress and shear strain. Vector components made up of: X - Parallel, G_k in Eurocode; Y - Parallel, G_k in Eurocode; Z - Perpendicular, G_r,05 in Eurocode. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| ShearModulusMean | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Mean Shear Modulus or Modulus of Rigidity. Ratio between shear stress and shear strain. Vector components made up of: X - Parallel, G_mean in Eurocode; Y - Parallel, G_mean in Eurocode; Z - Perpendicular, G_r,mean in Eurocode. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| BendingStrength | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Bending Strength. Tension stress parallel to the grain at failure in bending as calculated from beam equations. Called F_b in American codes, f_mk in Eurocode. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| TensionParallelStrength | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Tension Parallel Strength. Tension stress parallel to the grain at failure in net tension. Called F_t∥ in American codes, f_t0k in Eurocode. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| TensionPerpendicularStrength | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Tension Perpendicular Strength. Tension stress perpendicular to the grain at failure in net tension. Called F_t⟂ in American codes, f_t90k in Eurocode. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| CompressionParallelStrength | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Compression Parallel Strength. Compression stress parallel to the grain at failure in net compression. Called F_c∥ in American codes, f_c0k in Eurocode. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| CompressionPerpendicularStrength | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Compression Perpendicular Strength. Compression stress perpendicular to the grain at failure in net compression. Called F_c⟂ in American codes, f_c90k in Eurocode. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| ShearStrength | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Shear Strength. Shear stress parallel to the grain at failure in net shear, i.e. shear relevant to beam bending. Called F_v in American codes, f_vk in Eurocode. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| RollingShearStrength | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Rolling Shear Strength. Shear stress perpendicular to the grain at failure in net shear. Called F_s in American codes, F_rk in Eurocode. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |


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
| Description | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the material based on its properties. | - | Structure_Engine |
| DescriptionOrName | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Gets the name from a IProperty. If null or empty, a default description name is provided instead. | - | Structure_Engine |
| IDescription | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the IProperty, based on its properties. | - | Structure_Engine |
| IMaterialType | [MaterialType](/api/oM/Analytical/Structure/MaterialFragments/Enums/MaterialType) | Gets the material type from the MaterialFragment. | - | Structure_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a MaterialFragment is null and outputs relevant error message. | - | Structure_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a ITimber is null and outputs relevant error message. | - | Structure_Engine |
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |
| MaterialType | [MaterialType](/api/oM/Analytical/Structure/MaterialFragments/Enums/MaterialType) | Gets the material type from the MaterialFragment. For a Timber material this will always return type Timber. | - | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class Timber : BH.oM.Base.BHoMObject,
BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Structure.MaterialFragments.ITimber,
BH.oM.Structure.MaterialFragments.IOrthotropic,
BH.oM.Structure.MaterialFragments.IMaterialFragment,
BH.oM.Base.IFragment,
BH.oM.Physical.Materials.IMaterialProperties,
BH.oM.Structure.IProperty,
BH.oM.Physical.Materials.IDensityProvider
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [Timber.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/MaterialFragments\Timber.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/MaterialFragments/Timber.json"
}
```

The JSON Schema is available on github here:

- [Timber.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/MaterialFragments/Timber.json)
