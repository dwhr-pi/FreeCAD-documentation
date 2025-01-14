# PartDesign MultiTransform/es
---
- GuiCommand:/es   Name:PartDesign_MultiTransform   Workbenches:[[PartDesign Workbench/es   Diseño de Piezas]], Complete|MenuLocation:Diseño de Piezas-> MultiTransformación---


</div>


<div class="mw-translate-fuzzy">

## Introducción

\'Crea un patrón con una combinación de transformaciones\' - Esta herramienta toma un conjunto de una o más operaciones seleccionadas y sus entradas (los \'originales\'), y permite aplicarles varias transformaciones en secuencia. Por ejemplo, para producir una brida con una doble hilera de taladros, el taladro (el \'original\') se crea primero como un patrón lineal en dirección X, y luego como un patrón polar alrededor del eje Y. <img alt="" src=images/multitransform_example.png  style="width:600px;"> 


</div>

\'Make a pattern from combinations of transformations\' - The **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** tool takes one (or a set of) part \'features\' as its input, and allows the user to apply multiple transformations to that feature (or set of features) progressively, in sequence - creating a combined or compound transformation.

For example, to produce the flange with a double row of holes as pictured below, the user:

1.  selected the hole as the \'feature\' (base) in the Model tree
2.  clicked on the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** icon
3.  added a linear pattern with two occurrences in the X direction
4.  added a polar pattern with eight occurrences around the Y axis.

<img alt="" src=images/multitransform_example.png  style="width:600px;"> 
*Flange with double row of holes. Hole pattern created with 'MultiTransform' tool.*

## Usage

