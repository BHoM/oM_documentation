---
title: Cassette
---

# <small>BH.oM.Structure.SurfaceProperties.</small>**Cassette**

Property for 2D analytical elements, made up of two slabs with parallel ribs running in one direction between them. Ribs and slabs can all be made up of different materials.

## Class structure

### Implemented interfaces and base types

???+ bhom "The Cassette is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Structure.SurfaceProperties.[ISurfaceProperty](/api/oM/Analytical/Structure/SurfaceProperties/ISurfaceProperty)
    -  BH.oM.Structure.[IProperty](/api/oM/Analytical/Structure/IProperty)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Name | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | A unique Name is required for some structural packages to create and identify the object. | - |
| TopThickness | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The thickness of the slab sitting on top of the ribs. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| BottomThickness | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The thickness of the slab sitting beneath the ribs. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| RibThickness | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Width of each rib. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| RibHeight | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Height of the ribs, equal to the distance between the bottom of the top slab and top of the bottom slab. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| RibSpacing | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Centre-centre distance between the ribs. Measured perpendicular to the rib direction. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| Material | [IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment) | Structural material of the top slab. If no material is provided for the ribs and/or the bottom slab then this material is used for those parts as well. | - |
| RibMaterial | [IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment) | Structural material of the ribs. If nothing is provided, the Material will be used instead. | - |
| BottomMaterial | [IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment) | Structural material of the bottom slab. If nothing is provided, the Material will be used instead. | - |
| Direction | [PanelDirection](/api/oM/Analytical/Structure/SurfaceProperties/Enums/PanelDirection) | Specifies if the ribs are running in local x or y direction. | - |
| PanelType | [PanelType](/api/oM/Analytical/Structure/SurfaceProperties/Enums/PanelType) | Defines what type of element this property will be used. Used by some analysis packages. | - |


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
| Construction | [Construction](/api/oM/Physical/Physical/Constructions/Construction) | Creates a physical Construction from a structural ISurfaceProperty. Extracts the Structural MaterialFragment and creates a physical material with the same name. | - | Structure_Engine |
| Description | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the SurfaceProperty as 'Cassette Top: TopThickness THK TopMaterialName Bot: BottomThickness THK BottomMaterialName Ribs: RibHeight x RibThickness RibMaterialName spaced RibSpacing'. | - | Structure_Engine |
| DescriptionOrName | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Gets the name from a IProperty. If null or empty, a default description name is provided instead. | - | Structure_Engine |
| HasModifiers | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a SurfaceProperty has any modifiers by first checking if any modifiers has been assigned, and if any of them are set to a value different than 1. | - | Structure_Engine |
| IConstruction | [Construction](/api/oM/Physical/Physical/Constructions/Construction) | Creates a physical Construction from a structural ISurfaceProperty. Extracts the Structural MaterialFragment and creates a physical material with the same name. | - | Structure_Engine |
| IDescription | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the SurfaceProperty, based on type, dimensions and material. | - | Structure_Engine |
| IDescription | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Generates a default description for the IProperty, based on its properties. | - | Structure_Engine |
| IMassPerArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the mass per area for the property. | [MassPerUnitArea](/api/oM/Dimensional/Quantities/Attributes/MassPerUnitArea) [kg/m²] | Structure_Engine |
| InvalidSurfaceProperty | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks whether a surface property is unsupported in Lusas. Only ConstantThickness is currently supported. | - | Lusas_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a SurfaceProperty is null and outputs relevant error message. | - | Structure_Engine |
| ITotalThickness | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Gets the total thickness of the surface property. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] | Structure_Engine |
| IVolumePerArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Gets the volume per area of the property for the purpose of calculating solid volume. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] | Structure_Engine |
| MassPerArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Gets the mass per area for a Cassette. | [MassPerUnitArea](/api/oM/Dimensional/Quantities/Attributes/MassPerUnitArea) [kg/m²] | Structure_Engine |
| MaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Returns a SurfaceProperty's MaterialComposition. | - | Structure_Engine |
| Modifiers | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0)[] | Gets any modifiers from a property as an array of doubles. The modifiers are used to scale one or more of the property constants for analysis. Constants are multiplied with the modifiers, hence a modifier value of 1 means no change. <br>The values returned are in the following order: FXX, FXY, FYY, MXX, MXY, MYY, VXZ, VYZ, Mass, Weight. Method returns null if no modifiers are found. | - | Structure_Engine |
| TotalThickness | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Gets the total thickness of the surface property. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] | Structure_Engine |
| VolumePerArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Gets the volume per area of the property for the purpose of calculating solid volume. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class Cassette : BH.oM.Base.BHoMObject,
BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Structure.SurfaceProperties.ISurfaceProperty,
BH.oM.Structure.IProperty
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [Cassette.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/SurfaceProperties\Cassette.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/SurfaceProperties/Cassette.json"
}
```

The JSON Schema is available on github here:

- [Cassette.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/SurfaceProperties/Cassette.json)
