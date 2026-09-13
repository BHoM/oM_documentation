---
title: ConnectionAllowance
---

# <small>BH.oM.Structure.Fragments.</small>**ConnectionAllowance**

The connection allowance of an element. Used when evaluating takeoffs to account for additional mass due to connections of the element.

## Class structure

### Implemented interfaces and base types

???+ bhom "The ConnectionAllowance is inheriting from the following base type(s) and implements the following interfaces:"

    -  BH.oM.Base.[IFragment](/api/oM/Framework/Base/Interface/IFragment)
    -  BH.oM.Base.[IObject](/api/oM/Framework/Base/Interface/IObject)


## Properties



### Defining properties

The following properties are defined on the class

| Name             | Type             | Description      | Quantity         |
|------------------|------------------|------------------|------------------|
| Allowance | [double](https://learn.microsoft.com/en-us/dotnet/api/System.Double?view=netstandard-2.0) | Additional connection allowance expressed as a ratio of the mass of the element. For example, a value of 0.1 means a connection allowance equal to 10% of the mass of the element to which this fragment is applied. | [Ratio](/api/oM/Dimensional/Quantities/Attributes/Ratio) [-] |
| Material | [IMaterialFragment](/api/oM/Analytical/Structure/MaterialFragments/IMaterialFragment) | Optional material to be used for the connection. If null, the material of the element will be assumed. | - |
| Name | [string](https://learn.microsoft.com/en-us/dotnet/api/System.String?view=netstandard-2.0) | Optional name for the connection allowance. It will be assigned as the name of the takeoff material. If left empty, the name of the material (or the name of the material of the element) will be used instead.<br>This can be useful if one wants to differentiate between connection and element contributions in the takeoff. | - |


## Code and Schema

### C# implementation

``` C# title="C#"
public class ConnectionAllowance : BH.oM.Base.IFragment, BH.oM.Base.IObject
```

Assembly: Structure_oM.dll

The C# class definition is available on github:

- [ConnectionAllowance.cs](https://github.com/BHoM/BHoM/blob/develop/Structure_oM/Fragments\ConnectionAllowance.cs)

All history and changes of the class can be found by inspection the history.
