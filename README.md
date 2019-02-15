# Bootstrap
KursInfos Bootstrap3 Kurs

Schulung Bootstrap3/Less
Referent Bongers

Tolle Kursdoku auf https://github.com/grisham88

Fragen: 
- Nützliche VS Code Extensions?
- Warum nutzen wir in der DATEV nicht Angular Material für die Oberfläche als 
	alternative zu Bootstrap. Ist gut und modern in Angular integriert (? nicht jQuery)
- rollen in bootstrap; modul, element, rolle?


Less (CSS Präprozessor, Superset von CSS ):
hat
- Variablen
- Funktionen
Grundkonzepte Modulares CSS (SMACSS-Richlinie, oder BEM (von Yandex, Block Element Modifier)
- Module  (hat Klassennamen: z.B. .meinwidget) 
- Elemente (Klassenname hat Modulnamen: z.B. .meinwidget_headline, .meinwidget_content)
- State Modifier (.meinwidget_headline-isvisible)

CSS:
- Selector = <p>, <div> o.Ä.
- Id Selector => #content => im html z.B. <div id="content">
	im CSS (bzw. <style>), #content
	- Id Selector ist kritisch, weil schwer steuerbar, wechselwirkungen leichter möglich
- sensibel, was wann wo wirkt.
	-> möglichst nur Klassen verwenden (dienen dann auch der Rollenzuordnung
- Klassendefinitionen überlagern sich.
	-> class="btn btn-success" 
		es werden zuerst die btn eigenschaften zugewiesen und dann btn-success
		-> die Reihenfolge bestimmt was zählt und kann/sollte verfeinern

		
		
- Benennung nach Tiefe: in CSS auch diese Reihenfplge einhalten.
	-  -> allg. Layout
	- btn 
	- state/modifier/utilities  (.is-aktive; .has-sidebar; .is-disabled; .u-

Schreibweise:
Modul  Element state/modifier/utilities
.meinmodul_button-mystate

Site: lesscss.org

less compiler installieren: npm install i -g less

Nutzung : lessc lessdateiname zielcssdateiname

Extension Easy less -> automatisches Übersetzen

Grundsätzliches: 
- alles CSS geht
- Variablen: @name ; kann überall verwendet werden.
- Funktionen: 
	Farben: lighten, darken, spin (
	
Variablen:
- Mixins (wie komplette CSS Klassen die in anderen Verwendet werden können. auch mit parameter möglich)
- Hierarchien (über Parentselector (&) genau zuordnen)
- Modul
	
CSS wird immer asynchron geladen; JS synchron/blockierend
	
Bootstrp:
- CSS Präpozessor/Framework
- Bootstrap3 in Less geschrieben
- Bootstrap4 in Sess geschrieben

Man sieht (meist) ob eine Website mit Bootstrap gemacht wurde.

CSS-Frameworks: (z.B. Bootstrap, Skeleton, Pure.CSS, PrimeNG, ..., Angular Material ,Foundation ( sehr umfangreich))
- vordefinierte Klassen
- Gestaltungsraster (Grid)
- Verlässlich
- responsive 
- Resets/Normalisierung (z.B. neue Grid cleart, setzt Werte zurück)
- manche haben JS im Bauch

Bootstrap3:
- werden Funktionen aus der bootstrap.js benötigt, muss jquery zu installiert werden.


Bezeichnung:
- mt -> MarginTop
- mb -> marginBottom
- padding ...
- ...
- Es gibt fixed Layoutbreiten mit Sprungpunkten. Randbreite wechselt, damit Content stabiler bleibt. Ab einer bestimmten breite vollflexibel.
	Die Sprungpunkte hängen an den Geräteklassen. (xs, s, md, lg) Für 4K o.Ä. werden diese Werte hochgerechnet.
- Layout Schachtel im Container (responsiv); container-fluid (nutzt komplette device width)
- die classen von Bootstrap sind gut auf getboostrap.com zu finden.

Unterschiede Bootstrap3-> 4;
- z.B. abstände um Elemente 

Grid:
Gridbasis: <container> (bzw. container-fluid)
Gridzeile: <row>
Grid Items (abhäüngig von Geräteklassen): z.B. <col-xs-2> oder <col-md-3>
	xs gilt ab xs weiter, wenn nichts anderes definiert wird.
	- passen die Größen nicht mehr in eine Row, wird umgebrochen.
	- offset in Grideinheiten setzen: z.B. zwei Einheiten in Geräteklasse xs : col-xs-offset-2
	- vershieben im Grit mit push und pull: z.B. zwei Einheiten in Geräteklasse xs nach rechts verschieben: col-xs-push-2
	- sichtbarkeit nach geräteklasse (genau für diese Geräteklasse): z.B.  visible-xs, hidden-md, show-sm, hidden-print
		vererbt sich nicht (( -> außer bei Elementen die bei bestimmten Ausgaben wie print (hidden-print) besser zu nutzen))
		visible-xs-inline bzw. visible-xs-block bzw. visible-inline-block
	
	
allgemein: sichtbarkeit: visible bzw. hidden bzw. show

collapsable - zeigt oder versteckt inhalte (benötigt jquery -> in bootstrap4 einfacher, weil schon integriert)
	steuerung über id des zu collapsenden Element, beim Schalter wird per href #Id angegeben und über 
	data-toggle="collapse" getoggled. Wo kein href zur Verfügung steht (z.B. button) wird das Collapseziel über data-target bestimmt.
dropdownlist - ähnlich  wie collapsable zu bearbeiten. Auch mit jquery, und schalter.
navbar: 
- in container: class="navbar navbar-default" darin sind zwei child-container : header und callapse

spezielles: 
	sr-only -> für Barrierefreiheit ausgabe für Screenreader -> nicht in der Anzeige
	hidden-print -> nicht auf ausdrucken anzeigen.
	
modifizieren von Werten/Elementen: nicht in den Bootstrap sourcen sondern:
	zum nachschauen von variablen kann man in die bootstrap datei variables.less anschauen.

In vsc settings: (so wird immer bei änderungen an less dateien die bootstrap.less verarbeitet)
"less.compile": {
        "out": false,
        "main": "bootstrap.less", 
        "compress": false
    }

wie und wo kann man bootstrap Werte ändern. 
	a) bootstrap - main verwenden/kopieren und originale kopieren bzw datei mitgeänderten werten mit oldname.mod.less benennen und nach dem origingal einhängen.
		Gefährlich, wenn updates von bootstrap kommen.

Bootstrap4:
- flexgrids;
- active class muss bei Navigationen vom listenelement zum ankertag verschoben werden.
- kein extra laden von jquery nötig.
- nicht so weit abwärtskompatibel zu alten browsern (min ie9)

less -> sass:
less source keine gültige sass source -> z.B. andere variablen benennung.

Sonstiges:
NPM:
- npm init; Neustart npm Projekt -> mit anlegen package.json
- wichtig immer mit npm installieren, weil dann die package.json mitaktualisiert wird.
- genutzte Ressource; normal angeben potentiell mit @versionsnummer
- developer Ressource: Testframework, o.ä. -> mit --save-dev
- mit npm versionen eines Moduls feststellen (z.B. für jquery): npm view jquery versions
EMMET:
$ = fortlaufende Nummern

https://github.com/grisham88
