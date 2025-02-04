---
- GuiCommand:
   Name:Ship Load‏‎
   MenuLocation:Ship design → Load‏‎ an example ship geometry
   Workbenches:[Ship](Ship_Workbench.md)
   Shortcut:
   SeeAlso:
---

# Ship Geometries Examples/en

## Description

This tool loads example geometries.

Ship works over **Ship entities**, that must be created on top of provided geometry. Geometry must be a solid, or set of solids. The following criteria must be taken into account:

-   All hull geometry must be provided (including symmetric bodies).
-   Starboard geometry must be included at negatives *y* domain.
-   Origin (0,0,0) point is the **Midship section** (Midpoint between after and forward perpendicular) and **base line** intersection.

![](images/FreeCAD-Ship-SignCriteria.jpg ) 
*Ship sign criteria*

## Usage

In order to help new users, Ship includes a geometries examples loader, with the following to choose from:

-   Series 60 from Iowa University
-   Wigley Canonical Ship
-   Series 60 Catamaran
-   Wigley Catamaran

You can load one of those examples following the next steps:

1.  Invoke the Ship Geometries Example Loader by either
    -   pressing on the <img alt="" src=images/Ship_Load.svg  style="width:24px;"> icon in the toolbar
    -   select the **Ship design → Load‏‎ an example ship geometry** from the drop down menu
2.  A task dialog will display, prompting to choose one of the example ship geometries.
3.  Select the example you want to load and press **Accept**
4.  Result: The tool loads a new document with the selected geometry.


**Warning, before editing anything! You are now working with the original example file. To preserve the original unedited example, you must first save it as a new file before editing anything.**

## Tutorials

-   [FreeCAD-Ship s60 tutorial](FreeCAD-Ship_s60_tutorial.md)
-   [FreeCAD-Ship s60 tutorial (II)](FreeCAD-Ship_s60_tutorial_(II).md)





{{Ship_Tools_navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > Ship Geometries Examples/en
