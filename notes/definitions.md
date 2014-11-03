### Besitz

Seien $a,a'$ **Akteure** und sei A die Menge aller Akteure.


#### shares
Die Funktion $share_a: A \rightarrow \mathbb{N}$ gibt den Teil von a an, der im Besitz von einem Akteur $a'\in A$ ist.

Gilt $share_a(a') > 0$ für $a\neq a'\in A$, so nennt man $a'$ auch ein **Member** von $a$ und man schreibt $a'\in a$

$M_a$ ist die Menge aller Member von $a$.

$\sum_{m\in M_a} share_a(m) = |a|$ gibt die Größe des jeweiligen Akteurs an.

Gilt $share_a(a) = |a|$ so nennt man den Akteur $a$ **frei**.

> Für die vereinfachung werde ich hier auf die Beschreibung von zirkulären akteurzugehörigkeiten erst einmal verzichten.

#### zustand $s\in S$

Ein Zustand wird durch ein abstrakten Syntaxbaum(AST) repräsentiert.

Sei $K$ die Menge aller Knoten.

Ein Knoten heißt **unbestimmt**, wenn mehrere Optionen zur auswahl stehen. Andernfalls heißt der Knoten **bestimmt**.

Ein unbestimmter Knoten ist eine Menge von Optionen mit $o_i \in O \subseteq K\times V_a$

##### BSP.:
> 

#### voting 
Sei $k$ ein Kindknoten eines unbestimmten Knotens.

Akteure können nun ihre Prefferenz für den Knoten angeben

$V_k: M\rightarrow [0..1]$ ist eine Funktion, die für den Knoten $k$ jeden Member eine Preferenz für den Knoten zuordnet.

##### BSP.:
> $V_k$ 


##### Alternative

`constrain space gehört nicht zu alternativen, es ist ein seperater knoten`

Eine alternative ist ein Tupel $(C,O)$

Dabei ist 
* C eine Menge von tupeln der Form $(c,p)$ mit
  * c ist ein Ausdrücken `(vom Typ Bool)`
* O eine Menge von tupeln der Form (e,p) mit
  * e ist ein Ausdruck `s-expressions` eines Beliebigen Typs, welcher wiederum rekursiev knoten beinhalten kann
  * p ist eine Prefferenzmenge für e von a








## TODO











