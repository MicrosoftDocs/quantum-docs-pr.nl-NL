---
Titel: vectoren en matrices in Quantum Computing Description: Leer de basis beginselen van het werken met vectoren en matrices.
Auteur: QuantumWriter UID: micro soft. Quantum. concepten. vectoren MS. Author: v-benbra MS. date: 12/11/2017 MS. topic: artikel no-loc:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "\cdots"
- "bmatrix"
- "\ddots"
- "\equiv"
- "\sum"
- "\begin"
- "\end"
- "\sqrt"
- "\otimes"
- "{"
- "}"
- "\text"
- "\phi"
- "\kappa"
- "\psi"
- "\alpha"
- "\beta"
- "\gamma"
- "\delta"
- "\omega"
- "\bra"
- "\ket"
- "\boldone"
- "\\\\"
- "\\"
- "="
- "\frac"
- "\text"
- "\mapsto"
- "\dagger"
- "\to"
- "\begin{cases}"
- "\end{cases}"
- "\operatorname"
- "\braket"
- "\id"
- "\expect"
- "\defeq"
- "\variance"
- "\dd"
- "&"
- "\begin{align}"
- "\end{align}"
- "\Lambda"
- "\lambda"
- "\Omega"
- "\mathrm"
- "\left"
- "\right"
- "\qquad"
- "\times"
- "\big"
- "\langle"
- "\rangle"
- "\bigg"
- "\Big"
- "|"
- "\mathbb"
- "\vec"
- "\in"
- "\texttt"
- "\ne"
- "<"
- ">"
- "\leq"
- "\geq"
- "~~"
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- "\_"

---

# <a name="vectors-and-matrices"></a>Vectoren en matrices

