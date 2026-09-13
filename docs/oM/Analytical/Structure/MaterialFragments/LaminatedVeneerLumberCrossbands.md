---
title: LaminatedVeneerLumberCrossbands
---

# <small>BH.oM.Structure.MaterialFragments.</small>**LaminatedVeneerLumberCrossbands**

Structural timber material of type Laminated Veneer Lumber with crossband veneers. To be used on structural elements and properties, or as a fragment of the physical material.
Note: Properties for LVL are not part of a harmonised standard and therefore vary between manufacturers and products.

## Class structure

### Implemented interfaces and base types

???+ bhom "The LaminatedVeneerLumberCrossbands is inheriting from the following base type(s) and implements the following interfaces:"

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
| Name | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | A unique name is required for some structural packages to create and identify the object. | - |
| Density | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean Density. Used to calculate mass. Called ρmean in most manufacturer documentation. | [Density](/api/oM/Dimensional/Quantities/Attributes/Density) [kg/m³] |
| DensityCharacteristic | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Density. Used to calculate other mechanical properties (not mass). Called ρk in most manufacturer documentation. | [Density](/api/oM/Dimensional/Quantities/Attributes/Density) [kg/m³] |
| DampingRatio | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Dynamic Damping Ratio. Ratio between actual damping and critical damping. | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| YoungsModulus | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Modulus Of Elasticity of the material to be used for Analysis. Ratio between stress and strain in all directions.<br>Values can be automatically populated based on material parameters by calling the SetAnalysisParameters method.<br>Vector defines stiffnesses as follows:<br>X - Stiffness along the local x-axis of the element. For most cases this will be the parallel stiffness (E_0).<br>Y - Stiffness along the local y-axis of the element. For most cases this will be parallel to the transverse grain direction (E_90_edge) for Flatwise and perpendicular to the glue-planes (E_90_flat) for Edgewise. For most beam/slab element cases this this will be the horizontal perpendicular stiffness.<br>Z - Stiffness along the local z-axis of the element. For most cases this will be perpendicular to the glue-planes (E_90_flat) for Flatwise and parallel to the transverse grain direction (E_90_edge) for Edgewise. For most beam/slab element cases this this will be the vertical perpendicular stiffness. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| ShearModulus | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Shear Modulus or Modulus of Rigidity of the material to be used for Analysis. Ratio between shear stress and shear strain.<br>Values can be automatically populated based on material parameters by calling the SetAnalysisParameters method.<br>Vector components defined as:<br>X - Shear Modulus in the local xy-plane (Gxy). For most cases this will parallel shear modulus (G_0) - For flatwise use this will be G_0_Edge, for Edgewise use this will be G_0_Flat.<br>Y - Shear Modulus in the local yz-plane (Gyz). For most cases this will be the perpendicular shear modulus - For both flatwise and edgewise G_90_flat.<br>Z - Shear Modulus in the local zx-plane (Gzx). For most cases this will parallel shear modulus (G_0) - For flatwise use this will be G_0_Flat, for Edgewise use this will be G_0_Edge. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| PoissonsRatio | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Poisson's Ratio. Ratio between axial and transverse strain. Typically taken as 0.4 for X and Y component (νxy and νyz) and as 0.4*E_90/E_0 for the Z component, though value varies depending on timber species.<br>Vector components made up of:<br>X - Poisson's ratio for strain in the local y direction generated by unit strain in x direction (νxy). Generally strain in perpendicular direction caused by strain in longitudinal direction.<br>Y - Poisson's ratio for strain in the local z direction generated by unit strain in y direction (νyz). Generally strain in perpendicular direction caused by strain in other perpendicular direction.<br>Z - Poisson's ratio for strain in the local x direction generated by unit strain in z direction (νzx). Generally strain in longitudinal direction caused by strain in perpendicular direction. Note that this value generally is significantly lower than values for the other two components. | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| ThermalExpansionCoeff | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Thermal Expansion Coefficeint. Strain induced in the material per unit change of temperature. Typically taken as 5x10^-6 in all directions, though value varies depending on timber species, grain orientation and lamination.<br>Vector defines stiffnesses as follows:<br>X - Thermal expansion along the local x-axis of the element (αx).<br>Y - Thermal expansion along the local y-axis of the element (αy).<br>Z - Thermal expansion along the local z-axis of the element (αz). | [ThermalExpansionCoefficient](/api/oM/Dimensional/Quantities/Attributes/ThermalExpansionCoefficient) [1/K] |
| E_0_k | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic modulus of elasticity parallel to grain, E0,k in most manufacturer documentation. Value same for Em,0,edge,k, Em,0,flat,k, Et,0,k, and Ec,0,k. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| E_90_Flat_k | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic modulus of elasticity for flatwise compression and tension perpendicular to the grain, Ec,90,flat,k and Et,90,flat,k in most manufacturer documentation. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| E_90_m_k | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic modulus of elasticity for flatwise bending perpendicular to the grain, Em,90,flat,k in most manufacturer documentation.<br>Stiffness direction same as E_90_Edge_k. Load condition should define which of the two to be used in analysis. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| E_90_Edge_k | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic modulus of elasticity for edgewise axialforce perpendicular to the grain, Ec,90,edge,k and Et,90,edge,k in most manufacturer documentation.<br>Stiffness direction same as E_90_m_k. Load condition should define which of the two to be used in analysis. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| E_0_Mean | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean modulus of elasticity parallel to grain, E0,mean in most manufacturer documentation. Value same for Em,0,edge,mean, Em,0,flat,mean, Et,0,mean, and Ec,0,mean. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| E_90_Flat_Mean | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean modulus of elasticity for flatwise compression and tension perpendicular to the grain, Ec,90,flat,mean and Et,90,flat,mean in most manufacturer documentation. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| E_90_m_Mean | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean modulus of elasticity for flatwise bending perpendicular to the grain, Em,90,flat,mean in most manufacturer documentation.<br>Stiffness direction same as E_90_Edge_Mean. Load condition should define which of the two to be used in analysis. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| E_90_Edge_Mean | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean modulus of elasticity for edgewise axialforce perpendicular to the grain, Ec,90,edge,mean and Et,90,edge,mean in most manufacturer documentation.<br>Stiffness direction same as E_90_m_Mean. Load condition should define which of the two to be used in analysis. | [YoungsModulus](/api/oM/Dimensional/Quantities/Attributes/YoungsModulus) [Pa] |
| G_0_Edge_k | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic shear modulus for edgewise shear parallel to the grain, G0,edge,k in most manufacturer documentation. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| G_0_Flat_k | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic shear modulus for flatwise shear parallel to the grain, G0,flat,k in most manufacturer documentation. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| G_90_Flat_k | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic shear modulus for flatwise shear perpendicular to the grain, G90,flat,k in most manufacturer documentation. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| G_0_Edge_Mean | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean shear modulus for edgewise shear parallel to the grain, G0,edge,mean in most manufacturer documentation. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| G_0_Flat_Mean | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean shear modulus for flatwise shear parallel to the grain, G0,flat,mean in most manufacturer documentation. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| G_90_Flat_Mean | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Mean shear modulus for flatwise shear perpendicular to the grain, G90,flat,mean in most manufacturer documentation. | [ShearModulus](/api/oM/Dimensional/Quantities/Attributes/ShearModulus) [Pa] |
| BendingStrengthEdgeParallel | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Edgewise bending Strength, parallel to the grain. Called fm,0,edge,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| BendingStrengthFlatParallel | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Flatwise Bending Strength parallel to the grain. Called fm,0,flat,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| BendingStrengthFlatPerpendicular | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Flatwise Bending Strength perpendicular to the grain. Called fm,90,flat,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| SizeEffectParameter | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Size effect parameter for strength. | - |
| TensileStrengthParallel | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Tensile parallel Strength. Tension stress parallel to the grain at failure in net tension. Called ft,0,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| TensileStrengthEdgePerpendicular | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Edgewise tensile perpendicular Strength. Tension stress perpendicular to the grain at failure in net tension. Called ft,90,edge,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| TensileStrengthFlatPerpendicular | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Flatwise tensile perpendicular Strength. Tension stress perpendicular to the grain at failure in net tension. Called ft,90,flat,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| CompressiveStrengthParallel | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Compressive parallel Strength. Compression stress parallel to the grain at failure in net compression. Called fc,0,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| CompressiveStrengthEdgePerpendicular | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Edgewise compressive perpendicular Strength. Compression stress perpendicular to the grain at failure in net compression. Called fc,90,edge,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| CompressiveStrengthFlatPerpendicular | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Flatwise compressive perpendicular Strength. Compression stress perpendicular to the grain at failure in net compression. Called fc,90,flat,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| ShearStrengthEdge | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Edgewise Shear Strength parallel. Shear stress parallel to the grain at failure in net shear for edgewise shearing. Called fv,0,edge,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| ShearStrengthFlatParallel | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Flatwise Shear Strength parallel. Shear stress parallel to the grain at failure in net shear for flatwise shearing. Called fv,0,flat,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |
| ShearStrengthFlatPerpendicular | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Characteristic Flatwise Shear Strength parallel. Shear stress parallel to the grain at failure in net shear for flatwise shearing. Called fv,0,flat,k in most manufacturer documentation. | [Stress](/api/oM/Dimensional/Quantities/Attributes/Stress) [Pa] |


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
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a ITimber is null and outputs relevant error message. | - | Structure_Engine |
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class LaminatedVeneerLumberCrossbands : BH.oM.Base.BHoMObject,
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

- [LaminatedVeneerLumberCrossbands.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/MaterialFragments\LaminatedVeneerLumberCrossbands.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/MaterialFragments/LaminatedVeneerLumberCrossbands.json"
}
```

The JSON Schema is available on github here:

- [LaminatedVeneerLumberCrossbands.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/MaterialFragments/LaminatedVeneerLumberCrossbands.json)
