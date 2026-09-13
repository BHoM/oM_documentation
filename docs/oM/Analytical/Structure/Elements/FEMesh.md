---
title: FEMesh
---

# <small>BH.oM.Structure.Elements.</small>**FEMesh**

2D finite element mesh for structural analysis. Defined by a list of nodes and faces.

## Class structure

### Implemented interfaces and base types

???+ bhom "The FEMesh is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[BHoMObject](/api/oM/Framework/Base/BHoMObject)
    -  BH.oM.Base.[IBHoMObject](/api/oM/Framework/Base/Interface/IBHoMObject)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)
    -  BH.oM.Structure.Elements.[IAreaElement](/api/oM/Analytical/Structure/Elements/IAreaElement)
    -  BH.oM.Dimensional.[IElementM](/api/oM/Dimensional/Dimensional/IElementM)
    -  BH.oM.Analytical.Elements.[IMesh](/api/oM/Analytical/Analytical/Elements/IMesh)&lt;BH.oM.Structure.Elements.[Node](/api/oM/Analytical/Structure/Elements/Node), BH.oM.Structure.Elements.[FEMeshFace](/api/oM/Analytical/Structure/Elements/FEMeshFace)&gt;
    -  BH.oM.Analytical.[IAnalytical](/api/oM/Analytical/Analytical/IAnalytical)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Nodes | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Node](/api/oM/Analytical/Structure/Elements/Node)&gt; | The nodes of the FEMesh. Mesh faces reference these nodes by their position in this list, so it is important to maintain the order. | - |
