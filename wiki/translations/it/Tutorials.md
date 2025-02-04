# Tutorials/it
{{TOCright}}


<div class="mw-translate-fuzzy">

Questa pagina presenta una selezione di tutorial di alta qualità. Un elenco completo e non ordinato di esercitazioni si trova nella pagina: [:Category:Tutorials/it](:Category:Tutorials/it.md), uno elenco completo e ordinabile si trova nella [tabella sottostante](Tutorials/it#Tutorial_-_Elenco_completo.md).

Si può anche consultare le pagine [Tutorial in altri siti](Offsite_tutorials/it.md) e [Video guide per FreeCAD](Video_tutorials/it.md) che forniscono i link a esercitazioni ospitate su siti esterni. Un\'utile fonte di video tutorial è ovviamente anche una ricerca con la parole chiave \"FreeCAD\" su [YouTube](https://YouTube.com).


</div>

Se desiderate contribuire alla stesura di documentazione e tutorial wiki, consultate le linee guida generali del wiki in [WikiPages](WikiPages.md), e leggete [tutorial guidelines](tutorial_guidelines.md).

Si prega di notare la versione di FreeCAD utilizzata nel tutorial in quanto alcuni tutorial potrebbero utilizzare una vecchia versione del programma. Sebbene il processo di modellazione generale possa ancora funzionare, alcuni strumenti potrebbero essere cambiati.

See also [video tutorials](Video_tutorials.md).

## Architettura e BIM 

<File:Arch> tutorial 00.jpg\|link=[Arch tutorial/it](Arch_tutorial/it.md)\|[Tutorial di Architettura](Arch_tutorial/it.md) (v0.14)
Questo tutorial è una essenziale introduzione all\'ambiente Arch. È ampio e mostra un tipico flusso di lavoro, dall\'importazione di piani in formato DXF alla costruzione del modello 3D. <File:Exercise> arch 01.jpg\|link=[Manual:BIM\_modeling/it](Manual:BIM_modeling/it.md)\|[Modellazione BIM](Manual:BIM_modeling/it.md)
Come modellare una piccola casa, produrre un progetto con TechDraw ed esportarlo in IFC. <File:11_T01_window_all_symbol_top.png%7Clink=>[Tutorial\_for\_open\_windows/it](Tutorial_for_open_windows/it.md)\|[Tutorial per porte e finestre aperte](Tutorial_for_open_windows/it.md) (v0.18)
Come visualizzare porte e finestre aperte, con simboli di elevazione e di piano e creare una planimetria di base con TechDraw. <File:17_T02_sketch_2_attached_correctly.png%7Clink=>[Tutorial custom placing of windows and doors/it](Tutorial_custom_placing_of_windows_and_doors/it.md)\|[Progettare finestre personalizzate](Tutorial_custom_placing_of_windows_and_doors/it.md) (v0.18)
Come disegnare porte e finestre personalizzate usando Sketcher e regolare le loro normali per posizionarle correttamente nei muri. <File:Arch_panel_tutorial_01.jpg%7Clink=>[Arch panel tutorial/it](Arch_panel_tutorial/it.md)\|[Tutorial per i pannelli di Arch](Arch_panel_tutorial/it.md) (v0.15)
Modellazione di un pannello per il tetto di una microhouse utilizzando Sketcher, lo strumento Finestra e lo strumento Pannello. <File:Arch_Wikihouse_01.jpg%7Clink=>[Wikihouse porting tutorial/it](Wikihouse_porting_tutorial/it.md)\|[Modellazione di WikiHouse](Wikihouse_porting_tutorial/it.md)
Rimodellazione del progetto WikiHouse con schizzi e pannelli, a partire dall\'importazione di un modello mesh creato in SketchUp.

## Modellazione di parti 


<div class="mw-translate-fuzzy">

FreeCAD fornisce due flussi di lavoro principali per modellare le parti:

-   combinando oggetti, un metodo chiamato [Geometria solida costruttiva](Constructive_solid_geometry/it.md) (CSG) nell\'ambiente [Part](Part_Workbench/it.md), e
-   usando la metodologia di [Editazione delle funzioni](Feature_editing/it.md) nell\'ambiente [PartDesign](PartDesign_Workbench/it.md).


</div>

Notare che il flusso di lavoro di [PartDesign](PartDesign_Workbench/it.md) è stato notevolmente modificato da FreeCAD 0.17 in poi; alcune delle esercitazioni non sono state aggiornate e potrebbero riferirsi alla versione 0.16.


<div class="mw-translate-fuzzy">

<File:GGTuto1> Vue.PNG\|link=[Creating a simple part with PartDesign/it](Creating_a_simple_part_with_PartDesign/it.md)\|[Creare una semplice parte con PartDesign](Creating_a_simple_part_with_PartDesign/it.md) (v0.17)
Una introduzione al flusso di lavoro di PartDesign: tracciamento di uno schizzo, utilizzo di pad, tasca e spostamento dell\'oggetto. PD WB Tutorial018.png\|link=[Basic Part Design Tutorial 017/it](Basic_Part_Design_Tutorial_017/it.md)\|[Basi di Part Design](Basic_Part_Design_Tutorial_017/it.md) (v0.17)
Modellare una parte semplice utilizzando la metodologia di editazione delle funzioni: creando uno schizzo, usando pad, riferimenti esterni, tasca e simmetria. TBHS-model.png\|link=[Toothbrush Head Stand/it](Toothbrush_Head_Stand/it.md)\|[Supporto per testa di spazzolino da denti](Toothbrush_Head_Stand/it.md) (v0.16)
Utilizzare molteplici funzioni: schizzo, vincoli distanza e coincidenza, pad, riferimenti esterni, raccordo, smusso, schiera lineare e sformo. Exercise lego 01.jpg\|link=[Manual:Modeling for product design/it](Manual:Modeling_for_product_design/it.md)\|[Modellazione per la progettazione del prodotto](Manual:Modeling_for_product_design/it.md) (v0.16).
Modellare un mattoncino Lego: schizzi, vincoli di distanza verticale e orizzontale, pad, tasca, riferimento esterno, schiera lineare e assemblaggio. Exercise table complete.jpg\|link=[Manual:Traditional modeling, the CSG way/it](Manual:Traditional_modeling,_the_CSG_way/it.md)\|[Modellazione tradizionale, il metodo CSG](Manual:Traditional_modeling,_the_CSG_way/it.md)
Modellare un tavolo usando solidi semplici come cubi e cilindri ed eseguendo operazioni booleane di fusione e taglio. TutorialDraftShapeString\_Complete.jpg\|link=[Draft ShapeString tutorial/it](Draft_ShapeString_tutorial/it.md)\|[Forma da Testo con Draft](Draft_ShapeString_tutorial/it.md) (v0.16)
Incidere un testo in un solido: estrarre una forma da un testo per renderlo un solido, quindi utilizzare un taglio booleano per scolpirlo in un altro solido. Tutorial WhiffleBall.jpg\|link=[Whiffle Ball tutorial/it](Whiffle_Ball_tutorial/it.md)\|[Creare una sfera traforata](Whiffle_Ball_tutorial/it.md) (v0.16).
Usare le primitive solide, come cubi e cilindri, e le operazioni booleane, come l\'unione e il taglio, per creare una sfera vuota. Tutorial-normand06.jpg\|link=[Basic modeling tutorial/it](Basic_modeling_tutorial/it.md)\|[Guida introduttiva alla modellazione 3D](Basic_modeling_tutorial/it.md)
Creare un angolo di ferro con due metodi: usando le primitive solide e le operazioni booleane (CSG); e estrudendo un profilo planare.


</div>

The Raspberry Pi project has made simple tutorials that are easy to follow, particularly for those new to CAD systems:

-   [freecad-dice](https://projects.raspberrypi.org/en/projects/freecad-dice), model a die with six faces, and optionally 3D print it.
-   [freecad-headphone-tidy](https://projects.raspberrypi.org/en/projects/freecad-headphone-tidy), model a spool to organize and store earphones, and optionally 3D print it.
-   [freecad-chess-set](https://projects.raspberrypi.org/en/projects/freecad-chess-set), model and entire chess set in Bauhaus modernist style.
-   [raspberrypilearning](https://github.com/raspberrypilearning?utf8=%E2%9C%93&q=freecad&type=source&language=) repository (CC-BY 4.0) with other examples.

## Disegni e schizzi 


<div class="mw-translate-fuzzy">

Exercise cabin 01.jpg\|link=[Manual:Traditional 2D drafting/it](Manual:Traditional_2D_drafting/it.md)\|[Disegno tradizionale 2D](Manual:Traditional_2D_drafting/it.md)
Disegnare una pianta del pavimento con linee, polilinee, rettangoli, archi circolari e aggiungere modelli di tratteggio, annotazioni e dimensioni. Esportare il risultato in DXF. Draft\_tutorial\_result.png\|link=[Draft tutorial/it](Draft_tutorial/it.md)\|[Tutorial di Draft](Draft_tutorial/it.md)(v0.16)
Introduzione di base agli strumenti dell\'ambiente Draft: piano di lavoro, griglia, linea, arco, aggiornamento, rettangolo, cerchio, poligono, schiera, dimensioni, annotazioni e forma da testo. Sketcher tutorial result.png\|Link=[Basic\_Sketcher\_Tutorial/it](Basic_Sketcher_Tutorial/it.md)\|[Tutorial di Sketcher](Basic_Sketcher_Tutorial/it.md)(v0.16)
Introduzione di base agli strumenti di Sketcher: modalità costruzione, linea, cerchio, arco, vincoli (uguaglianza, verticale, orizzontale, tangente, distanza, angolo, raggio). Constrain3.png\|link=[Sketcher Micro Tutorial - Constraint Practices/it](Sketcher_Micro_Tutorial_-_Constraint_Practices/it.md)\|[ Micro Tutorial di Sketcher](Sketcher_Micro_Tutorial_-_Constraint_Practices/it.md)(v0.16)
Imparare a vincolare in modo efficace uno schizzo. Preferire i vincoli geometrici rispetto ai vincoli dimensionali.


</div>


<div class="mw-translate-fuzzy">


</gallery>

## Disegno tecnico 


</div>


<div class="mw-translate-fuzzy">

TDTut ProjGroup21.png\|link=[Basic TechDraw Tutorial/it](Basic_TechDraw_Tutorial/it.md)\|[ Tutorial Base di TechDraw](Basic_TechDraw_Tutorial/it.md) (v0.17)
Introduzione essenziale agli strumenti di TechDraw: pagina, vista, scala, dimensioni verticali e orizzontali, annotazioni, gruppi di proiezione, collegamento di dimensioni alla vista 3D. <File:FCTemplateHow.png%7Clink=>[TechDraw\_TemplateHowTo/it](TechDraw_TemplateHowTo/it.md)\|[Come creare dei modelli TechDraw personalizzati](TechDraw_TemplateHowTo/it.md) (v0.17)
Istruzioni per creare un nuovo modello di pagina in Inkscape per l\'utilizzo con TechDraw. Determinare la dimensione del foglio, disegnare una cornice per la pagina, definire un testo fisso ed i campi di testo modificabili.


</div>

## FEM


<div class="mw-translate-fuzzy">

FEM example01 pic00.jpg\|link=[FEM CalculiX Cantilever 3D/it](FEM_CalculiX_Cantilever_3D/it.md)\|[Esempio di analisi FEM su una trave.](FEM_CalculiX_Cantilever_3D/it.md) (v0.17)
Questo è un esempio incluso in ogni installazione di FreeCAD; descrive un\'analisi di base con il risolutore di CalculiX FE. Eliminare il risultato corrente, rieseguire il risolutore e visualizzare gli spostamenti e gli sforzi nella mesh deformata nella finestra. FEM tutorial result.png\|link=[FEM tutorial/it](FEM_tutorial/it.md)\|[Introduzione all\'ambiente FEM.](FEM_tutorial/it.md) (v0.17)
Breve introduzione ai passaggi necessari per eseguire un\'analisi FEM: modellare l\'oggetto, creare una mesh, aggiungere vincoli e forze, aggiungere un materiale, eseguire la risoluzione e visualizzare i risultati. Figure 11 Deformed Mesh.png\|link=[FEM Shear of a Composite Block/it](FEM_Shear_of_a_Composite_Block/it.md)\|[Taglio FEM di un blocco composito.](FEM_Shear_of_a_Composite_Block/it.md) (v0.17)
Studiare la deformazione di un blocco costituito da un nucleo duro circondato da un materiale più morbido: creare regioni di mesh, aggiungere i materiali, impostare i vincoli di scorrimento, aggiungere i carichi di taglio, eseguire la risoluzione e visualizzare i risultati con un piano di taglio. Femconcrete\_Wall\_3D\_rx\_PSS.png\|link=[Analysis\_of\_reinforced\_concrete\_with\_FEM](Analysis_of_reinforced_concrete_with_FEM.md)/it\|[Analisi del cemento armato con FEM](Analysis_of_reinforced_concrete_with_FEM/it.md) (v0.19)
Stimare il livello di rinforzo richiesto in una struttura in cemento per prevenire rotture sotto tensione o taglio.


</div>

## CNC & Stampa 3D 

Path-WalkThroughResult.gif\|link=[Path Walkthrough for the Impatient/it](Path_Walkthrough_for_the_Impatient/it.md)\|[Guida a Path per impazienti](Path_Walkthrough_for_the_Impatient/it.md)
Presentazione rapida del flusso di lavoro per Path: creare una lavorazione, definire l\'output, definire lo strumento di fresatura, definire le operazioni del percorso, avviare la simulazione e generare un file di output G-code. Exercise meshing 03.jpg\|link=[Manual:Preparing models for 3D printing/it](Manual:Preparing_models_for_3D_printing/it.md)\|[Preparare i modelli per la stampa 3D](Manual:Preparing_models_for_3D_printing/it.md) (v0.16)
Convertire un oggetto solido in un oggetto mesh usando lambiente Mesh, esportare la mesh nel formato STL e usare Slic3r per preparare il codice G. In alternativa, utilizzare l\'ambiente Cura o Path per generare il codice G.

## Rendering

Exercise raytracing 05.jpg\|link=[Manual:Creating renderings/it](Manual:Creating_renderings/it.md)\|[Creare il rendering](Manual:Creating_renderings/it.md)
Creare rapidamente un\'immagine di rendering dei modelli con POV-Ray e LuxRender, se sono installati nel sistema. Raytracing tutorial result.png\|link=[Raytracing tutorial/it](Raytracing_tutorial/it.md)\|[Tutorial di Raytracing](Raytracing_tutorial/it.md) (v0.16)
Descrive il flusso di lavoro di base di Raytracing usando POV-Ray o LuxRender: impostare il percorso per i renderer, creare un progetto, impostare la posizione della telecamera, selezionare il modello eseguire il renderer. 12\_T04\_FreeCAD\_POVray\_render\_floor\_wood\_walls\_radiosity\_final.png\|link=[Tutorial FreeCAD POV ray/it](Tutorial_FreeCAD_POV_ray/it.md)\|[Tutorial intermedio di FreeCAD e POV-ray](Tutorial_FreeCAD_POV_ray/it.md) (v0.18)
Flusso di lavoro per produrre un rendering migliore con POV-Ray: creare un progetto, aggiungere gli oggetti, impostare la fotocamera, salvare il file .pov, modificare manualmente il file per migliorare le informazioni su trame, piani, fotocamera, luci e quindi eseguire il renderer dalla riga di comando. 07\_T03\_FreeCAD\_Blender\_EEVEE\_render.png\|link=[Tutorial\_Render\_with\_Blender/it](Tutorial_Render_with_Blender/it.md)\|[Rendering con Blender di un assemblaggio di FreeCAD](Tutorial_Render_with_Blender/it.md) (v0.18)
Esportare i corpi da FreeCAD a Wavefront.obj, importare il file in Blender, impostare una semplice luce solare, assegnare i materiali di base con lo shader di base BSDF e produrre un\'immagine renderizzata con EEVEE e Cycles

## Robot workbench 


<div class="mw-translate-fuzzy">

## Ambiente Robot 


</div>


<div class="mw-translate-fuzzy">

Robot Tutorial RobotSimulation.gif\|link=[Robot tutorial/it](Robot_tutorial/it.md)\|[Tutorial di Robot](Robot_tutorial/it.md) (v0.17)
Simula il movimento di un robot industriale: imposta una traiettoria, imposta la posizione di partenza, modifica la posizione del robot, inserisce vari waypoint e simula il movimento del robot.


</div>

## Script

These are tutorials that are related to scripting or programming. They are geared towards more experienced users, who are already somewhat familiar with the program.

-   [Python scripting tutorial](Python_scripting_tutorial.md)
-   [How to install macros](How_to_install_macros.md)
-   [How to install additional workbenches](How_to_install_additional_workbenches.md)

## Tutorial - Elenco completo 

Qui sono elencati tutti i tutorial che non sono nel manuale **indipendentemente dalla loro qualità**. Se un tutorial è elencato in [:Category:Tutorials](:Category_Tutorials.md) e non in questa tabella, inseritelo.

++++++++
| Tutorial                                                                                                    | Topic                                        | Level                 | Time to complete hh:mm | Authors                                                                                        | FreeCAD version     | Example files                                                                                                                                                                                                                                                                                                                 |
|                                                                                                             |                                              |                       |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
|                                                                                                             |                                              |                       |                        |                                                                                                |                     | \<!\-- Template for new entries                                                                                                                                                                                                                                                                                               |
+=============================================================================================================+==============================================+=======================+========================+================================================================================================+=====================+===============================================================================================================================================================================================================================================================================================================================+
| [Tutorial](Tutorial.md)                                                                             | Topic                                        | Level                 | 0:00                   | [Name](User_Name.md)                                                                   | 1.0                 | None \--\>                                                                                                                                                                                                                                                                                                                    |
++++++++
| [Add Button to FEM Toolbar Tutorial](Add_Button_to_FEM_Toolbar_Tutorial.md)                         | Finite Element Analysis                      |                       |                        | [JohnWang](User_JohnWang.md)                                                           |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Add FEM Constraint Tutorial](Add_FEM_Constraint_Tutorial.md)                                       | Finite Element Analysis                      |                       |                        | [M42kus](User_M42kus.md)                                                               |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Add FEM Equation Tutorial](Add_FEM_Equation_Tutorial.md)                                           | Finite Element Analysis                      |                       |                        | [JohnWang](User_JohnWang.md)                                                           |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Aeroplane](Aeroplane.md)                                                                           | Part Workbench                               | Beginner              | 0:10                   | Hughthecat                                                                                     |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Analysis of reinforced concrete with FEM](Analysis_of_reinforced_concrete_with_FEM.md)             | Reinforced concrete with FEM                 | Intermediate          | 1:00                   | [HarryvL](User_HarryvL.md)                                                             | 0.19 or above       |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Arch panel tutorial](Arch_panel_tutorial.md)                                                       | Modeling an architectural panel              | Beginner              | 1:00                   | Yorik                                                                                          |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Arch tutorial](Arch_tutorial.md)                                                                   | Modeling                                     | Intermediate          |                        | [Yorik](User_Yorik.md)                                                                 | 0.14                |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Basic Attachment Tutorial](Basic_Attachment_Tutorial.md)                                           | Sketch attachment                            | Beginner/intermediate | 01:00                  | [Bance](User_Bance.md)                                                                 | 0.17 and above      | [Basic Attachment Tutorial.FCStd](https://github.com/BanceFC/Examples/blob/master/Basic_Attachment_Tutorial.FCStd)                                                                                                                                                                                                            |
++++++++
| [Basic modeling tutorial](Basic_modeling_tutorial.md)                                               | Introduction to modelling                    | Beginner              | 0:15                   | [NormandC](User_NormandC.md)                                                           | Any                 | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Basic Part Design Tutorial](Basic_Part_Design_Tutorial.md)                                         | Modeling                                     | Beginner              |                        | [Mark Stephen (Quick61)](User_Quick61.md) and [HarryGeier](User_HarryGeier.md) | 0.17 or above       | [Basic Part Design for v0.17](https://github.com/FreeCAD/Examples/blob/master/Basic_Part_Design_Tutorial_Example_017_Files/Basic_Part_Design_Tutorial_017.fcstd)                                                                                                                                                              |
++++++++
| [Basic Sketcher Tutorial](Basic_Sketcher_Tutorial.md)                                               | Sketcher                                     | Beginner              | 1:00                   | [Drei](User_Drei.md) and [Vocx](User_Vocx.md)                                  | 0.19                | [Basic Sketcher tutorial](https://forum.freecadweb.org/viewtopic.php?f=36&t=43594)                                                                                                                                                                                                                                            |
++++++++
| [Basic TechDraw Tutorial](Basic_TechDraw_Tutorial.md)                                               | TechDraw Workbench                           | Beginner              |                        | [WandererFan](User_WandererFan.md)                                                     | 0.17 and above      | [Basic Part Design for v0.17 Sample](https://github.com/FreeCAD/Examples/blob/master/Basic_Part_Design_Tutorial_Example_017_Files/Basic_Part_Design_Tutorial_017.fcstd) [Basic TechDraw Tutorial Sample](https://github.com/FreeCAD/Examples/blob/master/Basic_TechDraw_Tutorial_Example_Files/Basic_TechDraw_Tutorial.fcstd) |
++++++++
| [Code snippets](Code_snippets.md)                                                                   | Python                                       | Beginner              |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Creating a simple part with PartDesign](Creating_a_simple_part_with_PartDesign.md)                 | Modeling                                     | Beginner              | 1:00                   | GlouGlou                                                                                       | 0.17 or above       | [Creating a simple PartDesign Body.FCStd](https://github.com/FreeCAD/Examples/blob/master/Creating_a_simple_PartDesign_Body.FCStd)                                                                                                                                                                                            |
++++++++
| [Customize Toolbars](Customize_Toolbars.md)                                                         |                                              | Beginner              | 0:05                   | [Mario52](User_Mario52.md)                                                             | Any                 | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Draft ShapeString tutorial](Draft_ShapeString_tutorial.md)                                         | Product Design                               | Beginner              | 0:30                   | r-frank and vocx                                                                               | 0.17 and above      | [Draft\_Shapestring\_Text](https://github.com/FreeCAD/Examples/blob/master/Draft_Shapestring_Tutorial_Examples/Draft_Shapestring_Tutorial_Text.FCStd?raw=true)                                                                                                                                                                |
++++++++
| [Draft tutorial](Draft_tutorial.md)                                                                 | Drafting                                     | Beginner              | 0:30                   | [Drei](User_Drei.md) and vocx                                                          | 0.19                | [Draft tutorial updated](https://forum.freecadweb.org/viewtopic.php?f=36&t=43651)                                                                                                                                                                                                                                             |
++++++++
| [Drawing Template HowTo (obsolete)](Drawing_Template_HowTo.md)                                      | 2D Drafting                                  | Intermediate          | 1:00                   | [Mark Stephen (Quick61)](User_Quick61.md)                                              | 0.14.3700 or above  | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Drawing tutorial (obsolete)](Drawing_tutorial.md)                                                  | Blueprints / Drawings                        | Beginner              | 0:15                   | [Drei](User_Drei.md)                                                                   | 0.16 or above       |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Dxf Importer Install](Dxf_Importer_Install.md)                                                     |                                              | Intermediate          | 0:05                   | [Mario52](User_Mario52.md)                                                             | Any                 | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Engine Block Tutorial](Engine_Block_Tutorial.md)                                                   | Part Workbench                               | Beginner              | 1:00                   | Andrewbuck40                                                                                   | 0.14.3700           |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Export to STL or OBJ](Export_to_STL_or_OBJ.md)                                                     | Export to STL or OBJ                         | Beginner              | 0:20                   | r-frank                                                                                        | 0.16.6703           |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Extend FEM Module](Extend_FEM_Module.md)                                                           | Finite Element Analysis                      |                       |                        | [M42kus](User_M42kus.md)                                                               |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [FEM CalculiX Cantilever 3D](FEM_CalculiX_Cantilever_3D.md)                                         | Finite Element Analysis                      | Beginner              | 0:10                   | [Bernd](User_Bernd.md)                                                                 | 0.16.6377 or above  |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [FEM Shear of a Composite Block](FEM_Shear_of_a_Composite_Block.md)                                 | Finite Element Analysis                      | Beginner/Intermediate | 0:300                  | [HarryvL](User_HarryvL.md)                                                             | 0.17.12960 or above |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [FEM tutorial](FEM_tutorial.md)                                                                     | Finite Element Analysis                      | Beginner              | 0:10                   | [Drei](User_Drei.md)                                                                   | 0.16.6700 or above  |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [FEM Tutorial Python](FEM_Tutorial_Python.md)                                                       | Finite Element Analysis                      | Intermediate          | 0:30                   | [Bernd](User_Bernd.md)                                                                 | 0.18.15985 or above |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [FreeCAD-Ship s60 tutorial](FreeCAD-Ship_s60_tutorial.md)                                           | Ship Workbench                               | Beginner              |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [FreeCAD-Ship s60 tutorial (II)](FreeCAD-Ship_s60_tutorial_(II).md)                                 | Ship Workbench                               | Beginner              |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [How to install additional workbenches](How_to_install_additional_workbenches.md)                   | Programming                                  | Medium programmer     | 0:15                   | [r-frank](User:R-frank.md)                                                             | Any                 | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [How to install macros](How_to_install_macros.md)                                                   | Programming                                  | Medium programmer     | 0:15                   | [Mario52](User_Mario52.md)                                                             | Any                 | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Import from STL or OBJ](Import_from_STL_or_OBJ.md)                                                 | Import from STL or OBJ                       | Beginner              | 0:30                   | r-frank                                                                                        | 1.0                 | 0.16.6703                                                                                                                                                                                                                                                                                                                     |
++++++++
| [Import OpenSCAD code](Import_OpenSCAD_code.md)                                                     | Import OpenSCAD code                         | Beginner              | 0:30                   | r-frank                                                                                        | 0.16.6704           | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Import text and geometry from Inkscape](Import_text_and_geometry_from_Inkscape.md)                 | Import text and geometry from Inkscape       | Beginner              | 0:30                   | r-frank                                                                                        | 0.16.6704           |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Import/Export IFC - compiling IfcOpenShell](Import/Export_IFC_-_compiling_IfcOpenShell.md)         | Arch Workbench                               | Advanced              | 2:00                   | Pablo Gil                                                                                      |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Measurement Of Angles On Holes](Measurement_Of_Angles_On_Holes.md)                                 | TechDraw Workbench                           | Beginner              | 0:01                   | AnHi                                                                                           | 0.19                |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [PartDesign Bearingholder Tutorial I](PartDesign_Bearingholder_Tutorial_I.md)                       | Product design - Bearingholder \#1           | Beginner              | 60 minutes             | NormandC                                                                                       |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [PartDesign Bearingholder Tutorial II](PartDesign_Bearingholder_Tutorial_II.md)                     | Product design - Bearingholder \#2           | Beginner              | 60 minutes             | NormandC                                                                                       |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [PartDesign tutorial](PartDesign_tutorial.md)                                                       | Sketcher                                     | Beginner              | 0:15                   | [Drei](User_Drei.md)                                                                   | 0.16 or above       |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Path Walkthrough for the Impatient](Path_Walkthrough_for_the_Impatient.md)                         | Path Workbench                               |                       |                        | Chrisb                                                                                         |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Plot Basic tutorial](Plot_Basic_tutorial.md)                                                       | Plot Workbench Basic Tutorial                | Beginner              |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Plot MultiAxes tutorial](Plot_MultiAxes_tutorial.md)                                               | Plot workbench                               | Intermediate          |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Post-Processing of FEM Results with Paraview](Post-Processing_of_FEM_Results_with_Paraview.md)     | Post-Processing of FEM Results with ParaView | Intermediate          | 2:00                   | [HarryvL](User_HarryvL.md)                                                             | 0.19                | [Beam](https://forum.freecadweb.org/download/file.php?id=103403) and [wall](https://forum.freecadweb.org/download/file.php?id=103557)                                                                                                                                                                                         |
++++++++
| [Python scripting tutorial](Python_scripting_tutorial.md)                                           | Programming                                  | Intermediate          |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Raytracing tutorial](Raytracing_tutorial.md)                                                       | Raytracing                                   | Beginner              | 0:010                  | [Drei](User_Drei.md)                                                                   | 0.16 or above       |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Robot 6-Axis](Robot_6-Axis.md)                                                                     | Robot Workbench                              | Intermediate          |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Robot tutorial](Robot_tutorial.md)                                                                 | Robot Workbench                              | Beginner              |                        | r-frank                                                                                        |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Scripted Parts: Ball Bearing - Part 1](Scripted_Parts:_Ball_Bearing_-_Part_1.md)                   | Part Scripting - Ball Bearing \#1            | Beginner              | 0:30                   | r-frank                                                                                        | 0.16.6706           |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Scripted Parts: Ball Bearing - Part 2](Scripted_Parts:_Ball_Bearing_-_Part_2.md)                   | Part Scripting - Ball Bearing \#2            | Beginner              | 0:30                   | r-frank                                                                                        | 0.16.6706           |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Scripts](Scripts.md)                                                                               | Scripting                                    | Beginner              |                        | onekk Carlo                                                                                    | 0.19                |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Sketcher Micro Tutorial - Constraint Practices](Sketcher_Micro_Tutorial_-_Constraint_Practices.md) | Sketcher                                     | Beginner              | 0:30                   | [Mark Stephen (Quick61)](User_Quick61.md) and vocx                                     | 0.19                | [Sketcher Constraints practices](https://forum.freecadweb.org/viewtopic.php?f=36&p=371659#p371659)                                                                                                                                                                                                                            |
++++++++
| [Sketcher reference](Sketcher_reference.md)                                                         |                                              |                       |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Sketcher requirement for a sketch](Sketcher_requirement_for_a_sketch.md)                           | Sketcher                                     | Beginner              |                        | [Maker](User_Maker.md)                                                                 |                     | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Sketcher Tutorial](Sketcher_Tutorial.md)                                                           | Sketcher                                     | Beginner              |                        | Ulrich                                                                                         |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [TechDraw Pitch Circle Tutorial](TechDraw_Pitch_Circle_Tutorial.md)                                 | TechDraw Workbench                           | Beginner              | 0:10                   | Andergrin                                                                                      | 0.19                | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [TechDraw TemplateGenerator](TechDraw_TemplateGenerator.md)                                         | TechDraw Workbench                           | Intermediate          |                        | [FBXL5](User_FBXL5.md)                                                                 | 0.19                | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [TechDraw TemplateHowTo](TechDraw_TemplateHowTo.md)                                                 | TechDraw Workbench                           | Intermediate          | 1:00                   | wandererfan                                                                                    | 0.17                | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Thread for Screw Tutorial](Thread_for_Screw_Tutorial.md)                                           | Product design                               | Advanced              | 1:00                   | [DeepSOIC](User_DeepSOIC.md), [Murdic](User_Murdic.md), vocx                   | 0.19                | [Updated: Thread for screw tutorial](https://forum.freecadweb.org/viewtopic.php?f=36&t=44668)                                                                                                                                                                                                                                 |
++++++++
| [Toothbrush Head Stand](Toothbrush_Head_Stand.md)                                                   | Modeling                                     | Beginner              | 1:00                   | [EmmanuelG](User_EmmanuelG.md)                                                         | 0.16 or above       | [Thingiverse 2403310](https://www.thingiverse.com/thing:2403310)                                                                                                                                                                                                                                                              |
++++++++
| [Topological data scripting](Topological_data_scripting.md)                                         | Programming                                  | Intermediate          |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Transient FEM analysis](Transient_FEM_analysis.md)                                                 | Transient FEM analysis                       |                       |                        |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Tutorial custom placing of windows and doors](Tutorial_custom_placing_of_windows_and_doors.md)     | Architecture                                 | Intermediate          | 1:00                   | [Vocx](User_Vocx.md)                                                                   | 0.18 or above       | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Tutorial for open windows](Tutorial_for_open_windows.md)                                           | Architecture                                 | Beginner              | 1:00                   | [Vocx](User_Vocx.md)                                                                   | 0.18 or above       | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Tutorial FreeCAD POV ray](Tutorial_FreeCAD_POV_ray.md)                                             | Rendering                                    | Intermediate          | 2:00                   | [Vocx](User_Vocx.md)                                                                   | 0.18 or above       | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Tutorial Render with Blender](Tutorial_Render_with_Blender.md)                                     | Rendering                                    | Intermediate          | 1:00                   | [Vocx](User_Vocx.md)                                                                   | 0.18 or above       | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [VRML Preparation for Robot Simulation](VRML_Preparation_for_Robot_Simulation.md)                   | Robot Workbench                              | Intermediate          |                        |                                                                                                | 0.11.4252ppa1       |                                                                                                                                                                                                                                                                                                                               |
++++++++
| [Washers](Washers.md)                                                                               |                                              |                       |                        |                                                                                                |                     | None                                                                                                                                                                                                                                                                                                                          |
++++++++
| [Whiffle Ball tutorial](Whiffle_Ball_tutorial.md)                                                   | Product design                               | Beginner              | 0:30                   | r-frank and vocx                                                                               | 0.17 and above      | [WhiffleBall\_Tutorial\_FCWiki.FCStd](https://github.com/FreeCAD/Examples/blob/master/Whiffle_Ball_Tutorial_ExampleFiles/WhiffleBall_Tutorial_FCWiki.FCStd?raw=true)                                                                                                                                                          |
++++++++
| [Wikihouse porting tutorial](Wikihouse_porting_tutorial.md)                                         | Wikihouse porting tutorial                   | Intermediate/Advanced | 1:00                   |                                                                                                |                     |                                                                                                                                                                                                                                                                                                                               |
++++++++


<div class="mw-translate-fuzzy">


{{docnav/it|[Elenco dei comandi](List_of_Commands/it.md)|[Personalizzare l'interfaccia](Interface_Customization/it.md)}}


</div>



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Tutorials/it]],  uno elenco completo e ordinabile si trova  nella ](Category_Tutorials/it]],  uno elenco completo e ordinabile si trova  nella .md) > [Tutorials](Category_Tutorials.md) > Tutorials/it
