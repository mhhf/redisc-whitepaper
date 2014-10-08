Formale Entwicklung eines Moells zur Abbildung von demokratischen Prinzipien in Ethereum

### Abstract
Durch das Populärwerden von Blockchain basierter Technologien,
die durch die einführung des Bitcoin Konzeptes um 2009 gestartet wurde,
hat das Ethereum team ein generalisierendes konzept einer dezentralen, durch einen konsensalgorithmus determinierenden, virtuellen maschine (vm) mit einer turing vollständigen maschinensprache herrausbringen können.
Diese Erlaubt das sichere ausführen von Berrechnungen in einem dezentralen netzwerk, 
welches nicht nur einen Informationsfluss, 
sondern auch durch die einbindung der lokalen währung Ether, 
einen Wertefluss ermöglicht.
Hierdurch entstehet eine vielzahl von Anwendungen, wie Verbindliche, autonome Verträge zwischen mehreren Parteien oder Dezentrale Autonome Organisationen (DAO) und profitorientierte Cooperationen (DAC).
Ein Beispiel einer solchen DAO währe das "namecoin" konzept, welches als alternative zur ICANN Organisation die TLD ".bit" verwaltet. Die Regeln, unter denen DACs und DAOs funktionieren werden durch eine Programmiersprache in die Ethereum VM gespielt und auf dieser ausgeführt.

Moderne Programmiersprachen und Entwicklungsprozesse sind jedoch nur bedingt dafür geeignet, solche Organisationen abzubilden, weil den beteiligten Partein ein formaler prozess fehlt, sich demokratisch auf eben solche Regeln zu einigen unter denen Sie funktionieren werden.

Selbst große Open Source projekte besiten meist einen "wohlwollenden Diktator" der die letztendliche Entscheidungsgewallt über die Regeln besitzt.

Im meiner Arbeit möchte ich ein Vorschlag entwickeln und untersuchen, wie eine formale Beschreibung eines (demokratischen) einigungsprozesses Aussehen könnte.

Ziel der Arbeit ist ein Modell einer Programmiersprache, die den Anforderungen eines *sicheren*, *agilen*, *dezentralen* und *demokratischen* entwickeln auf der Ethereum VM genügt.

Das Modell soll mit formaler Logik sowie Modelltheoretischen konzepten beschrieben werden und anschließend gegen die Anforderungen verifiziert werden. 

Hierzu wird der prozess des "transitive delegatet voting" aus liquid Democraty mit formal beschrieben und ein Eigentümermodell, welches eine Rechte und Rollenverwaltung ermöglicht, erweitert.

Für die Programmiersprache wehle ich eine confluent persistente Datenstruktur die durch einen Gerichteten Graphen eine Versionierung verschachtelter s-expressions darstellt.
S-expressions, als ein lisp dialekt, dienen als datenspeicher, sowie als eine turing-vollständige programmiersprache.

Am Schluss werden einige Probleme und Anwendungsbeispiele beschrieben sowie weitere nicht beschriebene Berreiche wie 
Marktbasierte Mehrwertsflusse als zukünftiges vertiefungsgebiet in Aussucht gestellt.