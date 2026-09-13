---
title: ISurfaceProperty
---

# <small>BH.oM.Structure.SurfaceProperties.</small>**ISurfaceProperty**

Base interface for properties for 2D finite element structural objects such as Panels and FEMeshes.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The ISurfaceProperty is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Structure.[IProperty](/api/oM/Analytical/Structure/IProperty)


### Classes implementing this interface

???+ bhom "The following classes are implementing this interface:"

    - BH.oM.Adapters.GSA.SurfaceProperties.[FabricPanelProperty](/api/oM/Adapter/Adapters/GSA/SurfaceProperties/FabricPanelProperty)
    - BH.oM.Structure.SurfaceProperties.[BiDirectionalVoided](/api/oM/Analytical/Structure/SurfaceProperties/BiDirectionalVoided)
    - BH.oM.Structure.SurfaceProperties.[BuiltUpDoubleRibbed](/api/oM/Analytical/Structure/SurfaceProperties/BuiltUpDoubleRibbed)
    - BH.oM.Structure.SurfaceProperties.[BuiltUpRibbed](/api/oM/Analytical/Structure/SurfaceProperties/BuiltUpRibbed)
    - BH.oM.Structure.SurfaceProperties.[Cassette](/api/oM/Analytical/Structure/SurfaceProperties/Cassette)
    - BH.oM.Structure.SurfaceProperties.[ConstantThickness](/api/oM/Analytical/Structure/SurfaceProperties/ConstantThickness)
    - BH.oM.Structure.SurfaceProperties.[CorrugatedDeck](/api/oM/Analytical/Structure/SurfaceProperties/CorrugatedDeck)
    - BH.oM.Structure.SurfaceProperties.[HollowCore](/api/oM/Analytical/Structure/SurfaceProperties/HollowCore)
    - BH.oM.Structure.SurfaceProperties.[Layered](/api/oM/Analytical/Structure/SurfaceProperties/Layered)
    - BH.oM.Structure.SurfaceProperties.[LoadingPanelProperty](/api/oM/Analytical/Structure/SurfaceProperties/LoadingPanelProperty)
    - BH.oM.Structure.SurfaceProperties.[OneDirectionalVoided](/api/oM/Analytical/Structure/SurfaceProperties/OneDirectionalVoided)
    - BH.oM.Structure.SurfaceProperties.[Ribbed](/api/oM/Analytical/Structure/SurfaceProperties/Ribbed)
    - BH.oM.Structure.SurfaceProperties.[SlabOnDeck](/api/oM/Analytical/Structure/SurfaceProperties/SlabOnDeck)
    - BH.oM.Structure.SurfaceProperties.[ToppedSlab](/api/oM/Analytical/Structure/SurfaceProperties/ToppedSlab)
    - BH.oM.Structure.SurfaceProperties.[Waffle](/api/oM/Analytical/Structure/SurfaceProperties/Waffle)


## Properties



### Defining properties

The following properties are defined on the interface

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Material | [IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment) | Structural material of the property. | - |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| Construction | [Construction](/api/oM/Physical/Physical/Constructions/Construction) | Creates a physical Construction from a structural ISurfaceProperty. Extracts the Structural MaterialFragment and creates a physical material with the same name. | - | Structure_Engine |
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
| MaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Returns a SurfaceProperty's MaterialComposition. | - | Structure_Engine |
| Modifiers | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0)[] | Gets any modifiers from a property as an array of doubles. The modifiers are used to scale one or more of the property constants for analysis. Constants are multiplied with the modifiers, hence a modifier value of 1 means no change. <br>The values returned are in the following order: FXX, FXY, FYY, MXX, MXY, MYY, VXZ, VYZ, Mass, Weight. Method returns null if no modifiers are found. | - | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface ISurfaceProperty : BH.oM.Base.IBHoMObject, BH.oM.Base.IObject, BH.oM.Structure.IProperty
```

Assembly: Structure_oM.dll

The C# interface definition is available on github:

- [ISurfaceProperty.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/SurfaceProperties\ISurfaceProperty.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/SurfaceProperties/ISurfaceProperty.json"
}
```

The JSON Schema is available on github here:

- [ISurfaceProperty.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/SurfaceProperties/ISurfaceProperty.json)
