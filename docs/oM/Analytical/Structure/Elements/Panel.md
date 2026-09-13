---
title: Panel
---

# <small>BH.oM.Structure.Elements.</small>**Panel**

2D element for structural analysis. 
The Panel is a planar surface object defined by a list of planar 'Edges' (curves with properties) for both external and internal edges (openings).

## Class structure

### Implemented interfaces and base types

???+ bhom "The Panel is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Structure.Elements.[IAreaElement](/api/oM/Analytical/Structure/Elements/IAreaElement)
    -  BH.oM.Dimensional.[IElementM](/api/oM/Dimensional/Dimensional/IElementM)
    -  BH.oM.Dimensional.[IElement2D](/api/oM/Dimensional/Dimensional/IElement2D)
    -  BH.oM.Dimensional.[IElement](/api/oM/Dimensional/Dimensional/IElement)
    -  BH.oM.Analytical.Elements.[IPanel](/api/oM/Analytical/Analytical/Elements/IPanel)&lt;BH.oM.Structure.Elements.[Edge](/api/oM/Analytical/Structure/Elements/Edge), BH.oM.Structure.Elements.[Opening](/api/oM/Analytical/Structure/Elements/Opening)&gt;
    -  BH.oM.Analytical.[IAnalytical](/api/oM/Analytical/Analytical/IAnalytical)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| ExternalEdges | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Edge](/api/oM/Analytical/Structure/Elements/Edge)&gt; | A list of coplanar Edges defining the external contour and potential constraints of the Panel. | - |
