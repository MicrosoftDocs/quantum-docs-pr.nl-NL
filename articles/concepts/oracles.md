---
Titel: Quantum Oracle description Beschrijving: informatie over het werken met en het definiëren van Quantum Oracle, Black Box-bewerkingen die worden gebruikt als invoer voor een ander algoritme.
Auteur: cgranade UID: micro soft. Quantum. concepten. Oracle MS. Author: Christopher.Granade@microsoft.com MS. date: 07/11/2018 MS. topic: artikel no-loc:
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
# <a name="quantum-oracles"></a>Quantum Oracle

Een Oracle $ O $ is een "Black Box"-bewerking die als invoer wordt gebruikt voor een ander algoritme.
Dergelijke bewerkingen worden vaak gedefinieerd met behulp van een klassieke functie $ f: \\ { 0, 1 \\ } ^ n \to \\ { 0, 1 \\ } ^ m, $ waarbij een $ n $ -bits binaire invoer wordt gebruikt en een $ m $ -bits binaire uitvoer wordt gegenereerd.
Als u dit wilt doen, moet u een bepaalde binaire invoer $ x = (x_ { 0 } , x_ { 1 } , \dots, x_ { n-1 } ) overwegen $ .
We kunnen Qubit Staten labelen als $ \ket { \vec { x } } = \ket { x_ { 0 } } \otimes \ket { x_ { 1 } } \otimes \cdots \otimes \ket { x_ { n-1 } } $ .

We kunnen eerst proberen om o te definiëren, $ $ zodat de $ o \ket { x } = \ket { f (x) } $ , maar dit heeft een aantal problemen.
Ten eerste $ $ kan f een andere grootte hebben van de invoer en uitvoer ( $ n \ne m $ ), zodat $ $ het aantal qubits in het REGI ster kan worden gewijzigd.
Ten tweede, zelfs als $ n = m $ , mag de functie niet omkeerbaar zijn: als $ f (x) = f (y) $ voor sommige $ x \ne y $ , dan $ o \ket { x } = o y, \ket { } $ maar $ o ^ \dagger o \ket { x } \ne o ^ \dagger o \ket { y } $ .
Dit betekent dat we de adjoint $ -bewerking O ^ niet kunnen maken \dagger $ en dat er voor Oracle een adjoint moet worden gedefinieerd.

## <a name="defining-an-oracle-by-its-effect-on-computational-basis-states"></a>Het definiëren van een Oracle op basis van de reken status
Deze problemen kunnen worden opgelost door een tweede REGI ster van $ m $ qubits te introduceren om ons antwoord te houden.
Vervolgens definiëren we het effect van de Oracle op alle reken kundige basis Staten: voor alle $ x \in \\ { 0, 1 \\ } ^ n $ en $ y \in \\ { 0, 1 \\ } ^ m $ ,

$$
\begin{align}
    O ( \ket { x } \otimes \ket { y } ) = \ket { x } \otimes \ket { y \oplus f (x) } .
\end{align}
$$

Nu $ o = ^ \dagger $ per constructie, waardoor we beide problemen hebben opgelost.

> [!TIP]
>$ = { \dagger } $ Houd er rekening mee dat $ o ^ 2 = \boldone $ sinds $ a \oplus b \oplus b = a $ voor alle $ a, b \in \: :: No-Loc ({)::: 0, 1 \: :: No-Loc (})::: is $ .
>Als gevolg hiervan is de $ O \ket { x } \ket { y \oplus f (x) } = \ket { x } \ket { y \oplus f (x) \oplus f (x) } = \ket { x } \ket { y } $ .

Belang rijk: als u een Oracle op deze manier definieert voor elke reken kundige basis status $ \ket { x } \ket { y, } $ wordt ook gedefinieerd hoe $ O moet worden uitgevoerd $ voor een andere status.
Dit volgt onmiddellijk van het feit dat $ O $ , zoals alle Quantum bewerkingen, lineair is in de status waarop het wordt uitgevoerd.
Houd rekening met de Hadamard-bewerking, bijvoorbeeld, die wordt gedefinieerd door $ H \ket { 0 } = \ket { + } $ en $ H \ket { 1 } = \ket { - } $ .
Als we willen weten hoe $ h $ op kan worden uitgevoerd $ \ket { + } $ , kunnen we die $ h gebruiken $ lineair,

