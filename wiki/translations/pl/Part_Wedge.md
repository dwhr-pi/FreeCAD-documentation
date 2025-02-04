---
- GuiCommand:
   Name:Part Wedge
   MenuLocation:Part → Create primitives → Wedge
   Workbenches:[Part](Part_Workbench.md)
   SeeAlso:[Part Primitives](Part_Primitives.md)
---

# Part Wedge/pl

## Description

Create a parametric Wedge object. This Wedge defaults to a larger square base and a smaller square top.

## Usage

### Default Size and Placement 

**Placement:** The default orientation places the base in the XZ plane and the top outward in the Y axis direction. The default base corner is the 0,0,0 origin.

**Base Face:**

-   X : 10 mm
-   Z : 10 mm

**Height:**

-   Y : 0-10 mm

**Top Face:**

-   X : 2-8 mm
-   Z : 2-8 mm

![](images/PartWedgeProperty.png ) 

### Parametric Inputs 

+++
| ![](images/PartWedgeProperty_Inputs.png ) | Using the default placement, the below inputs are: |
|                                                                  |                                                    |
|                                                                  | -                                   |
|                                                                  |     **X min/max**                     |
|                                                                  |                                                 |
|                                                                  |     : Base face X axis span                        |
|                                                                  |                                                    |
|                                                                  | -                                   |
|                                                                  |     **Y min/max**                     |
|                                                                  |                                                 |
|                                                                  |     : Wedge height span                            |
|                                                                  |                                                    |
|                                                                  | -                                   |
|                                                                  |     **Z min/max**                     |
|                                                                  |                                                 |
|                                                                  |     : Base face Z axis span                        |
|                                                                  |                                                    |
|                                                                  | -                                   |
|                                                                  |     **X2 min/max**                    |
|                                                                  |                                                 |
|                                                                  |     : Top face X axis span                         |
|                                                                  |                                                    |
|                                                                  | -                                   |
|                                                                  |     **Z2 min/max**                    |
|                                                                  |                                                 |
|                                                                  |     : Top face Z axis span                         |
+++

### More examples for wedges 

![](images/Wedge_examples.png )



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Part](Part_Workbench.md) > Part Wedge/pl
