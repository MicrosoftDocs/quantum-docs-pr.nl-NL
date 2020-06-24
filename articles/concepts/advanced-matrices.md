---
title: Geavanceerde matrixconcepten
description: Meer informatie over eigenvectors, eigenvalues en matrix exponentiëles, de belangrijkste hulpprogram ma's voor het beschrijven en simuleren van Quantum algoritmen.
author: QuantumWriter
uid: microsoft.quantum.concepts.matrix-advanced
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
no-loc:
- $
- $
- $
- $
- $
- $
- $$
- $$
- $$
- '\cdots'
- bmatrix
- '\ddots'
- '\equiv'
- '\sum'
- '\begin'
- '\end'
- '\sqrt'
- '\otimes'
- '{'
- '}'
- '\text'
- '\phi'
- '\kappa'
- '\psi'
- '\alpha'
- '\beta'
- '\gamma'
- '\delta'
- '\omega'
- '\bra'
- '\ket'
- '\boldone'
- '\\\\'
- '\\'
- =
- '\frac'
- '\text'
- '\mapsto'
- '\dagger'
- '\to'
- "\begin{cases}"
- "\end{cases}"
- '\operatorname'
- '\braket'
- '\id'
- '\expect'
- '\defeq'
- '\variance'
- '\dd'
- '&'
- "\begin{align}"
- "\end{align}"
- '\Lambda'
- '\lambda'
- '\Omega'
- '\mathrm'
- '\left'
- '\right'
- '\qquad'
- '\times'
- '\big'
- '\langle'
- '\rangle'
- '\bigg'
- '\Big'
- '|'
- '\mathbb'
- '\vec'
- '\in'
- '\texttt'
- '\ne'
- <
- '>'
- '\leq'
- '\geq'
- ~~
- "~"
- "\begin{bmatrix}"
- "\end{bmatrix}"
- '\_'
ms.openlocfilehash: 71923247121eae6a1d4e26d2664d8e547370ba3a
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85269453"
---
# <a name="advanced-matrix-concepts"></a>Geavanceerde matrix concepten #

