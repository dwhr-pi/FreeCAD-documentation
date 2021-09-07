---
- GuiCommand:/it   Name:FEM_MeshClear   Name/it:FEM MeshClear   Icon:Fem-femmesh-clear-mesh.svg   MenuLocation: Menu contestuale dell'oggetto mesh → FEM mesh clear   |Workbenches:[Shortcut:   SeeAlso:[[FEM_tutorial/it|Tutorial FEM](FEM_Workbench/it___FEM]].md)---


</div>

## Descrizione

Enables the user to reiniitialize the mesh from the FreeCAD FEM mesh object. The mesh still exists but does not have any vertices, edges, faces or elements. The meshing information, Netgen/Gmsh parameters, mesh regions, mesh groups and mesh boundary layer remain in the Model Tree, which means the mesh can be reproduced later. The main use of this function is to lighten the FreeCAD file, either to improve performance when using FreeCAD, to save disk space or enable easy transfer of files without losing meshing data.

## Utilizzo

1.  Right click on the mesh object in the Model Tree <img alt="" src=images/FEM_MeshGmshFromShape.svg  style="width:32px;"> [FEM mesh from shape by Gmsh](FEM_MeshGmshFromShape.md).
2.  Select the <img alt="" src=images/FEM_MeshClear.svg  style="width:32px;"> Clear FEM mesh.

## Notes


<div class="mw-translate-fuzzy">

Da fare


</div>


<div class="mw-translate-fuzzy">





</div>


{{FEM Tools navi

}} 