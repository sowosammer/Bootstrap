# Bootstrap
KursInfos Bootstrap3 Kurs

Schulung Bootstrap3/Less
Referent Bongers

Tolle Kursdoku auf https://github.com/grisham88

Fragen: 
- Nützliche VS Code Extensions?
- Warum nutzen wir in der DATEV nicht Angular Material für die Oberfläche als 
	alternative zu Bootstrap. Ist gut und modern in Angular integriert (? nicht jQuery)


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
- Mixins (wie komplette CSS Klassen die in anderen Verwendet werden können.
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




Bootstrap4:
- flexgrids;
- active class muss bei Navigationen vom listenelement zum ankertag verschoben werden.

Sonstiges:
NPM:
- npm init; Neustart npm Projekt -> mit anlegen package.json
- wichtig immer mit npm installieren, weil dann die package.json mitaktualisiert wird.
- genutzte Ressource; normal angeben potentiell mit @versionsnummer
- developer Ressource: Testframework, o.ä. -> mit --save-dev

https://github.com/grisham88
