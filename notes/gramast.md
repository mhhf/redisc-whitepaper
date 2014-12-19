## Einleitung


In dieser Arbeit möchte ich eine Meta-Programmiersprache (**$SCFG$**) für eine beliebige eindeutige kontextfreie Grammatik $G$ herrausarbeiten, die das verteilte Programmieren ermöglichen soll. 
Hierfür werden in (1) zwei Funktion angegeben. Eine erweitert eine gegebene kontextfreie Grammatik zu einer $SCFG$, die andere erzeugt aus einem Wort der Sprache $L(SCFG)$, ein Wort in der ursprünglichen Sprache $L(G)$. Manipulationen eines Wortes einer SCFG-Sprache sind bedingungen unterworfen, die in (2) angegeben sind. 


## 1. Meta - Programmiersprache

### Einleitung

Die Idee hinter der erweiterung der SCFG Sprache ist, dass der Besitz eines Programms eindeutig beteiligten Akteuren zugeordnet ist. Die Zuordnung repräsentiert auch das mitspracherecht der Akteure. Manipulationen am Programm können jederzeit vorgenommen werden, diese werden als Option gespeichert.

Eine Konsensfunktion bestimmt dann eine Option, welche das Programm wieder eindeutig macht. Optionsmengen, können an jeder Stelle gebildet werden, solange die neue Option auch ein gültiges Wort in $L(G)$ ergibt. Um den Konsensprozess effizienter zu gestalten, können Akteure ihre Stimme für bestimmte Bereiche der Sprache an andere Akteure Delegieren.

### Intuition

Eine **Optionsmenge**, oder Kurz eine **Option**, können wir als eine Menge von Kandidaten modellieren, von denen jeder ein Gültiger Kandidat für eine Spezifikation ist. 
Ist eine **Option** im Besitz mehrerer **Akteure**, so müssen die Akteure einen Weg finden über die Option zu entscheiden. Dies bedeutet durch einen Konsensprozess sich auf einen kandidaten Einigen.


```
Optionsmengen können als Mengen von Aussagen angesehen werden. Eine Ableitung durch eine Konsesnfunktion vielleicht durch eine Logische Ableitung einer Akteurgruppe.

Vielleicht ist das Konzept, welches ich Modelliere eine contextsensitive Sprache, da Optionen nur im Kontext ihre gültigkeit besitzen.

was ist mit der 'löschungs' Regel, sie ist nicht Teil der Kontextsensitiven Grammatik


```

### 1.1 erweiterung einer CFG zu einer SCFG

Sei $G = (N,T,S,P)$ eine eindeutige contextfreie Grammatik.

Eine Erweiterung auf eine SCFG definieren wir als $S(G) := (N',T',S',P')$, mit:

$N' := N \cup \{O,D,A\}\ mit\ O,D,A\notin N$

$T' := T \cup \{[ , ], \oplus, number, float, hash \}\ mit\ [,],\oplus \notin T$

**number** stellt eine ganzzahlige Nummer dar.
**float** stellt eine fließkommazahl dar.
**hash** ist ein identifikatior für einen akteur, hier ein 64 bit hex string.

$P' := P\cup P_{Options} \cup P_{Start} \cup P_{Delegations} \cup P_{Voting} \cup P_{Acteurs}$

$P_{Options} := \{R \rightarrow [O][D], O \rightarrow r\oplus [V] O |R\rightarrow r\in P$ mit $r\in\Sigma^*\}\cup\{ O \rightarrow \varepsilon \}$

$P_{Start} := \{S'\rightarrow [A]S\}$

$P_{Delegations} := \{D\rightarrow [hash\ hash];D,D\rightarrow [hash\ hash]\}$

$P_{Voting} := \{V\rightarrow [hash\ float]V, V \rightarrow \varepsilon\}$

$P_{Acteurs} := \{A\rightarrow[hash\ number]A,A\rightarrow \varepsilon\}$

#### zu zeigen

* eindeutigkeit der SCFG


### 1.2 erzeugung eines Wortes der Ursprungsgrammatik aus einem Wort der SCFG

Die Idee hier ist, dass die transitive Hülle der Delegationen als Attribut während der Ableitung vererbt(inherited) wird. Die Votemenge wird hingegen als Attribut synthetisiert. Die Delegationen zusammen mit den Stimmen quantifizieren jede Option aus einer Optionsmenge und wählen eine Konsens-Option. 


#### zu untersuchen
* zirkuläre delegationen
* implekation von Arrow's Theorem auf strategisches voten


## 2. Manipulation der Wörder einer SCFG-Sprache

Die Idee hier ist, dass Optionen nur hinzu kommen, jedoch nicht gelöscht werden können. Jeder Akteur kann Delegationen und Stimmen abgeben sowie die eigenen löschen, hat jedoch keine Macht über die Stimmen und Delegationen der Anderen. 

Die Manipulation wird durch eine **Abstract State Maschine** beschrieben.

Sei $G = (N,T,S,P)$ eine eindeutige Grammatik sowie $G'=S(G)=(N',T',S',P')$ die dazugehörige SCFG.

### States
Ein Zustand der ASM ist eine Struktur der form $(U, compile, w)$

U ist das Universum der Struktur und wird definiert durch:
$$U=\{w|S'\rightarrow_p^* w \land w\in T'^*\}$$

$compile$ ist die in (1.2) definierte Funktion der Form: $compile: L(G') \rightarrow L(G)$

$w\in U$ ist das derzeitige Wort


### Transitionen
Bei der Interaktion eines Programms, ist der Akteur bekannt und wird durch ein Public Key ausgewiesen. Der Akteur kann in einem Interaktionsschritt das derzeitige Wort altuallisieren, wenn es bestimmte Bedingungen erfüllt. Eine Interaktion ist also ein Tupel $(h,w')$ so, dass $h$ der Public Key des Akteurs ist, sowie $w'$ das neue Wort.

Die Transitionen können zu den Auslösenden Akteuren ebenfalls durch eine Kontextuelle Grammatik beschrieben werden.

#### Erzeugen einer Optionsmenge

Sei $\alpha,\beta,o_1,o_2 \in T'^*$ sowie $R\in N$ und $V \rightarrow_P^* v$
Sei $w=\alpha o_1 \beta \oplus [v]$
Sei weiter $R\rightarrow_p^* o_1$ sowie $R\rightarrow_p^* o_2$
Dann ist $w:=\alpha [o_1\oplus [v] o_2\oplus []][]\beta$ eine valide Transition.

#### Erweitern einer Optionsmenge

Sei $w=\alpha[o]\beta \land S'\rightarrow_P^* \alpha R \beta$ mit $O\rightarrow_P^* o, o\in T'^*, R\in N$
Dann ist $w:=\alpha[o r\oplus []]\beta$ mit $R \rightarrow_P^* r, r\in T'^*$ eine valide Transition.

#### Hinzufügen einer Stimme

Sei $w=\alpha r\oplus [v]\beta$ 

Dann ist $w:=\alpha r \oplus [v[h n]]\beta$ mit $n=float$ eine valide Transition.

#### Löschen einer Stimme
Sei $w=\alpha [hn]\beta$ 

Dann ist $w:=\alpha\beta$ mit eine valide Transition.

#### Hinzufügen einer Delegation
#### Löschen einer Delegation


### zu untersuchen
* wie werden neue anteile vergeben




