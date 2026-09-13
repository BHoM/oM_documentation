---
title: IResultItem
---

# <small>BH.oM.Analytical.Results.</small>**IResultItem**

Base interface to flag that the result is a simple result line.
A class implementing the IResultItem interface should only contain basic properties such as doubles, ints, strings, DateTime and similar.
For instance, a class implementing this interface could be represented as a single row in a table (e.g. Excel or a SQL database) with its properties explicitly readable.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The IResultItem is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Analytical.Results.[IResult](/api/oM/Analytical/Analytical/Results/IResult)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  [IComparable](https://learn.microsoft.com/en-us/dotnet/api/System.IComparable-1?view=netstandard-2.0)&lt;BH.oM.Analytical.Results.[IResult](/api/oM/Analytical/Analytical/Results/IResult)&gt;
    -  BH.oM.Base.[IImmutable](/api/oM/Framework/Base/Interface/IImmutable)


### Interfaces implementing this interface

???+ bhom "The following interfaces are implementing this interface:"

    - BH.oM.LifeCycleAssessment.Results.[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[T](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult#t)&gt;
    - BH.oM.LifeCycleAssessment.Results.[IEnvironmentalResult](/api/oM/Analytical/LifeCycleAssessment/Results/IEnvironmentalResult)
    - BH.oM.Structure.Results.[IBarDisplacement](/api/oM/Analytical/Structure/Results/Bar Results/IBarDisplacement)
    - BH.oM.Structure.Results.[IDisplacement](/api/oM/Analytical/Structure/Results/IDisplacement)
    - BH.oM.Structure.Results.[IReaction](/api/oM/Analytical/Structure/Results/IReaction)
    - BH.oM.Structure.Results.[IMeshDisplacement](/api/oM/Analytical/Structure/Results/Mesh/IMeshDisplacement)
    - BH.oM.Structure.Results.[INodeDisplacement](/api/oM/Analytical/Structure/Results/Nodal Results/INodeDisplacement)


### Classes implementing this interface

??? bhom "The following classes are implementing this interface:"

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
    - BH.oM.LifeCycleAssessment.Results.[AbioticDepletionFossilResourcesMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/AbioticDepletionFossilResourcesMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[AbioticDepletionMineralsAndMetalsMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/AbioticDepletionMineralsAndMetalsMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[AcidificationMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/AcidificationMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeBiogenicMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/ClimateChangeBiogenicMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeFossilMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/ClimateChangeFossilMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeLandUseMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/ClimateChangeLandUseMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeTotalMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/ClimateChangeTotalMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[ClimateChangeTotalNoBiogenicMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/ClimateChangeTotalNoBiogenicMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationAquaticFreshwaterMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/EutrophicationAquaticFreshwaterMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationAquaticMarineMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/EutrophicationAquaticMarineMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationCMLMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/EutrophicationCMLMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationTerrestrialMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/EutrophicationTerrestrialMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[EutrophicationTRACIMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/EutrophicationTRACIMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[OzoneDepletionMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/OzoneDepletionMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[PhotochemicalOzoneCreationCMLMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/PhotochemicalOzoneCreationCMLMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[PhotochemicalOzoneCreationMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/PhotochemicalOzoneCreationMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[PhotochemicalOzoneCreationTRACIMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/PhotochemicalOzoneCreationTRACIMaterialResult)
    - BH.oM.LifeCycleAssessment.Results.[WaterDeprivationMaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/WaterDeprivationMaterialResult)
    - BH.oM.Structure.Results.[BarDeformation](/api/oM/Analytical/Structure/Results/Bar Results/BarDeformation)
    - BH.oM.Structure.Results.[BarDisplacement](/api/oM/Analytical/Structure/Results/Bar Results/BarDisplacement)
    - BH.oM.Structure.Results.[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)
    - BH.oM.Structure.Results.[BarModeShape](/api/oM/Analytical/Structure/Results/Bar Results/BarModeShape)
    - BH.oM.Structure.Results.[BarRequiredArea](/api/oM/Analytical/Structure/Results/Bar Results/BarRequiredArea)
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
    - BH.oM.Structure.Results.[MeshDisplacement](/api/oM/Analytical/Structure/Results/Mesh/MeshDisplacement)
    - BH.oM.Structure.Results.[MeshForce](/api/oM/Analytical/Structure/Results/Mesh/MeshForce)
    - BH.oM.Structure.Results.[MeshModeShape](/api/oM/Analytical/Structure/Results/Mesh/MeshModeShape)
    - BH.oM.Structure.Results.[MeshRequiredArea](/api/oM/Analytical/Structure/Results/Mesh/MeshRequiredArea)
    - BH.oM.Structure.Results.[MeshStress](/api/oM/Analytical/Structure/Results/Mesh/MeshStress)
    - BH.oM.Structure.Results.[MeshVonMises](/api/oM/Analytical/Structure/Results/Mesh/MeshVonMises)
    - BH.oM.Structure.Results.[NodeAcceleration](/api/oM/Analytical/Structure/Results/Nodal Results/NodeAcceleration)
    - BH.oM.Structure.Results.[NodeDisplacement](/api/oM/Analytical/Structure/Results/Nodal Results/NodeDisplacement)
    - BH.oM.Structure.Results.[NodeModalMass](/api/oM/Analytical/Structure/Results/Nodal Results/NodeModalMass)
    - BH.oM.Structure.Results.[NodeModalResults](/api/oM/Analytical/Structure/Results/Nodal Results/NodeModalResults)
    - BH.oM.Structure.Results.[NodeModeShape](/api/oM/Analytical/Structure/Results/Nodal Results/NodeModeShape)
    - BH.oM.Structure.Results.[NodeReaction](/api/oM/Analytical/Structure/Results/Nodal Results/NodeReaction)
    - BH.oM.Structure.Results.[NodeVelocity](/api/oM/Analytical/Structure/Results/Nodal Results/NodeVelocity)
    - BH.oM.Structure.Design.[DesignResult](/api/oM/Analytical/Structure/Design/DesignResult)


## Properties

### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| AllIdentifierProperties | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets the name of all properties of the result that are of identifier types. This is all properties tagged with any IdentifierAttribute. | - | Results_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a Result is null and outputs relevant error message. | - | Results_Engine |
| ObjectIdentifierProperties | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets the name of all properties of the result that are of ObjectIdentifier types. This is all properties tagged with the ObjectIdentifierAttribute. | - | Results_Engine |
| ResultPropertyKeys | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Returns the result value carrying properties available for the result type provided. Currently only supported for IResultItem and IResultCollection&lt;IResultItem&gt; type results. | - | Results_Engine |
| ResultValuePropertiesItem | [Dictionary](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.Dictionary-2?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0), [Tuple](https://learn.microsoft.com/en-us/dotnet/api/System.Tuple-2?view=netstandard-2.0)&lt;[Func](https://learn.microsoft.com/en-us/dotnet/api/System.Func-2?view=netstandard-2.0)&lt;T, [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0)&gt;, [QuantityAttribute](/api/oM/Dimensional/Quantities/Attributes/Abstract/QuantityAttribute)&gt;&gt; | Extract all potential result carrying property getters from a result class, i.e. properties of type double that is defined on the class. Properties defined on a base class are ignored.<br>Also extracts methods returning a double that has the result type as the only argument.<br>Func&lt;T,double&gt; returned together with corresponding QuantityAttribute in a Dictionary with the property or method name as the Key. | - | Results_Engine |
| ScenarioIdentifierProperties | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets the name of all properties of the result that are of Scenario types. This is all properties tagged with the ScenarioIdentifierAttribute. | - | Results_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public interface IResultItem : BH.oM.Analytical.Results.IResult,
BH.oM.Base.IObject,
System.IComparable<BH.oM.Analytical.Results.IResult>,
BH.oM.Base.IImmutable
```

Assembly: Analytical_oM.dll

The C# interface definition is available on github:

- [IResultItem.cs](https://github.com/BHoM/BHoM/blob/develop/Analytical_oM/Results\IResultItem.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Analytical_oM/Results/IResultItem.json"
}
```

The JSON Schema is available on github here:

- [IResultItem.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Analytical_oM/Results/IResultItem.json)
