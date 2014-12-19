Sei $G = (N,T,S,P)$ eine eindeutige contextfreie Grammatik über das Alphabet $\Sigma = (N\cup T)$.

Eine erweiterung auf eine SCFG definieren wir als $S(G) := (N',T',S',P')$, mit:

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


