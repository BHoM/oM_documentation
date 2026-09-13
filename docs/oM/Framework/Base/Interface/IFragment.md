---
title: IFragment
---

# <small>BH.oM.Base.</small>**IFragment**

Describes objects that can exist independently or can be attached to other BHoM objects as part of their `FragmentSet` property.

## Interface structure

### Implemented interfaces and base types

???+ bhom "The IFragment is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)


### Interfaces implementing this interface

???+ bhom "The following interfaces are implementing this interface:"

    - BH.oM.Analytical.Fragments.[IDependencyFragment](/api/oM/Analytical/Analytical/Fragments/IDependencyFragment)
    - BH.oM.Analytical.Fragments.[IProjectionFragment](/api/oM/Analytical/Analytical/Fragments/IProjectionFragment)
    - BH.oM.Base.[IAdapterId](/api/oM/Framework/Base/Interface/IAdapterId)
    - BH.oM.Base.[IHashFragment](/api/oM/Framework/Base/Interface/IHashFragment)
    - BH.oM.Base.[IPersistentAdapterId](/api/oM/Framework/Base/Interface/IPersistentAdapterId)
    - BH.oM.Environment.MaterialFragments.[IEnvironmentMaterial](/api/oM/Analytical/Environment/MaterialFragments/IEnvironmentMaterial)
    - BH.oM.Graphics.Fragments.[IRepresentationFragment](/api/oM/Graphics/Graphics/Fragments/IRepresentationFragment)
    - BH.oM.MEP.System.MaterialFragments.[IInsulationMaterial](/api/oM/Analytical/MEP/System/MaterialFragments/IInsulationMaterial)
    - BH.oM.Adapters.Revit.Parameters.[IRevitParameterFragment](/api/oM/Adapter/Adapters/Revit/Parameters/IRevitParameterFragment)
    - BH.oM.Adapters.SAP2000.Fragments.[IPanelAutoMesh](/api/oM/Adapter/Adapters/SAP2000/Fragments/IPanelAutoMesh)
    - BH.oM.Adapters.SAP2000.Fragments.[IPanelOffset](/api/oM/Adapter/Adapters/SAP2000/Fragments/IPanelOffset)
    - BH.oM.Structure.MaterialFragments.[IIsotropic](/api/oM/Analytical/Structure/MaterialFragments/IIsotropic)
    - BH.oM.Structure.MaterialFragments.[IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment)
    - BH.oM.Structure.MaterialFragments.[IOrthotropic](/api/oM/Analytical/Structure/MaterialFragments/IOrthotropic)
    - BH.oM.Structure.MaterialFragments.[ITimber](/api/oM/Analytical/Structure/MaterialFragments/ITimber)


### Classes implementing this interface

