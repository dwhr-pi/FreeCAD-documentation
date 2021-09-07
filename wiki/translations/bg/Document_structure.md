





{{TOCright}}

![](images/Screenshot_treeview.jpg ) Документът в FreeCAD се състои от всички обекти във вашата сцена. Може да съдържа групи от обекти (самата група може да се третира като обект). Един документ може да съдържа едновременно обекти от всеки работен плот. Може да сменяте между работните плотове колкото често желаете докато работите върху един документ. Целия документ (със всички създадени обекти) се запазва върху твърдия диск всеки път когато натиснете Save. Може да отворите няколко документа едновременно в FreeCAD, както и да отворите различни изгледи към същия документ.


<div class="mw-translate-fuzzy">

В документът обектите може да се събират в групи, като всеки обект (и всяка група) имат уникално име. Тъй като всяка група сама по себе си също е обект, може да бъде сложена в друга група. Така групите и обектите образуват дърво. Управлението на групи, обекти и техните имена се извършва основно в прозореца Tree view (прозореца съдържащ дървото на обектите). Също може да се извършва и програматически от python.. В прозорецът Tree view може да създавате групи, да местите обекти между групи, да изтривате обекти или групи (натиснете десния бутон върху обекта/групата и изберете Delete от появилото се меню) и да променяте името на обект/група (натиснете 2 пъти левия бутон на мишката върху обекта). В зависимост от работния плот избран в момента, може да имате достъп и до други операции в прозореца.


</div>


<div class="mw-translate-fuzzy">

Обектите в документа имат различни типове. Всеки работен плот може да създава обекти от своите собствени типове. Нашример [Mesh Workbench](Mesh_Workbench.md) създава mesh обекти (3D повърхности изградени от триъгълници) , [Part Workbench](Part_Workbench.md) създава Part обкети (елементи изградени от по-прости форми), [Draft Workbench](Draft_Workbench.md) също съзадава Part обекти, и т.н.


</div>

Дори да има няколко едновременно отворени документи в FreeCAD, само един от тях може да бъде активен в определен момент. Активния документ е този чиито обекти се виждат в момента в прозореца 3D view.

## Application and User Interface 


<div class="mw-translate-fuzzy">

В FreeCAD, потребителския интерфейс(Gui) е отделен модул от основната програма (App). Същото правило важи и за документите. Документа се състои от 2 части: Application частта,която съдържа нашите обекти (видима в Tree View) и View частта, която съдържа репрезентацията на екрана на вашите обекти (видима в 3D View прозореца).


</div>


<div class="mw-translate-fuzzy">

Дефинициите на вашите обекти са разделени на 2 части. Техните конструктувни параметри (например форма - дали е куб? размер на страните? и т.н.) се намират в Application частта на документа, докато графичното описание (с какъв цвят линии е нарисуван обекта? С какъв цвят страни?) се намира в View частта на документа. Това разделение е с цел да може да се използва FreeCAD и със и без графичен интерфейс. Например FreeCAD може да се внедрява в други програми, където да манипулира обекти дори и да не рисува нищо на екрана.


</div>

Във вашия отворен документ, в View частта имате 3D изгледи към вашите обекти. В един и същи активен документ може да отворите няколко изгледи едновременно, така че да разгледате вашия обект от няколко гледни точки. Например може да отворите поглед отгоре и отпред към вашия обект едновременно? Тогава в документа ви ще има 2 различни погледа. Може да отваряте и затваряте нови погледи от менюто View или като натиснете десния бутон върху таб-а view.

## Скрпитиране


<div class="mw-translate-fuzzy">

Документ може лесно да се създава и манипулира от интерпретаторът на python. Например:


</div>


```python
FreeCAD.ActiveDocument
```

Ще върне активния в момента документ. 
```python
FreeCAD.ActiveDocument.Blob
``` Ще върне обект наречен \"Blob\" вътре в вашия документ. 
```python
FreeCADGui.ActiveDocument
``` Ще върне отворения 3D поглед свързан с вашия документ. 
```python
FreeCADGui.ActiveDocument.Blob
``` Ще върне графичната репрезентация на обкета Blob в документа. 
```python
FreeCADGui.ActiveDocument.ActiveView
``` Ще върне активния изглед в момента.


<div class="mw-translate-fuzzy">


{{docnav|Mouse Model/bg|Preferences Editor/bg}}


</div>


