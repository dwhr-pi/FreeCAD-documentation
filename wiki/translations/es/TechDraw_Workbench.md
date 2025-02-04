# <img alt="El icono del Ambiente de trabajo Dibujo Técnico" src=images/Workbench_TechDraw.svg  style="width:64px;"> TechDraw Workbench/es

## Introducción

El <img alt="" src=images/Workbench_TechDraw.svg  style="width:24px;"> [Ambiente de trabajos Croquizador](TechDraw_Workbench/es.md) se utiliza para producir dibujos técnicos básicos a partir de modelos 3D creados con otro Ambiente de trabajos como [Part](Part_Workbench/es.md), [PartDesign](PartDesign_Workbench/es.md), o [Arch](Arch_Workbench/es.md), o importados de otras aplicaciones. Cada dibujo es una Página, que puede contener varias Vistas de objetos dibujables como Part::Características, PartDesign::Cuerpos, App::Grupos de piezas, y Grupos de objetos de documentos. Los dibujos resultantes pueden ser utilizados para cosas como documentación, instrucciones de fabricación, contratos, permisos, etc.

Dimensiones, secciones, áreas sombreadas, anotaciones y [SVG](SVG/es.md) símbolos se pueden añadir a la página, que se pueden exportar a diferentes formatos como [DXF](DXF/es.md), [SVG](SVG/es.md) y [PDF](PDF/es.md).

Dibujo Técnico se incluyó oficialmente en FreeCAD a partir de la versión 0.17; su intención es reemplazar el [Ambiente des trabajo Dibujo](Drawing_Workbench/es.md) no soportado. Ambos Ambiente des trabajo siguen estando disponibles en la versión 0.17, pero el dibujo Ambiente des trabajo puede ser eliminado en futuras versiones. Para mantenerse al día con los planes y desarrollos de TechDraw, visite el [Dibujo Técnico Hoja de ruta](TechDraw_Roadmap/es.md).


<div class="mw-translate-fuzzy">

