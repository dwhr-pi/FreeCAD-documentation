---
- GuiCommand:/it
   Name:SheetMetal_Unfold
   Name/it:Dispiega
   MenuLocation:SheetMetal → Unfold
   Workbenches:[SheetMetal](SheetMetal_Workbench/it.md)
   Shortcut:None
   Version:
   SeeAlso:[SheetMetal UnattendedUnfold](SheetMetal_UnattendedUnfold.md)
---

# SheetMetal Unfold/it


</div>

## Description

The <img alt="" src=images/SheetMetal_Unfold.svg  style="width:24px;"> **SheetMetal Unfold** command unfolds a sheet metal object.

## Usage

To unfold a sheet metal part:

1.  Switch to the <img alt="" src=images/Sheetmetal_workbench_icon.svg  style="width:22px;"> [SheetMetal Workbench](SheetMetal_Workbench.md).
2.  Select a flat face of the sheet metal part. **Note**:the face should be a plane, the thickness should be constant
3.  Click on the <img alt="" src=images/SheetMetal_Unfold.svg  style="width:24px;"> **Unfold** tool to display a menu in task panel to manage unfolding options.
4.  Select projection options of future flattened sketch
5.  Select the rule for bend deduction with [Kfactor](https://github.com/shaise/FreeCAD_SheetMetal#terminology):
    -   Use [Material Definition Sheet](https://github.com/shaise/FreeCAD_SheetMetal#material-definition-sheet)
    -   Or select a manual [Kfactor](https://github.com/shaise/FreeCAD_SheetMetal#terminology) then the ANSI or DIN standard to apply

## Properties

See also: [Property editor](Property_editor.md).

This tool creates an Unfold object and has no representation of its own in the [Tree view](Tree_view.md) or elsewhere and so has no properties.

The **Unfold** object, on the other hand, is derived from a [Part Feature](Part_Feature.md) object and inherits all its properties. It has no additional properties, but its label has a default value:

### Data


{{Properties_Title|Base}}

-    **Label|String**: Default value: The user editable name of this object, it may be any arbitrary UTF8 string.

## Limitations

-   Sheet metal should have constant thickness
-   Flat faces should be planar with no split lines
-   Bend angles should be radius with cylindrical faces
-   Unfold feature is not parametric at the moment.



---
![](images/Right_arrow.png) [documentation index](../README.md) > [SheetMetal](Category_SheetMetal.md) > [Addons](Category_Addons.md) > [External Command Reference](Category_External Command Reference.md) > SheetMetal Unfold/it
