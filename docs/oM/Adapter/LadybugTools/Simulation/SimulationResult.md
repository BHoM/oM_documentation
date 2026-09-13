---
title: SimulationResult
---

# <small>BH.oM.LadybugTools.</small>**SimulationResult**



## Class structure

### Implemented interfaces and base types

???+ bhom "The SimulationResult is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.LadybugTools.[ILadybugTools](/api/oM/Adapter/LadybugTools/ILadybugTools)
    -  BH.oM.Base.[IImmutable](/api/oM/Framework/Base/Interface/IImmutable)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| EpwFile | [FileSettings](/api/oM/Framework/Adapter/FileSettings) | The EPW file associated with this object. | - |
| GroundMaterial | [IEnergyMaterialOpaque](/api/oM/Adapter/LadybugTools/Constructions/IEnergyMaterialOpaque) | The ground material used in the processing of this object. | - |
| ShadeMaterial | [IEnergyMaterialOpaque](/api/oM/Adapter/LadybugTools/Constructions/IEnergyMaterialOpaque) | The shade material used in the processing of this object. | - |
| Identifier | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | The identifier used to distinguish existing results for this object. | - |
| ShadedDownTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Shaded Down Temperature used in the processing of this object | - |
| ShadedUpTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Shaded Up Temperature used in the processing of this object | - |
| ShadedRadiantTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Shaded Radiant Temperature used in the processing of this object | - |
| ShadedLongwaveMeanRadiantTemperatureDelta | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Shaded Longwave Mean Radiant Temperature Delta used in the processing of this object | - |
| ShadedShortwaveMeanRadiantTemperatureDelta | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Shaded Shortwave Mean Radiant Temperature Delta used in the processing of this object | - |
| ShadedMeanRadiantTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Shaded Mean Radiant Temperature used in the processing of this object | - |
| UnshadedDownTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Unshaded Down Temperature used in the processing of this object | - |
| UnshadedUpTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Unshaded Up Temperature used in the processing of this object | - |
| UnshadedRadiantTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Unshaded Radiant Temperature used in the processing of this object | - |
| UnshadedLongwaveMeanRadiantTemperatureDelta | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Unshaded Longwave Mean Radiant Temperature Delta used in the processing of this object | - |
| UnshadedShortwaveMeanRadiantTemperatureDelta | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Unshaded Shortwave Mean Radiant Temperature Delta used in the processing of this object | - |
| UnshadedMeanRadiantTemperature | [HourlyContinuousCollection](/api/oM/Adapter/LadybugTools/Collections/HourlyContinuousCollection) | The Unshaded Mean Radiant Temperature used in the processing of this object | - |


### Inherited properties
The following properties are inherited from the base class of the object

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| BHoM_Guid | [Guid](https://learn.microsoft.com/en-us/dotnet/api/System.Guid?view=netstandard-2.0) | - | - |
| Name | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | - | - |
| Fragments | [FragmentSet](/api/oM/Framework/Base/FragmentSet) | - | - |
| Tags | [HashSet](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.HashSet-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | - | - |
| CustomData | [Dictionary](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.Dictionary-2?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0), [object](https://learn.microsoft.com/en-us/dotnet/api/System.Object?view=netstandard-2.0)&gt; | - | - |


## Code and Schema

### C# implementation

``` C# title="C#"
public class SimulationResult : BH.oM.Base.BHoMObject, BH.oM.Base.IBHoMObject, BH.oM.Base.IObject, BH.oM.LadybugTools.ILadybugTools, BH.oM.Base.IImmutable
```

Assembly: LadybugTools_oM.dll

The C# class definition is available on github:

- [SimulationResult.cs](https://github.com/BHoM/LadybugTools_Toolkit/blob/develop/LadybugTools_oM/Simulation\SimulationResult.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/LadybugTools_oM/SimulationResult.json"
}
```

The JSON Schema is available on github here:

- [SimulationResult.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/LadybugTools_oM/SimulationResult.json)