We gaan nu onze manipulatie van matrices uitbreiden naar [*eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) en [*exponenten*](https://en.wikipedia.org/wiki/Matrix_exponential) die een fundamentele set hulpprogram ma's vormen die we Quantum algoritmen moeten beschrijven en implementeren.

## <a name="eigenvalues-and-eigenvectors"></a>Eigenvalues en Eigenvectors ##

Laat $M $ een vier Kante matrix zijn en $v $ een vector is die niet de enige 0-vector is (dat wil zeggen, de vector met alle vermeldingen die gelijk zijn aan $0 $ ).

We zeggen $ dat $v een [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) is van $M $ als $MV = avk $ voor een aantal $c $ . We zeggen dat $c $ de [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) is die overeenkomt met de eigenvector $v $ . In het algemeen een matrix $M $ kan een vector omzetten in een andere vector, maar een eigenvector is een speciale waarde omdat deze ongewijzigd blijft, behalve als vermenigvuldigd met een getal. Houd er rekening mee dat als $v $ een eigenvector is met eigenvalue $c $ , $AV $ ook een eigenvector (voor elke niet-nul $a $ ) met dezelfde eigenvalue.

Voor de ID-matrix is bijvoorbeeld elke vector $v $ een eigenvector met eigenvalue $1 $ .

Een ander voor beeld is dat u een [*diagonale matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $D $ die alleen niet-nul vermeldingen bevat op de diagonaal:

$ $ \begin{bmatrix}
d_1 & 0 & 0 \\ \\ 0 & d_2 & 0 \\ \\ 0 & 0 & D_3 \end{ bmatrix } .
$$

De vectoren

$ $ \begin{ bmatrix } 1 \\ \\ 0 \\ \\ 0 \end{ bmatrix } , \begin{ bmatrix } 0 \\ \\ 1 \\ \\ 0 \end{bmatrix} en \begin{ bmatrix } 0 \\ \\ 0 \\ \\ 1\end{bmatrix}$$

zijn eigenvectors van deze matrix met respectievelijk eigenvalues $d _1 $ , $d _2 $ en $d _3 $ . Als $d _1 $ , $d _2 $ en $d _3 $ afzonderlijke getallen zijn, zijn deze vectoren (en hun veelvouden) de enige eigenvectors van de matrix $D $ . Over het algemeen kunt u voor een diagonale matrix eenvoudig de eigenvalues en eigenvectors lezen. De eigenvalues zijn alle getallen die worden weer gegeven op de diagonaal en hun respectieve eigenvectors zijn de eenheids vectoren met één vermelding gelijk aan $1 $ en de resterende vermeldingen gelijk zijn aan $0 $ .

In het bovenstaande voor beeld ziet u dat de eigenvectors van $D $ een basis vormt voor $3 $ -dimensionale vectoren. Een basis is een set vectoren waarmee elke vector als een lineaire combi natie ervan kan worden geschreven. Meer expliciet, $v _1 $ , $v _2 $ en $v _3 $ vormen een basis als een vector $v $ kan worden geschreven als $v = a_1 v_1 + a_2 v_2 + a_3 v_3 $ voor sommige cijfers $a _1 $ , $a _2 $ en $a _3 $ .

Terughalen dat een Hermitian-matrix (ook wel Self-adjoint genoemd) een complexe vier Kante matrix is die gelijk is aan zijn eigen complexe geconjugeerde, terwijl een unitary-matrix een complexe vier Kante matrix is waarvan de inverse is gelijk aan de complex geconjugeerde.
Voor Hermitian-en unitary-matrices, die in feite de enige matrices zijn die zich voordoen bij Quantum Computing, is er een algemeen resultaat bekend als de [*Spectral theorema*](https://en.wikipedia.org/wiki/Spectral_theorem), waarbij het volgende wordt door berekend: voor elke Hermitian-of unitary matrix $M $ , bestaat er een unitary $U, $ zodat $M = U ^ \dagger D u $ voor sommige diagonale matrix $D $ . Bovendien zijn de diagonale items van $D $ de eigenvalues van $M $ .

U weet al hoe u de eigenvalues en eigenvectors van een matrix met diagonale $D wilt berekenen $ . Met deze theorema weten we dat als $v $ een eigenvector is van $D $ met eigenvalue $c $ , dat wil zeggen $DV = avk $ , en $U ^ \dagger v $ een eigenvector is van $M $ met eigenvalue $c $ . Dit komt doordat

$ $M (U ^ \dagger v) = U ^ \dagger D U (U ^ \dagger v) = U ^ \dagger D (U U ^ \dagger) v = U ^ \dagger D v = c U ^ \dagger v. $ $

## <a name="matrix-exponentials"></a>Matrix exponentiële waarde
Een [*exponentiële matrix*](https://en.wikipedia.org/wiki/Matrix_exponential) kan ook worden gedefinieerd in exacte analoge waarde naar de exponentiële functie.  De matrix exponentiële waarde van een matrix $A $ kan worden uitgedrukt als

$ $ e ^ A = \boldone + a + \frac{A ^ 2 } {2!} + \frac{A ^ 3 } {3!} + \cdots $ $

Dit is belang rijk omdat quantum-mechanische tijd wordt beschreven in een unitary matrix van het formulier $e ^ {iB } $ voor Hermitian matrix $B $ .  Daarom is het uitvoeren van matrix exponentiëlen een fundamenteel onderdeel van Quantum Computing, en biedt dit Q # intrinsieke routines voor het beschrijven van deze bewerkingen.
Er zijn veel manieren in de praktijk om een matrix exponentiële waarde te berekenen op een klassieke computer, en in het algemeen is een dergelijke exponentiële benadering fraught met Peril.  Zie [*Cleve moler en Jeroen van bruikleen. "19 dubious manieren om de exponentiële waarde van een matrix te berekenen." SIAM beoordeling 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) voor meer informatie over de betrokken uitdagingen.

De eenvoudigste manier om inzicht te krijgen in het berekenen van de exponentiële waarde van een matrix is via de eigenvalues en eigenvectors van die matrix.  Met name de hierboven besproken Spectral theorema geeft aan dat voor elke Hermitian of unitary matrix $A $ er een unitary matrix $U $ en een diagonale matrix $D $ dat $A = U ^ \dagger D u $ .  Vanwege de eigenschappen van unitarity hebben we dat $A ^ 2 = U ^ \dagger D ^ 2 U $ en ook voor alle power $p $ $A ^ p = U ^ \dagger D ^ p U $ .  Als we dit vervangen door de operator definitie van de operator exponentiële, krijgen we het volgende:

$ $ e ^ A = U ^ \dagger \left (\boldone + D + \frac{D ^ 2 } {2!} + \cdots \right) U = u ^ \dagger \begin{ bmatrix } \exp (D_ {11 } ) & 0 & \cdots &0 \\\\ 0 & \exp (D_ {22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0&0 & \cdots & \exp (D_ {nn } ) \end{ bmatrix } U. $ $

Met andere woorden, als u overschakelt naar de eigenbasis van de matrix $A $ wordt de matrix exponentiële waarde gelijk aan het berekenen van de normale exponentieel van de eigenvalues van de matrix.  Net als veel bewerkingen in Quantum Computing moeten matrix-exponentiële waarden worden uitgevoerd, wordt deze truc omgezet in de eigenbasis van een matrix om het uitvoeren van de operator exponentieel te vereenvoudigen, en dit is de basis achter veel Quantum algoritmen, zoals Trotter – Suzuki-stijl, verderop in deze hand leiding besproken.

Een andere nuttige eigenschap is als $B $ zowel unitary als Hermitian is, dat wil zeggen $B = b ^ {-1 } = B ^ \dagger $ $B ^ 2 = \boldone $ . Door deze regel toe te passen op de bovenstaande uitbrei ding van de matrix exponentiële en door het groeperen van de $ \boldone $ en de voor waarden van de $B $ , kan het worden weer geven dat voor elke feitelijke waarde $x $ de identiteit

$ $e ^ {iBx } = \boldone \cos (x) + iB\sin (x) $ $


keringen. Dit is met name nuttig omdat het de oorzaak is van de exponentiële waarde van de acties matrix, zelfs als de dimensie van $B $ exponentieel groot is, voor het speciale geval wanneer $B $ zowel unitary als Hermitian is.
