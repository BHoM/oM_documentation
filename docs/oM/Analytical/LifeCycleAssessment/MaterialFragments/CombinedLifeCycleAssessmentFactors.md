---
title: CombinedLifeCycleAssessmentFactors
---

# <small>BH.oM.LifeCycleAssessment.MaterialFragments.</small>**CombinedLifeCycleAssessmentFactors**

An Combined Life Cycle Assessment Factors is aggregate class to compute final impact factors.
This object is commonly created based on a EPD for cradle to gate metrics (A1 - A3) with addional project and site specific data added for relevant stages beyond the product stage.

## Class structure

### Implemented interfaces and base types

???+ bhom "The CombinedLifeCycleAssessmentFactors is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Physical.Materials.[IMaterialProperties](/api/oM/Physical/Physical/Materials/IMaterialProperties)
    -  BH.oM.LifeCycleAssessment.MaterialFragments.[IEnvironmentalFactorsProvider](/api/oM/Analytical/LifeCycleAssessment/MaterialFragments/IEnvironmentalFactorsProvider)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| EnvironmentalProductDeclaration | [EnvironmentalProductDeclaration](/api/oM/Analytical/LifeCycleAssessment/MaterialFragments/EnvironmentalProductDeclaration) | THe Environmental Product Declaration as the basis for the life cycle assessment. Commnly outlines the metrics for A1-A3 modules, but might contain metrics beyond those modules. | - |
| A4TransportFactors | [ITransportFactors](/api/oM/Analytical/LifeCycleAssessment/MaterialFragments/Transport/ITransportFactors) | Factors for computing the emissions relating to Module A4 which captures the impacts associated with the transportation of the materials and components from the factory gate to and from the project site. | - |
| A5_3ConstructionWasteEmissions | [ConstructionWasteEmissions](/api/oM/Analytical/LifeCycleAssessment/MaterialFragments/Construction/ConstructionWasteEmissions) | Factors for computing the emissions relating to the Construction and instalation process (A5). | - |
| C2TransportFactors | [ITransportFactors](/api/oM/Analytical/LifeCycleAssessment/MaterialFragments/Transport/ITransportFactors) | Factors for computing the emissions relating to Module C2. Module C2 Transport impacts consists of any carbon impacts associated with the transportation of material from deconstruction and demolition to the appropriate final location, including any interim stations. | - |
| C3C4WasteAndDisposalFactors | [WasteAndDisposalFactors](/api/oM/Analytical/LifeCycleAssessment/MaterialFragments/EndOfLife/WasteAndDisposalFactors) | Factors for computing the emissions relating to Module C3 (waste processing) and C4 (disposal). WasteAndDisposalFactors defines the end of life waste processing and disposal factors to be applied to the material fragment. These factors are applied in addition to any end of life factors provided by an Environmental Product Declaration, and can be used to fill gaps where no EPD data is available. If applied this will help populate all Climate change metrics available, with LandUseFactor being set to 0. | - |


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
| MaterialClassification | [MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification) | Evaluates the material classification of a material. | - | Matter_Engine |
| MaterialEndOfLifeTreatment | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Returns End of Life processing information contained within an EPD dataset. | - | LifeCycleAssessment_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class CombinedLifeCycleAssessmentFactors : BH.oM.Base.BHoMObject,
BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Physical.Materials.IMaterialProperties,
BH.oM.LifeCycleAssessment.MaterialFragments.IEnvironmentalFactorsProvider
```

Assembly: LifeCycleAssessment_oM.dll

The C# class definition is available on github:

- [CombinedLifeCycleAssessmentFactors.cs](https://github.com/BHoM/BHoM/blob/develop/LifeCycleAssessment_oM/MaterialFragments\CombinedLifeCycleAssessmentFactors.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/LifeCycleAssessment_oM/MaterialFragments/CombinedLifeCycleAssessmentFactors.json"
}
```

The JSON Schema is available on github here:

- [CombinedLifeCycleAssessmentFactors.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/LifeCycleAssessment_oM/MaterialFragments/CombinedLifeCycleAssessmentFactors.json)
