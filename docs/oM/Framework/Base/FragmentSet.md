---
title: FragmentSet
---

# <small>BH.oM.Base.</small>**FragmentSet**



## Class structure

### Implemented interfaces and base types

???+ bhom "The FragmentSet is inheriting from the following base type(s) and implements the following interfaces:"

    -  [KeyedCollection](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.ObjectModel.KeyedCollection-2?view=netstandard-2.0)&lt;[Type](https://learn.microsoft.com/en-us/dotnet/api/System.Type?view=netstandard-2.0), BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)&gt;
    -  [Collection](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.ObjectModel.Collection-1?view=netstandard-2.0)&lt;BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)&gt;
    -  [IList](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.IList-1?view=netstandard-2.0)&lt;BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)&gt;
    -  [ICollection](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.ICollection-1?view=netstandard-2.0)&lt;BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)&gt;
    -  [IEnumerable](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.IEnumerable-1?view=netstandard-2.0)&lt;BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)&gt;
    -  [IEnumerable](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.IEnumerable?view=netstandard-2.0)
    -  [IList](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.IList?view=netstandard-2.0)
    -  [ICollection](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.ICollection?view=netstandard-2.0)
    -  [IReadOnlyList](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.IReadOnlyList-1?view=netstandard-2.0)&lt;BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)&gt;
    -  [IReadOnlyCollection](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.IReadOnlyCollection-1?view=netstandard-2.0)&lt;BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)&gt;
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)


## Properties