FreeCAD es principalmente una aplicación de modelado en 3D, y por lo tanto no tiene muchas herramientas de dibujo en 2D, las cuales están incluidas en su mayoría en el [Draft](Draft_Workbench/es.md) y [Ambiente des trabajo Croquizador](Sketcher_Workbench/es.md). Si su objetivo principal es la producción de complejos dibujos 2D y archivos [DXF](DXF/es.md), y no necesita modelado 3D, puede considerar un programa de software dedicado al dibujo técnico como [LibreCAD](https://en.wikipedia.org/wiki/LibreCAD), [QCad](https://en.wikipedia.org/wiki/QCad), TurboCad, y otros.


</div>


{{TOCright}}

<img alt="" src=images/TechDraw_Workbench_Example.png  style="width:600px;">

## Páginas

Estas son herramientas para crear objetos de la página.

-   <img alt="" src=images/TechDraw_PageDefault.svg  style="width:32px;"> [Insertar página predeterminada](TechDraw_PageDefault/es.md): Agrega una nueva página usando el predeterminado [Plantilla](TechDraw_Templates/es.md).

-   <img alt="" src=images/TechDraw_PageTemplate.svg  style="width:32px;"> [Insertar la página usando la plantilla](TechDraw_PageTemplate/es.md): Agrega una nueva página usando un seleccionado [Plantilla](TechDraw_Templates/es.md).

-   <img alt="" src=images/TechDraw_RedrawPage.svg  style="width:32px;"> [Redibujar página](TechDraw_RedrawPage/es.md): fuerza una actualización de la página seleccionada. <small>(v0.19)</small> 

## Vistas

Estas son herramientas para crear objetos de la Vista.

-   <img alt="" src=images/TechDraw_View.svg  style="width:32px;"> [Insertar Vista](TechDraw_View/es.md): Agrega una vista de proyección 2D de un objeto.

-   <img alt="" src=images/TechDraw_ActiveView.svg  style="width:32px;"> [Insertar la vista activa](TechDraw_ActiveView/es.md): inserta una vista de la vista 3D activa. <small>(v0.19)</small> 

-   <img alt="" src=images/TechDraw_ProjectionGroup.svg  style="width:32px;"> [Insertar el Grupo de Proyección](TechDraw_ProjectionGroup/es.md): Invoca un diálogo para crear vistas de uno o más objetos dibujables desde múltiples direcciones.

-   <img alt="" src=images/TechDraw_SectionView.svg  style="width:32px;"> [Insertar vista de sección](TechDraw_SectionView/es.md): inserta una vista de sección transversal de una vista existente.

-   <img alt="" src=images/TechDraw_DetailView.svg  style="width:32px;"> [Insertar la vista detallada](TechDraw_DetailView/es.md): Agrega una vista detallada de una parte de una vista existente.

-   <img alt="" src=images/TechDraw_DraftView.svg  style="width:32px;"> [Insertar el borrador del objeto de l\'ambiente de trabajo](TechDraw_DraftView/es.md) Inserta una vista de un objeto [Draft ambiente de trabajo](Draft_Workbench/es.md).

-   <img alt="" src=images/TechDraw_ArchView.svg  style="width:32px;"> [Insertar Ambiente de trabajo architectura Objeto](TechDraw_ArchView/es.md): Agrega una vista de un [Architectura Ambiente de trabajo](Arch_Workbench/es.md) [Plano de la sección](Arch_SectionPlane/es.md) objeto.

-   <img alt="" src=images/TechDraw_SpreadsheetView.svg  style="width:32px;"> [Insertar Spreadsheet Vista](TechDraw_SpreadsheetView/es.md): Inserta una vista de una [Spreadsheet Ambiente de trabajo](Spreadsheet_Workbench/es.md) sheet.

## Recortes

Estas son herramientas para crear y administrar objetos clip (vistas recortadas).

-   <img alt="" src=images/TechDraw_ClipGroup.svg  style="width:32px;"> [Inserta un grupo de clip](TechDraw_ClipGroup/es.md): Inserta un grupo de clip en una página.

-   <img alt="" src=images/TechDraw_ClipGroupAdd.svg  style="width:32px;"> [Agrega vista al grupo de clips](TechDraw_ClipGroupAdd.md): Agrega una vista existente a un grupo de clip.

-   <img alt="" src=images/TechDraw_ClipGroupRemove.svg  style="width:32px;"> [Eliminar la vista del grupo de clips](TechDraw_ClipGroupRemove/es.md): Elimina una vista de un grupo de clip.

## Decoración

Estas son herramientas para decorar páginas o vistas:

-   <img alt="" src=images/TechDraw_Hatch.svg  style="width:32px;"> [Achurado plano utilizar un archivo de imagen](TechDraw_Hatch/es.md): Aplica un achurado patrón desde un archivo a uno plano.

-   <img alt="" src=images/TechDraw_GeometricHatch.svg  style="width:32px;"> [Geometric Hatch](TechDraw_GeometricHatch/es.md): aplica una sombrea uno plano usando una especificación PAT de Autodesk.

-   <img alt="" src=images/TechDraw_Symbol.svg  style="width:32px;"> [Insertar símbolo SVG](TechDraw_Symbol/es.md): inserta un símbolo de un archivo [SVG](SVG/es.md) en una página.

-   <img alt="" src=images/TechDraw_Image.svg  style="width:32px;"> [Insertar Bitmap imagen](TechDraw_Image/es.md): inserta una imagen PNG o JPG [bitmap](bitmap/es.md) en una página.

-   <img alt="" src=images/TechDraw_ToggleFrame.svg  style="width:32px;"> [Turn View Frames On/Off](TechDraw_ToggleFrame/es.md): activa y desactiva ver marcos y etiquetas que rodean una vista.

## Dimensiones

Estas son herramientas para crear y trabajar con los objetos de las Dimensiones.

Las dimensiones lineales pueden basarse en dos puntos, en una línea o en dos líneas.


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_LengthDimension.svg  style="width:32px;"> [Nueva longitud](TechDraw_LengthDimension/es.md): Agrega una dimensión de longitud.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_HorizontalDimension.svg  style="width:32px;"> [Nuevo Horizontal](TechDraw_HorizontalDimension/es.md): Agrega una dimensión de distancia horizontal.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_VerticalDimension.svg  style="width:32px;"> [Nueva vertical](TechDraw_VerticalDimension/es.md): Agrega una dimensión de distancia vertical.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_RadiusDimension.svg  style="width:32px;"> [Nuevo radio](TechDraw_RadiusDimension/es.md): Agrega una dimensión de radio a un círculo o arco circular.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_DiameterDimension.svg  style="width:32px;"> [Nuevo Diámetro](TechDraw_DiameterDimension/es.md): Agrega una dimensión de Diámetro a un círculo o un arco circular.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_AngleDimension.svg  style="width:32px;"> [Nuevo Ángulo](TechDraw_AngleDimension/es.md): Agrega una dimensión de Ángulo entre dos bordes rectos.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_3PtAngleDimension.svg  style="width:32px;"> [Nuevo ángulo3Pt](TechDraw_3PtAngleDimension/es.md):

Agrega una dimensión de ángulo usando tres vértices.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_HorizontalExtentDimension.svg  style="width:32px;"> [Nueva extensión horizontal](TechDraw_HorizontalExtentDimension/es.md): agrega una dimensión de extensión horizontal. <small>(v0.19)</small> 


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_VerticalExtentDimension.svg  style="width:32px;"> [Nueva extensión vertical](TechDraw_VerticalExtentDimension/es.md): agrega una dimensión de extensión vertical. <small>(v0.19)</small> 


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_LinkDimension.svg  style="width:32px;"> [Nuevos enlaces](TechDraw_LinkDimension/es.md): Vincula 1 o más dimensiones a la geometría 3D.


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_Balloon.svg  style="width:32px;"> [Globo nuevo](TechDraw_Balloon/es.md): agrega una anotación de \"globo\" a una página. <small>(v0.19)</small> 


</div>


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_LandmarkDimension.svg  style="width:32px;"> [Nueva dimensión del hito](TechDraw_LandmarkDimension/es.md): agrega una dimensión de distancia de referencia. <small>(v0.19)</small> 


</div>


<div class="mw-translate-fuzzy">

## Anotación


</div>

Los instrumentos de anotación sirven para \"marcar\" un dibujo con información adicional.

-   <img alt="" src=images/TechDraw_Annotation.svg  style="width:32px;"> [Insertar Anotación](TechDraw_Annotation/es.md): Agrega un bloque de texto simple como anotación.

-   <img alt="" src=images/TechDraw_LeaderLine.svg  style="width:24px;"> [Añadir Leaderline a la vista](TechDraw_LeaderLine/es.md): añade una línea de anotación a una vista. {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_RichTextAnnotation.svg  style="width:24px;"> [Insertar Anotación de Texto Enriquecido](TechDraw_RichTextAnnotation/es.md): añade un bloque de texto enriquecido como anotación a una línea de liderazgo o a una vista. {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_CosmeticVertex.svg  style="width:24px;"> [Agrega Vértice Cosmético](TechDraw_CosmeticVertex/es.md): agrega un Vértice que no es parte de la geometría de la fuente. {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_Midpoints.svg  style="width:24px;"> [Agregar Punto Medio Vértices](TechDraw_Midpoints/es.md): agrega vértices cosméticos en los puntos medios de los bordes seleccionados. {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_Quadrants.svg  style="width:24px;"> [Agregar Vértices de Cuadrante](TechDraw_Quadrants/es.md): agrega Vértices Cosméticos en los cuartos de punto de los bordes seleccionados (circulares). {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_FaceCenterLine.svg  style="width:24px;"> [Añadir línea central a las caras](TechDraw_FaceCenterLine/es.md): añade una línea central a las caras seleccionadas. {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_2LineCenterLine.svg  style="width:24px;"> [Añadir línea central entre 2 líneas](TechDraw_2LineCenterLine/es.md): añade una línea central entre 2 líneas. {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_2PointCenterLine.svg  style="width:24px;"> [Añadir línea central entre 2 puntos](TechDraw_2PointCenterLine/es.md): añade una línea central entre 2 puntos. {{Version/es|0.19}}


<div class="mw-translate-fuzzy">

-   <img alt="" src=images/TechDraw_2PointCosmeticLine.svg  style="width:24px;"> [Añadir una línea cosmética](TechDraw_2PointCosmeticLine/es.md): añade una línea cosmética que conecta 2 vértices. {{Version/es|0.19}}


</div>

-   <img alt="" src=images/TechDraw_CosmeticEraser.svg  style="width:24px;"> [Eliminar objeto cosmético](TechDraw_CosmeticEraser/es.md): elimina los objetos cosméticos de una página.{{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_DecorateLine.svg  style="width:24px;"> [Cambiar la apariencia de las líneas](TechDraw_DecorateLine/es.md): cambia la apariencia de la(s) línea(s) seleccionada(s). {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_ShowAll.svg  style="width:24px;"> [Mostrar/Ocultar Bordes Invisibles](TechDraw_ShowAll/es.md): muestra/oculta las líneas/bordes invisibles en una vista. {{Version/es|0.19}}

-   <img alt="" src=images/TechDraw_WeldSymbol.svg  style="width:24px;"> [Añadir información de soldadura a la línea de mando](TechDraw_WeldSymbol/es.md): añade especificaciones de soldadura a una línea de mando existente. {{Version/es|0.19}}

## Extensions

These are tools to improve your TechDraw drawings.


**Some of these tools have yet to be released.**

### Attributes and modifications 

-   <img alt="" src=images/TechDraw_ExtensionSelectLineAttributes.svg  style="width:32px;"> [Aspect](TechDraw_ExtensionSelectLineAttributes.md): select style, width and colour of lines. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionExtendLine.svg  style="width:32px;"> [Stretch](TechDraw_ExtensionExtendLine.md): extend a line at both ends. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionShortenLine.svg  style="width:32px;"> [Shorten](TechDraw_ExtensionShortenLine.md): shorten a line at both ends. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionLockUnlockView.svg  style="width:32px;"> [Lock/Unlock](TechDraw_ExtensionLockUnlockView.md): Lock/Unlock a view. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionPositionSectionView.svg  style="width:32px;"> [Align Section](TechDraw_ExtensionPositionSectionView.md): align a section view orthogonal to its source view. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionPosHorizChainDimension.svg  style="width:32px;"> [Align Horizontal](TechDraw_ExtensionPosHorizChainDimension.md): align a horizontal dimension chain. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionPosVertChainDimension.svg  style="width:32px;"> [Align Vertical](TechDraw_ExtensionPosVertChainDimension.md): align a vertical dimension chain. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionPosObliqueChainDimension.svg  style="width:32px;"> [Align Oblique](TechDraw_ExtensionPosObliqueChainDimension.md): align an oblique dimension chain. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCascadeHorizDimension.svg  style="width:32px;"> [Horizontal Spacing](TechDraw_ExtensionCascadeHorizDimension.md): cascade horizontal dimensions. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCascadeVertDimension.svg  style="width:32px;"> [Vertical Spacing](TechDraw_ExtensionCascadeVertDimension.md): cascade vertical dimensions. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCascadeObliqueDimension.svg  style="width:32px;"> [Oblique Spacing](TechDraw_ExtensionCascadeObliqueDimension.md): cascade oblique dimensions. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionChangeLineAttributes.svg  style="width:32px;"> [Change Aspect](TechDraw_ExtensionChangeLineAttributes.md): change style, width and colour of lines. <small>(v0.20)</small> 

### Centerlines and threading 

-   <img alt="" src=images/TechDraw_ExtensionCircleCenterLines.svg  style="width:32px;"> [Arc-Circle Centerlines](TechDraw_ExtensionCircleCenterLines.md): adds centerlines to circles and arcs. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionHoleCircle.svg  style="width:32px;"> [Circular Series Centerlines](TechDraw_ExtensionHoleCircle.md): draw the centerlines of a hole/bolt circle. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionVertexAtIntersection.svg  style="width:32px;"> [Intersection Point](TechDraw_ExtensionVertexAtIntersection.md): create the vertexes at intersection of lines. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionDrawCosmCircle.svg  style="width:32px;"> [Circunference](TechDraw_ExtensionDrawCosmCircle.md): draw a cosmetic circumference using center and radius vertex. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionDrawArc.svg  style="width:32px;"> [Arch](TechDraw_ExtensionDrawArc.md): draw an arc rotating counterclockwise. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionLinePerpendicular.svg  style="width:32px;"> [Perpendicular](TechDraw_ExtensionLinePerpendicular.md): draw a line perpendicular to another line through a vertex. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionLineParallel.svg  style="width:32px;"> [Parallel](TechDraw_ExtensionLineParallel.md): draw a line parallel to another line through a vertex. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionThreadHoleSide.svg  style="width:32px;"> [Thread section Hole](TechDraw_ExtensionThreadHoleSide.md): adds a symbolic thread to the side view of a hole. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionThreadBoltSide.svg  style="width:32px;"> [Thread section Shaft](TechDraw_ExtensionThreadBoltSide.md): adds a symbolic thread to the side view of a bolt. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionThreadHoleBottom.svg  style="width:32px;"> [Thread Hole](TechDraw_ExtensionThreadHoleBottom.md): adds symbolic threads to the bottom view of holes. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionThreadBoltBottom.svg  style="width:32px;"> [Thread Shaft](TechDraw_ExtensionThreadBoltBottom.md): adds symbolic threads to the bottom view of bolts. <small>(v0.20)</small> 

### Dimensions

-   <img alt="" src=images/TechDraw_ExtensionInsertDiameter.svg  style="width:32px;"> [Diameter Symbol](TechDraw_ExtensionInsertDiameter.md): insert diameter sign as praefix character. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionInsertSquare.svg  style="width:32px;"> [Tubular Symbol](TechDraw_ExtensionInsertSquare.md): insert square sign as praefix character. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateHorizChainDimension.svg  style="width:32px;"> [Horizontal Series](TechDraw_ExtensionCreateHorizChainDimension.md): create a horizontal dimension chain. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateVertChainDimension.svg  style="width:32px;"> [Vertical Series](TechDraw_ExtensionCreateVertChainDimension.md): create a vertical dimension chain. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateObliqueChainDimension.svg  style="width:32px;"> [Oblique Series](TechDraw_ExtensionCreateObliqueChainDimension.md): create an oblique dimension chain. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateHorizCoordDimension.svg  style="width:32px;"> [Parallel Horizontal](TechDraw_ExtensionCreateHorizCoordDimension.md): create cascaded horizontal dimensions. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateVertCoordDimension.svg  style="width:32px;"> [Parallel Vertical](TechDraw_ExtensionCreateVertCoordDimension.md): create cascaded vertical dimensions. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateObliqueCoordDimension.svg  style="width:32px;"> [Parallel Oblique](TechDraw_ExtensionCreateObliqueCoordDimension.md): create cascaded oblique dimensions. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateHorizChamferDimension.svg  style="width:32px;"> [Horizontal Chamfer](TechDraw_ExtensionCreateHorizChamferDimension.md): create a horizontal chamfer dimension. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateVertChamferDimension.svg  style="width:32px;"> [Vertical Chamfer](TechDraw_ExtensionCreateVertChamferDimension.md): create a vertical chamfer dimension. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionCreateLengthArc.svg  style="width:32px;"> [Arc Length](TechDraw_ExtensionCreateLengthArc.md): create an arc length dimension. <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionIncreaseDecimal.svg  style="width:32px;"> [Increase Accuracy](TechDraw_ExtensionIncreaseDecimal.md): increase decimal places . <small>(v0.20)</small> 

-   <img alt="" src=images/TechDraw_ExtensionDecreaseDecimal.svg  style="width:32px;"> [Decrease Accuracy](TechDraw_ExtensionDecreaseDecimal.md): decrease decimal places . <small>(v0.20)</small> 


<div class="mw-translate-fuzzy">

## Importar/Exportar


</div>

Estas son herramientas para exportar páginas a otras aplicaciones.

-   <img alt="" src=images/TechDraw_ExportPageSVG.svg  style="width:32px;"> [Exportar página como SVG](TechDraw_ExportPageSVG/es.md): guarda la página actual como archivo [SVG](SVG/es.md).

-   <img alt="" src=images/TechDraw_ExportPageDXF.svg  style="width:32px;"> [Exportar página como DXF](TechDraw_ExportPageDXF/es.md): guarda la página actual como archivo [DXF](DXF/es.md).

## Características adicionales 


<div class="mw-translate-fuzzy">

-   [Grupos de líneas](TechDraw_LineGroup/es.md): para controlar la aparición de varios tipos de líneas.
-   [Plantillas](TechDraw_Templates/es.md): las plantillas por defecto definidas para las páginas de dibujo.
-   [Achurado](TechDraw_Hatching/es.md): explicación de las diferentes técnicas de achurado.
-   [Dimensionamiento y tolerancia geométricos](TechDraw_Geometric_dimensioning_and_tolerancing/es.md): explicación sobre cómo lograr el dimensionamiento y tolerancia geométricos.


</div>

## Preferences


<div class="mw-translate-fuzzy">

## Preferencias

-   <img alt="" src=images/Preferences-techdraw.svg  style="width:32px;"> [Preferencias](TechDraw_Preferences/es.md): preferencias para los valores por defecto de la página de dibujo como el ángulo de proyección, los colores, los tamaños de texto y los estilos de línea.


</div>

## Scripting


<div class="mw-translate-fuzzy">

## Guión

Las herramientas de TechDraw pueden ser utilizadas en [macros](macros/es.md) y desde la consola [Python](Python/es.md) utilizando dos APIs.

-   [TechDraw API](TechDraw_API/es.md)
-   [TechDrawGui API](TechDrawGui_API/es.md)


</div>

## Limitations


<div class="mw-translate-fuzzy">

## Limitaciones

-   Los dibujos de TechDraw y la API de Python no son intercambiables con el viejo módulo de Dibujo. Es posible convertir páginas de dibujo en páginas de TechDraw con Python (moveViews.py).
-   Es posible tener tanto TechDraw como Dibujo Paginas en el mismo documento de FreeCAD.
-   Existen pequeñas diferencias en la especificación de textos editables en plantillas en comparación con el módulo de dibujo. Vea la discusión del foro [Escala de plantillas DibujoTécnico](https://forum.freecadweb.org/viewtopic.php?f=3&t=24981&p=196271#p196271) para más detalles.
-   No corte, copie y pegue objetos de DibujoTécnico en la vista de árbol, ya que generalmente no funciona bien.


</div>

## Tutoriales


<div class="mw-translate-fuzzy">

-   [Tutorial básico de DibujoTécnico](Basic_TechDraw_Tutorial/es.md): Introducción a la creación de dibujos con el ambiente de trabajo DibujoTécnico.
-   [Creando una nueva plantilla](TechDraw_TemplateHowTo/es.md): instrucciones para crear una nueva plantilla de página en Inkscape para usarla con el ambiente de trabajo DibujoTécnico.
-   [Medición de los ángulos en los agujeros](Measurement_Of_Angles_On_Holes/es.md): instrucciones para añadir líneas centrales y posteriores representaciones de ángulos en los agujeros.
-   [Misceláneos](TechDraw_HowTo_Page/es.md): Instrucciones para diferentes configuraciones como marcas centrales, etc.
-   [Crear un círculo de cabeceo](TechDraw_Pitch_Circle_Tutorial/es.md): instrucciones para añadir un círculo de cabeceo


</div>

Tutoriales de vídeo de sliptonic

-   Ambiente de trabajo TechDraw [Parte 1 (Básico)](https://www.youtube.com/watch?v=7LbOmSGW9F0), [Parte 2 (Dimensiones)](https://www.youtube.com/watch?v=z3w84RfvqaE), [Parte 3 (Multiview)](https://www.youtube.com/watch?v=uNjXg-m38aI)
-   Ambiente de trabajo de TechDraw [Parte 4 (Sección y detalle)](https://www.youtube.com/watch?v=3zSdeFV6I5o), [Parte 5 (Plantillas de personalización)](https://www.youtube.com/watch?v=kcmdJ7xa7gg)





{{TechDraw Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Workbenches](Category_Workbenches.md) > [TechDraw](Category_TechDraw.md) > TechDraw Workbench/es
