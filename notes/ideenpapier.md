## Formales Modell einer Domänenspezifische Sprache zur verteilten Programmierung mit Mehrheitenbildung

Im Internet werden zunehmend inhalte kollaborativ erzeugt. 
Dabei entsteht ein Ergebnis, durch Beiträge einzelner **Akteure**.
Eine zentrale Frage ist die Bewertung der einzelnen Beiträge,
und damit ihren Anteil am Gesamtergebnis.

Wikipedia folgt einem streng hierarchischem Modell, in welchem Vertrauenspersonen die Ihnalte der Benutzer filtern. Die Verantwortung liegt bei der Organisation.
Effizienter sind jedoch selbstregulierende Systheme, bei denen die Benutzer die Inhalte der Anderen bewerten. Beispiele währen die auf *voting* und *reputation* basierende Plattformen Reddit[^reddit] und StackOverflow[^stackoverflow].

Ein solches Prinzip könnte man auf das Verwalten aller digital geteilter Inhalte veralgemeinern.

Nehmen wir z.B. an, es gibt eine Webseite, die sich im Besitz von Akteuren befindet. Alle Akteure wollen **gerecht**, also proportional zu ihrem Besitz, über die Inhalte der Webseite entscheiden können, sowie ihre Entscheidungsgewalt in bestimmten Bereichen an andere vertrauenswürdige Akteure delegieren können. Dieses gilt für Mediale Inhalte, für die Programmierung, Architektur, Werteflüsse wie ein Geteiltes Budget oder eine Einkommensverteilung sowie nicht automatisierbare Prozesse, wie das valiediren neuer Beiträge. Das eigendliche Ergebnis wird anhand von einer Mehrheit der Besitzer bestimmt.

Die Piratenpartei hat mit *Liquid Democracy*[^Lindenberg:2010] einen deligierten Abstimmungsprozess digital abgebildet. Jedoch bedarf es bei ihrem Ansatz eines zentralisierten Servers, welcher als Angrifspunkt die Sicherheit des Prozesses gefährdet. 

Auch eignet sich das Konzept nur bedingt um damit geteiltes Eigentum wie z.B. eine Webseite zu modellieren, da der Besitz und somit die Stimmengewichtung in solchen nicht unter den Mitgliedern gleichverteilt ist. Auch fehlt es an eienr Rechte- und Rollenverteilung. 

Das 2009 eingeführte Konzept des Bitcoins[^Nakamoto:2009] hat zumindest den Aspekt der Sicherheit gelöst, in dem sie die Verteilung von Tokens unter Akteuren auf eine dezentrale Weise modellieren. Die Manipulation der Tokens ist durch eine Identität und ein Kryptografisches systhem **gesichert**.

Sicher bedeutet hierbei, dass einmal getroffene Vereinbarungen auch eingehalten werden.

Das Ethereum Team hat die grundlegende Technologie des Bitcoins generalisiert[^Wood:2014].
Sie haben eine Virtuellen Maschine mit einer turing vollständigen Maschinensprache herausbringen können.
Diese Erlaubt das *sichere* Ausführen von Berechnungen in einem dezentralen Netzwerk, 
welches nicht nur einen Informationsfluss, 
sondern auch durch die Einbindung der lokalen Währung Ether, 
einen Wertefluss ermöglicht.

Es entstehet eine Vielzahl von neuen Anwendungsmöglichkeiten: verbindliche, autonome Verträge zwischen mehreren Parteien, Dezentrale Autonome Organisationen (DAO) oder profitorientierte Kooperationen (DAC).

Ein Beispiel einer solchen DAO ist das *namecoin* Konzept, welches als Alternative zur ICANN Organisation die TLD ".bit" verwaltet und in naher zukunft die ICANN ablösen könnte.[^ICANN:2014] Die Regeln unter denen DACs und DAOs funktionieren, wie das Bewilligen einer neuen TLD, werden auf der Ethereum VM programmiert.
Die Einigung der Akteure auf ein Programmstand geschieht noch durch eine Vertrauensinstanz, z.b. bestimmte Schlüsselpersonen.

*In dieser Arbeit möchte ich ein Modell für eine Meta-Programmiersprache für verteiltes Programmieren auf Basis von Ehtereum entwickeln und untersuchen. In dieser werden Einigungsprozesse als Bestandteil des Entwicklungsprozesses angesehen.*

Grundlegende Aktionen eines Akteurs ist das Vorschlagen von Alternativknoten (klassisches Programmieren), sowie das Partizipieren an Wahlen über Alternativen.

Das Modell soll mit formaler Logik sowie modelltheoretischen Konzepten beschrieben werden und anschließend auf Machbarkeit und Wiederspruchsfreiheit untersucht werden. 

Der Prozess des "transitive delegatet voting" aus Liquid Democraty dient als Grundlage des Wahlprozesses. Diese wird durch das Modell von Eigentum und Delegationsbedinungen erweitert, welches eine Rechte- und Rollenverwaltung ermöglicht. Eine Mehrheit der Besitzer bestimmt dabei die für die Programmausführung gewählte Optionen.

Die Syntax der Programmiersprache ist ein LISP Dialekt, mit dem Paradigma, dass Knoten des Abstrakten Syntaxbaumes als Daten sowie als Code interpretiert werden können. Die Daten befinden sich teilweise in einem kryptografisch gesicherten verteilten Netzwerk ähnlich der auf BitTorrent aufbauenden IPFS[^IPFS:2014] oder der Maidsafe[^Maidsafe:2014] Architektur und teilweise in dem Ethereum Speicher.

Diese Sprache soll das oben beschriebene Problem der *gerechten* und *sicheren* verwaltung der geteilten Webseite lösen.


[^reddit]: http://reddit.com
[^stackoverflow]: http://stackoverflow.com

[^Maidsafe:2014]: David Irvine, MaidSafe Distributed File System. http://maidsafe.net/Whitepapers/pdf/MaidSafeDistributedFileSystem.pdf
[^IPFS:2014]: Juan Benet, IPFS - Content Addressed, Versioned, P2P File System. http://static.benet.ai/t/ipfs.pdf

[^Lindenberg:2010]: Friedrich Lindenberg. Konzeption und Erprobung einer Liquid Democracy Plattform anhand von Gruppendiskussionen.  TU Ilmenau, 2010.

[^Nakamoto:2009]: Satoshi Nakamoto, Bitcoin: A peer-to-peer electronic cash system. http://bitcoin.org/bitcoin.pdf

[^Wood:2014]: Gavin Wood, ETHEREUM: A SECURE DECENTRALISED GENERALISED TRANSACTION LEDGER. http://gavwood.com/paper.pdf

[^ICANN:2014]: ICANN, Identifier Technology Innovation Panel - Draft Report. https://www.icann.org/en/system/files/files/report-21feb14-en.pdf
