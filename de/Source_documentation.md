<languages/>

<div class="mw-translate-fuzzy">
{{Docnav/de
|[[Extra python modules/de|Zusätzliche Python Module]]
|[[List of Commands/de|Liste der Befehle]]
}}
</div>

{{TOCright}}

## Überblick  
Der FreeCAD Quellcode ist kommentiert, um eine automatische Generierung der Programmierdokumentation mit (Doxygen)[Doxygen/de|], einem beliebten Quellcode Dokumentationssystem, zu ermöglichen. Doxygen kann sowohl die C++ als auch die Python Teile von FreeCAD dokumentieren, was zu HTML Seiten mit Hyperlinks zu jeder dokumentierten Funktion und Klasse führt.

Die Dokumentation ist online auf der [https://freecad.github.io/SourceDoc/
 FreeCAD API Website] verfügbar. Bitte beachte, dass diese Dokumentation möglicherweise nicht immer auf dem neuesten Stand ist; wenn Du mehr Details benötigst, lade den neuesten Quellcode von FreeCAD herunter und erstelle die Dokumentation selbst. Wenn Du dringende Fragen zum Code hast, stelle diese bitte im Entwicklerbereich des [https://forum.freecadweb.org/index.php FreeCAD Forum].

Die Kompilierung der API Dokumentation folgt den gleichen allgemeinen Schritten wie die Kompilierung der FreeCAD Ausführdatei, wie auf der [[Compile_on_Linux/Unix/de|Kompilieren auf Linux]] Seite angegeben.

![compilation_workflow](https://wiki.freecadweb.org/images/7/7a/FreeCAD_documentation_compilation_workflow.svg)

{{Caption|Allgemeiner Arbeitsablauf zur Erstellung der Programmierdokumentation von FreeCAD. Die Pakete Doxygen und Graphviz müssen sich im System befinden, ebenso wie der FreeCAD Quellcode selbst. CMake konfiguriert das System so, dass mit einer einzigen make Anweisung die Dokumentation für das gesamte Projekt in vielen HTML Dateien mit Diagrammen zusammengefasst wird.}}

== Quelldokumentation erstellen ==

=== Komplette Dokumentation ===

Wenn du Doxygen installiert hast, ist es sehr einfach, die Dokumentation zu erstellen. Installiere auch [https://www.graphviz.org/ Graphviz], um Diagramme erstellen zu können, die die Beziehungen zwischen verschiedenen Klassen und Bibliotheken im FreeCAD Code zeigen. Graphviz wird auch von FreeCADs [[Std_DependencyGraph/de|Abhängigkeitsgraph]] verwendet, um die Beziehungen zwischen verschiedenen Objekten anzuzeigen.
{{Code|code=
sudo apt install doxygen graphviz
}}

<div class="mw-translate-fuzzy">
Folge dann den gleichen Schritten, die Du bei der Kompilierung von FreeCAD durchführen würdest, wie auf der Seite [[Compile_on_Linux/Unix/de|Kompilieren auf Unix]] beschrieben, und hier aus Gründen der Übersichtlichkeit zusammengefasst.
* Hole Dir den Quellcode von FreeCAD und lege ihn in ein eigenes Verzeichnis {{incode|freecad-source}}.
* Erstelle ein anderes Verzeichnis {{incode|freecad-build}}, in dem Du FreeCAD und seine Dokumentation kompilieren wirst.
* Konfiguriere die Quellen mit {{incode|cmake}}, stelle sicher, dass Du das Quellverzeichnis angibst und die erforderlichen Optionen für Dein Build angibst .
* Triggere die Erstellung der Dokumentation mit {{incode|make}}.
</div>
{{Code|code=
git clone https://github.com/FreeCAD/FreeCAD.git freecad-source
mkdir freecad-build
cd freecad-build
cmake -DBUILD_QT5=ON -DPYTHON_EXECUTABLE=/usr/bin/python3 ../freecad-source
}}

Während Du Dich im Build-Verzeichnis befindest, gib die folgende Anweisung aus, um nur die Dokumentation zu erstellen.
{{Code|code=
make -j$(nproc --ignore=2) DevDoc
}}
Wie unter [[Compiling (Speeding up)/de|Kompilieren (Beschleunigen)]] erwähnt, legt die Option {{incode|-j}} die Anzahl der CPU Kerne fest, die für die Kompilierung verwendet werden. Die resultierenden Dokumentationsdateien erscheinen im Verzeichnis
{{Code|code=
freecad-build/doc/SourceDocu/html/
}}

Der Einstiegspunkt in die Dokumentation ist die Datei {{incode|index.html}}, die du mit einem Webbrowser öffnen kannst:
{{Code|code=
xdg-open freecad-build/doc/SourceDocu/html/index.html
}}

Das {{incode|DevDoc}} Ziel erzeugt eine beträchtliche Datenmenge, etwa 5 GB neue Dateien, insbesondere aufgrund der von Graphviz erstellten Diagramme.

=== Gekürzte Dokumentation ===

Die komplette Dokumentation belegt etwa 3 GB Plattenplatz. Eine alternative, kleinere Version der Dokumentation, die nur ca. 600 MB benötigt, kann mit einem anderen Ziel erstellt werden. Dies ist die Version, die auf der [https://freecad.github.io/SourceDoc/ FreeCAD API Webseite] angezeigt wird.
{{Code|code=
make -j$(nproc --ignore=2) WebDoc
}}

The documentation on the [https://freecad.github.io/SourceDoc/ FreeCAD API website] is produced automatically from https://github.com/FreeCAD/SourceDoc . Anyone can rebuild it and submit a pull request:

* Fork the repo at https://github.com/FreeCAD/SourceDoc
* on your machine: clone the FreeCAD code (if you haven't yet), create a build dir for the doc, and clone the above SourceDoc repo inside. That SourceDoc will be updated when you rebuild the doc, and you'll be able to commit & push the results afterwards:
{{Code|code=
git clone https://github.com/FreeCAD/FreeCAD
cd FreeCAD
mkdir build
cd build
mkdir -p doc/SourceDocu/html
cd doc/SourceDocu/html
git clone your-fork-url
cd ../../..
cmake -DBUILD_QT5=ON -DPYTHON_EXECUTABLE=/usr/bin/python3 ..
make WebDoc
cd doc/SourceDocu/html
git commit
git push
}}
* Go to your fork online, and create a pull request.

<div class="mw-translate-fuzzy">
== Andere Versionen ==
[http://free-cad.sf.net/SrcDocu/index.html FreeCAD 0.12] Dokumentation, die in Sourceforge untergebracht ist.
</div>

== Coin3D Dokumentation integrieren ==

Auf Unix Systemen ist es möglich, die Coin3D Quelldokumentation mit der von FreeCAD zu verknüpfen. Dies ermöglicht eine einfachere Navigation und vollständige Vererbungsdiagramme für Coin abgeleitete Klassen.

*Installiere das {{incode|libcoin-doc}}, {{incode|libcoin80-doc}}, oder ein ähnlich benanntes Paket.
*Entpacke das Archiv {{incode|coin.tar.gz}}, das sich in {{incode|/usr/share/doc/libcoin-doc/html}} befindet; die Dateien sind möglicherweise bereits auf deinem System entpackt.
*Erzeuge die Quelldokumentation erneut.

Wenn du das Dokumentationspaket für Coin nicht installierst, werden die Verknüpfungen generiert, um auf die Online Dokumentation unter [https://coin3d.bitbucket.io/Coin/ BitBucket] zuzugreifen. Dies geschieht, wenn eine Doxygen Kennzeichendatei zur Konfigurationszeit mit {{incode|wget}} heruntergeladen werden kann.

== Doxygen Anwenden ==

Auf der Seite [[Doxygen/de|Doxygen]] findest du eine ausführliche Erklärung, wie man C++- und Python Quellcode kommentiert, damit er von Doxygen zur automatischen Erstellung der Dokumentation verarbeitet werden kann.

Im Wesentlichen muss vor jeder Klassen- oder Funktionsdefinition ein Kommentarblock, beginnend mit {{incode|/**}} oder {{incode|///}} für C++ oder {{incode|##}} für Python, erscheinen, damit er von Doxygen aufgenommen wird. Viele [[Doxygen#Doxygen markup/de|Spezielle Befehle]], die mit {{incode|\}} oder {{incode|@}} beginnen, können verwendet werden, um Teile des Codes zu definieren und die Ausgabe zu formatieren. Auch [[Doxygen#Markdown support/de|Markdown Syntax]] wird innerhalb des Kommentarblocks verstanden, was es bequem macht, bestimmte Teile der Dokumentation hervorzuheben.
{{Code|code=
/**
 * Returns the name of the workbench object.
 */
std::string name() const;

/**
 * Set the name to the workbench object.
 */
void setName(const std::string&);

/// remove the added TaskWatcher
void removeTaskWatcher(void);
}}


<div class="mw-translate-fuzzy">
{{Docnav/de
|[[Extra python modules/de|Zusätzliche Python Module]]
|[[List of Commands/de|Liste der Befehle]]
}}
</div>

{{Userdocnavi{{#translation:}}}}
[[Category:Developer Documentation{{#translation:}}]]
{{clear}}