### Inherited properties
The following properties are inherited from the base class of the object

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Comparer | [IEqualityComparer](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.IEqualityComparer-1?view=netstandard-2.0)&lt;[Type](https://learn.microsoft.com/en-us/dotnet/api/System.Type?view=netstandard-2.0)&gt; | - | - |
| Item | [IFragment](/api/oM/Framework/Base/Interface/IFragment) | - | - |
| Count | [int](https://learn.microsoft.com/en-us/dotnet/api/System.Int32?view=netstandard-2.0) | - | - |
| Item | [IFragment](/api/oM/Framework/Base/Interface/IFragment) | - | - |


### Derived properties

The following properties are defined as extension methods in one of the BHoM_Engines

| Name             | Type             | Description      | Quantity         | Engine           |
|------------------|------------------|------------------|------------------|------------------|
| AbsoluteMaxEnvelope | [BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce) | - | - | Results_Engine |
| AbsoluteMaxEnvelopeByCase | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | - | - | Results_Engine |
| AbsoluteMaxEnvelopeByObject | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | - | - | Results_Engine |
| AbsoluteMaxForces | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | - | - | Results_Engine |
| AvailableCategories | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty categories from the material classifications in a collection of materials, optionally filtered by type, grade, and constituent. | - | Matter_Engine |
| AvailableCategories | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty categories from the material classifications in a collection of material properties, optionally filtered by type, grade, and constituent. | - | Matter_Engine |
| AvailableConstituents | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty constituents from the material classifications in a collection of material properties, optionally filtered by category, type, and grade. | - | Matter_Engine |
| AvailableConstituents | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty constituents from the material classifications in a collection of materials, optionally filtered by category, type, and grade. | - | Matter_Engine |
| AvailableGrades | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty grades from the material classifications in a collection of materials, optionally filtered by category, type, and constituent. | - | Matter_Engine |
| AvailableGrades | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty grades from the material classifications in a collection of material properties, optionally filtered by category, type, and constituent. | - | Matter_Engine |
| AvailableTypes | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty types from the material classifications in a collection of materials, optionally filtered by category, grade, and constituent. | - | Matter_Engine |
| AvailableTypes | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Gets all distinct non-empty types from the material classifications in a collection of material properties, optionally filtered by category, grade, and constituent. | - | Matter_Engine |
| Average | [Point](/api/oM/Dimensional/Geometry/Vector/Point) | Calculates the average (centroid) Point from a collection of Points. | - | Geometry_Engine |
| Bounds | [BoundingBox](/api/oM/Dimensional/Geometry/Misc/BoundingBox) | Queries the IElements BoundingBox. Acts on the elements geometrical definition of the IElement through the Geometry_Engine. | - | Spatial_Engine |
| Centroid | [Point](/api/oM/Dimensional/Geometry/Vector/Point) | Queries the combined centre of area enclosed by a set of ICurves with an optional set of openings.<br>To give a correct result all input curves must be planar, coplanar, closed and non-self-intersecting.<br>Opening curves should also be inside of outline curves. | - | Geometry_Engine |
| ElementCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Queries the geometrically defining curves of the IElements geometries. | - | Spatial_Engine |
| ElementVertices | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Returns the discontinuity points from the defining ICurves of the IElements. | - | Spatial_Engine |
| ExternalEdges | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElement1D](/api/oM/Dimensional/Dimensional/IElement1D)&gt; | Returns external edges from a collection of 2D elements. | - | Facade_Engine |
| FilterByClassification | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Material](/api/oM/Physical/Physical/Materials/Material)&gt; | Filters a collection of Material by classification properties. Requires the provided Materials to contain a MaterialClassification as one of its properties to be able to filter. The filtering is done by matching all non-empty provided properties, e.g. if the category and type are provided, but grade and constituent are empty, then all materials with the same category and type will be returned. | - | Matter_Engine |
| FilterUniqueRevitElements | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)&gt; | Filters the given collection of BHoM objects to return only unique Revit elements based on their UniqueId. | - | Revit_Engine |
| GetDistinctEdges | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Edge](/api/oM/Analytical/Structure/Elements/Edge)&gt; | Returns a distinct list of edges by comparing the midpoint of each edge's curve, rounded to 3 decimal places. | - | Lusas_Engine |
| GetDistinctPoints | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Returns a distinct list of points by comparing their X, Y, and Z coordinates, rounded to 3 decimal places. | - | Lusas_Engine |
| MaxBarRequiredArea | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarRequiredArea](/api/oM/Analytical/Structure/Results/Bar Results/BarRequiredArea)&gt; | Returns a list of BarRequiredArea results, one for each component, that contain the maximum value for each required area and its concurrent required areas. | - | Results_Engine |
| MaxEnvelope | [BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce) | Determines the maximum force in each component of the BarForce and returns a single BarForce object with the enveloped forces. | - | Results_Engine |
| MaxEnvelope | [BarRequiredArea](/api/oM/Analytical/Structure/Results/Bar Results/BarRequiredArea) | Determines the maximum required in each component of the BarRequiredArea and returns a single BarRequiredArea object with the enveloped required areas. | - | Results_Engine |
| MaxEnvelope | [MeshRequiredArea](/api/oM/Analytical/Structure/Results/Mesh/MeshRequiredArea) | Determines the maximum required in each component of the MeshRequiredArea and returns a single MeshRequiredArea object with the enveloped required areas. | - | Results_Engine |
| MaxEnvelopeByCase | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | Groups the BarForces by case and finds the maximum envelope returning a single enveloped BarForce for each case. The resulting BarForce will not contain concurrent forces. | - | Results_Engine |
| MaxEnvelopeByObject | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | Groups the BarForces by id and finds the maximum envelope returning a single enveloped BarForce for each id. The resulting BarForce will not contain concurrent forces. | - | Results_Engine |
| MaxForces | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | Returns a list of BarForces, one for each component, that contain the maximum value for each components and its concurrent forces. | - | Results_Engine |
| MaxMeshRequiredArea | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[MeshRequiredArea](/api/oM/Analytical/Structure/Results/Mesh/MeshRequiredArea)&gt; | Returns a list of MeshRequiredAreas results, one for each component, that contain the maximum value for each required area and its concurrent required areas. | - | Results_Engine |
| MinBarRequiredArea | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarRequiredArea](/api/oM/Analytical/Structure/Results/Bar Results/BarRequiredArea)&gt; | Returns a list of BarRequiredArea results, one for each component, that contain the minimum value for each required area and its concurrent required areas. | - | Results_Engine |
| MinEnvelope | [BarRequiredArea](/api/oM/Analytical/Structure/Results/Bar Results/BarRequiredArea) | Determines the minimum required in each component of the BarRequiredArea and returns a single BarRequiredArea object with the enveloped required areas. | - | Results_Engine |
| MinEnvelope | [MeshRequiredArea](/api/oM/Analytical/Structure/Results/Mesh/MeshRequiredArea) | Determines the minimum required in each component of the MeshRequiredArea and returns a single MeshRequiredArea object with the enveloped required areas. | - | Results_Engine |
| MinEnvelope | [BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce) | Determines the minimum force in each component of the BarForce and returns a single BarForce object with the enveloped forces. | - | Results_Engine |
| MinEnvelopeByCase | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | Groups the BarForces by case and finds the minimum envelope returning a single enveloped BarForce for each case. The resulting BarForce will not contain concurrent forces. | - | Results_Engine |
| MinEnvelopeByObject | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | Groups the BarForces by id and finds the minimum envelope returning a single enveloped BarForce for each id. The resulting BarForce will not contain concurrent forces. | - | Results_Engine |
| MinForces | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[BarForce](/api/oM/Analytical/Structure/Results/Bar Results/BarForce)&gt; | Returns a list of BarForces, one for each component, that contain the minimum value for each components and its concurrent forces. | - | Results_Engine |
| MinMeshRequiredArea | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[MeshRequiredArea](/api/oM/Analytical/Structure/Results/Mesh/MeshRequiredArea)&gt; | Returns a list of MeshRequiredAreas results, one for each component, that contain the minimum value for each required area and its concurrent required areas. | - | Results_Engine |
| MostSevereStatus | [TestStatus](/api/oM/Framework/Test/TestStatus) | Returns the most severe status from any of the provided test information. This is, if any error is existing this returns error, else if any warnings exists returns warning, else returns pass. | - | Test_Engine |
| ObjectsByType | [Dictionary](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.Dictionary-2?view=netstandard-2.0)&lt;[Type](https://learn.microsoft.com/en-us/dotnet/api/System.Type?view=netstandard-2.0), [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[object](https://learn.microsoft.com/en-us/dotnet/api/System.Object?view=netstandard-2.0)&gt;&gt; | - | - | Reflection_Engine |
| Sum | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Calculates the sum of a collection of vectors by adding all vector components together. | - | Geometry_Engine |
| SumModuleDataValues | [Dictionary](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.Dictionary-2?view=netstandard-2.0)&lt;[Module](/api/oM/Analytical/LifeCycleAssessment/Enums/Module), [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0)&gt; | Gets a list of doubles corresponding to the sum of values for each property of the provided ILifeCycleAssessmentPhaseData, i.e. the first value will be the sum of A1 for all the provided ILifeCycleAssessmentPhaseDatas. | - | LifeCycleAssessment_Engine |
| TotalMaterialBreakdown | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt; | Gets total MaterialResults for all provided element results grouped by MaterialName, EPDName and Metric, and returns a single MaterialResult for each group containing the total evaluated. | - | LifeCycleAssessment_Engine |
| TotalMaterialBreakdown | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt; | Gets total MaterialResults from list of individual material results grouped by MaterialName, EPDName and Type, and returns a single MaterialResult for each group containing the total evaluated. | - | LifeCycleAssessment_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class FragmentSet : System.Collections.ObjectModel.KeyedCollection<System.Type, BH.oM.Base.IFragment>,
System.Collections.ObjectModel.Collection<BH.oM.Base.IFragment>,
System.Collections.Generic.IList<BH.oM.Base.IFragment>,
System.Collections.Generic.ICollection<BH.oM.Base.IFragment>,
System.Collections.Generic.IEnumerable<BH.oM.Base.IFragment>,
System.Collections.IEnumerable,
System.Collections.IList,
System.Collections.ICollection,
System.Collections.Generic.IReadOnlyList<BH.oM.Base.IFragment>,
System.Collections.Generic.IReadOnlyCollection<BH.oM.Base.IFragment>,
BH.oM.Base.IObject
```

Assembly: BHoM.dll

The C# class definition is available on github:

- [FragmentSet.cs](https://github.com/BHoM/BHoM/blob/develop/BHoM/FragmentSet.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/BHoM/FragmentSet.json"
}
```

The JSON Schema is available on github here:

- [FragmentSet.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/BHoM/FragmentSet.json)
