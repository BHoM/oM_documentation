---
title: Bar
---

# <small>BH.oM.Structure.Elements.</small>**Bar**

1D finite element for structural analysis. Linear 2-noded element defined by a start and end node.For structural conventions and orientation of the bar please see the [documentation](https://bhom.xyz/documentation/BHoM_oM/Structure_oM/BHoM-Structural-Conventions/).

## Class structure

### Implemented interfaces and base types

???+ bhom "The Bar is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Dimensional.[IElement1D](/api/oM/Dimensional/Dimensional/IElement1D)
    -  BH.oM.Dimensional.[IElement](/api/oM/Dimensional/Dimensional/IElement)
    -  BH.oM.Dimensional.[IElementM](/api/oM/Dimensional/Dimensional/IElementM)
    -  BH.oM.Analytical.Elements.[ILink](/api/oM/Analytical/Analytical/Elements/ILink)&lt;BH.oM.Structure.Elements.[Node](/api/oM/Analytical/Structure/Elements/Node)&gt;
    -  BH.oM.Analytical.[IAnalytical](/api/oM/Analytical/Analytical/IAnalytical)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Start | [Node](/api/oM/Analytical/Structure/Elements/Node) | Defines the start position of the element. Note that Nodes can contain Supports which should not be confused with Releases. | - |
| End | [Node](/api/oM/Analytical/Structure/Elements/Node) | Defines the end position of the element. Note that Nodes can contain Supports which should not be confused with Releases. | - |
| SectionProperty | [ISectionProperty](/api/oM/Analytical/Structure/SectionProperties/ISectionProperty) | Section property of the bar, containing all sectional constants and material as well as profile geometry and dimensions, where applicable. | - |
| OrientationAngle | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Controls the local axis orientation of the bar <br>For non-vertical members the local z is aligned with the global Z and rotated with the orientation angle about the local x. <br>For vertical members the local y is aligned with the global Y and rotated with the orientation angle about the local x. <br>A bar is vertical if its projected length to the horizontal plane is less than 0.0001, i.e. a tolerance of 0.1mm on verticality. <br>For general structural conventions please see the [documentation](https://bhom.xyz/documentation/BHoM_oM/Structure_oM/BHoM-Structural-Conventions/). | [Angle](/api/oM/Dimensional/Quantities/Attributes/Angle) [rad] |
| Release | [BarRelease](/api/oM/Analytical/Structure/Constraints/BarRelease) | Defines the start and end release of the Bar. The releases defines how the bar is attached to its end nodes. If not set, full fixity will be assumed. | - |
| FEAType | [BarFEAType](/api/oM/Analytical/Structure/Elements/Enums/BarFEAType) | - | - |
| Support | [Constraint4DOF](/api/oM/Analytical/Structure/Constraints/Constraint4DOF) | Linear support for the bar. Three translational degrees of freedom and one rotational. The rotational DOF defines constraint about the axis of the bar. | - |
| Offset | [Offset](/api/oM/Analytical/Structure/Offsets/Offset) | Offset of the bar as two vectors, one per end node, in bar local coordinates. Defines offsets from centreline to be applied in analysis packages. | - |


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
| AutoLengthOffset | [AutoLengthOffset](/api/oM/Adapter/Adapters/ETABS/Fragments/AutoLengthOffset) | Gets the ETABS AutoLengthOffset fragment from a Bar, if one has been assigned. | - | ETABS_Engine |
| BarAutoMesh | [BarAutoMesh](/api/oM/Adapter/Adapters/SAP2000/Fragments/BarAutoMesh) | Returns the SAP2000 BarAutoMesh settings for a bar. You can also use the method FindFragment() with the type BarAutoMesh as an argument. | - | SAP2000_Engine |
| BarDesignProcedure | [BarDesignProcedure](/api/oM/Adapter/Adapters/SAP2000/Fragments/BarDesignProcedure) | Returns the SAP2000 BarDesignProcedure settings for a bar. You can also use the method FindFragment() with the type BarDesignProcedure as an argument. | - | SAP2000_Engine |
| BarInsertionPoint | [BarInsertionPointLocation](/api/oM/Adapter/Adapters/SAP2000/Enums/BarInsertionPointLocation) | Returns the SAP2000 BarInsertionPointLocation settings for a bar. You can also use the method FindFragment() with the type BarInsertionPoint as an argument. | - | SAP2000_Engine |
| BarModifyStiffnessInsertionPoint | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if SAP2000 is set to modify the stiffness of a bar based on its insertion point. You can also use the method FindFragment() with the type BarInsertionPoint as an argument, and check the ModifyStiffness property of that fragment. | - | SAP2000_Engine |
| BarSectionTranformation | [TransformMatrix](/api/oM/Dimensional/Geometry/Misc/TransformMatrix) | Constructs the transformation matrix needed to move the section curves of the Bar from the default drawing position around the global origin to the start of the Bar and aligned with its tangent. | - | Structure_Engine |
| Bounds | [BoundingBox](/api/oM/Dimensional/Geometry/Misc/BoundingBox) | Queries the IElement1Ds BoundingBox. Acts on the ICurve definition of the IElement1D through the Geometry_Engine. | - | Spatial_Engine |
| CellularOpeningCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Distributes a series of cellular openings along the centreline of the bar centreline. Method will fit in as many openings along the curve as it can, starting from the start of the curve.<br>An empty list is returned if the bar does not contain a cellular section. | - | Structure_Engine |
| Centreline | [Line](/api/oM/Dimensional/Geometry/Curve/Line) | Returns the centreline of the Bar as the line between the StratNode and EndNode. No offsets or similar is accounted for. | - | Structure_Engine |
| Centroid | [Point](/api/oM/Dimensional/Geometry/Vector/Point) | Queries the centre of weight for a IElement1Ds ICurve representation. | - | Spatial_Engine |
| CheckFlipBar | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Evaluates if the Bar would have its endpoints flipped on Push to ETABS in ETABS16. | - | ETABS_Engine |
| ControlPoints | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Queries the control points of the one dimensional representation of the IElement1D. | - | Spatial_Engine |
| CoordinateSystem | [Cartesian](/api/oM/Dimensional/Geometry/CoordinateSystem/Cartesian) | Get the carteseian coordinate system descibring the position and local orientation of the Bar in the global coordinate system where the Bar tangent is the local x-axis and the normal is the local z-axis. | - | Structure_Engine |
| DominantVector | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Gets the dominant vector (orientation) of an Element1D based on its line lengths. | - | Spatial_Engine |
| ElementCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Queries the defining curves of an IElement1D. | - | Spatial_Engine |
| ElementEmbodiedCarbon | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt;&gt; | Evaluates the embodied carbon on the provided element based on IStructE methodology of evaluation.<br>If you would like to evaluate other EPD metrics, please use one of the Query.EnvironmentalResults methods. <br>TemplateMaterials can be provided helping with picking the correct EPD corresponding to each material on the element. Please note that this evaluation method only support mass-based EPDs. | - | LifeCycleAssessment_Engine |
| ElementMaterialNames | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Query the element's MaterialComposition to form a Material Hint to aid in EPD-Material Mapping. | - | LifeCycleAssessment_Engine |
| Elements0D | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElement0D](/api/oM/Dimensional/Dimensional/IElement0D)&gt; | Gets the Element0Ds of an ILink, which for the case of a ILink means getting the StartNode and EndNode. Method necessary for IElement pattern. | - | Analytical_Engine |
| ElementScope | [ScopeType](/api/oM/Analytical/LifeCycleAssessment/Enums/ScopeType) | Returns the enumerable type of the scope found on an element. | - | LifeCycleAssessment_Engine |
| ElementVertices | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Returns the discontinuity points from the defining ICurve of the IElement1D. | - | Spatial_Engine |
| EnvironmentalResults | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt;&gt; | Evaluates the EnvironmentalMetrics for the provided element and returns an ElementResult for each evaluated metric type.<br>Evaluation is done by extracting the material takeoff for the provided element, giving quantities and Materiality.<br>Each Material in the takeoff is then evaluated by finding the EnvironmentalProductDeclaration (EPD), either stored on the material or from the list of template materials.<br>Each metric, or filtered chosen metrics, on the EPD is then evaluated.<br>Finally, an element result is returned per metric type. Each element result being the sum result of all metrics of the same type. | - | LifeCycleAssessment_Engine |
| Extrude | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IGeometry](/api/oM/Dimensional/Geometry/Interface/IGeometry)&gt; | Computes an extrusion of the section along the Bar centreline. | - | Structure_Engine |
| GeneralMaterialTakeoff | [GeneralMaterialTakeoff](/api/oM/Physical/Physical/Materials/GeneralMaterialTakeoff) | Returns a Bar's GeneralMaterialTakeoff which contains information about the Bar's materiality and corresponding quantities. | - | Structure_Engine |
| Geometry | [Line](/api/oM/Dimensional/Geometry/Curve/Line) | Gets the geometry of a ILink as its centreline. Method required for automatic display in UI packages. | - | Analytical_Engine |
| Geometry3D | [IGeometry](/api/oM/Dimensional/Geometry/Interface/IGeometry) | Gets the BH.oM.Geometry.Extrusion out of the Bar as its Geometry3D. | - | Structure_Engine |
| HasReinforcement | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Returns true if the Bar has a ConcreteSection with BarRebarIntent defined with at least one IBarReinforcement in it. False if the Bar, ConcreteSection or BarRebarIntent is null or the IBarReinforcement count is zero. | - | Structure_Engine |
| IArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Queries the area of the geometrical representation of an IElement. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Spatial_Engine |
| IBounds | [BoundingBox](/api/oM/Dimensional/Geometry/Misc/BoundingBox) | Queries the IElements BoundingBox. Acts on the elements geometrical definition of the IElement through the Geometry_Engine. | - | Spatial_Engine |
| ICentroid | [Point](/api/oM/Dimensional/Geometry/Vector/Point) | Queries the centre of weight for the homogeneous geometrical representation of an IElement. | - | Spatial_Engine |
| IControlPoints | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Queries the control points of the geometrical representation of an IElement. | - | Spatial_Engine |
| IElementCurves | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Queries the geometrically defining curves of the IElements geometry. | - | Spatial_Engine |
| IElements0D | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElement0D](/api/oM/Dimensional/Dimensional/IElement0D)&gt; | Queries the IElement0Ds from a IElement1D. Returns null if no IElement0Ds are defined for the type of IElement1D. | - | Spatial_Engine |
| IElementVertices | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Returns the discontinuity points from the defining ICurves of the IElement. | - | Spatial_Engine |
| IGeneralMaterialTakeoff | [GeneralMaterialTakeoff](/api/oM/Physical/Physical/Materials/GeneralMaterialTakeoff) | Gets the unique Materials along with their volumes defining an object's make-up. | - | Matter_Engine |
| IGeometry | [ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve) | Queries the defining geometrical object which all spatial operations will act on. | - | Spatial_Engine |
| IIsPlanar | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks whether all control points of an element lie in a single plane. | - | Spatial_Engine |
| IIsSelfIntersecting | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if any of the curves defining an IElement is closer to itself than the tolerance at any two points (is self intersecting). In case of IElement2D, does not check for intersections between external and internal curves, or between different internal curves. | - | Spatial_Engine |
| IMaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Gets the unique Materials along with their relative proportions defining an object's make-up. | - | Matter_Engine |
| InsertionPoint | [BarInsertionPoint](/api/oM/Adapter/Adapters/ETABS/Enums/BarInsertionPoint) | Gets the ETABS insertion point of a Bar. Returns Centroid if no insertion point fragment is assigned. | - | ETABS_Engine |
| IPrimaryPropertyName | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Returns the name of an elements primary defining property | - | Facade_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a Bar or its defining properties are null and outputs relevant error message. | - | Structure_Engine |
| ISolidVolume | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Returns an element's solid volume, i.e. the the volume of the element that had any materiality, excluding cavities, openings and voids. | [Volume](/api/oM/Dimensional/Quantities/Attributes/Volume) [m³] | Matter_Engine |
| IsPlanar | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks whether all control points of an element lie in a single plane. | - | Spatial_Engine |
| IsSelfIntersecting | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if the one dimensional representation of the IElement1D is closer to itself than the tolerance at any two points. | - | Spatial_Engine |
| IsVertical | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if a Bar is vertical. A Bar is vertical if its projected length to the horizontal plane is less than 0.0001, i.e. a tolerance of 0.1mm on verticality. <br>For general structural conventions please see the [documentation](https://bhom.xyz/documentation/BHoM_oM/Structure_oM/BHoM-Structural-Conventions/). | - | Structure_Engine |
| IVolumetricMaterialTakeoff | [VolumetricMaterialTakeoff](/api/oM/Physical/Physical/Materials/VolumetricMaterialTakeoff) | Gets the unique Materials along with their volumes defining an object's make-up. | - | Matter_Engine |
| Length | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Returns the length of the IElement1Ds curve. | [Length](/api/oM/Dimensional/Quantities/Attributes/Length) [m] | Spatial_Engine |
| Mass | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the mass of a Bar as its solid volume (generally taken as length times section area) times density(ies) of its material. No offsets or similar are taken into account. | [Mass](/api/oM/Dimensional/Quantities/Attributes/Mass) [kg] | Structure_Engine |
| Mass | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Evaluates the mass of an object based its VolumetricMaterialTakeoff and Density. | [Mass](/api/oM/Dimensional/Quantities/Attributes/Mass) [kg] | Matter_Engine |
| MaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Returns a Bar's homogeneous MaterialComposition. | - | Structure_Engine |
| ModifyStiffnessInsertionPoint | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Gets whether stiffness modification is enabled for the insertion point of a Bar. Returns true if no insertion point fragment is assigned. | - | ETABS_Engine |
| Normal | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Returns the bars local z-axis, generally the major axis direction of the section of the Bar. <br>For non - vertical members the local z-axis is aligned with the global Z-axis and rotated with the orientation angle around the local x-axis. <br>For vertical members the local y-axis is aligned with the global Y-axis and rotated with the orientation angle around the local x-axis. For this case the normal will be the vector orthogonal to the local x-axis and local y-axis. | - | Structure_Engine |
| ReinforcementLayout | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Gets all the reinforcement centrelines in the Bar as a list of Curves. | - | Structure_Engine |
| ReinforcingBars | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IReinforcingBar](/api/oM/Physical/Physical/Reinforcement/IReinforcingBar)&gt; | Extract all physical ReinforcingBars from the structural Bar. Only extracts reinforcement for bars owning a ConcreteSection, for other section types, an empty list will be returned. | - | Structure_Engine |
| SolidVolume | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Returns a Bar's solid volume based on its SectionProperty area and the CentreLine length. | [Volume](/api/oM/Dimensional/Quantities/Attributes/Volume) [m³] | Structure_Engine |
| Tangent | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Gets the tangent Vector of a Bar as the direction Vector from StartNode to EndNode. No offsets or similar are taken into account. | - | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class Bar : BH.oM.Base.BHoMObject,
BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Dimensional.IElement1D,
BH.oM.Dimensional.IElement,
BH.oM.Dimensional.IElementM,
BH.oM.Analytical.Elements.ILink<BH.oM.Structure.Elements.Node>,
BH.oM.Analytical.IAnalytical
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [Bar.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/Elements\Bar.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/Elements/Bar.json"
}
```

The JSON Schema is available on github here:

- [Bar.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/Elements/Bar.json)
### Example JSON instance

Example JSON instance of type Bar.

``` json title="Example JSON"
{
  "_t": "BH.oM.Structure.Elements.Bar",
  "Start": {
    "_t": "BH.oM.Structure.Elements.Node",
    "Position": {
      "_t": "BH.oM.Geometry.Point",
      "X": -4.0,
      "Y": 1.0,
      "Z": 0.0
    },
    "Orientation": null,
    "Support": null,
    "BHoM_Guid": "fbee2fad-dc9d-4b72-a99a-a1ac31c1190e",
    "Name": ""
  },
  "End": {
    "_t": "BH.oM.Structure.Elements.Node",
    "Position": {
      "_t": "BH.oM.Geometry.Point",
      "X": -1.0,
      "Y": 1.0,
      "Z": 0.0
    },
    "Orientation": null,
    "Support": null,
    "BHoM_Guid": "9794ca28-2d94-405d-8326-407951c07771",
    "Name": ""
  },
  "SectionProperty": {
    "_t": "BH.oM.Structure.SectionProperties.ConcreteSection",
    "Name": "",
    "RebarIntent": null,
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
    "SectionProfile": {
      "_t": "BH.oM.Spatial.ShapeProfiles.CircleProfile",
      "Shape": "Circle",
      "Diameter": 0.5,
      "Edges": [
        {
          "_t": "BH.oM.Geometry.Circle",
          "Centre": {
            "_t": "BH.oM.Geometry.Point",
            "X": 0.0,
            "Y": 0.0,
            "Z": 0.0
          },
          "Normal": {
            "_t": "BH.oM.Geometry.Vector",
            "X": 0.0,
            "Y": 0.0,
            "Z": 1.0
          },
          "Radius": 0.25
        }
      ],
      "BHoM_Guid": "4877fe63-23c7-45f2-81b1-f8c7b4894014",
      "Name": ""
    },
    "Area": 0.19634954084936207,
    "Rgy": 0.125,
    "Rgz": 0.125,
    "J": 0.0061359231515425647,
    "Iy": 0.0030679615757712823,
    "Iz": 0.0030679615757712823,
    "Iw": 0.0,
    "Wely": 0.012271846303085129,
    "Welz": 0.012271846303085129,
    "Wply": 0.020833333333333332,
    "Wplz": 0.020833333333333332,
    "CentreZ": 0.0,
    "CentreY": 0.0,
    "Vz": 0.25,
    "Vpz": 0.25,
    "Vy": 0.25,
    "Vpy": 0.25,
    "Asy": 0.1768018468995684,
    "Asz": 0.1768018469014255,
    "BHoM_Guid": "c7a0ddf9-af63-482a-8de2-3dc9e906788c"
  },
  "OrientationAngle": 0.0,
  "Release": {
    "_t": "BH.oM.Structure.Constraints.BarRelease",
    "Name": "FixFix",
    "StartRelease": {
      "_t": "BH.oM.Structure.Constraints.Constraint6DOF",
      "Name": "Fix",
      "TranslationalStiffnessX": 0.0,
      "TranslationalStiffnessY": 0.0,
      "TranslationalStiffnessZ": 0.0,
      "RotationalStiffnessX": 0.0,
      "RotationalStiffnessY": 0.0,
      "RotationalStiffnessZ": 0.0,
      "TranslationX": "Fixed",
      "TranslationY": "Fixed",
      "TranslationZ": "Fixed",
      "RotationX": "Fixed",
      "RotationY": "Fixed",
      "RotationZ": "Fixed",
      "BHoM_Guid": "ae2f65d1-a2f2-4c17-8c38-b353e2bba03d"
    },
    "EndRelease": {
      "_t": "BH.oM.Structure.Constraints.Constraint6DOF",
      "Name": "Fix",
      "TranslationalStiffnessX": 0.0,
      "TranslationalStiffnessY": 0.0,
      "TranslationalStiffnessZ": 0.0,
      "RotationalStiffnessX": 0.0,
      "RotationalStiffnessY": 0.0,
      "RotationalStiffnessZ": 0.0,
      "TranslationX": "Fixed",
      "TranslationY": "Fixed",
      "TranslationZ": "Fixed",
      "RotationX": "Fixed",
      "RotationY": "Fixed",
      "RotationZ": "Fixed",
      "BHoM_Guid": "da939579-bc56-456d-ac2c-987179c64d9b"
    },
    "BHoM_Guid": "6f72abaa-c583-449d-890b-735c5b1e5b8d"
  },
  "FEAType": "Flexural",
  "Support": null,
  "Offset": null,
  "BHoM_Guid": "c617ccbc-2c1e-466e-a255-06a1d36f0dc7",
  "Name": "Bar Name",
  "_bhomVersion": "8.2"
}
```

