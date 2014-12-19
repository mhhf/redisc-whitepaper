bibtex:         library.bib

## Strukturen


### Gloede2006
* Mittelpunkt der modernen Mathematik
* Struktur S ist ein 4-Tupel: $(A,R_i^S,f_j^S,c_k^S)$
    * $A \neq \emptyset$ ist der **Individuenbereich** (**Grundbereich**,**Träger**) der Struktur S
    * $R_i^S \subseteq A^{n_i}$ ist eine $n_i$-stellige **Relation** auf A
    * $f_j^S: A^{m_j} \rightarrow A$ ist eine $m_j$-stellige **Funktion** auf A
    * $c_k^S \in A$ ist ein **Element** (eine **Konstante** ) von A
* *die Anzahl* der Relationen, Funktionen und Konstanten, sowie die Stellenzahlen werden in der **Signatur** (**Typ**) festgelet: im Tripel $((n_i),(m_j),K)$

BSP.: Die geordnete Gruppe $(\mathbb{Z},<,+,0)$ ist eine Struktur mit der Signatur ((2),(2),{0})


### Wisnewski2003

* Funktions-, Relations-, Konstanten- und Variablensymbolen sowie Termen und Ausdrücken wird durch mathematische Strukturen eine Bedeutung gegeben.
* S-Struktur ist ein Paar (A,a)
    * A ist eine Menge
    * $R_n$ sind n-stellige Relationssymbole
    * $F_n$ sind n-stellige Funktionssymbole
    * $K$ sind Konstantensymbole
    * $K_n\cap F_n \cap K = \emptyset$
    * a ist eine Abbildung mit Definitionsbereich $S := \bigcup_n R_n \cup \bigcup_n F_n \cup K$,
        * $f\in F_n \Rightarrow a(f): A^n\rightarrow A$
        * $R\in R_n \Rightarrow a(R)\subseteq A^n$
        * $c\in K \Rightarrow a(c) \in A$
        

### Reisig

* a structure $S = (U, f_i, ..., f_k)$ is consisting of 
    * a set U, the universe of S
    * finitely many constants
    * finitely many functions over U, shaped $f: U^n \rightarrow U$, n is the arity of f
    * Constants can be conceived as degenerated functions, with arity zero.
    * With $n_i$ the arity of the constant of function $f_i$, the arity tuple $(n_1,...,n_k)$ is the type of S.
    * A signature $\Sigma$ with symbols $f_1, ..., f_l$ is usually written $\Sigma = (f_1,...,f_l,a_1,...,a_l)$
    

### Glausch2003
* **Signatur** $\Sigma$ ist ein Tupel $(f_1,...,f_k,n_1,...,n_k)$
    * $f_i$ sind **Funktionssymbole**
    * $n_i$ ist die Stelligkeit des Funktionssymbol $f_i$
* **$\Sigma$-Algebra** Algebra $\mathfrak{A}$ über der Signatur $\Sigma$ ist ein Tupel $(U,g_1,...,g_k)$
    * ist eine semantische Interpretation einer Signatur $\Sigma$
    * $U$ eine nichtleere Menge (Universum)
    * $g_i$ ist eine $n_i$ stellige Funktion mit Werte- und Bildbereich in U
        * $g_i$ wird auch mit $[\![f_i]\!]_\mathfrak{A}$  der **Interpretation** von $f_i$ durch die Algebra $\mathfrak{A}$ bezeichnet
