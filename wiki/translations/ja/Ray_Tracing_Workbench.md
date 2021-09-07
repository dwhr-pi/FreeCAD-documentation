 


{{VeryImportantMessage|The Raytracing workbench is essentially obsolete. New development is happening in the [https://github.com/FreeCAD/FreeCAD-render Render Workbench], which is intended as its replacement. This workbench is fully programmed in Python so it is much easier to extend.

Nevertheless, the information in this page is generally useful for the new workbench, as both modules work basically in the same way.
}}

<img alt="Raytracing workbench icon" src=images/Workbench_Raytracing.svg  style="width:128px;">

このモジュールはシーンの内容を外部の[レンダラー](http://en.wikipedia.org/wiki/Rendering_(computer_graphics))に送り出し、作業物のフォトリアリスティックな画像を生成することを目標にしています。レイトレーシングモジュールはまだまだ未完成な初期段階にあり、今のところはそう多くの機能はありません。現在はパートオブジェクトを[POV-ray](http://en.wikipedia.org/wiki/POV-Ray)ファイルとしてエクスポートするための基本的なツールのみ実装されています。エクスポートしたファイルはPOV-rayで読み込んでレンダリングすることができます。

### GUIツール


{{Raytracing Tools/jp}}

### ビューのエクスポート

もっとも簡単な方法は現在の3Dビューとその内容全てを[POV-ray](http://www.povray.org/)ファイルにエクスポートするというものです。まずCADデータを読み込むか作成するかし、適当な3D表示の位置に設定する必要があります。その後、Raytracingメニューから\"Export View\...\"を選択します。

<img alt="" src=images/FreeCAD_Raytracing.jpg  style="width:800px;">

結果\*.povファイルの保存位置を尋ねられます。保存が終わると[POV-ray](http://www.povray.org/)でそれを開き、レンダリングすることができます。

![](images/Povray.jpg )

普段、レンダラーで行うのと同じように大きくてきれいな画像を作成できます：

<img alt="" src=images/Scharniergreifer_render.jpg  style="width:800px;">

### スクリプト処理

モジュールの機能をPythonから使用する方法です：

import Raytracing,RaytracingGui
OutFile = open('C:/Documents and Settings/jriegel/Desktop/test.pov','w')
OutFile.write(open(App.getResourceDir()+'Mod/Raytracing/Templates/ProjectStd.pov').read())
OutFile.write(RaytracingGui.povViewCamera())
OutFile.write(Raytracing.getPartAsPovray('Box',App.activeDocument().Box.Shape,0.800000,0.800000,0.800000))
OutFile.close()
del OutFile


{{TOCright}}

The <img alt="" src=images/Workbench_Raytracing.svg  style="width:24px;"> [Raytracing Workbench](Raytracing_Workbench.md) is used to generate photorealistic images of your models by processing them with an external renderer.

The Raytracing Workbench works with [templates](Raytracing_templates.md), which are project files that define a scene for your 3D model. You can place lights and geometry such as ground planes, and it also contains placeholders for the position of the camera, and for the material information of the objects in the scene. The project can then be exported to a ready-to-render file, or be rendered directly within FreeCAD.

Currently, two renderers are supported: [POV-Ray](POV-Ray.md) and [LuxRender](LuxRender.md). To be able to render from within FreeCAD, at least one of these programs must be installed and configured in your system. However, if no renderer is installed, you will still be able to export a project file to be rendered at another time.

------------------------------------------------------------------------

現在、Lux RendererやYafarayなどの複数のバックエンドをサポートするための新しいRenderer Workbenchが開発中です。開発版を使用するための情報は[Render\_projectで見ることができます](Render_project.md)。

<img alt="" src=images/Raytracing_example.jpg  style="width:1024px;">

## Typical workflow 

1.  Create or open a FreeCAD project, add some solid objects ([Part-based](Part_Workbench.md) or [PartDesign-based](PartDesign_Workbench.md)); meshes are currently not supported.
2.  Create a Raytracing project (povray or luxrender).
3.  Select the objects that you wish to add to the Raytracing project and add them.
4.  Export the project file or render it directly.

<img alt="" src=images/Raytracing_Workbench_workflow.svg  style="width:600px;">


*Workflow of the Raytracing Workbench; the workbench prepares a project file from a given template, and then calls an external program to produce the actual rendering of the scene. The external renderer can be used independently of FreeCAD.*

## 構築用ツール

### Project tools 

These are the main tools for exporting your 3D work to external renderers.

-   <img alt="" src=images/Raytrace_New.svg  style="width:32px;"> [New PovRay project](Raytracing_New.md): Insert new PovRay project in the document
-   <img alt="" src=images/Raytrace_Lux.svg  style="width:32px;"> [New LuxRender project](Raytracing_Lux.md): Insert new LuxRender project in the document
-   <img alt="" src=images/Raytrace_NewPartSegment.svg  style="width:32px;"> [Insert part](Raytracing_InsertPart.md): Insert a view of a Part in a raytracing project
-   <img alt="" src=images/Raytrace_ResetCamera.svg  style="width:32px;"> [Reset camera](Raytracing_ResetCamera.md): Matches the camera position of a raytracing project to the current view
-   <img alt="" src=images/Raytrace_ExportProject.svg  style="width:32px;"> [Export project](Raytracing_ExportProject.md): Exports a raytracing project to a scene file for rendering in an external renderer
-   <img alt="" src=images/Raytrace_Render.svg  style="width:32px;"> [Render](Raytracing_Render.md): Renders a raytracing project with an external renderer

### Utilities

These are helper tools to perform specific tasks manually.

-   <img alt="" src=images/Raytracing_WriteView.svg  style="width:32px;"> [Export view to povray](Raytracing_WriteView.md): Write the active 3D view with camera and all its content to a povray file
-   <img alt="" src=images/Raytracing_WriteCamera.svg  style="width:32px;"> [Export camera to povray](Raytracing_WriteCamera.md): Export the camera position of the active 3D view in POV-Ray format to a file
-   <img alt="" src=images/Raytracing_WritePart.svg  style="width:32px;"> [Export part to povray](Raytracing_WritePart.md): Write the selected Part (object) as a povray file

## Preferences

-   <img alt="" src=images/Preferences-raytracing.svg  style="width:32px;"> [Preferences](Raytracing_Preferences.md): Preferences available in for the Raytracing tools.

## Tutorials

-   [Basic Raytracing tutorial](Raytracing_tutorial.md)
-   [Intermediate Raytracing tutorial](Tutorial_FreeCAD_POV_ray.md)

## Creating a povray file manually 

The utility tools described above allow you to export the current 3D view and all of its content to a [Povray](http://www.povray.org/) file. First, you must load or create your CAD data and position the 3D View orientation as you wish. Then choose \"Utilities → Export View\...\" from the raytracing menu.

![](images/FreeCAD_Raytracing.jpg )

You will be asked for a location to save the resulting \*.pov file. After that you can open it in [Povray](http://www.povray.org/) and render: ![](images/Povray.jpg )

As usual in a renderer you can make big and nice pictures: <img alt="" src=images/Scharniergreifer_render.jpg  style="width:800px;">

## スクリプト処理 

See the [Raytracing API example](Raytracing_API_example.md) for information on writing scenes programmatically.

## リンク

### POV-Rayについて： 

-   <http://www.spiritone.com/~english/cyclopedia/>
-   <http://www.povray.org/>
-   <http://en.wikipedia.org/wiki/POV-Ray>

------------------------------------------------------------------------

現在、LuxRendererやYafarayといった複数のバックエンドをサポートするために新しくレンダラーワークベンチが開発中です。開発版を使用するための情報は[レンダラープロジェクトで見ることができます](Render_project.md)。

レンダラーモジュールの開発ステータスについては[レイトレーシングプロジェクト](Raytracing_project/jp.md) を見てください。

### オープンソースのレンダラー（将来的に実装予定）

-   <http://www.yafaray.org/>
-   <http://www.mitsuba-renderer.org/>
-   <http://www.kerkythea.net/>
-   <http://www.artofillusion.org/>

## Exporting to Kerkythea 

Although direct export to the Kerkythea XML-File-Format is not supported yet, you can export your Objects as Mesh-Files (.obj) and then import them in Kerkythea.

-   if using Kerkythea for Linux, remember to install the WINE-Package (needed by Kerkythea for Linux to run)
-   you can convert your models with the help of the mesh workbench to meshes and then export these meshes as .obj-files
-   If your mesh-export resulted in errors (flip of normals, holes \...) you may try your luck with [netfabb studio basic](http://www.netfabb.com/downloadcenter.php?basic=1)

:   Free for personal use, available for Windows, Linux and Mac OSX.
:   It has standard repair tools which will repair you model in most cases.

-   another good program for mesh analysing/repairing is [Meshlab](http://sourceforge.net/projects/meshlab/)

:   Open Source, available for Windows, Linux and Mac OSX.
:   It has standard repair tools which will repair you model in most cases (fill holes, re-orient normals, etc.)

-   you can use \"make compound\" and then \"make single copy\" or you can fuse solids to group them before converting to meshes
-   remember to set in Kerkythea an import-factor of 0.001 for obj-modeler, since Kerkythea expects the obj-file to be in m (but standard units-scheme in FreeCAD is mm)

:   Within WIndows 7 64-bit Kerkythea does not seem to be able to save these settings.
:   So remember to do that each time you start Kerkythea

-   if importing multiple objects in Kerkythea you can use the \"File → Merge\" command in Kerkythea

## リンク 

-   [Render project](Render_project.md)
-   [Raytracing tutorial](Raytracing_tutorial.md)

These pages refer to the new workbench, programmed in Python, meant to replace the current Raytracing Workbench.

-   [Render Workbench](https://github.com/FreeCAD/FreeCAD-render)
-   [Render Workbench](https://forum.freecadweb.org/viewtopic.php?f=9&t=25933) (announcement only, no discussion)
-   [FreeCAD Renderer Workbench improvements](https://forum.freecadweb.org/viewtopic.php?t=39168)

**Outdated**

These pages refer to a replacement workbench, programmed in C++, proposed around 2012, which was never completed.

-   [Raytracing project](Raytracing_project.md)
-   [Render project](Render_project.md)

!!FUZZY!!{{docnav|Drawing Workbench|Image Workbench}}


{{Raytracing Tools navi

}} 

[Category:Workbenches{{\#translation:}}](Category:Workbenches.md)