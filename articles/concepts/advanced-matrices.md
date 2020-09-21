---
Titel: beschrijving van geavanceerde matrix concepten: meer informatie over eigenvectors, eigenvalues en matrix exponentiëles, de belangrijkste hulpprogram ma's voor het beschrijven en simuleren van Quantum algoritmen.
Auteur: QuantumWriter UID: micro soft. Quantum. concepten. matrix-Geavanceerd MS. Author: v-benbra MS. date: 12/11/2017 MS. topic: artikel no-loc:
- "Q#"
- "$$v"
- "$$"
- "$$"
- "$"
- "$"
- "$"
- "$$"
- "$$$"
- "$$$"
- "$$$"
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
# <a name="advanced-matrix-concepts"></a>Geavanceerde matrix concepten #

We gaan nu onze manipulatie van matrices uitbreiden naar [*eigenvalues, Eigenvectors*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) en [*exponenten*](https://en.wikipedia.org/wiki/Matrix_exponential) die een fundamentele set hulpprogram ma's vormen die we Quantum algoritmen moeten beschrijven en implementeren.

## <a name="eigenvalues-and-eigenvectors"></a>Eigenvalues en Eigenvectors ##

U $ kunt $ een vier Kante matrix maken en $ v $ een vector zijn die niet de Nulls vector is (dat wil zeggen, de vector met alle vermeldingen die gelijk zijn aan $ 0 $ ).

We zeggen $ $ dat v een [*eigenvector*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) is van  $ M als de waarde van $ $ MV = $ voor een bepaalde $ c $ . We zeggen $ $ dat c de [*eigenvalue*](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors) is die overeenkomt met de eigenvector $ v $ . In het algemeen een matrix $ M $ kan een vector omzetten in een andere vector, maar een eigenvector is een speciale waarde omdat deze ongewijzigd blijft, behalve als vermenigvuldigd met een getal. Houd er rekening mee dat als $ v $ een eigenvector is met eigenvalue $ c $ , $ AV $ ook een eigenvector (voor elke niet $ -nul a $ ) met dezelfde eigenvalue.

Voor de ID-matrix is bijvoorbeeld elke vector $ v $ een eigenvector met eigenvalue $ 1 $ .

Een ander voor beeld is dat u een [*diagonale matrix*](https://en.wikipedia.org/wiki/Diagonal_matrix) $ $ hebt die alleen niet-nul vermeldingen bevat op de diagonaal:

$$
\begin{bmatrix}
d_1 & 0 & 0 \\\\ 0 & d_2 & 0 \\\\ 0 & 0 & D_3 \end{bmatrix} .
$$

De vectoren

$$\begin{bmatrix}1 \\\\ 0 \\\\ 0 \end{bmatrix} , \begin{bmatrix} 0 \\\\ 1 \\\\ 0 \end{bmatrix} en \begin{bmatrix} 0 \\\\ 0 \\\\ 1\end{bmatrix}$$

zijn eigenvectors van deze matrix met  $ respectievelijk eigenvalues d_1 $ , $ d_2 $ en $ D_3 $ . Als $ d_1 $ , $ d_2 $ en $ D_3 $ afzonderlijke getallen zijn, zijn deze vectoren (en hun veelvouden) de enige eigenvectors van de matrix $ d $ . Over het algemeen kunt u voor een diagonale matrix eenvoudig de eigenvalues en eigenvectors lezen. De eigenvalues zijn alle getallen die worden weer gegeven op de diagonaal en hun respectieve eigenvectors zijn de eenheids vectoren met één vermelding die gelijk is aan $ 1 $ en de resterende vermeldingen gelijk zijn aan $ 0 $ .

In het bovenstaande voor beeld ziet u dat de eigenvectors van $ D $ een basis vormt voor driedimensionale $ $ vectoren. Een basis is een set vectoren waarmee elke vector als een lineaire combi natie ervan kan worden geschreven. Meer expliciet, $ v_1 $ , $ v_2 $ en $ v_3 $ vormen een basis als een vector $ v $ kan worden geschreven als $ v = a_1 v_1 + a_2 v_2 + a_3 v_3 $ voor sommige cijfers $ a_1 $ , a_2 en $ $ $ a_3 $ .

Terughalen dat een Hermitian-matrix (ook wel Self-adjoint genoemd) een complexe vier Kante matrix is die gelijk is aan de eigen complex geconjugeerde getransponeerd, terwijl een unitary-matrix een complexe vier Kante matrix is waarvan de inverse gelijk is aan de adjoint of de complex geconjugeerde getransponeerde.
Voor Hermitian-en unitary-matrices, die in feite de enige matrices opleveren die worden aangetroffen in de Quantum Computing, is er een algemeen resultaat bekend als de [*Spectral theorema*](https://en.wikipedia.org/wiki/Spectral_theorem), waarbij het volgende wordt door berekend: voor elke Hermitian-of unitary $ -matrix M $ , bestaat er een unitary $ U $ zodat u $ M = u ^ \dagger d u $ voor sommige diagonale matrix $ d $ . Bovendien is de diagonale invoer van $ D $ de eigenvalues van $ M $ .

U weet al hoe u de eigenvalues en eigenvectors van een diagonale matrix D kunt berekenen $ $ . Als u deze theorema gebruikt, weet $ u dat als v $ een eigenvector is van $ D $ met eigenvalue $ c $ , d.w.z. $ DV = AVK $ , vervolgens $ ^ \dagger v $ een eigenvector van M is $ $ met eigenvalue $ c $ . Dit komt doordat

$$M (U ^ \dagger v) = u ^ \dagger d u (u ^ \dagger v) = U ^ \dagger d (u u ^ \dagger ) v = U ^ \dagger d v = c u ^ \dagger v.$$

## <a name="matrix-exponentials"></a>Matrix exponentiële waarde
Een [*exponentiële matrix*](https://en.wikipedia.org/wiki/Matrix_exponential) kan ook worden gedefinieerd in exacte analoge waarde naar de exponentiële functie.  De matrix exponentiële van een matrix $ a $ kan worden uitgedrukt als

$$
e ^ A = \boldone + a + a \frac { ^ 2 } { 2! } + \frac { Een ^ 3 } { 3!}+\cdots
$$

Dit is belang rijk omdat de quantum-mechanische tijd wordt beschreven in een unitary-matrix van de vorm $ e ^ { IB } $ voor Hermitian matrix $ B $ .  Daarom is het uitvoeren van matrix-exponentiëlen een fundamenteel onderdeel van Quantum Computing en biedt het een aantal Q# ingebouwde routines voor het beschrijven van deze bewerkingen.
Er zijn veel manieren in de praktijk om een matrix exponentiële waarde te berekenen op een klassieke computer, en in het algemeen is een dergelijke exponentiële benadering fraught met Peril.  Zie [*Cleve moler en Jeroen van bruikleen. "19 dubious manieren om de exponentiële waarde van een matrix te berekenen." SIAM beoordeling 20,4 (1978): 801-836*](https://doi.org/10.1137/S00361445024180) voor meer informatie over de betrokken uitdagingen.

De eenvoudigste manier om inzicht te krijgen in het berekenen van de exponentiële waarde van een matrix is via de eigenvalues en eigenvectors van die matrix.  Met name de hierboven besproken Spectral theorema heeft aangegeven dat er voor elke Hermitian-of unitary-matrix $ een $ unitary matrix $ u $ en een diagonale matrix is, $ D $ zodat $ = u een u ^ \dagger D u $ .  Vanwege de eigenschappen van unitarity hebben we $ een ^ 2 = u ^ \dagger d ^ 2 u $ en op dezelfde manier voor Power $ p $ $ A ^ p = u ^ \dagger d ^ p u $ .  Als we dit vervangen door de operator definitie van de operator exponentiële, krijgen we het volgende:

$$
e ^ a = U ^ \dagger \left ( \boldone + d + \frac { d ^ 2 } { 2! } + \cdots \right ) U = u ^ \dagger \begin{bmatrix} \exp (D_ { 11 } ) & 0 & \cdots & 0 \\\\ 0 & \exp (D_ { 22 } ) & \cdots & 0 \\\\ \vdots & \vdots & \ddots & \vdots \\\\ 0 & 0 & \cdots & \exp (D_ { nn } ) \end{bmatrix} U.$$

Met andere woorden, als u overschakelt naar de eigenbasis van de matrix $ A, $ is de matrix exponentieel gelijk aan het berekenen van de normale exponentiële waarde van de eigenvalues van de matrix.  Net als veel bewerkingen in Quantum Computing moeten matrix-exponentiële waarden worden uitgevoerd, wordt deze truc omgezet in de eigenbasis van een matrix om het uitvoeren van de operator exponentieel te vereenvoudigen, en dit is de basis achter veel Quantum algoritmen, zoals Trotter – Suzuki-stijl, verderop in deze hand leiding besproken.

Een andere nuttige eigenschap is als $ b $ zowel unitary als Hermitian is, D.w.z. $ b = b ^ { -1 } = B ^ \dagger $ en $ B ^ 2 = \boldone $ . Door deze regel toe te passen op de bovenstaande uitbrei ding van de matrix exponentieel en door de $ \boldone $ samen met de $ B $ -voor waarden te groeperen, kan het worden weer geven dat voor elke reële waarde $ x $ de identiteit

$$e ^ { iBx } = \boldone \cos (x) + iB\sin (x)$$


keringen. Dit is met name nuttig omdat het de oorzaak is van de exponentiële waarde van de acties matrix, zelfs als de dimensie $ b $ exponentieel groot is, voor het speciale geval wanneer $ B $ zowel unitary als Hermitian is.
