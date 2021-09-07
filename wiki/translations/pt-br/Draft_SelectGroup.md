---
- GuiCommand:
   Name:Draft SelectGroup
   MenuLocation:Utilities → Select group
   Workbenches:[Draft](Draft_Workbench.md), [Arch](Arch_Workbench.md)
   SeeAlso:[Std Group](Std_Group.md), [Draft AddToGroup](Draft_AddToGroup.md), [Draft AddConstruction](Draft_AddConstruction.md), [Draft AutoGroup](Draft_AutoGroup.md)
---

## Descrição

The <img alt="" src=images/Draft_SelectGroup.svg  style="width:24px;"> **Draft SelectGroup** command selects the content of [Draft Layers](Draft_Layer.md), [Std Groups](Std_Group.md) or group-like [Arch](Arch_Workbench.md) objects.

The command currently does not work well with layers and can produce confusing results for objects that occur in both a layer and a group.

## Utilização

1.  To use this command at least one group or layer must exist.
2.  Select one or more objects, the selection can include groups selected in the [Tree view](Tree_view.md).
3.  There are several ways to invoke the command:
    -   Press the **<img src="images/Draft_SelectGroup.svg" width=16px> [Draft SelectGroup](Draft_SelectGroup.md)** button.
    -   Select the **Utilities → <img src="images/Draft_SelectGroup.svg" width=16px> Select group** option from the menu.
    -   Select the **Utilities → <img src="images/Draft_SelectGroup.svg" width=16px> Select group** option from the [Tree view](Tree_view.md) or [3D view](3D_view.md) context menu.
4.  The results of the command depend on the provided selection:
    -   For a simple nested object the group or layer the object is in, and its other content, the siblings of the given object, are selected. The sibling objects can include groups, but the content of those nested groups is not selected.
    -   For a given group the group itself, the content of the group, and the content of all nested groups, irrespective of their nesting level, are selected, but the nested groups themselves are not.

## Notes

-   For more information about organizing your model see [Document structure](Document_structure.md) and [Arch tutorial](Arch_tutorial#Organizing_your_model.md).


<div class="mw-translate-fuzzy">





</div>


 