Before beginning any of the methods below, make sure the necessary **![](images/)_[Body](PartDesign_Body.md)** object is [active](PartDesign_Body#Usage_Notes.md); if not, you will receive a pop-up error message stating you need an active **![](images/)_[Body](PartDesign_Body.md)** object before using the **![](images/)_[_MultiTransform](PartDesign_MultiTransform.md)** tool.

### Standard Method 

This method starts with no existing transformation features and no selections in the viewport or the Model object tree.
When initiated and completed with this method, the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** should correctly become the \"Tip\" of the Body object.

1.  Click on the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** icon to initiate the operation.
2.  You will be prompted with the **Select feature** window.
    From the list, select one initial feature to be used for the transformations and click **OK** to proceed.
    You may add additional features in the next step.

    :   <img alt="" src=images/PartDesign-MultiTransform-Select_feature.png  style="width:300px;">
3.  The **Transformed features messages** and **MultiTransform parameters** window will appear.
    You will see the label of the feature you selected in the feature list view, below the **Add feature** and **Remove feature** buttons.

    :   <img alt="" src=images/PartDesign-MultiTransform-General.png  style="width:300px;">
    :   If you want to include additional features for the transformations, follow these instructions:

    1.  Click the **Add feature** button in the transform tool
    2.  Switch to the Model tree view (Click on **Model** tab)
    3.  Select the feature you want to add, and make it visible(spacebar, ***or*** right-click and toggle visibility).

        :   **Note:** This will hide the previously visible feature.
    4.  Click on anything in 3D view (viewport).
    5.  Click on **Tasks** tab in Combo View to return to **MultiTransform parameters** window.
    6.  You should see the label of the recently selected feature appear in the feature list view.
4.  Below the feature list view is the **Transformations** list view. Within you should see the text, \"*Right-click to add*\".
5.  Add a transformation by right-clicking in the **Transformations** list view to display the options list.

    :   <img alt="" src=images/PartDesign-MultiTransform-Transformations_Right_Click.png  style="width:300px;">

    1.  Add the desired transformation by selecting it in the options list.
    2.  The new transformation entry will appear in the **Transformations** list with corresponding settings appearing below the list.

        :   <img alt="" src=images/PartDesign-MultiTransform-Transformations-add_linear_pattern.png  style="width:300px;">
    3.  Adjust the settings for the new transformation. (*You will see the preview in the viewport.*)
    4.  Click the **OK** button underneath these settings to save the new transformation.
6.  Continue to add transformations in the order you wish to apply them using Step 5 above.
7.  You may also edit, delete, and move (change the order of) the transformations as needed by right-clicking on a transformation in the **Transformations** list and selecting the corresponding option.
8.  When you are finished adding and editing the transformations, click the **OK** button at the very top to save the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** and exit.

### Alternate Method 1 

This method starts with one existing transformation feature in the **![](images/)_[Body](PartDesign_Body.md)** object.

1.  In the Model tree, within the active Body object, select the existing features to be included.
2.  Click on the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** icon to initiate the operation.
3.  In the feature list view, you will see the label(s) of the previously selected feature(s).
    To add additional features, see **Step 3** in the [Standard Method](PartDesign_MultiTransform#Standard_Method.md) above.
4.  Finish using **Steps 5-8** in the [Standard Method](PartDesign_MultiTransform#Standard_Method.md) above.

### Alternate Method 2 

This method starts with multiple existing, independent feature transformations in the **![](images/)_[Body](PartDesign_Body.md)** object - with the idea of combining them. **NOTE:** to combine existing transformations, they must be within the same Body object and should all use the same feature or feature set in each.

1.  In the Model tree, within the active Body object, select one of existing transformation of those you wish to include.
2.  Click on the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** icon to initiate the operation.
3.  Click the **OK** button at top to save and exit.
4.  In the object tree, select the newly created **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)**.
5.  In the *Property View* window, locate the **Transformations** property in the *Data* tab.
6.  Edit the **Transformations** property by clicking on its value, then click on the ellipse box that appeared to open the **Links** window for this property.
7.  Select all existing feature transformations that should be included. Multiple selections are permitted using **CTRL** + click.
8.  Click **OK** to save and close the **Links** window.
9.  Click the **![](images/)_[Refresh](Std_Refresh.md)** button if activated.

When initiated and completed in this way, the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** might fail to become the \"Tip\" of the Body object. If you need it to be the \"Tip\":

1.  Right click on the newly created **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)**.
2.  If available, choose \"**Set tip**\".

### Usage Notes 

-   Supported feature transformations are: **<img src="images/PartDesign_Mirrored.svg" width=20px> [Mirrored](PartDesign_Mirrored.md)**, **<img src="images/PartDesign_LinearPattern.svg" width=20px> [Linear Pattern](PartDesign_LinearPattern.md)**, **<img src="images/PartDesign_PolarPattern.svg" width=20px> [Polar Pattern](PartDesign_PolarPattern.md)**, and SCALED transformation.
-   Each transformation linked to the **![](images/)_[MultiTransform](PartDesign_MultiTransform.md)** should use the same feature, or set of features, in each.

### Limitations


<div class="mw-translate-fuzzy">

## Limitaciones

-   Una transformación de escala no debería ser la primera en la lista
-   La trasformación de escala debe tener el mismo número de ocurrencias que la transformación inmediatamente precedente en la lista
-   Para ver más limitaciones, mira [operación de matriz lineal](PartDesign_LinearPattern/es.md)





</div>

## Options


<div class="mw-translate-fuzzy">

## Opciones

+++
| ![](images/Multitransfrom_parameters.png ) | Cuando se crea una operación de multitransformación, el diálogo de \'parámetros de multitransformación\' ofrece dos listas diferentes de listas.                                                                                                                                                                                                      |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | ### Seleccionar los originales                                                                                                                                                                                                                                                                                           |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | La lista de los \'originales\', muestra las operaciones a partir de las cuales crear un patrón. Designando cualquier operación se añadirá a la lista.                                                                                                                                                                                                 |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | ### Selecciona las transformaciones                                                                                                                                                                                                                                                                                 |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | Esta lista se puede rellenar con una combinación de transformaciones simples [simetrías](PartDesign_Mirrored/es.md), [matrices lineales](PartDesign_LinearPattern/es.md), [matrices polares](PartDesign_PolarPattern/es.md) y [escalas](PartDesign_Scaled/es.md). Las transformaciones serán aplicadas una tras otra. |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | El menú contextual ofrece las siguientes entradas:                                                                                                                                                                                                                                                                                                    |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | #### Editar                                                                                                                                                                                                                                                                                                                                           |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | Permite editar los parámetros de una transformación en la lista (doble clic tendrá el mismo efecto)                                                                                                                                                                                                                                                   |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | #### Borrar                                                                                                                                                                                                                                                                                                                                           |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | Elimina una transformación de la lista                                                                                                                                                                                                                                                                                                                |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | #### Añadir transformación                                                                                                                                                                                                                                                                                                    |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | Añade una transformación a la lista                                                                                                                                                                                                                                                                                                                   |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | #### Mover Arriba/Abajo                                                                                                                                                                                                                                                                                                           |
|                                                                    |                                                                                                                                                                                                                                                                                                                                                       |
|                                                                    | Permite cambiar el orden de las transformaciones en la lista                                                                                                                                                                                                                                                                                          |
+++





</div>

### Select originals 

The list view shows the \'originals\', the features that are to be patterned. Clicking on any feature will add it to the list.

### Select transformations 

This list can be filled with a combination of the simple transformations [mirrored](PartDesign_Mirrored.md), [linear pattern](PartDesign_LinearPattern.md), [polar pattern](PartDesign_PolarPattern.md) and [scaled](PartDesign_Scaled.md). The transformations will be applied one after the other. The context menu offers the following entries:

#### Edit

Allows editing the parameters of a transformation in the list (double-clicking will have the same effect)

#### Delete

Removes a transformation from the list

#### Add transformation 

Adds a transformation to the list

#### Move Up/Down 

Allows changing the order of transformations in the list \|}

## Examples


<div class="mw-translate-fuzzy">

## Ejemplos

![c\|center\|800px](images/mt_example2.png )

A partir del pequeño saliente se crea un patrón 3 veces en la dirección del eje X y luego escalado por un factor de escalado de dos (de modo que las tres instancias se escalan con los factores 1.0, 1.5 y 2.0). Luego una matriz polar se aplica 8 veces.

![c\|center\|800px](images/mt_example3.png )

A partir de la cajera se crea una simetría respecto al plano YZ y luego se aplican dos matrices lineales para crear una matriz rectangular.





</div>





{{PartDesign Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [PartDesign](PartDesign_Workbench.md) > PartDesign MultiTransform/es