??? bhom "The following classes are implementing this interface:"

    - BH.oM.Analytical.Fragments.[ProjectionFragment](/api/oM/Analytical/Analytical/Fragments/ProjectionFragment)
    - BH.oM.Analytical.Fragments.[RoutingFragment](/api/oM/Analytical/Analytical/Fragments/RoutingFragment)
    - BH.oM.Analytical.Fragments.[SourcesDependencyFragment](/api/oM/Analytical/Analytical/Fragments/SourcesDependencyFragment)
    - BH.oM.Analytical.Fragments.[TargetsDependencyFragment](/api/oM/Analytical/Analytical/Fragments/TargetsDependencyFragment)
    - BH.oM.Base.[HashFragment](/api/oM/Framework/Base/HashFragment)
    - BH.oM.Diffing.[RevisionFragment](/api/oM/Framework/Diffing/RevisionFragment)
    - BH.oM.Environment.MaterialFragments.[GasMaterial](/api/oM/Analytical/Environment/MaterialFragments/GasMaterial)
    - BH.oM.Environment.MaterialFragments.[SolidMaterial](/api/oM/Analytical/Environment/MaterialFragments/SolidMaterial)
    - BH.oM.Environment.Fragments.[AnalyticalConstruction](/api/oM/Analytical/Environment/Fragments/AnalyticalConstruction)
    - BH.oM.Environment.Fragments.[BuildingAnalyticalFragment](/api/oM/Analytical/Environment/Fragments/BuildingAnalyticalFragment)
    - BH.oM.Environment.Fragments.[BuildingContextFragment](/api/oM/Analytical/Environment/Fragments/BuildingContextFragment)
    - BH.oM.Environment.Fragments.[BuildingResultFragment](/api/oM/Analytical/Environment/Fragments/BuildingResultFragment)
    - BH.oM.Environment.Fragments.[CoefficientFragment](/api/oM/Analytical/Environment/Fragments/CoefficientFragment)
    - BH.oM.Environment.Fragments.[EnvironmentConstructionFragment](/api/oM/Analytical/Environment/Fragments/EnvironmentConstructionFragment)
    - BH.oM.Environment.Fragments.[LightReflectanceFragment](/api/oM/Analytical/Environment/Fragments/LightReflectanceFragment)
    - BH.oM.Environment.Fragments.[LightTransmittanceFragment](/api/oM/Analytical/Environment/Fragments/LightTransmittanceFragment)
    - BH.oM.Environment.Fragments.[LoadFragment](/api/oM/Analytical/Environment/Fragments/LoadFragment)
    - BH.oM.Environment.Fragments.[OriginContextFragment](/api/oM/Analytical/Environment/Fragments/OriginContextFragment)
    - BH.oM.Environment.Fragments.[PanelAnalyticalFragment](/api/oM/Analytical/Environment/Fragments/PanelAnalyticalFragment)
    - BH.oM.Environment.Fragments.[PanelContextFragment](/api/oM/Analytical/Environment/Fragments/PanelContextFragment)
    - BH.oM.Environment.Fragments.[RadiationFragment](/api/oM/Analytical/Environment/Fragments/RadiationFragment)
    - BH.oM.Environment.Fragments.[SpaceAnalyticalFragment](/api/oM/Analytical/Environment/Fragments/SpaceAnalyticalFragment)
    - BH.oM.Environment.Fragments.[SpaceContextFragment](/api/oM/Analytical/Environment/Fragments/SpaceContextFragment)
    - BH.oM.Adapters.ETABS.[ETABSId](/api/oM/Adapter/Adapters/ETABS/Fragments/ETABSId)
    - BH.oM.Adapters.ETABS.Fragments.[ShellTypeFragment](/api/oM/Adapter/Adapters/ETABS/Fragments/ShellTypeFragment)
    - BH.oM.Adapters.ETABS.Fragments.[Tower](/api/oM/Adapter/Adapters/ETABS/Fragments/Tower)
    - BH.oM.Adapters.ETABS.Elements.[Diaphragm](/api/oM/Adapter/Adapters/ETABS/Elements/Diaphragm)
    - BH.oM.Adapters.ETABS.Elements.[Pier](/api/oM/Adapter/Adapters/ETABS/Elements/Pier)
    - BH.oM.Adapters.ETABS.Elements.[Spandrel](/api/oM/Adapter/Adapters/ETABS/Elements/Spandrel)
    - BH.oM.Adapters.ETABS.Elements.[AutoLengthOffset](/api/oM/Adapter/Adapters/ETABS/Fragments/AutoLengthOffset)
    - BH.oM.Adapters.ETABS.Elements.[InsertionPoint](/api/oM/Adapter/Adapters/ETABS/Fragments/InsertionPoint)
    - BH.oM.Facade.Fragments.[ConstructionOffset](/api/oM/Analytical/Facade/Fragments/ConstructionOffset)
    - BH.oM.Facade.Fragments.[FrameExtensionBox](/api/oM/Analytical/Facade/Fragments/FrameExtensionBox)
    - BH.oM.Facade.Fragments.[GlazingLocation](/api/oM/Analytical/Facade/Fragments/GlazingLocation)
    - BH.oM.Facade.Fragments.[PsiGlassEdge](/api/oM/Analytical/Facade/Fragments/PsiGlassEdge)
    - BH.oM.Facade.Fragments.[PsiJoint](/api/oM/Analytical/Facade/Fragments/PsiJoint)
    - BH.oM.Facade.Fragments.[UValueCavity](/api/oM/Analytical/Facade/Fragments/UValueCavity)
    - BH.oM.Facade.Fragments.[UValueContinuous](/api/oM/Analytical/Facade/Fragments/UValueContinuous)
    - BH.oM.Facade.Fragments.[UValueFrame](/api/oM/Analytical/Facade/Fragments/UValueFrame)
    - BH.oM.Facade.Fragments.[UValueGlassCentre](/api/oM/Analytical/Facade/Fragments/UValueGlassCentre)
    - BH.oM.Facade.Fragments.[UValueGlassEdge](/api/oM/Analytical/Facade/Fragments/UValueGlassEdge)
    - BH.oM.Graphics.[ColourFragment](/api/oM/Graphics/Graphics/Colours/ColourFragment)
    - BH.oM.Graphics.[RenderMesh](/api/oM/Graphics/Graphics/Render/RenderMesh)
    - BH.oM.Graphics.Fragments.[EntityRepresentation](/api/oM/Graphics/Graphics/Fragments/EntityRepresentation)
    - BH.oM.Graphics.Fragments.[GraphRepresentation](/api/oM/Graphics/Graphics/Fragments/GraphRepresentation)
    - BH.oM.Graphics.Fragments.[GroupRepresentation](/api/oM/Graphics/Graphics/Fragments/GroupRepresentation)
    - BH.oM.Graphics.Fragments.[RelationRepresentation](/api/oM/Graphics/Graphics/Fragments/RelationRepresentation)
    - BH.oM.Adapters.GSA.[AnalysisTaskFragment](/api/oM/Adapter/Adapters/GSA/Fragments/AnalysisTaskFragment)
    - BH.oM.Adapters.GSA.[DummyTag](/api/oM/Adapter/Adapters/GSA/Fragments/DummyTag)
    - BH.oM.Adapters.GSA.[GSAId](/api/oM/Adapter/Adapters/GSA/Fragments/GSAId)
    - BH.oM.Adapters.GSA.[IsRigidConstraint](/api/oM/Adapter/Adapters/GSA/Fragments/IsRigidConstraint)
    - BH.oM.Adapters.GSA.MaterialFragments.[Fabric](/api/oM/Adapter/Adapters/GSA/MaterialFragments/Fabric)
    - BH.oM.Adapters.GSA.Fragments.[PanelBoundaryNodeFragment](/api/oM/Adapter/Adapters/GSA/Fragments/PanelBoundaryNodeFragment)
    - BH.oM.IES.Fragments.[SurfaceIndexFragment](/api/oM/Adapter/IES/Fragments/SurfaceIndexFragment)
    - BH.oM.LifeCycleAssessment.[LifeCycleAssessmentScope](/api/oM/Analytical/LifeCycleAssessment/Fragments/LifeCycleAssessmentScope)
    - BH.oM.LifeCycleAssessment.[Scope](/api/oM/Analytical/LifeCycleAssessment/Fragments/Scope)
    - BH.oM.LifeCycleAssessment.Fragments.[AdditionalEPDData](/api/oM/Analytical/LifeCycleAssessment/Fragments/AdditionalEPDData)
    - BH.oM.LifeCycleAssessment.Fragments.[EPDDensity](/api/oM/Analytical/LifeCycleAssessment/Fragments/EPDDensity)
    - BH.oM.Adapters.Lusas.[LusasId](/api/oM/Adapter/Adapters/Lusas/Fragments/LusasId)
    - BH.oM.Adapters.Lusas.Fragments.[MeshSettings1D](/api/oM/Adapter/Adapters/Lusas/Fragments/MeshSettings1D)
    - BH.oM.Adapters.Lusas.Fragments.[MeshSettings2D](/api/oM/Adapter/Adapters/Lusas/Fragments/MeshSettings2D)
    - BH.oM.MEP.System.MaterialFragments.[InsulationMaterial](/api/oM/Analytical/MEP/System/MaterialFragments/InsulationMaterial)
    - BH.oM.MEP.System.MaterialFragments.[LiningMaterial](/api/oM/Analytical/MEP/System/MaterialFragments/LiningMaterial)
    - BH.oM.MEP.Fragments.[GeometryFragment](/api/oM/Analytical/MEP/Fragments/GeometryFragment)
    - BH.oM.MEP.Fragments.[IdentityFragment](/api/oM/Analytical/MEP/Fragments/IdentityFragment)
    - BH.oM.MEP.Fragments.[PlumbingFlowFragment](/api/oM/Analytical/MEP/Fragments/PlumbingFlowFragment)
    - BH.oM.MEP.Fragments.[PlumbingLoadingFixtureUnitFragment](/api/oM/Analytical/MEP/Fragments/PlumbingLoadingFixtureUnitFragment)
    - BH.oM.Adapters.MidasCivil.[MidasCivilId](/api/oM/Adapter/Adapters/MidasCivil/Fragments/MidasCivilId)
    - BH.oM.Adapters.MidasCivil.[TimeHistorySettings](/api/oM/Adapter/Adapters/MidasCivil/Fragments/TimeHistorySettings)
    - BH.oM.Physical.Reinforcement.[ReinforcementFragment](/api/oM/Physical/Physical/Reinforcement/ReinforcementFragment)
    - BH.oM.Physical.Materials.[MaterialClassification](/api/oM/Physical/Physical/Materials/MaterialClassification)
    - BH.oM.Physical.Materials.[VolumetricMaterialTakeoff](/api/oM/Physical/Physical/Materials/VolumetricMaterialTakeoff)
    - BH.oM.Adapters.RAM.[RAMDeckData](/api/oM/Adapter/Adapters/RAM/Fragments/RAMDeckData)
    - BH.oM.Adapters.RAM.[RAMFrameData](/api/oM/Adapter/Adapters/RAM/Fragments/RAMFrameData)
    - BH.oM.Adapters.RAM.[RAMGridData](/api/oM/Adapter/Adapters/RAM/Fragments/RAMGridData)
    - BH.oM.Adapters.RAM.[RAMId](/api/oM/Adapter/Adapters/RAM/Fragments/RAMId)
    - BH.oM.Adapters.RAM.[RAMNodeForceData](/api/oM/Adapter/Adapters/RAM/Fragments/RAMNodeForceData)
    - BH.oM.Adapters.Revit.[RevitGeometry](/api/oM/Adapter/Adapters/Revit/Misc/RevitGeometry)
    - BH.oM.Adapters.Revit.[RevitRepresentation](/api/oM/Adapter/Adapters/Revit/Misc/RevitRepresentation)
    - BH.oM.Adapters.Revit.[RevitTypeFragment](/api/oM/Adapter/Adapters/Revit/Misc/RevitTypeFragment)
    - BH.oM.Adapters.Revit.Parameters.[RevitIdentifiers](/api/oM/Adapter/Adapters/Revit/Parameters/RevitIdentifiers)
    - BH.oM.Adapters.Revit.Parameters.[RevitParametersToPush](/api/oM/Adapter/Adapters/Revit/Parameters/RevitParametersToPush)
    - BH.oM.Adapters.Revit.Parameters.[RevitPulledParameters](/api/oM/Adapter/Adapters/Revit/Parameters/RevitPulledParameters)
    - BH.oM.Adapters.Revit.Elements.[PipeDesignData](/api/oM/Adapter/Adapters/Revit/Elements/PipeDesignData)
    - BH.oM.Revit.[RevitHostFragment](/api/oM/Adapter/Revit/Misc/RevitHostFragment)
    - BH.oM.Adapters.RFEM5.[RFEM5Id](/api/oM/Adapter/Adapters/RFEM5/RFEM5Id)
    - BH.oM.Adapters.RFEM6.[RFEM6ID](/api/oM/Adapter/Adapters/RFEM6/Fragments/RFEM6ID)
    - BH.oM.Adapters.RFEM6.[RFEMHinge](/api/oM/Adapter/Adapters/RFEM6/IntermediateDatastructure/Support/RFEMHinge)
    - BH.oM.Adapters.RFEM6.[RFEMLineSupport](/api/oM/Adapter/Adapters/RFEM6/IntermediateDatastructure/Support/RFEMLineSupport)
    - BH.oM.Adapters.RFEM6.[RFEMNodalSupport](/api/oM/Adapter/Adapters/RFEM6/IntermediateDatastructure/Support/RFEMNodalSupport)
    - BH.oM.Adapters.RFEM6.IntermediateDatastructure.Geometry.[RFEMLine](/api/oM/Adapter/Adapters/RFEM6/IntermediateDatastructure/Geometry/RFEMLine)
    - BH.oM.Adapters.RFEM6.IntermediateDatastructure.Geometry.[RFEMOpening](/api/oM/Adapter/Adapters/RFEM6/IntermediateDatastructure/Geometry/RFEMOpening)
    - BH.oM.Adapters.RFEM6.BHoMDataStructure.SupportDatastrures.[RFEM6GeometricalLineLoadTypes](/api/oM/Adapter/Adapters/RFEM6/BHoMDataStructure/SupportDatastrures/RFEM6GeometricalLineLoadTypes)
    - BH.oM.Adapters.Robot.[ContourLoadPanelNumbers](/api/oM/Adapter/Adapters/Robot/Fragments/ContourLoadPanelNumbers)
    - BH.oM.Adapters.Robot.[LoadCaseLabel](/api/oM/Adapter/Adapters/Robot/Fragments/LoadCaseLabel)
    - BH.oM.Adapters.Robot.[LoadCombinationType](/api/oM/Adapter/Adapters/Robot/Fragments/LoadCombinationType)
    - BH.oM.Adapters.Robot.[PanelFiniteElementIds](/api/oM/Adapter/Adapters/Robot/Fragments/PanelFiniteElementIds)
    - BH.oM.Adapters.Robot.[RobotId](/api/oM/Adapter/Adapters/Robot/Fragments/RobotId)
    - BH.oM.Adapters.Robot.[FramingElementDesignProperties](/api/oM/Adapter/Adapters/Robot/Structural/Properties/FramingElementDesignProperties)
    - BH.oM.Adapters.SAP2000.[SAP2000Id](/api/oM/Adapter/Adapters/SAP2000/Fragments/SAP2000Id)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelAutoMeshByCookieCutLines](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelAutoMeshByCookieCutLines)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelAutoMeshByCookieCutPoints](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelAutoMeshByCookieCutPoints)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelAutoMeshByGeneralDivide](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelAutoMeshByGeneralDivide)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelAutoMeshByMaximumSize](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelAutoMeshByMaximumSize)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelAutoMeshByNumberOfObjects](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelAutoMeshByNumberOfObjects)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelAutoMeshByPointsOnEdges](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelAutoMeshByPointsOnEdges)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelEdgeConstraint](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelEdgeConstraint)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelOffsetByJointPattern](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelOffsetByJointPattern)
    - BH.oM.Adapters.SAP2000.Fragments.[PanelOffsetByPoint](/api/oM/Adapter/Adapters/SAP2000/Fragments/PanelOffsetByPoint)
    - BH.oM.Adapters.SAP2000.Elements.[BarAutoMesh](/api/oM/Adapter/Adapters/SAP2000/Fragments/BarAutoMesh)
    - BH.oM.Adapters.SAP2000.Elements.[BarDesignProcedure](/api/oM/Adapter/Adapters/SAP2000/Fragments/BarDesignProcedure)
    - BH.oM.Adapters.SAP2000.Elements.[BarInsertionPoint](/api/oM/Adapter/Adapters/SAP2000/Fragments/BarInsertionPoint)
    - BH.oM.Structure.Reinforcement.[PanelRebarIntent](/api/oM/Analytical/Structure/Reinforcement/PanelRebarIntent)
    - BH.oM.Structure.MaterialFragments.[Aluminium](/api/oM/Analytical/Structure/MaterialFragments/Aluminium)
    - BH.oM.Structure.MaterialFragments.[Concrete](/api/oM/Analytical/Structure/MaterialFragments/Concrete)
    - BH.oM.Structure.MaterialFragments.[GenericIsotropicMaterial](/api/oM/Analytical/Structure/MaterialFragments/GenericIsotropicMaterial)
    - BH.oM.Structure.MaterialFragments.[GenericOrthotropicMaterial](/api/oM/Analytical/Structure/MaterialFragments/GenericOrthotropicMaterial)
    - BH.oM.Structure.MaterialFragments.[Glulam](/api/oM/Analytical/Structure/MaterialFragments/Glulam)
    - BH.oM.Structure.MaterialFragments.[LaminatedVeneerLumberCrossbands](/api/oM/Analytical/Structure/MaterialFragments/LaminatedVeneerLumberCrossbands)
    - BH.oM.Structure.MaterialFragments.[LaminatedVeneerLumberParallel](/api/oM/Analytical/Structure/MaterialFragments/LaminatedVeneerLumberParallel)
    - BH.oM.Structure.MaterialFragments.[SawnTimber](/api/oM/Analytical/Structure/MaterialFragments/SawnTimber)
    - BH.oM.Structure.MaterialFragments.[Steel](/api/oM/Analytical/Structure/MaterialFragments/Steel)
    - BH.oM.Structure.MaterialFragments.[Timber](/api/oM/Analytical/Structure/MaterialFragments/Timber)
    - BH.oM.Structure.Fragments.[ConnectionAllowance](/api/oM/Analytical/Structure/Fragments/ConnectionAllowance)
    - BH.oM.Structure.Fragments.[ReinforcementDensity](/api/oM/Analytical/Structure/Fragments/ReinforcementDensity)
    - BH.oM.Structure.Fragments.[SectionModifier](/api/oM/Analytical/Structure/Fragments/SectionModifier)
    - BH.oM.Structure.Fragments.[SurfacePropertyModifier](/api/oM/Analytical/Structure/Fragments/SurfacePropertyModifier)
    - BH.oM.Test.Adapter.[TestAdapterId](/api/oM/Framework/Test/Adapter/TestAdapterId)
    - BH.oM.UI.[ParamOldIndexFragment](/api/oM/UI/UI/ParamOldIndexFragment)
    - BH.oM.UI.[PreviousNamesFragment](/api/oM/UI/UI/PreviousNamesFragment)
    - BH.oM.XML.Fragments.[XMLBuildingType](/api/oM/Adapter/XML/Fragments/XMLBuildingType)


## Properties

## Code and Schema

### C# implementation

``` C# title="C#"
public interface IFragment : BH.oM.Base.IObject
```

Assembly: BHoM.dll

The C# interface definition is available on github:

- [IFragment.cs](https://github.com/BHoM/BHoM/blob/develop/BHoM/Interface\IFragment.cs)

All history and changes of the class can be found by inspection the history.
### JSON Schema implementation

The object is defined as a JSON schema. You can validate a JSON instance against this schema by reference. To do this, use the schema reference below in a validator like [this one](https://www.jsonschemavalidator.net/).

``` json title="JSON Schema"
{
 "$ref" : "https://raw.githubusercontent.com/BHoM/BHoM_JSONSchema/develop/BHoM/IFragment.json"
}
```

The JSON Schema is available on github here:

- [IFragment.json](https://github.com/BHoM/BHoM_JSONSchema/blob/develop/BHoM/IFragment.json)
