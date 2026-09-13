---
title: PanelReinforcement
---

# <small>BH.oM.Structure.Reinforcement.</small>**PanelReinforcement**

Defines the  reinforcement of a Panel in the longitudinal and transverse direction specified by the Basis of the ReinforcementRegion.
If the diameter of the reinforcement is set to 0, it will be assumed that no reinforcement is present in this direction.

## Class structure

### Implemented interfaces and base types

???+ bhom "The PanelReinforcement is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Material | [IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment) | Material of the reinforcement. | - |
| Region | [ReinforcementRegion](/api/oM/Analytical/Structure/Reinforcement/ReinforcementRegion) | The region defining the area of the Panel to be reinforced. | - |
| LongitudinalDiameter | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The diameter of the reinforcement in the longitudinal direction, denoted by the local x direction of the ReinforcementRegion.<br>If the diameter is set 0, it will be assumed that no reinforcement is present in the longitudinal direction. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| LongitudinalSpacing | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The spacing of the reinforcement in the longitudinal direction, measured perpindicular to the local x direction of the ReinforcementRegion. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| LongitudinalDepth | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The depth of longitudinal reinforcement measured from the centre of Panel along the normal. This will be negative for bottom reinforcement. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| TransverseDiameter | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The diameter of the reinforcement in the transverse direction, denoted by the local y direction of the ReinforcementRegion.<br>If the diameter is set 0, it will be assumed that no reinforcement is present in the longitudinal direction. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| TransverseSpacing | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The spacing of the reinforcement in the transverse direction, measured perpindicular to the local y direction of the ReinforcementRegion. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| TransverseDepth | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | The depth of transverse reinforcement measured from the centre of Panel along the normal. This will be negative for bottom reinforcement. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |
| MinimumCover | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Minimum cover for the reinforcement defined in this PanelReinforcement. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] |


### Inherited properties
The following properties are inherited from the base class of the object

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| BHoM_Guid | [Guid](https://learn.microsoft.com/en-us/dotnet/api/System.Guid?view=netstandard-2.0) | - | - |
| Name | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | - | - |
| Fragments | [FragmentSet](/api/oM/Framework/Base/FragmentSet) | - | - |
| Tags | [HashSet](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.HashSet-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | - | - |
| CustomData | [Dictionary](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.Dictionary-2?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0), [object](https://learn.microsoft.com/en-us/dotnet/api/System.Object?view=netstandard-2.0)&gt; | - | - |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a PanelReinforcement is null and outputs relevant error message. | - | Structure_Engine |
| LongitudinalBarArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the area of a single rebar in the PanelReinforcement in the logitudinal direction. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Structure_Engine |
| TransversalBarArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the area of a single rebar in the PanelReinforcement in the logitudinal direction. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class PanelReinforcement : BH.oM.Base.BHoMObject, BH.oM.Base.IBHoMObject, BH.oM.Base.IObject
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [PanelReinforcement.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/Reinforcement\PanelReinforcement.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/Reinforcement/PanelReinforcement.json"
}
```

The JSON Schema is available on github here:

- [PanelReinforcement.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/Reinforcement/PanelReinforcement.json)