Enige kennis met vectoren en matrices is essentieel voor het begrijpen van Quantum Computing. Hieronder vindt u een korte inleiding en geïnteresseerde lezers worden aanbevolen om een standaard referentie te lezen op lineaire algebra zoals *Strang, G. (1993). Inleiding tot lineaire algebra (vol. 3). Wellesley, MA: Wellesley-Cambridge Press* of een online verwijzing zoals [lineair algebra](http://joshua.smcvt.edu/linearalgebra/).

Een kolom vector (of alleen [*Vector*](https://en.wikipedia.org/wiki/Vector_(mathematics_and_physics))) $ v $ van dimensie (of grootte) $ n $ is een verzameling van $ n $ complexe getallen $ (v_1, v_2, \ldots, v_n), $ gerangschikt als een kolom:

$$v =\begin{bmatrix}
v_1\\\\
v_2\\\\
\vdots\\\\
v_n \end{bmatrix}$$

De norm van een vector $ v $ is gedefinieerd als $ \sqrt { \sum \_ i | v \_ i | ^ 2 } $ . Een vector is bedoeld als eenheids norm (of ook wel een [*eenheids vector*](https://en.wikipedia.org/wiki/Unit_vector)genoemd) als de norm $ 1 is $ . De [*adjoint van een vector*](https://en.wikipedia.org/wiki/Adjoint_matrix) $ v $ wordt aangegeven $ als v ^ \dagger $ en is gedefinieerd als de volgende rij Vector $ \* $ , waarbij de complex geconjugeerde is aangegeven,

$$\begin{bmatrix}v_1 \\\\ \vdots \\\\ v_n \end{bmatrix} ^ \dagger = \begin{bmatrix} v_1 ^ * & \cdots & v_n ^ *\end{bmatrix}$$

De meest voorkomende manier om twee vectoren samen te vermenigvuldigen is via het [*binnenste product*](https://en.wikipedia.org/wiki/Inner_product_space), ook wel een punt product genoemd.  Het binnenste product geeft de projectie van één vector op een andere en is inwaardevol bij het beschrijven hoe u een vector kunt uitdrukken als een som van andere eenvoudiger vectoren.  Het binnenste product tussen $ u $ en $ v, het $ teken $ \left \langle u, v \right \rangle $ is gedefinieerd als

$$
\langleu, v \rangle = u ^ \dagger v = u \_ 1 ^ { \* } v_1 + \cdots + u \_ n ^ { \* } v \_ n.
$$

Deze notatie zorgt er ook voor dat de norm van een vector $ v $ als $ \sqrt { \langle v, v \rangle } $ wordt geschreven.

We kunnen een vector met een getal c vermenigvuldigen $ $ om een nieuwe vector te vormen waarvan de items door c worden vermenigvuldigd $ $ . We kunnen ook twee vectoren $ u $ en v $ toevoegen $ om een nieuwe vector te vormen waarvan de gegevens de som van de vermeldingen van $ u $ en v zijn $ $ . Deze bewerkingen worden hieronder weer gegeven:

$$\mathrm{Als } ~ u=\begin{bmatrix}
u_1\\\\
u_2\\\\
\vdots\\\\
u_n \end{bmatrix} ~ \mathrm { en}~
verticale =\begin{bmatrix}
    v_1\\\\
    v_2\\\\
    \vdots\\\\
    v_n \end{bmatrix} en ~ \mathrm { vervolgens}~
au + BV =\begin{bmatrix}
au_1 + bv_1\\\\
au_2 + bv_2\\\\
\vdots\\\\
au_n + bv_n \end{bmatrix} .
$$

Een [*matrix*](https://en.wikipedia.org/wiki/Matrix_(mathematics)) met een grootte van $ m \times n $ is een verzameling van $ MN $ complexe getallen die zijn gerangschikt in $ m $ rijen en $ n $ kolommen, zoals hieronder wordt weer gegeven:

$$M = 
\begin{bmatrix}
M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\
M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\
\ddots\\\\
M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { mn}\\\\
\end{bmatrix}.$$

Houd er rekening mee dat een vector van dimensie $ n $ slechts een matrix met de grootte $ n \times 1 is $ . Net als bij vectoren kunnen we een matrix met een nummer c vermenigvuldigen $ $ om een nieuwe matrix te verkrijgen waarin elk item wordt vermenigvuldigd met $ c $ . Daarnaast kunnen we twee matrices van dezelfde grootte toevoegen om een nieuwe matrix te maken waarvan de gegevens de som van de respectieve vermeldingen van de twee matrices zijn. 

## <a name="matrix-multiplication-and-tensor-products"></a>Matrix vermenigvuldiging en tensor-producten

We kunnen ook twee matrices $ $ van dimensie $ m \times n $ en $ n $ van dimensie $ n p vermenigvuldigen \times $ om een nieuwe matrix $ p $ van Dimension $ m p te \times krijgen $ :

\begin{align}
&\begin{bmatrix}
    M_ { 11 } ~~ M_ { 12 } ~~ \cdots ~~ M_ { 1N}\\\\
    M_ { 21 } ~~ M_ { 22 } ~~ \cdots ~~ M_ { 2n}\\\\
    \ddots\\\\
    M_ { M1 } ~~ M_ { m2 } ~~ \cdots ~~ M_ { mn}
\end{bmatrix}
\begin{bmatrix}
N_ { 11 } ~~ N_ { 12 } ~~ \cdots ~~ N_ { 1p}\\\\
N_ { 21 } ~~ N_ { 22 } ~~ \cdots ~~ N_ { 2p}\\\\
\ddots\\\\
N_ { N1 } ~~ N_ { N2 } ~~ \cdots ~~ N_ { NP}
\end{bmatrix}=\begin{bmatrix}
P_ { 11 } ~~ P_ { 12 } ~~ \cdots ~~ P_ { 1p}\\\\
P_ { 21 } ~~ P_ { 22 } ~~ \cdots ~~ P_ { 2p}\\\\
\ddots\\\\
P_ { M1 } ~~ P_ { m2 } ~~ \cdots ~~ P_ { MP}
\end{bmatrix}
\end{align}

waarbij de items $ P $ $ P_ ik heb { } = \sum _j M_ { ij } N_ { JK } $ . De vermelding $ P_ { 11 } $ is bijvoorbeeld het binnenste product van de eerste rij van $ M $ met de eerste kolom van $ N $ . Houd er rekening mee dat omdat een vector gewoon een speciaal geval van een matrix is, de definitie wordt uitgebreid naar matrix-vector vermenigvuldigen. 

Alle matrices die we overwegen, zijn vier Kante matrices, waarbij het aantal rijen en kolommen gelijk is, of vectoren, die overeenkomen met slechts $ één $ kolom. Een speciale vier Kante matrix is de [*identiteits matrix*](https://en.wikipedia.org/wiki/Identity_matrix), aangeduid met $ \boldone $ alle diagonale elementen gelijk aan $ 1 $ en de resterende elementen gelijk aan $ 0 $ :

$$\boldone=\begin{bmatrix}
1 ~~ 0 ~~ \cdots ~~ 0\\\\
0 ~~ 1 ~~ \cdots ~~ 0\\\\
~~ \ddots\\\\
0 ~~ 0 ~~ \cdots ~~ 1 \end{bmatrix} .$$

Voor een vier Kante matrix $ $ wordt gedicteerd dat een matrix $ B $ de [*inverse*](https://en.wikipedia.org/wiki/Invertible_matrix) is die is omgekeerd als $ AB = BA = \boldone $ . De inverse van een matrix hoeft niet te bestaan, maar wanneer deze bestaat, is deze uniek en wordt het $ een ^ { -1 } $ . 

Voor elke matrix $ M $ is de adjoint of de geconjugeerde van $ M $ een matrix $ N $ zodanig dat $ N_ { ij } = M_ { Ji } ^ \* $ . De adjoint van $ m $ wordt doorgaans aangeduid met $ m ^ \dagger $ . U zegt dat een $ matrix $ U [*unitary*](https://en.wikipedia.org/wiki/Unitary_matrix) als $ uu ^ \dagger = u ^ \dagger u = \boldone $ of een vergelijk bare, $ ^ { -1 } = U ^ \dagger $ .  Misschien is de belangrijkste eigenschap van unitary-matrices dat ze de norm van een vector behouden.  Dit gebeurt omdat 

$$\langlev, v \rangle = v ^ \dagger v = v ^ \dagger u ^ { -1 } u v = v ^ \dagger u ^ \dagger u d = \langle u v, u v \rangle .$$  

Een matrix $ M $ wordt [*Hermitian*](https://en.wikipedia.org/wiki/Hermitian_matrix) als $ m = m ^ \dagger $ .

Ten slotte is het [*tensor-product*](https://en.wikipedia.org/wiki/Tensor_product) (of het Kronecker-product) van twee matrices met $ $ een grootte van $ m \times n $ en $ n $ van grootte $ p \times q $ een grotere matrix $ p = M \otimes n $ van grootte $ MP \times NQ $ , en wordt $ als volgt opgehaald van M $ en $ n $ :

\begin{align}
    M \otimes N &=
    \begin{bmatrix}
        M_ { 11 } ~~ \cdots ~~ M_ { 1N }\\\\
        \ddots\\\\
        M_ { M1 } ~~ \cdots ~~ M_ { mn  }
    \end{bmatrix}
    \otimes
    \begin{bmatrix}
        N_ { 11 } ~~ \cdots ~~ N_ { 1k  }\\\\
        \ddots\\\\
        N_ { P1 } ~~ \cdots ~~ N_ { pq}
    \end{bmatrix}\\\\
    &=
    \begin{bmatrix}
        M_ { 11 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1k } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { 1N } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1k } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}\\\\
        \ddots\\\\
        M_ { M1 } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1k } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq } \end{bmatrix} ~~ \cdots  ~~ 
        M_ { MN } \begin{bmatrix} N_ { 11 } ~~ \cdots ~~ N_ { 1k } \\\\ \ddots \\\\ N_ { P1 } ~~ \cdots ~~ N_ { pq }  \end{bmatrix}
    \end{bmatrix}.
\end{align}

Dit is beter te demonstreren met enkele voor beelden:

$$
    \begin{bmatrix}
        a \\\\ b \end{bmatrix} \otimes \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}=
    \begin{bmatrix}
        een \begin{bmatrix} c \\\\ d \\\\ e \end{bmatrix}
        \\\\[1.5 em] b \begin{bmatrix} c \\\\ d \\\\ e\end{bmatrix}
    \end{bmatrix}
    =\begin{bmatrix}a a c \\\\ a d \\\\ a e \\\\ b c \\\\ b d \\\\\end{bmatrix}
$$

en

$$
    \begin{bmatrix}
        a \ b \\\\ c \ d \end{bmatrix}
    \otimes 
    \begin{bmatrix}
        e \ f \\\\ g \ h \end{bmatrix}
     =
    \begin{bmatrix}
    één\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    b\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    \\\\[1em] c\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    !\begin{bmatrix}
    e \ f \\\\ g \ h \end{bmatrix}
    \end{bmatrix}
    =
    \begin{bmatrix}
    AE \ af \ BF \\\\
    AG \ ah \ BG \ BH \\\\
    CE \ CF \ de \ DF \\\\
    CG \ CH \ DG \ DH \end{bmatrix} .
$$

Een laatste nuttige notatie Conventie rondom tensor-producten is dat, voor vector $ v $ of matrix $ M $ , $ v ^ { \otimes n } $ of $ M ^ { \otimes n } $ korte hand voor een $ $ herhaald tensor-product.  Bijvoorbeeld:

\begin{align}
&\begin{bmatrix}1 \\\\ 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ 0 \end{bmatrix} ^ { \otimes 2 } = \begin{bmatrix} 1 \\\\ 0 \\\\ 0 \\\\ \end{bmatrix} , \qquad \begin{bmatrix} 1 \\\\ -1 \end{bmatrix} ^ { \otimes 2 1-1 } = \begin{bmatrix} \\\\ \\\\ -1 \\\\ 1 \end{bmatrix} ,\\\\
  &\begin{bmatrix}0 & 1 \\\\ 1 & 0 \end{bmatrix} ^ { \otimes 1 } = \begin{bmatrix} 0 & 1 \\\\ 1 & 0 \end{bmatrix} , \qquad \begin{bmatrix} 0 1 1 0 2 0 0 0 1 0 0 & \\\\ & \end{bmatrix} ^ { \otimes } = \begin{bmatrix} & & & \\\\ & & 1 & 0 0 \\\\ 1 0 & & & 0 \\\\ 1 & 0 & 0 & 0 \end{bmatrix} .
\end{align}