| Openings | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Opening](/api/oM/Analytical/Structure/Elements/Opening)&gt; | A list of Openings of the panel. The edges that make up the openings must be coplanar with the external edges. | - |
| Property | [ISurfaceProperty](/api/oM/Analytical/Structure/SurfaceProperties/ISurfaceProperty) | Defines the thickness property and material of the Panel. Orientation of non-isotropic properties are controlled by the OrientationAngle. | - |
| OrientationAngle | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Defines the angle that the local x and y axes are rotated around the normal (i.e. local z) of the Panel.<br>The normal of the Panel is determined by the right hand curl rule dictated by the order of the edge list.<br>Local x is found by projecting the global X to the plane of the Panel and is then rotated with the OrientationAngle, except for the case when the Normal is parallel with the global X. For this case the local y is instead found by projecting global Y to the plane of the Panel and is then rotated with the OrientationAngle.<br>The remaining local axis is determined by the right hand rule. | [Angle](/api/oM/Dimensional/Quantities/Attributes/Angle) [rad] |


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
| Area | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Queries the IElement2Ds area defined as the area confined by the outline curves subtracting the area of the internal elements. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Spatial_Engine |
| Bounds | [BoundingBox](/api/oM/Dimensional/Geometry/Misc/BoundingBox) | Queries the IElement2Ds BoundingBox. Acts on the element curve definition of the IElement2D through the Geometry_Engine. | - | Spatial_Engine |
| Centroid | [Point](/api/oM/Dimensional/Geometry/Vector/Point) | Queries the centre of area for a IElement2Ds surface representation. For an IElement2D with homogeneous material and thickness this will also be the centre of weight. | - | Spatial_Engine |
| ControlPoints | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Queries the control points of the element curve representation of the IElement2D. | - | Spatial_Engine |
| CoordinateSystem | [Cartesian](/api/oM/Dimensional/Geometry/CoordinateSystem/Cartesian) | Get the Cartesian coordinate system describing the position and local orientation of the Panel in the global coordinate system where the z-axis is the normal of the Panel and the x and y axes are the directions of the local in-plane axes. | - | Structure_Engine |
| Diaphragm | [Diaphragm](/api/oM/Adapter/Adapters/ETABS/Elements/Diaphragm) | Gets the ETABS Diaphragm fragment from a Panel, if one has been assigned. | - | ETABS_Engine |
| DominantVector | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Gets the dominant vector (orientation) of an Element2D based on its line lengths. | - | Spatial_Engine |
| ElementCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Queries the geometrically defining curves of the IElement2Ds surface. | - | Spatial_Engine |
| ElementEmbodiedCarbon | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt;&gt; | Evaluates the embodied carbon on the provided element based on IStructE methodology of evaluation.<br>If you would like to evaluate other EPD metrics, please use one of the Query.EnvironmentalResults methods. <br>TemplateMaterials can be provided helping with picking the correct EPD corresponding to each material on the element. Please note that this evaluation method only support mass-based EPDs. | - | LifeCycleAssessment_Engine |
| ElementMaterialNames | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Query the element's MaterialComposition to form a Material Hint to aid in EPD-Material Mapping. | - | LifeCycleAssessment_Engine |
| ElementScope | [ScopeType](/api/oM/Analytical/LifeCycleAssessment/Enums/ScopeType) | Returns the enumerable type of the scope found on an element. | - | LifeCycleAssessment_Engine |
| ElementVertices | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Returns the discontinuity points from the defining ICurves of the IElement2D. | - | Spatial_Engine |
| EnvironmentalResults | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt;&gt; | Evaluates the EnvironmentalMetrics for the provided element and returns an ElementResult for each evaluated metric type.<br>Evaluation is done by extracting the material takeoff for the provided element, giving quantities and Materiality.<br>Each Material in the takeoff is then evaluated by finding the EnvironmentalProductDeclaration (EPD), either stored on the material or from the list of template materials.<br>Each metric, or filtered chosen metrics, on the EPD is then evaluated.<br>Finally, an element result is returned per metric type. Each element result being the sum result of all metrics of the same type. | - | LifeCycleAssessment_Engine |
| ExternalElementCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Queries the geometrically defining external curves of the IElement2Ds surface. | - | Spatial_Engine |
| ExternalPolyCurve | [PolyCurve](/api/oM/Dimensional/Geometry/Curve/PolyCurve) | Gets the polycurve that defines the outline of the panel and checks for a single continuous linear curve | - | Analytical_Engine |
| GeneralMaterialTakeoff | [GeneralMaterialTakeoff](/api/oM/Physical/Physical/Materials/GeneralMaterialTakeoff) | Returns an Area Element's (Panel, FEMesh, Surface etc.) GeneralMaterialTakeoff which contains information about the element's materiality and corresponding quantities. | - | Structure_Engine |
| Geometry | [PlanarSurface](/api/oM/Dimensional/Geometry/Surface/PlanarSurface) | Gets the geometry of a analytical IPanel at its centre. Method required for automatic display in UI packages. | - | Analytical_Engine |
| Geometry3D | [IGeometry](/api/oM/Dimensional/Geometry/Interface/IGeometry) | Gets a CompositeGeometry made of the boundary surfaces of the Panel envelope, or only its central Surface. | - | Structure_Engine |
| IArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Queries the area of the geometrical representation of an IElement. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Spatial_Engine |
| IArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the area of an IAreaElement. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Structure_Engine |
| IBounds | [BoundingBox](/api/oM/Dimensional/Geometry/Misc/BoundingBox) | Queries the IElements BoundingBox. Acts on the elements geometrical definition of the IElement through the Geometry_Engine. | - | Spatial_Engine |
| ICentroid | [Point](/api/oM/Dimensional/Geometry/Vector/Point) | Queries the centre of weight for the homogeneous geometrical representation of an IElement. | - | Spatial_Engine |
| IControlPoints | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Queries the control points of the geometrical representation of an IElement. | - | Spatial_Engine |
| IEdges | [IEnumerable](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.IEnumerable-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Extracts all the edge curves from an AreaElement. | - | Structure_Engine |
| IElementCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Queries the geometrically defining curves of the IElements geometry. | - | Spatial_Engine |
| IElementVertices | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Returns the discontinuity points from the defining ICurves of the IElement. | - | Spatial_Engine |
| IGeneralMaterialTakeoff | [GeneralMaterialTakeoff](/api/oM/Physical/Physical/Materials/GeneralMaterialTakeoff) | Gets the unique Materials along with their volumes defining an object's make-up. | - | Matter_Engine |
| IInternalElements2D | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElement2D](/api/oM/Dimensional/Dimensional/IElement2D)&gt; | Queries the IElement2Ds internal IElement2Ds. Returns an empty list for objects without defined internal elements. | - | Spatial_Engine |
| IIsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if an AreaElement is null and outputs relevant error message. | - | Structure_Engine |
| IIsPlanar | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks whether all control points of an element lie in a single plane. | - | Spatial_Engine |
| IIsSelfIntersecting | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if any of the curves defining an IElement is closer to itself than the tolerance at any two points (is self intersecting). In case of IElement2D, does not check for intersections between external and internal curves, or between different internal curves. | - | Spatial_Engine |
| IMaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Gets the unique Materials along with their relative proportions defining an object's make-up. | - | Matter_Engine |
| INewInternalElement2D | [IElement2D](/api/oM/Dimensional/Dimensional/IElement2D) | Creates a IElement2D of a type which can be assigned to the IElement2D. | - | Spatial_Engine |
| INormal | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Returns the local z-axis of the IAreaElement. | - | Structure_Engine |
| InternalElementCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Queries the geometrically defining internal curves, such as Openings, of the IElement2Ds surface. | - | Spatial_Engine |
| InternalElements2D | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElement2D](/api/oM/Dimensional/Dimensional/IElement2D)&gt; | Gets inner IElement2Ds from a IPanel. Method required for all IElement2Ds. <br>For a IPanel this method will return a list of all of its openings. | - | Analytical_Engine |
| InternalOutlineCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[PolyCurve](/api/oM/Dimensional/Geometry/Curve/PolyCurve)&gt; | Queries the IElement2Ds internal IElement2Ds outline curves. | - | Spatial_Engine |
| IOutlineElements1D | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElement1D](/api/oM/Dimensional/Dimensional/IElement1D)&gt; | Returns every IElement1D which makes up the exterior perimeter of the IElement2D. | - | Spatial_Engine |
| IPointGrid | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Generates a rectangular grid of points on an IAreaElement. Used for load visualisation. | - | Structure_Engine |
| IPrimaryPropertyName | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Returns the name of an elements primary defining construction property | - | Facade_Engine |
| IsHorizontal | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if the IPanel is aligned with the horizontal plane (global XY). | - | Analytical_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a Panel or its defining properties are null and outputs relevant error message. | - | Structure_Engine |
| ISolidVolume | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Returns an element's solid volume, i.e. the the volume of the element that had any materiality, excluding cavities, openings and voids. | [Volume](/api/oM/Dimensional/Quantities/Attributes/Volume) [m³] | Matter_Engine |
| IsOutlineQuad | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Determines whether a Panel's outline is a quadilateral. | - | Analytical_Engine |
| IsOutlineRectangular | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Determines whether a Panel's outline is a rectangular. | - | Analytical_Engine |
| IsOutlineSquare | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Determines whether a Panel's outline is a square. | - | Analytical_Engine |
| IsOutlineTriangular | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Determines whether a Panel's outline is triangular. | - | Analytical_Engine |
| IsPlanar | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks whether all control points of an element lie in a single plane. | - | Spatial_Engine |
| IsSelfIntersecting | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if any of the element curves of the IElement2D is closer to itself than the tolerance at any two points. Does not check for intersections between external and internal curves, or between different internal curves. | - | Spatial_Engine |
| IsVertical | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if the IPanel is aligned with any vertical plane. | - | Analytical_Engine |
| IVolumetricMaterialTakeoff | [VolumetricMaterialTakeoff](/api/oM/Physical/Physical/Materials/VolumetricMaterialTakeoff) | Gets the unique Materials along with their volumes defining an object's make-up. | - | Matter_Engine |
| LocalOrientation | [Basis](/api/oM/Dimensional/Geometry/Vector/Basis) | Get the Vector basis system descibring the local axis orientation of the Panel in the global coordinate system where the z-axis is the normal of the panel and the x and y axes are the directions of the local in-plane axes. | - | Structure_Engine |
| Mass | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Evaluates the mass of an object based its VolumetricMaterialTakeoff and Density. | [Mass](/api/oM/Dimensional/Quantities/Attributes/Mass) [kg] | Matter_Engine |
| Mass | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the mass of a Panel as its area times mass per area. The mass per area is for a constant thickness calculated as thickness multiplied by the density. | [Mass](/api/oM/Dimensional/Quantities/Attributes/Mass) [kg] | Structure_Engine |
| MaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Returns an AreaElement's homogeneous MaterialComposition. | - | Structure_Engine |
| NewInternalElement2D | [IElement2D](/api/oM/Dimensional/Dimensional/IElement2D) | Creates a new Element2D, appropriate to the input type. For this case the appropriate type for the Panel will be a new Opening, in the position provided. <br>Method required for any IElement2D that contians internal IElement2Ds. | - | Analytical_Engine |
| Normal | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Returns the normal to the IElement2D which is perpendicular to its plane and oriented according to the right hand rule in relation to the outline curve. | - | Spatial_Engine |
| OutlineCurve | [PolyCurve](/api/oM/Dimensional/Geometry/Curve/PolyCurve) | Returns a single polycurve outline created from the external elements. | - | Spatial_Engine |
| OutlineElements1D | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElement1D](/api/oM/Dimensional/Dimensional/IElement1D)&gt; | Gets the edge elements from an IPanel defining the boundary of the element. Method required for all IElement2Ds. <br>For an IPanel this will return a list of its ExternalEdges. | - | Analytical_Engine |
| PanelAutoMesh | [IPanelAutoMesh](/api/oM/Adapter/Adapters/SAP2000/Fragments/IPanelAutoMesh) | Returns the SAP2000 PanelAutoMesh settings for a panel. You can also use the method FindFragment() with the type IPanelAutoMesh as an argument. | - | SAP2000_Engine |
| PanelEdgeConstraint | [PanelEdgeConstraint](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelEdgeConstraint) | Returns the SAP2000 PanelEdgeConstraint settings for a panel. You can also use the method FindFragment() with the type PanelEdgeConstraint as an argument. | - | SAP2000_Engine |
| PanelOffset | [IPanelOffset](/api/oM/Adapter/Adapters/SAP2000/Fragments/IPanelOffset) | Returns the SAP2000 PanelOffset settings for a panel. You can also use the method FindFragment() with the type IPanelOffset as an argument. | - | SAP2000_Engine |
| Pier | [Pier](/api/oM/Adapter/Adapters/ETABS/Elements/Pier) | Gets the ETABS Pier fragment from a Panel, if one has been assigned. | - | ETABS_Engine |
| PointGrid | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Generates a rectangular grid of points on the Panel, scaled depending on Panel size. Used for load visualisation. | - | Structure_Engine |
| SolidVolume | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Returns a IAreaElement's solid volume as the area of the element times the average thickness of its SurfaceProperty. The average thickness is evaluated as if it was applied to an infinite plane. | [Volume](/api/oM/Dimensional/Quantities/Attributes/Volume) [m³] | Structure_Engine |
| Spandrel | [Spandrel](/api/oM/Adapter/Adapters/ETABS/Elements/Spandrel) | Gets the ETABS Spandrel fragment from a Panel, if one has been assigned. | - | ETABS_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class Panel : BH.oM.Base.BHoMObject,
BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Structure.Elements.IAreaElement,
BH.oM.Dimensional.IElementM,
BH.oM.Dimensional.IElement2D,
BH.oM.Dimensional.IElement,
BH.oM.Analytical.Elements.IPanel<BH.oM.Structure.Elements.Edge, BH.oM.Structure.Elements.Opening>,
BH.oM.Analytical.IAnalytical
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [Panel.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/Elements\Panel.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/Elements/Panel.json"
}
```

The JSON Schema is available on github here:

- [Panel.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/Elements/Panel.json)
### Example JSON instance

Example JSON instance of type Panel.

``` json title="Example JSON"
{
  "_t": "BH.oM.Structure.Elements.Panel",
  "ExternalEdges": [
    {
      "_t": "BH.oM.Structure.Elements.Edge",
      "Curve": {
        "_t": "BH.oM.Geometry.Line",
        "Start": {
          "_t": "BH.oM.Geometry.Point",
          "X": -5.0,
          "Y": 0.0,
          "Z": 0.0
        },
        "End": {
          "_t": "BH.oM.Geometry.Point",
          "X": 0.0,
          "Y": 0.0,
          "Z": 0.0
        },
        "Infinite": false
      },
      "Release": null,
      "Support": null,
      "BHoM_Guid": "320d4d53-e4f4-4eec-8798-96830ef13cd4",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Edge",
      "Curve": {
        "_t": "BH.oM.Geometry.Line",
        "Start": {
          "_t": "BH.oM.Geometry.Point",
          "X": 0.0,
          "Y": 0.0,
          "Z": 0.0
        },
        "End": {
          "_t": "BH.oM.Geometry.Point",
          "X": 0.0,
          "Y": 5.0,
          "Z": 0.0
        },
        "Infinite": false
      },
      "Release": null,
      "Support": null,
      "BHoM_Guid": "f660ee89-9ac6-40f4-9e1c-c5736f5bdf52",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Edge",
      "Curve": {
        "_t": "BH.oM.Geometry.Line",
        "Start": {
          "_t": "BH.oM.Geometry.Point",
          "X": 0.0,
          "Y": 5.0,
          "Z": 0.0
        },
        "End": {
          "_t": "BH.oM.Geometry.Point",
          "X": -5.0,
          "Y": 5.0,
          "Z": 0.0
        },
        "Infinite": false
      },
      "Release": null,
      "Support": null,
      "BHoM_Guid": "4da9c4b1-2802-4542-bd22-bce2ae9ce988",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Edge",
      "Curve": {
        "_t": "BH.oM.Geometry.Line",
        "Start": {
          "_t": "BH.oM.Geometry.Point",
          "X": -5.0,
          "Y": 5.0,
          "Z": 0.0
        },
        "End": {
          "_t": "BH.oM.Geometry.Point",
          "X": -5.0,
          "Y": 0.0,
          "Z": 0.0
        },
        "Infinite": false
      },
      "Release": null,
      "Support": null,
      "BHoM_Guid": "4939e8d6-696f-4450-a0cf-e95997449327",
      "Name": ""
    }
  ],
  "Openings": [
    {
      "_t": "BH.oM.Structure.Elements.Opening",
      "Edges": [
        {
          "_t": "BH.oM.Structure.Elements.Edge",
          "Curve": {
            "_t": "BH.oM.Geometry.Line",
            "Start": {
              "_t": "BH.oM.Geometry.Point",
              "X": -4.0,
              "Y": 3.0,
              "Z": 0.0
            },
            "End": {
              "_t": "BH.oM.Geometry.Point",
              "X": -1.0,
              "Y": 3.0,
              "Z": 0.0
            },
            "Infinite": false
          },
          "Release": null,
          "Support": null,
          "BHoM_Guid": "a8fefee3-8ae8-40e6-af4c-46fbaf4756ba",
          "Name": ""
        },
        {
          "_t": "BH.oM.Structure.Elements.Edge",
          "Curve": {
            "_t": "BH.oM.Geometry.Line",
            "Start": {
              "_t": "BH.oM.Geometry.Point",
              "X": -1.0,
              "Y": 3.0,
              "Z": 0.0
            },
            "End": {
              "_t": "BH.oM.Geometry.Point",
              "X": -1.0,
              "Y": 4.0,
              "Z": 0.0
            },
            "Infinite": false
          },
          "Release": null,
          "Support": null,
          "BHoM_Guid": "67766e83-f953-439e-b8e2-67666c3dce58",
          "Name": ""
        },
        {
          "_t": "BH.oM.Structure.Elements.Edge",
          "Curve": {
            "_t": "BH.oM.Geometry.Line",
            "Start": {
              "_t": "BH.oM.Geometry.Point",
              "X": -1.0,
              "Y": 4.0,
              "Z": 0.0
            },
            "End": {
              "_t": "BH.oM.Geometry.Point",
              "X": -4.0,
              "Y": 4.0,
              "Z": 0.0
            },
            "Infinite": false
          },
          "Release": null,
          "Support": null,
          "BHoM_Guid": "f40b6303-7616-4080-beb1-f430212cbac1",
          "Name": ""
        },
        {
          "_t": "BH.oM.Structure.Elements.Edge",
          "Curve": {
            "_t": "BH.oM.Geometry.Line",
            "Start": {
              "_t": "BH.oM.Geometry.Point",
              "X": -4.0,
              "Y": 4.0,
              "Z": 0.0
            },
            "End": {
              "_t": "BH.oM.Geometry.Point",
              "X": -4.0,
              "Y": 3.0,
              "Z": 0.0
            },
            "Infinite": false
          },
          "Release": null,
          "Support": null,
          "BHoM_Guid": "6e61c5a0-5a23-46b2-ae91-123208d4710d",
          "Name": ""
        }
      ],
      "BHoM_Guid": "5b1ebb72-d613-493c-834e-85148134feeb",
      "Name": ""
    }
  ],
  "Property": {
    "_t": "BH.oM.Structure.SurfaceProperties.ConstantThickness",
    "Name": null,
    "Thickness": 0.10000000000000001,
    "Material": {
      "_t": "BH.oM.Structure.MaterialFragments.Concrete",
      "Name": "C30/37",
      "Density": 2548.5376999999999,
      "DampingRatio": 0.0,
      "PoissonsRatio": 0.20000000000000001,
      "ThermalExpansionCoeff": 1.0000000000000001E-05,
      "YoungsModulus": 33000000000.0,
      "CylinderStrength": 30000000.0,
      "CubeStrength": 37000000.0,
      "BHoM_Guid": "647d6ed4-4a60-4f7d-b7a1-4d13fa15b04a"
    },
    "PanelType": "Slab",
    "BHoM_Guid": "7e4c2d08-0b70-4fe5-800b-492056b08694"
  },
  "OrientationAngle": 0.0,
  "BHoM_Guid": "ced97e6f-254e-498d-962b-4de99d349340",
  "Name": "Panel Name",
  "_bhomVersion": "8.2"
}
```

