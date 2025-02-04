---
- GuiCommand:
   Name:Draft SetStyle
   MenuLocation:Utilities → Set style
   Workbenches:[Draft](Draft_Workbench.md), [Arch](Arch_Workbench.md)
   Shortcut:**S** **S**
   Version:0.19
   SeeAlso:[Draft AnnotationStyleEditor](Draft_AnnotationStyleEditor.md), [Draft ApplyStyle](Draft_ApplyStyle.md)
---

# Draft SetStyle

## Description

The <img alt="" src=images/Draft_SetStyle.svg  style="width:24px;"> **Draft SetStyle** command sets the default style for new objects.

Note that several features do not work in the V0.19 version of this command.

 ![](images/Draft_SetStyle_taskpanel.png )  
*The Style settings task panel*

## Usage

1.  There are several ways to invoke the command:
    -   Press the ![](images/Draft_tray_button_style.png ) button in the [Draft Tray](Draft_Tray.md). Depending on the current style settings this button can look different.
    -   Select the **Utilities → <img src="images/Draft_SetStyle.svg" width=16px> Set style** option from the menu.
    -   Use the keyboard shortcut: **S** then **S**. <small>(v0.20)</small> 
2.  The **Style settings** task panel opens. See [Options](#Options.md) for more information.
3.  Optionally change one or more settings.
4.  Press the **OK** button.
5.  The button in the [Draft Tray](Draft_Tray.md) is updated.

## Options

-   From the dropdown list at the top of the task panel an exiting style can be selected. <small>(v0.20)</small> 
-   Press the {{button|<img src="images/Document-save.svg" width=16px> Save style}} button to save the style settings. <small>(v0.20)</small> 
-   In the **Lines and faces** section the following settings can be specified:
    -   
        **Line color**
        
        . This is also used for [Draft Labels](Draft_Label.md) and for the **Point Color** of objects.

    -   
        **Line width**
        
        . This is also used for [Draft Labels](Draft_Label.md).

    -   
        **Draw style**
        
        .

    -   
        **Display mode**
        
        .

    -   
        **Shape color**
        
        .

    -   
        **Transparency**
        
        .
-   In the **Annotations** section the following settings can be specified:
    -   
        **Text font**
        
        .

    -   
        **Text size**
        
        . This is in fact the line height, the letters are smaller.

    -   
        **Text spacing**
        
        . This is used for [Draft Dimensions](Draft_Dimension.md). It is the distance between the text and the dimension line. <small>(v0.20)</small> 

    -   
        **Text color**
        
        . This is also used for the **Line Color** of [Draft Dimensions](Draft_Dimension.md), which defines the color of the whole dimension including the text.

    -   
        **Line spacing**
        
        . This scale factor is applied to the line height. <small>(v0.20)</small> 

    -   
        **Arrow style**
        
        .

    -   
        **Arrow size**
        
        .

    -   
        **Show units**
        
        .

    -   
        **Unit override**
        
        .
-   Press the {{button|<img src="images/Draft_SetStyle.svg" width=16px> Selected}} button to apply the settings to selected objects or groups. <small>(v0.20)</small> 
-   Press the {{button|<img src="images/Draft_Text.svg" width=16px> Texts/dims}} button to apply the settings to all [Draft Texts](Draft_Text.md) and [Draft Dimensions](Draft_Dimension.md). <small>(v0.20)</small> 
-   Press the **Cancel** button to abort the command.

## Notes

-   The **Line color**, **Line width** and **Shape color** settings are not only used for Draft objects, but also for objects created with other workbenches.
-   Styles are saved in a file with a fixed name: {{FileName|StylePresets.json}} which is stored in FreeCAD\'s user {{FileName|Draft}} folder:
    -   On Linux it is usually {{FileName|/home/<username>/.FreeCAD/Draft/}}.
    -   On Windows it is {{FileName|%APPDATA%\FreeCAD\Draft\}}, which is usually {{FileName|C:\Users\<username>\Appdata\Roaming\FreeCAD\Draft\}}.
    -   On macOS it is usually {{FileName|/Users/<username>/Library/Preferences/FreeCAD/Draft/}}.

## Preferences

See also: [Preferences Editor](Preferences_Editor.md) and [Draft Preferences](Draft_Preferences.md).

The following preferences are involved:

-   Line color: **Edit → Preferences... → Part design → Shape appearance → Default Shape view properties → Line color**.
-   Line width: **Edit → Preferences... → Part design → Shape appearance → Default Shape view properties → Line width**.
-   Draw style: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Draft → DefaultDrawStyle**.
-   Display mode: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Draft → DefaultDisplayMode**.
-   Shape color: **Edit → Preferences... → Part design → Shape appearance → Default Shape view properties → Shape color**.
-   Transparency: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Draft → DefaultTransparency**.
-   Text font: **Edit → Preferences... → Draft → Texts and dimensions → Text settings → Font family**.
-   Text size: **Edit → Preferences... → Draft → Texts and dimensions → Text settings → Font size**.
-   Text spacing: **Edit → Preferences... → Draft → Texts and dimensions → Dimension settings → Text spacing**.
-   Text color: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Draft → DefaultTextColor**.
-   Line spacing: **Tools → Edit parameters... → BaseApp → Preferences → Mod → Draft → LineSpacing**.
-   Arrow style: **Edit → Preferences... → Draft → Texts and dimensions → Dimension settings → Arrow style**.
-   Arrow size: **Edit → Preferences... → Draft → Texts and dimensions → Dimension settings → Arrow size**.
-   Show units: **Edit → Preferences... → Draft → Texts and dimensions → Dimension settings → Show the unit suffix in dimensions**.
-   Unit override: **Edit → Preferences... → Draft → Texts and dimensions → Dimension settings → Override unit**.



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft SetStyle