| Faces | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[FEMeshFace](/api/oM/Analytical/Structure/Elements/FEMeshFace)&gt; | The faces of the FEMesh. Each face contains a list of indices referring to the nodes in the node list it is connecting. | - |
| Property | [ISurfaceProperty](/api/oM/Analytical/Structure/SurfaceProperties/ISurfaceProperty) | Defines the thickness property and material of the FEMesh. | - |


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
| Area | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the area of a FEMesh as the sum of the area of all faces. Quad faces will be triangulated to perform the area calculation. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Structure_Engine |
| CoordinateSystem | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Cartesian](/api/oM/Dimensional/Geometry/CoordinateSystem/Cartesian)&gt; | Get the Cartesian coordinate system descibring the position and local orientation of the FEMeshFaces of the FEMesh in the global coordinate system where the z-axis is the normal of the FEMeshFace and the x and y axes are the directions of the local in-plane axes. | - | Structure_Engine |
| ElementEmbodiedCarbon | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt;&gt; | Evaluates the embodied carbon on the provided element based on IStructE methodology of evaluation.<br>If you would like to evaluate other EPD metrics, please use one of the Query.EnvironmentalResults methods. <br>TemplateMaterials can be provided helping with picking the correct EPD corresponding to each material on the element. Please note that this evaluation method only support mass-based EPDs. | - | LifeCycleAssessment_Engine |
| ElementMaterialNames | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0)&gt; | Query the element's MaterialComposition to form a Material Hint to aid in EPD-Material Mapping. | - | LifeCycleAssessment_Engine |
| ElementScope | [ScopeType](/api/oM/Analytical/LifeCycleAssessment/Enums/ScopeType) | Returns the enumerable type of the scope found on an element. | - | LifeCycleAssessment_Engine |
| EnvironmentalResults | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[IElementResult](/api/oM/Analytical/LifeCycleAssessment/Results/IElementResult)&lt;[MaterialResult](/api/oM/Analytical/LifeCycleAssessment/Results/MaterialResults/MaterialResult)&gt;&gt; | Evaluates the EnvironmentalMetrics for the provided element and returns an ElementResult for each evaluated metric type.<br>Evaluation is done by extracting the material takeoff for the provided element, giving quantities and Materiality.<br>Each Material in the takeoff is then evaluated by finding the EnvironmentalProductDeclaration (EPD), either stored on the material or from the list of template materials.<br>Each metric, or filtered chosen metrics, on the EPD is then evaluated.<br>Finally, an element result is returned per metric type. Each element result being the sum result of all metrics of the same type. | - | LifeCycleAssessment_Engine |
| GeneralMaterialTakeoff | [GeneralMaterialTakeoff](/api/oM/Physical/Physical/Materials/GeneralMaterialTakeoff) | Returns an Area Element's (Panel, FEMesh, Surface etc.) GeneralMaterialTakeoff which contains information about the element's materiality and corresponding quantities. | - | Structure_Engine |
| Geometry | [Mesh](/api/oM/Dimensional/Geometry/Mesh/Mesh) | Gets the geometry of a analytical IMesh as a geometrical Mesh. A geometrical mesh only supports 3 and 4 nodes faces, while a FEMesh does not have this limitation. For FEMeshFaces with more than 4 nodes or less than 3 this operation is therefore not possible. Method required for automatic display in UI packages. | - | Analytical_Engine |
| IArea | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Calculates the area of an IAreaElement. | [Area](/api/oM/Dimensional/Quantities/Attributes/Area) [m²] | Structure_Engine |
| IEdges | [IEnumerable](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.IEnumerable-1?view=netstandard-2.0)&lt;[ICurve](/api/oM/Dimensional/Geometry/Curve/ICurve)&gt; | Extracts all the edge curves from an AreaElement. | - | Structure_Engine |
| IGeneralMaterialTakeoff | [GeneralMaterialTakeoff](/api/oM/Physical/Physical/Materials/GeneralMaterialTakeoff) | Gets the unique Materials along with their volumes defining an object's make-up. | - | Matter_Engine |
| IIsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if an AreaElement is null and outputs relevant error message. | - | Structure_Engine |
| IMaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Gets the unique Materials along with their relative proportions defining an object's make-up. | - | Matter_Engine |
| INormal | [Vector](/api/oM/Dimensional/Geometry/Vector/Vector) | Returns the local z-axis of the IAreaElement. | - | Structure_Engine |
| IPointGrid | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt; | Generates a rectangular grid of points on an IAreaElement. Used for load visualisation. | - | Structure_Engine |
| IsNull | [bool](https://learn.microsoft.com/en-us/dotnet/api/System.Boolean?view=netstandard-2.0) | Checks if an FEMesh or its defining properties are null and outputs relevant error message. | - | Structure_Engine |
| ISolidVolume | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Returns an element's solid volume, i.e. the the volume of the element that had any materiality, excluding cavities, openings and voids. | [Volume](/api/oM/Dimensional/Quantities/Attributes/Volume) [m³] | Matter_Engine |
| IVolumetricMaterialTakeoff | [VolumetricMaterialTakeoff](/api/oM/Physical/Physical/Materials/VolumetricMaterialTakeoff) | Gets the unique Materials along with their volumes defining an object's make-up. | - | Matter_Engine |
| LocalOrientations | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Basis](/api/oM/Dimensional/Geometry/Vector/Basis)&gt; | Get the Vector basis system descibring the local axes orientation of the faces of the FEMesh in the global coordinate system where the z-axis is the normal of each face and the x and y axes are the directions of the local in-plane axes. | - | Structure_Engine |
| Mass | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Evaluates the mass of an object based its VolumetricMaterialTakeoff and Density. | [Mass](/api/oM/Dimensional/Quantities/Attributes/Mass) [kg] | Matter_Engine |
| MaterialComposition | [MaterialComposition](/api/oM/Physical/Physical/Materials/MaterialComposition) | Returns an AreaElement's homogeneous MaterialComposition. | - | Structure_Engine |
| Normals | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Vector](/api/oM/Dimensional/Geometry/Vector/Vector)&gt; | Returns the local z-axes of all FEMeshFaces in the FEMesh. Can only extract normals for 3 or 4-sided faces. | - | Structure_Engine |
| PointGrid | [List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[List](https://learn.microsoft.com/en-us/dotnet/api/System.Collections.Generic.List-1?view=netstandard-2.0)&lt;[Point](/api/oM/Dimensional/Geometry/Vector/Point)&gt;&gt; | Generates a rectangular grid of points on the each face of the FEMesh. Used for load visualisation. | - | Structure_Engine |
| SolidVolume | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Returns a IAreaElement's solid volume as the area of the element times the average thickness of its SurfaceProperty. The average thickness is evaluated as if it was applied to an infinite plane. | [Volume](/api/oM/Dimensional/Quantities/Attributes/Volume) [m³] | Structure_Engine |


## Code and Schema

### C# implementation

``` C# title="C#"
public class FEMesh : BH.oM.Base.BHoMObject,
BH.oM.Base.IBHoMObject,
BH.oM.Base.IObject,
BH.oM.Structure.Elements.IAreaElement,
BH.oM.Dimensional.IElementM,
BH.oM.Analytical.Elements.IMesh<BH.oM.Structure.Elements.Node, BH.oM.Structure.Elements.FEMeshFace>,
BH.oM.Analytical.IAnalytical
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [FEMesh.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/Elements\FEMesh.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/Structure_oM/Elements/FEMesh.json"
}
```

The JSON Schema is available on github here:

- [FEMesh.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/Structure_oM/Elements/FEMesh.json)
### Example JSON instance

Example JSON instance of type FEMesh.

``` json title="Example JSON"
{
  "_t": "BH.oM.Structure.Elements.FEMesh",
  "Nodes": [
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 0.0,
        "Y": 0.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "cb1d104c-fa41-4232-97b5-239a226485d2",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 2.0,
        "Y": 0.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "42619555-d19f-439d-9a98-7df92ea880ca",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 4.0,
        "Y": 0.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "a90bdab3-dd69-43d9-b71c-36708c14f952",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 6.0,
        "Y": 0.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "4342092f-3df6-4b93-b0c1-607db9a56887",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 0.0,
        "Y": 2.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "50b5490d-a805-40f5-b1ee-baab8e257b0c",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 2.0,
        "Y": 2.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "4d1f6875-394c-49b6-9224-ce9e046acecb",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 4.0,
        "Y": 2.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "e8d90256-827d-4008-8ab7-52eb1967d90b",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 6.0,
        "Y": 2.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "c37c5b0b-1de2-47d5-8ac4-ba622a50b887",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 0.0,
        "Y": 4.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "87e7582e-073b-4109-be3f-6681fb197625",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 2.0,
        "Y": 4.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "d042e3cf-dd53-4b1e-8bf3-3d23cf5563b6",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 4.0,
        "Y": 4.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "960bf755-a1aa-4b91-bb4c-41a7ea9d4ddc",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 6.0,
        "Y": 4.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "ca36edff-372e-4c13-a9f3-40c22ee1caa9",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 0.0,
        "Y": 6.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "99b54c87-3290-420c-8a69-85ec3ec71733",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 2.0,
        "Y": 6.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "8523605d-c27c-4b88-9110-f2b5ac9abb92",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 4.0,
        "Y": 6.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "7b7f3635-7e17-4df5-9185-2b24cd5c0bf0",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.Node",
      "Position": {
        "_t": "BH.oM.Geometry.Point",
        "X": 6.0,
        "Y": 6.0,
        "Z": 0.0
      },
      "Orientation": null,
      "Support": null,
      "BHoM_Guid": "fd93a9ea-627b-4c26-aa98-2bb7cea08534",
      "Name": ""
    }
  ],
  "Faces": [
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        0,
        1,
        5,
        4
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "985b63a7-dfa6-4f57-8c08-16af54953017",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        1,
        2,
        6,
        5
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "84dfa840-a128-4a8b-a7d7-c23516ae6492",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        2,
        3,
        7,
        6
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "0e350386-d327-4897-b763-677d82c252ac",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        4,
        5,
        9,
        8
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "5b4e0c9d-b07b-4d5c-968d-2e5bd0beca68",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        5,
        6,
        10,
        9
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "0fe1d395-34a8-4720-9123-60bd5bee2c9b",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        6,
        7,
        11,
        10
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "2c1950fd-67e2-4508-9f40-c4db568d3965",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        8,
        9,
        13,
        12
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "c6b6c0d6-6674-420e-95cc-672806b0dc1c",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        9,
        10,
        14,
        13
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "9f75082c-1d2f-4ff6-9b47-84e45c12a223",
      "Name": ""
    },
    {
      "_t": "BH.oM.Structure.Elements.FEMeshFace",
      "NodeListIndices": [
        10,
        11,
        15,
        14
      ],
      "OrientationAngle": 0.0,
      "BHoM_Guid": "19dd6cfc-0b68-43a8-804e-3439d1cc03c5",
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
  "BHoM_Guid": "7022b048-4843-4b89-ba3a-d5f1af52284d",
  "Name": "FEMesh Name",
  "_bhomVersion": "8.2"
}
```

