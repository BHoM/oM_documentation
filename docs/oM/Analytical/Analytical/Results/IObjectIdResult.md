---
title: IObjectIdResult
---

# <small>BH.oM.Analytical.Results.</small>**IObjectIdResult**

Interface for Results belonging to a particular object. The owning object is identified and correlated to the Results by its ID.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The IObjectIdResult is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Analytical.Results.[IResult](/api/oM/Analytical/Analytical/Results/IResult)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  [IComparable](https://learn.microsoft.com/en-us/dotnet/api/System.IComparable-1?view=netstandard-2.0)&lt;BH.oM.Analytical.Results.[IResult](/api/oM/Analytical/Analytical/Results/IResult)&gt;
    -  BH.oM.Base.[IImmutable](/api/oM/Framework/Base/Interface/IImmutable)


### Interfaces implementing this interface

???+ bhom "The following interfaces are implementing this interface:"

    - BH.oM.Analytical.Results.[IElement1DResult](/api/oM/Analytical/Analytical/Results/IElement1DResult)
    - BH.oM.Analytical.Results.[IMeshResult](/api/oM/Analytical/Analytical/Results/IMeshResult)&lt;[T](/api/oM/Analytical/Analytical/Results/IMeshResult#t)&gt;
    - BH.oM.Analytical.Results.[IObjectResult](/api/oM/Analytical/Analytical/Results/IObjectResult)
    - BH.oM.LifeCycleAssessment.Results.[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[T](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult#t)&gt;
    - BH.oM.Structure.Results.[IBarDisplacement](/api/oM/Analytical/Structure/Results/Bar Results/IBarDisplacement)
    - BH.oM.Structure.Results.[IDisplacement](/api/oM/Analytical/Structure/Results/IDisplacement)
    - BH.oM.Structure.Results.[IReaction](/api/oM/Analytical/Structure/Results/IReaction)
    - BH.oM.Structure.Results.[IStructuralResult](/api/oM/Analytical/Structure/Results/IStructuralResult)
    - BH.oM.Structure.Results.[IMeshDisplacement](/api/oM/Analytical/Structure/Results/Mesh/IMeshDisplacement)
    - BH.oM.Structure.Results.[INodeDisplacement](/api/oM/Analytical/Structure/Results/Nodal Results/INodeDisplacement)


### Classes implementing this interface

??? bhom "The following classes are implementing this interface:"

    - BH.oM.Analytical.Elements.[ShortestPathResult](/api/oM/Analytical/Analytical/Results/ShortestPathResult)
    - BH.oM.Environment.Results.Mesh.[MeshElementResult](/api/oM/Analytical/Environment/Results/Mesh/MeshElementResult)
    - BH.oM.Environment.Results.Mesh.[MeshResult](/api/oM/Analytical/Environment/Results/Mesh/MeshResult)
    - BH.oM.Environment.Results.Illuminance.[Lux](/api/oM/Analytical/Environment/Results/Illuminance/Lux)
    - BH.oM.Adapters.ETABS.Results.[PierForce](/api/oM/Adapter/Adapters/ETABS/Results/PierForce)
    - BH.oM.Adapters.ETABS.Results.[SpandrelForce](/api/oM/Adapter/Adapters/ETABS/Results/SpandrelForce)
    - BH.oM.Humans.ViewQuality.[Avalue](/api/oM/Physical/Humans/ViewQuality/Results/Avalue)
    - BH.oM.Humans.ViewQuality.[Cvalue](/api/oM/Physical/Humans/ViewQuality/Results/Cvalue)
    - BH.oM.Humans.ViewQuality.[Evalue](/api/oM/Physical/Humans/ViewQuality/Results/Evalue)
    - BH.oM.Humans.ViewQuality.[ViewQualityResult](/api/oM/Physical/Humans/ViewQuality/Results/ViewQualityResult)
    - BH.oM.LifeCycleAssessment.Results.[AbioticDepletionFossilResourcesElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/AbioticDepletionFossilResourcesElementResult)
    - BH.oM.LifeCycleAssessment.Results.[AbioticDepletionMineralsAndMetalsElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/AbioticDepletionMineralsAndMetalsElementResult)
    - BH.oM.LifeCycleAssessment.Results.[AcidificationElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/AcidificationElementResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeBiogenicElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/ClimateChangeBiogenicElementResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeFossilElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/ClimateChangeFossilElementResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeLandUseElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/ClimateChangeLandUseElementResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeTotalElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/ClimateChangeTotalElementResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeTotalNoBiogenicElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/ClimateChangeTotalNoBiogenicElementResult)
    - BH.oM.LifeCycleAssessment.Results.[ElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/ElementResult)&lt;[T](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/ElementResult#t)&gt;
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationAquaticFreshwaterElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/EutrophicationAquaticFreshwaterElementResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationAquaticMarineElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/EutrophicationAquaticMarineElementResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationCMLElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/EutrophicationCMLElementResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationTerrestrialElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/EutrophicationTerrestrialElementResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationTRACIElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/EutrophicationTRACIElementResult)
    - BH.oM.LifeCycleAssessment.Results.[OzoneDepletionElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/OzoneDepletionElementResult)
    - BH.oM.LifeCycleAssessment.Results.[PhotochemicalOzoneCreationCMLElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/PhotochemicalOzoneCreationCMLElementResult)
    - BH.oM.LifeCycleAssessment.Results.[PhotochemicalOzoneCreationElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/PhotochemicalOzoneCreationElementResult)
    - BH.oM.LifeCycleAssessment.Results.[PhotochemicalOzoneCreationTRACIElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/PhotochemicalOzoneCreationTRACIElementResult)
    - BH.oM.LifeCycleAssessment.Results.[WaterDeprivationElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/ElementResults/WaterDeprivationElementResult)
    - BH.oM.Lighting.Results.Mesh.[MeshElementResult](/api/oM/Analytical/Lighting/Results/Mesh/MeshElementResult)
    - BH.oM.Lighting.Results.Mesh.[MeshResult](/api/oM/Analytical/Lighting/Results/Mesh/MeshResult)
    - BH.oM.Lighting.Results.Illuminance.[Lux](/api/oM/Analytical/Lighting/Results/Illuminance/Lux)
    - BH.oM.Adapters.SAP2000.Results.[AISCSteelUtilisation](/api/oM/Adapter/Adapters/SAP2000/Elements/AISCSteelUtilisation)
    - BH.oM.Structure.Results.[BarDeformation](/api/oM/Analytical/Structure/Results/Bar Results/BarDeformation)
    - BH.oM.Structure.Results.[BarDisplacement](/api/oM/Analytical/Structure/Results/Bar Results/BarDisplacement)
    - BH.oM.Structure.Results.[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)
    - BH.oM.Structure.Results.[BarModeShape](/api/oM/Analytical/Structure/Results/Bar Results/BarModeShape)
    - BH.oM.Structure.Results.[BarRequiredArea](/api/oM/Analytical/Structure/Results/Bar Results/BarRequiredArea)
    - BH.oM.Structure.Results.[BarResult](/api/oM/Analytical/Structure/Results/Bar Results/BarResult)
    - BH.oM.Structure.Results.[BarStrain](/api/oM/Analytical/Structure/Results/Bar Results/BarStrain)
    - BH.oM.Structure.Results.[BarStress](/api/oM/Analytical/Structure/Results/Bar Results/BarStress)
    - BH.oM.Structure.Results.[CompositeUtilisation](/api/oM/Analytical/Structure/Results/Bar Results/CompositeUtilisation)
    - BH.oM.Structure.Results.[SteelUtilisation](/api/oM/Analytical/Structure/Results/Bar Results/SteelUtilisation)
    - BH.oM.Structure.Results.[GlobalReactions](/api/oM/Analytical/Structure/Results/Global Results/GlobalReactions)
    - BH.oM.Structure.Results.[ModalDynamics](/api/oM/Analytical/Structure/Results/Global Results/ModalDynamics)
    - BH.oM.Structure.Results.[ModalMassAndFrequency](/api/oM/Analytical/Structure/Results/Global Results/ModalMassAndFrequency)
    - BH.oM.Structure.Results.[StoreyDrift](/api/oM/Analytical/Structure/Results/Global Results/StoreyDrift)
    - BH.oM.Structure.Results.[StructuralGlobalResult](/api/oM/Analytical/Structure/Results/Global Results/StructuralGlobalResult)
    - BH.oM.Structure.Results.[LinkDisplacement](/api/oM/Analytical/Structure/Results/Link Results/LinkDisplacement)
    - BH.oM.Structure.Results.[LinkForce](/api/oM/Analytical/Structure/Results/Link Results/LinkForce)
    - BH.oM.Structure.Results.[LinkResult](/api/oM/Analytical/Structure/Results/Link Results/LinkResult)
    - BH.oM.Structure.Results.[MeshDisplacement](/api/oM/Analytical/Structure/Results/Mesh/MeshDisplacement)
    - BH.oM.Structure.Results.[MeshElementResult](/api/oM/Analytical/Structure/Results/Mesh/MeshElementResult)
    - BH.oM.Structure.Results.[MeshForce](/api/oM/Analytical/Structure/Results/Mesh/MeshForce)
    - BH.oM.Structure.Results.[MeshModeShape](/api/oM/Analytical/Structure/Results/Mesh/MeshModeShape)
    - BH.oM.Structure.Results.[MeshRequiredArea](/api/oM/Analytical/Structure/Results/Mesh/MeshRequiredArea)
    - BH.oM.Structure.Results.[MeshResult](/api/oM/Analytical/Structure/Results/Mesh/MeshResult)
    - BH.oM.Structure.Results.[MeshStress](/api/oM/Analytical/Structure/Results/Mesh/MeshStress)
    - BH.oM.Structure.Results.[MeshVonMises](/api/oM/Analytical/Structure/Results/Mesh/MeshVonMises)
    - BH.oM.Structure.Results.[NodeAcceleration](/api/oM/Analytical/Structure/Results/Nodal Results/NodeAcceleration)
    - BH.oM.Structure.Results.[NodeDisplacement](/api/oM/Analytical/Structure/Results/Nodal Results/NodeDisplacement)
    - BH.oM.Structure.Results.[NodeModalMass](/api/oM/Analytical/Structure/Results/Nodal Results/NodeModalMass)
    - BH.oM.Structure.Results.[NodeModalResults](/api/oM/Analytical/Structure/Results/Nodal Results/NodeModalResults)
    - BH.oM.Structure.Results.[NodeModeShape](/api/oM/Analytical/Structure/Results/Nodal Results/NodeModeShape)
    - BH.oM.Structure.Results.[NodeReaction](/api/oM/Analytical/Structure/Results/Nodal Results/NodeReaction)
    - BH.oM.Structure.Results.[NodeResult](/api/oM/Analytical/Structure/Results/Nodal Results/NodeResult)
    - BH.oM.Structure.Results.[NodeVelocity](/api/oM/Analytical/Structure/Results/Nodal Results/NodeVelocity)
    - BH.oM.Structure.Design.[DesignResult](/api/oM/Analytical/Structure/Design/DesignResult)
    - BH.oM.Test.Results.[InputOutputComparisonDiffing](/api/oM/Framework/Test/Results/InputOutputComparisonDiffing)
    - BH.oM.Test.Results.[InputOutputComparisonSummary](/api/oM/Framework/Test/Results/InputOutputComparisonSummary)
    - BH.oM.Test.Results.[InputOutputDifference](/api/oM/Framework/Test/Results/InputOutputDifference)


## Properties



### Defining properties

The following properties are defined on the interface

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| ObjectId | [IComparable](https://learn.microsoft.com/en-us/dotnet/api/System.IComparable?view=netstandard-2.0) | The ID of the object to which the result belongs. The ID could be for example the AdapterID, Name or BHoM_Guid of the object. | - |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| AllIdentifierProperties | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets the name of all properties of the result that are of identifier types. This is all properties tagged with any IdentifierAttribute. | - | Results_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a Result is null and outputs relevant error message. | - | Results_Engine |
| ObjectIdentifierProperties | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets the name of all properties of the result that are of ObjectIdentifier types. This is all properties tagged with the ObjectIdentifierAttribute. | - | Results_Engine |
| ResultPropertyKeys | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Returns the result value carrying properties available for the result type provided. Currently only supported for IResultItem and IResultCollection&lt;IResultItem&gt; type results. | - | Results_Engine |
| ScenarioIdentifierProperties | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets the name of all properties of the result that are of Scenario types. This is all properties tagged with the ScenarioIdentifierAttribute. | - | Results_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface IObjectIdResult : BH.oM.Analytical.Results.IResult,
BH.oM.Base.IObject,
System.IComparable<BH.oM.Analytical.Results.IResult>,
BH.oM.Base.IImmutable
```

Assembly: Analytical_oM.dll

The C# interface definition is available on github:

- [IObjectIdResult.cs](https://github.com/BHoM/BHoM/blob/develop/Analytical_oM/Results\IObjectIdResult.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Analytical_oM/Results/IObjectIdResult.json"
}
```

The JSON Schema is available on github here:

- [IObjectIdResult.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Analytical_oM/Results/IObjectIdResult.json)
