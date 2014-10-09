Formales Modell zur verteilten programmierung mit demokratischer Prinzipien

#### Idee

Im Internet werden zunehmend inhalte kollaborativ erzeugt. 
Dabei entsteht ein Produkt, durch Beiträge einzelner **Akteure**.
Eine zentrale Frage dabei die Bewertung der einzelnen Beiträge,
und damit ihren Anteil am Gesamtergebniss, sowie die Verantwortung des Ergebnisses.
Wikipedia folgt hierbei einem streng hirarchischem Modell worin Vertrauenspersonen
die Ihnalte der Benutzer filtern. Die Verantwortung liegt bei der Organisation.
Der Trend geht jedoch zu demokratischen Prinzipien (Voting) wie z.B. bei Reddit oder StackOverflow,
wobei die Benutzer Inhalte Beitragen und die Inhalte der Anderen filtern.
Ein solches demokratischens Prinzip könnte man auch auf das Verwalten aller digitaler geteilter Inhalte veralgemeinern.

Nehmen wir o.B.d.A. an, es gibt eine Webseite, die sich im Besitz von n Akteuren befindet. Alle Akteure wollen **gerecht**, also proportional zu ihrem Besitz, über die Ihnalte der Webseite entscheiden können, sowie ihre Entscheidungsgewalt in bestimten Berreichen an andere Akteure delegieren können. Dieses gilt für Mediale Inhalte, sowie für die Programmierung, Architektur und Prozesse, im Zusammenhang mit der Webseite, wie das validiren neuer Beiträge.

Die Piratenbartei hat durch *"liquid Democraty"* einen deligierten Abstimmungsprozess digital Abgebildet. Jedoch bedarf es bei ihrem Ansatz einers zentralisierten Servers, wecher als Angrifspunkt die Sicherheit des Prozesses gefährdet.

Auch eignet sich das Konzept auch nur bedingt um damit geteiltes Eigentum wie z.B. ein Unternehmen zu modellieren, da der Besitz und somit die mitbestimmung in solchen nicht unter den mitgliedern Gleichverteilt ist. Auch fehlt es an eienr Rechte und Rollenverteilung. 

Das 2009 eingeführte Konzept des Bitcoins hat zumindest den Aspekt der sicherheit gelöst, in dem sie die verteilung von Tokens under Akteuren auf eine dezentrale weise modellieren. Die manipulation der Tokens ist durch ein Kryptografisches systhem gesichert.

Das Ethereum Team hat die grundlegende Technologie des Bitcoins generalisiert.
Sie haben eine Virtuellen Maschine (vm) mit einer turing vollständigen maschinensprache herrausbringen können.
Diese Erlaubt das sichere ausführen von Berrechnungen in einem dezentralen netzwerk, 
welches nicht nur einen Informationsfluss, 
sondern auch durch die einbindung der lokalen währung Ether, 
einen Wertefluss ermöglicht.

Hierdurch entstehet eine vielzahl von neuen Anwendungsmöglichkeiten, wie Verbindliche, autonome Verträge zwischen mehreren Parteien oder Dezentrale Autonome Organisationen (DAO) und profitorientierte Cooperationen (DAC).

Ein Beispiel einer solchen DAO ist das "namecoin" konzept, welches als alternative zur ICANN Organisation die TLD ".bit" verwaltet. Die Regeln, unter denen DACs und DAOs funktionieren werden durch eine Programmiersprache in die Ethereum VM gespielt und auf dieser ausgeführt.

Jedoch fehlt den beteiligten Aktoren ein formaler Prozess, sich demokratisch auf eben solche Regeln zu einigen unter denen Sie funktionieren werden. 
Der Einigung geschieht noch auf einer vertrauensinstanz, z.b. durch bestimmte Schlüsselpersonen.

Im dieser Arbeit möchte ich ein Modell für eine Meta-Programmiersprache für verteiltes programmieren auf Basis von Ehtereum entwickeln und analysieren. In dieser werden demokratische Einigungsprozesse als Bestandteil des Entwicklungsprozesses angesehen.

```
Dabei wird das LISP Paradigma, das Information als Daten sowie als Code interpretiert werden können, verwendet. Ein Programm wird dabei als Baumstruktur repräsentiert, bei dem zu jedem Knoten alternativen vorgeschlagen werden können. Der tatsächlich gewählte Option wird dabei durch eine mehrheit der Besitzer bestimmt, wodurch sich eine Einigung auf ein Stand des Programms ergibt. 
```

Das Modell soll mit formaler Logik sowie modelltheoretischen Konzepten beschrieben werden und anschließend auf `machbarkeit und wiederspruchsfreiheit` Analysiert werden. 

Hierzu dient der Prozess des "transitive delegatet voting" aus Liquid Democraty als Basis der Sprache. Diese wird durch das Modell von Eigentum und Delegationsbedinungen erweitert, welches eine Rechte und Rollenverwaltung ermöglicht.

Die Syntax der Programmiersprache wird ein LISP dialekt sein der durch eine "confluent persistente" Datenstruktur die durch einen Gerichteten Graphen eine Versionierung eines Abstrakten Syntaxbaumes darstellt.