$$
\begin{align}
H \ket { + } & = \frac { 1 } { \sqrt { 2 } } uur ( \ket { 0 }  +  \ket { 1 } ) = \frac { 1 } { \sqrt { 2 } } (h \ket { 0 } + H \ket { 1 } )\\\\
           &= \frac{ 1 } { \sqrt { 2 } } ( \ket { + }  +  \ket { - } ) = \frac 12 ( \ket { 0 }  +  \ket { 1 }  +  \ket { 0 }  -  \ket { 1 } ) = \ket { 0 } .
\end{align}
$$

In het geval van het definiëren van onze Oracle $ O $ , kunnen we ook gebruiken dat elke staat $ \ket { \psi } $ op $ n + m $ qubits kan worden geschreven als

$$
\begin{align}
\ket{\psi}& = \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y}
\end{align}
$$

waarbij $ \alpha : \\ { 0, 1 \\ } ^ n \times \\ { 0, 1 \\ } ^ m \to \mathbb { C } $ staat voor de coëfficiënten van de status $ \ket { \psi } $ . Zeep

$$
\begin{align}
O \ket { \psi } & = o \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y } x \\\\ 0 & , = 1 ^ n, y 0, 1 ^ m (x, y) O \sum _ { \in \\ { \\ } \in \\ { \\ } } \alpha \ket { x } \ket { y }\\\\
             &= \sum _ { x \in \\ { 0, 1 \\ } ^ n, y \in \\ { 0, 1 \\ } ^ m } \alpha (x, y) \ket { x } \ket { y \oplus f (x) } .
\end{align}
$$

## <a name="phase-oracles"></a>Fase Oracle
U kunt ook $ f coderen $ in een Oracle $ O $ door een _fase_ toe te passen op basis van de invoer voor $ O $ . We kunnen bijvoorbeeld $ O definiëren $ dat$$
\begin{align}
    O \ket { x } = (-1) ^ { f (x) } \ket { x } .
\end{align}
$$
Als een Phase Oracle in eerste instantie op een registratie wordt uitgevoerd in een reken kundige basis status $ \ket { x } $ , is deze fase een globale fase en daarom niet waarneembaar.
Maar zo'n Oracle kan een zeer krachtige bron zijn als deze wordt toegepast op een superpositie of als een beheerde bewerking.
Denk bijvoorbeeld aan een Oracle O_f- $ fase $ voor een functie f met één $ Qubit $ .
Kies$$
\begin{align}
    O_f\ket{+}
        &=O_f ( \ket { 0 }  +  \ket { 1 } )/ \sqrt { 2 }\\\\
        &=((-1) ^ { f (0) } \ket { 0 } + (-1) ^ { f (1) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } ( \ket { 0 } + (-1) ^ { f (1)-f (0) } \ket { 1 } )/ \sqrt { 2 }\\\\
        &=(-1) ^ { f (0) } Z ^ { f (0)-f (1) } \ket { + } .
\end{align}
$$

In het algemeen kunnen beide weer gaven van Oracle worden uitgebreid met klassieke functies die echte aantallen retour neren in plaats van slechts één bit.

Het kiezen van de beste manier om een Oracle te implementeren, is afhankelijk van hoe deze Oracle wordt gebruikt binnen een bepaalde algoritme.
Zo is [Deutsch-Jozsa-algoritme](https://en.wikipedia.org/wiki/Deutsch%E2%80%93Jozsa_algorithm) afhankelijk van de Oracle die in de eerste manier is geïmplementeerd, terwijl het [algoritme van Grover afhankelijk is](https://en.wikipedia.org/wiki/Grover's_algorithm) van de Oracle die op de tweede manier is geïmplementeerd.


Voor meer informatie wordt de discussie in [Gilyén *et al*. 1711,00465](https://arxiv.org/abs/1711.00465)voorgesteld.
