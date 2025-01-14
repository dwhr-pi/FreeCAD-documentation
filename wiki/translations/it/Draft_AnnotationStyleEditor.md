---
- GuiCommand:/it
   Name:Draft AnnotationStyleEditor
   Name/it:Draft AnnotationStyleEditor
   MenuLocation:Annotazioni → Stile delle annotazioni...
   Workbenches:[Draft](Draft_Workbench/it.md)
   Shortcut:
   SeeAlso:[Testo](Draft_Text/it.md), [Quota](Draft_Dimension/it.md), [Etichetta](Draft_Label/it.md)
   Version:0.19
---

# Draft AnnotationStyleEditor/it


</div>

## Descrizione


<div class="mw-translate-fuzzy">

Lo strumento <img alt="" src=images/Draft_AnnotationStyleEditor.svg  style="width:16px;"> [Stile delle annotazioni](Draft_AnnotationStyleEditor/it.md) permette di definire stili che influenzano le proprietà visive di oggetti simili ad annotazioni, come quelli creati da <img alt="" src=images/Draft_Text.svg  style="width:16px;"> [Testo](Draft_Text/it.md), <img alt="" src=images/Draft_Dimension.svg  style="width:16px;"> [Quota](Draft_Dimension/it.md), e <img alt="" src=images/Draft_Label.svg  style="width:16px;"> [Etichetta](Draft_Label/it.md).


</div>

![](images/Draft_AnnotationStyleEditor_example.png )


<div class="mw-translate-fuzzy">

<img alt="" src=images/Draft_AnnotationStyleEditor_example.png  style="width:400px;"> 
*Editor di stile per configurare le annotazioni.*


</div>

## Utilizzo


<div class="mw-translate-fuzzy">

1.  Premere il pusante **<img src="images/Draft_AnnotationStyleEditor.svg" width=16px> [Stile delle annotazioni](Draft_AnnotationStyleEditor/it.md)**.
2.  Aprire la casella combinata, quindi scegliere **Aggiungi nuovo...** per definire un nuovo stile o selezionare uno degli stili esistenti.
3.  Regolare le proprietà dello stile, quindi premere **OK**.


</div>

## Script

See also: [Autogenerated API documentation](https://freecad.github.io/SourceDoc/) and [FreeCAD Scripting Basics](FreeCAD_Scripting_Basics.md).

Gli stili di annotazione vengono salvati come dizionari serializzati nell\'attributo `Meta` del documento. Questo attributo viene ispezionato dall\'editor dello stile di annotazione quando viene aperto.


```python
>>> print(App.ActiveDocument.Meta["Draft_Style_Lane 1:100"])
{"FontName": "DejaVu Sans", "FontSize": "8.0000 ", "LineSpacing": "1 cm", "ScaleMultiplier": 1.0, "ShowUnit": false, "UnitOverride": "", "Decimals": 2, "ShowLines": true, "LineWidth": 2, "LineColor": 1095216660480, "ArrowType": 0, "ArrowSize": "5.0000 ", "DimensionOvershoot": "1.0000 ", "ExtensionLines": "5.0000 ", "ExtensionOvershoot": "1.0000 "}
```

Ogni stile che appare nell\'editor viene salvato internamente con il nome dello stile preceduto da `Draft_Style_`; questo evita i conflitti di nomi con altre chiavi che possono essere salvate in `Meta`, che può contenere informazioni arbitrarie.

Si può definire qualsiasi nuovo stile aggiungendo le informazioni necessarie a una chiave che inizia con `Draft_Style_`. Il valore corrispondente di questa chiave deve essere un dizionario serializzato usando `json`. 
```python
import json

meta = App.ActiveDocument.Meta
props = {"LineWidth": 6, "ArrowSize": "7"}
meta["Draft_Style_Thick_lines"] = json.dumps(props)
App.ActiveDocument.Meta = meta
``` I valori non inseriti verranno riempiti automaticamente quando si seleziona questo stile nell\'editor di stile.

Allo stesso modo, qualsiasi dizionario serializzato può essere decompresso per essere editato. 
```python
meta = App.ActiveDocument.Meta
new_dict = json.loads(meta["Draft_Style_Thick_lines"])
```

Poiché i widget dell\'interfaccia grafica controllano le unità dei valori di input, molti di questi valori devono essere salvati come stringhe anziché come numeri in virgola mobile.

Stringhe: 
```python
props = {
  "FontName": "DejaVu Sans",
  "FontSize": "12.0000 ",
  "LineSpacing": "1 cm",
  "UnitOverride": "m",
  "ArrowSize": "5.0000 ",
  "DimensionOvershoot": "1.0000 ",
  "ExtensionLines": "5.0000 ",
  "ExtensionOvershoot": "1.0000 "
}
```

Numeri: 
```python
props = {
  "ScaleMultiplier": 1.0,
  "Decimals": 2,
  "LineWidth": 1,
  "LineColor": 1095216660480,
  "ArrowType": 0
}
``` Il colore della linea corrisponde all\'intero a 32 bit, dal quale è possibile estrarre i singoli valori RGBA.

Booleane: 
```python
props = {
  "ShowUnit": False,
  "ShowLines": True
}
```



---
![](images/Right_arrow.png) [documentation index](../README.md) > [Draft](Draft_Workbench.md) > Draft AnnotationStyleEditor/it
