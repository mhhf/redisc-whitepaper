Formales Modell zur Abbildung demokratischer Prinzipien

#### Idee
	
	eine entscheidene frage ist die verantwortung von Inhalten
	
	wer entscheidet darüber welche inhalte genommen werden
	
	2 extremen - reddit und wikipedia und linux
	
	im internet werden zunehmend inhalte kollaborativ produziert
	dabei entsteht ehtsteht das Produkt durch beiträge einzelner akteure
	
	Eine zentrale Frage dabei ist die bewertung der Inhalte/ Ergebnisse.
	
	BSP: Wikipedia/Reddit
	
	Die Tendenz entwickelt sich zunähmend hin zu demokratischen Prinzipien (voting) 
	
	wikipedia - freiwillige helfer
	
	reddit - sehr grob
	-> granular in bezug auf programmiersprachen
	
	weiter gehen und um alles voten:
	eg.
		seite um ein open source projekt
	
	metasprache
	weite produktion an inhalten
	
	 
`nahezu löschen`
Im verlauf der Zeit haben einzelne Personen, oder Interessensgruppen (**Akteure**) Wege gefunden sich zu Organisieren. Ziel der Organisation ist das geregelte verwalten einer geteilten Ressource. Jeder Akteur versucht sein eigenes Interesse durchzusetzen. 

Dabei gilt eine Organisation als **gerecht**, wenn jeder Akteur auch zu dem Teil über die geteilte Ressource verfügen kann, zu welchem die Ressource ihm auch gehört. Sie gilt als **sicher** wenn einmal getroffenen Vereinbarungen auch eingehalten werden.

`wo kommt die sicherheit her im internet?`

`2 Absätze zusammenmergen`
Ein Beispiel für eine Organisation ist der Staat, in dem politische Partein als Akteure`Menschen` versuchen ihr Interesse durchzusetzen. Dies geschieht durch ein Abstimmungsprozess worurch sich Mehrheiten bilden.

Die Piratenbartei hat durch *"liquid Democraty"* diesen Prozess digital Abgebildet. Jedoch bedarf es bei ihrem Ansatz einers zentralisierten Servers, wecher einen Angrifspunkt bietet und dadurch die sicherheit `des Prozesses / Wahprozesses` der Oranisation gefährdet wird.

Das Konzept eignet sich auch nur bedingt um damit geteiltes Eigentum wie z.B. ein Unternehmen zu modellieren, da der Besitz und somit die mitbestimmung in solchen nicht unter den mitgliedern Gleichverteilt ist. Auch fehlt es an eienr Rechte und Rollenverteilung. 

---

Das 2009 eingeführte Konzept des Bitcoins hat zumindest den Aspekt der sicherheit gelöst, in dem sie die verteilung von Tokens under Akteuren auf eine dezentrale weise modellieren. Der Zugriffsverwaltung ist durch ein Kryptografisches systhem gesichert.

Das Ethereum Team hat die grundlegende Technologie des Bitcoins generalisiert.
Sie haben eine Virtuellen Maschine (vm) mit einer turing vollständigen maschinensprache herrausbringen können.
Diese Erlaubt das sichere ausführen von Berrechnungen in einem dezentralen netzwerk, 
welches nicht nur einen Informationsfluss, 
sondern auch durch die einbindung der lokalen währung Ether, 
einen Wertefluss ermöglicht.

Hierdurch entstehet eine vielzahl von neuen Anwendungsmöglichkeiten, wie Verbindliche, autonome Verträge zwischen mehreren Parteien oder Dezentrale Autonome Organisationen (DAO) und profitorientierte Cooperationen (DAC).

Ein Beispiel einer solchen DAO ist das "namecoin" konzept, welches als alternative zur ICANN Organisation die TLD ".bit" verwaltet. Die Regeln, unter denen DACs und DAOs funktionieren werden durch eine Programmiersprache in die Ethereum VM gespielt und auf dieser ausgeführt.

Jedoch fehlt den beteiligten Aktoren ein formaler Prozess, sich demokratisch auf eben solche Regeln zu einigen unter denen Sie funktionieren werden. 
Der Einigung geschieht noch auf einer vertrauensinstanz. 

Im dieser Arbeit möchte ich ein Modell für eine Programmiersprache auf Basis von Ehtereum entwickeln und analysieren, die den Prozess der demokratischen Einigung mit beinhaltet.
`die demokratische einigung auf ein zustand des codes`

`sprache für verteiltes programmieren`

Das Modell soll mit formaler Logik sowie modelltheoretischen Konzepten beschrieben werden und anschließend auf `machbarkeit und wiederspruchsfreiheit` Analysiert werden. 

Hierzu dient der Prozess des "transitive delegatet voting" aus Liquid Democraty als Basis der Sprache. Diese wird durch das Modell von Eigentum und Delegationsbedinungen erweitert, welches eine Rechte und Rollenverwaltung ermöglicht.

Die Syntax der Programmiersprache wird ein LISP dialekt sein der durch eine "confluent persistente" Datenstruktur die durch einen Gerichteten Graphen eine Versionierung eines Abstrakten Syntaxbaumes darstellt.