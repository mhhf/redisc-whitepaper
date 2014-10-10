## Formales Modell einer Domänenspezifische Sprache zur verteilten Programmierung mit Mehrheitenbildung

Im Internet werden zunehmend inhalte kollaborativ erzeugt. 
Dabei entsteht ein Ergebnis, durch Beiträge einzelner **Akteure**.
Eine zentrale Frage dabei die Bewertung der einzelnen Beiträge,
und damit ihren Anteil am Gesamtergebnis.
Wikipedia folgt hierbei einem streng hirarchischem Modell, in welchem Vertrauenspersonen die Ihnalte der Benutzer filtern. Die Verantwortung liegt bei der Organisation.
Der Trend geht jedoch zu demokratischen Prinzipien (Voting) wie z.B. bei Reddit[^reddit] oder StackOverflow[^stackoverflow],
bei denen die Benutzer die Inhalte der Anderen bewerten.
Ein solches demokratischens Prinzip könnte man auf das Verwalten aller digitaler geteilter Inhalte veralgemeinern.

Nehmen wir z.B. an, es gibt eine Webseite, die sich im Besitz von n Akteuren befindet. Alle Akteure wollen **gerecht**, also proportional zu ihrem Besitz, über die Ihnalte der Webseite entscheiden können, sowie ihre Entscheidungsgewalt in bestimten Bereichen an andere vertrauenswürdige Akteure delegieren können. Dieses gilt für Mediale Inhalte, sowie für die Programmierung, Architektur und Prozesse, im Zusammenhang mit der Webseite, wie das validiren neuer Beiträge. Das eigendliche Ergebnis wird anhand von einer Mehrheit der Besitzer bestimmt.

Die Piratenbartei hat durch *"liquid Democraty"*[^Lindenberg:2010] einen deligierten Abstimmungsprozess digital Abgebildet. Jedoch bedarf es bei ihrem Ansatz einers zentralisierten Servers, wecher als Angrifspunkt die Sicherheit des Prozesses gefährdet. 

Auch eignet sich das Konzept auch nur bedingt um damit geteiltes Eigentum wie z.B. eine Webseite zu modellieren, da der Besitz und somit die Stimmengewichtung in solchen nicht unter den mitgliedern Gleichverteilt ist. Auch fehlt es an eienr Rechte und Rollenverteilung. 

Das 2009 eingeführte Konzept des Bitcoins[^Nakamoto:2009] hat zumindest den Aspekt der sicherheit gelöst, in dem sie die verteilung von Tokens under Akteuren auf eine dezentrale weise modellieren. Die manipulation der Tokens ist durch ein Identität und ein Kryptografisches systhem **gesichert**.

Das Ethereum Team hat die grundlegende Technologie des Bitcoins generalisiert[^Wood:2014].
Sie haben eine Virtuellen Maschine (vm) mit einer turing vollständigen maschinensprache herrausbringen können.
Diese Erlaubt das sichere ausführen von Berrechnungen in einem dezentralen netzwerk, 
welches nicht nur einen Informationsfluss, 
sondern auch durch die einbindung der lokalen währung Ether, 
einen Wertefluss ermöglicht.

Sicher bedeutet hierbei, dass einmal getroffene Vereinbarungen auch eingehalten werden.

Hierdurch entstehet eine vielzahl von neuen Anwendungsmöglichkeiten, wie Verbindliche, autonome Verträge zwischen mehreren Parteien oder Dezentrale Autonome Organisationen (DAO) und profitorientierte Cooperationen (DAC).

Ein Beispiel einer solchen DAO ist das "namecoin" konzept, welches als alternative zur ICANN Organisation die TLD ".bit" verwaltet und in naher zukunft die ICANN ablösen könnte.[^ICANN:2014] Die Regeln, unter denen DACs und DAOs funktionieren werden durch eine Programmiersprache in die Ethereum VM gespielt und auf dieser ausgeführt.

Jedoch fehlt den beteiligten Aktoren ein formaler Prozess, sich demokratisch auf eben solche Regeln zu einigen unter denen Sie funktionieren werden. 
Der Einigung geschieht noch auf einer vertrauensinstanz, z.b. durch bestimmte Schlüsselpersonen.

Im dieser Arbeit möchte ich ein Modell für eine Meta-Programmiersprache für verteiltes programmieren auf Basis von Ehtereum entwickeln und analysieren. In dieser werden Einigungsprozesse als Bestandteil des Entwicklungsprozesses angesehen.

Das Modell soll mit formaler Logik sowie modelltheoretischen Konzepten beschrieben werden und anschließend auf machbarkeit und wiederspruchsfreiheit Analysiert werden. 

Hierzu dient der Prozess des "transitive delegatet voting" aus Liquid Democraty als eine Grundlage des Wahlprozesses. Diese wird durch das Modell von Eigentum und Delegationsbedinungen erweitert, welches eine Rechte und Rollenverwaltung ermöglicht. Die für die Programmausführung gewählte Option wird dabei durch eine mehrheit der Besitzer bestimmt. 

Die Syntax der Programmiersprache ist ein LISP dialekt, mit dem Paradigma, dass Knoten des Abstrakten Syntaxbaumes als Daten sowie als Code interpretiert werden können. Die Daten befinden sich in einem kryptografisch gesicherten verteilten netzwerk ähnlich der auf BitTorrent aufbauenden IPFS[^IPFS:2014] oder der Maidsafe[^Maidsafe:2014] Architektur.

Grundlegende Aktionen eines Akteurs ist das vorschlagen von Alternativknoten (klassisches Programmieren), sowie das partizipieren an Wahlen über alternativen.


[^reddit]: http://reddit.com
[^stackoverflow]: http://stackoverflow.com

[^Maidsafe:2014]: David Irvine, MaidSafe Distributed File System. http://maidsafe.net/Whitepapers/pdf/MaidSafeDistributedFileSystem.pdf
[^IPFS:2014]: Juan Benet, IPFS - Content Addressed, Versioned, P2P File System. http://static.benet.ai/t/ipfs.pdf

[^Lindenberg:2010]: Friedrich Lindenberg. Konzeption und Erprobung einer Liquid Democracy Plattform anhand von Gruppendiskussionen.  TU Ilmenau, 2010.

[^Nakamoto:2009]: Satoshi Nakamoto, Bitcoin: A peer-to-peer electronic cash system. http://bitcoin.org/bitcoin.pdf

[^Wood:2014]: Gavin Wood, ETHEREUM: A SECURE DECENTRALISED GENERALISED TRANSACTION LEDGER. http://gavwood.com/paper.pdf

[^ICANN:2014]: ICANN, Identifier Technology Innovation Panel - Draft Report. https://www.icann.org/en/system/files/files/report-21feb14-en.pdf
