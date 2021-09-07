  

<img alt="Image workbench icon" src=images/Workbench_Image.svg  style="width:128px;">

## Introduction

 

The <img alt="" src=images/Workbench_Image.svg  style="width:24px;"> [Image Workbench](Image_Workbench.md) manages different types of [bitmap](bitmap.md) images, and allows you to open them in FreeCAD.

## Tools

-   <img alt="" src=images/Image_Open.svg  style="width:32px;"> [Open](Image_Open.md): open an image on a new viewport.
-   <img alt="" src=images/Image-import-to-plane.svg  style="width:32px;"> [Import to plane](Image_CreateImagePlane.md): import an image to a plane in the 3D view.
-   <img alt="" src=images/Image-scale.svg  style="width:32px;"> [Scaling](Image_Scaling.md): scale an image imported to a plane.

## Features

-   Like a [Sketch](Sketcher_Workbench.md), an imported image can be attached to one of the main planes XY, XZ, or YZ, and given a positive or negative offset.
-   The image is imported with relation of 1 pixel to 1 millimeter.
-   The recommendation is to have the imported image at a reasonable resolution.

## Workflow

A major use of this workbench is tracing over the image, with the [Draft](Draft_Workbench.md) or [Sketcher](Sketcher_Workbench.md) tools, in order to generate a solid body based on the contours of the image.

Tracing over an image works best if the image has a small negative offset, for example, -0.1 mm, from the working plane. This means that the image will be slightly behind the plane where you draw your 2D geometry, so you won\'t draw on the image itself.

The offset of the image can be set during import, or changed later through its properties.




 {{Image Tools navi}} 

[Category:Workbenches{{\#translation:}}](Category:Workbenches.md)