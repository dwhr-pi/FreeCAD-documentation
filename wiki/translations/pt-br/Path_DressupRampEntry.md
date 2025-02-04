---
- GuiCommand:
   Name:Path DressupRampEntry
   MenuLocation:Path → Path Dressup → RampEntry Dressup
   Workbenches:[Path](Path_Workbench.md)
   SeeAlso:[Path DressupTag](Path_DressupTag.md), [Path DressupDogbone](Path_DressupDogbone.md), [Path DressupDragKnife](Path_DressupDragKnife.md)
---

# Path DressupRampEntry/pt-br

## Description

This tool dresses up an existing path to add a ramp entry

## Usage

1.  Select a contour or profile path [Path](Path_Workbench.md) objects
2.  click the <img alt="" src=images/Path_DressupRampEntry.svg  style="width:16px;"> [RampEntry Dress-up](Path_DressupRampEntry.md) menu item

## Properties

-   **Ramp Feed Rate** can either be the current vertical or horizontal feed rate or some other custom value
-   **Angle** of the ramp against the vertical axis. A smaller value makes the ramp steeper.
-   **Method** is used to select different modes of ramping:
    -   RampMethod1 goes down at the ramp angle and the moves horizontal to the target point
    -   RampMethod2 goes horizontal first and then down at the ramp angle to the target point
    -   RampMethod3 goes down in a zigzag way
    -   Helix goes down spiraling
-   **Dressup Start Depth** is the distance above the target level where ramping starts
-   **UseStartDepth** indicates that the ramping does not start above the stock level. If it is not set to true the first ramp can be steeper than expected.





{{Path_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Path](Path_Workbench.md) > Path DressupRampEntry/pt-br
