---
- GuiCommand:/cs
   Name:PartDesign_PolarPattern
   Name/cs:Návrh dílu Polární vzorky
   Workbenches:[Návrh dílu](PartDesign_Workbench/cs.md)
   MenuLocation:Návrh dílu -> Polární vzorky
---

# PartDesign PolarPattern/cs


</div>

## Popis


<div class="mw-translate-fuzzy">

Tento nástroj vezme skupinu jednoho nebo více objektů (originály) a vytvoří z nich druhou skupinu objektů pootočenou kolem dané osy.


</div>

![](images/PartDesign_PolarPattern_example.png )

*Above: a slot-shaped pocket (B) made on top of a base solid (A, also referred to as support) is used for a polar pattern. The result (C) is shown on the right.*


<div class="mw-translate-fuzzy">

## Použití


</div>

#### To create a pattern 

1.  (Optional) Select the feature (or <small>(v0.19)</small>  several features) to be patterned.
2.  Press the **<img src="images/PartDesign_PolarPattern.svg" width=16px> '''PolarPattern'''** button.
    -   If you didn\'t initially select any features, you\'ll be able to select a *single* base feature
3.  Define the **Axis**. See [Options](#Options.md).
4.  Define the **Angle** between the last copied occurrence and the original feature.
5.  Set the number of **Occurrences**.
6.  If you have several features in the pattern, their order can be important, see the image below.
7.  Press **OK**.

#### Ordering features 

![](images/PartDesign_feature-order.gif ) 
*Effect of the feature order*


<small>(v0.19)</small> 

You can change the order by dragging the feature in the list and you will see the result immediately as preview.

#### Adding features 

###### v0.18

1.  Press **Add feature** to add a feature to be patterned. The feature must be visible in the [3D view](3D_view.md):
2.  Switch to the Model tree;
3.  Select in the tree the feature to be added and press **Spacebar** to make it visible in the [3D view](3D_view.md);
4.  Switch back to the Tasks panel;
5.  Select the feature in the 3D view; it will be added to the list.
6.  Repeat to add other features.

###### v0.19

1.  Press **Add feature** to add a feature to be patterned.
2.  Switch to the Model tree;
3.  Select in the tree the feature to be added.
4.  Repeat to add other features.

#### Removing features 

-   Right-click on the feature in the list and select *Remove*.

or

###### v0.18 

1.  Press **Remove feature** to remove a feature from the list. The feature must be visible in the [3D view](3D_view.md):
2.  Switch to the Model tree;
3.  Select in the tree the feature to be removed and press **Spacebar** to make it visible in the [3D view](3D_view.md);
4.  Switch back to the Tasks panel;
5.  Select the feature in the 3D view; it will have been removed from the list.
6.  Repeat to remove other features.

###### v0.19 

1.  Press **Remove feature** to remove a feature from the list.
2.  Switch to the Model tree;
3.  Select in the tree the feature to be removed.
4.  Repeat to remove other features.

## Volby

![](images/Polarpattern_parameters.png )

### Axis

Při vytvoření polárních vzorků nabízí doalogové okno \'parametry polarního vzoru\' dva odlišné způsoby specifikování rotační osy.

#### Normal sketch axis 

An axis being normal to the sketch and starting in the origin of the sketch of the feature being used is taken as axis for the polar pattern.
The pattern direction can be reversed by ticking \'Reverse direction\'.

#### Horizontal sketch axis 

Uses the horizontal axis of the sketch for axis.

#### Vertical sketch axis 

Uses the vertical axis of the sketch for axis.

#### Custom Sketch Axis 

If the sketch which defines the feature to be patterned also contains a construction line (or lines), then the drop down list will contain one custom sketch axis for each construction line. The first construction line will be labelled *Sketch axis 0*.

#### Base (X/Y/Z) axis 


<small>(v0.17)</small> 

Select one of the Body Origin\'s standard axis (X, Y or Z) as axis.

#### Select reference\... 

Allows you to select either a DatumLine or an edge of an object or a line of a sketch to use for axis.

### Angle and Occurrences 


<div class="mw-translate-fuzzy">

### Úhel a výskyty 

Určuje úhel, který má být vzorky pokryt a celkový počet vzorků (včetně originálního). Například čtyři výskyty v úhlu 180 stupňů dá 60 stupnů mezi vzorky. Je zde jedna výjimka: Je-li úhel 360, protože první a poslední výskyt je identický, čtyři výskyty budou po 90 stupních.


</div>

## Omezení


<div class="mw-translate-fuzzy">

-   Podívejte se na [Lineární vzorky](PartDesign_LinearPattern/cs.md)





</div>





{{PartDesign Tools navi

}}



---
![](images/Right_arrow.png) [documentation index](../README.md) > [PartDesign](PartDesign_Workbench.md) > PartDesign PolarPattern/cs
