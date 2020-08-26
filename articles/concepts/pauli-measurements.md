---
Titel: beschrijving van Pauli-metingen: meer informatie over het werken met bewerkingen met een Pauli-meting met één en meerdere Qubit.
Auteur: QuantumWriter UID: micro soft. Quantum. concepten. Pauli MS. Author: nawiebe@microsoft.com MS. date: 12/11/2017 MS. topic: artikel no-loc:
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

# <a name="pauli-measurements"></a>Pauli metingen

In de vorige discussies hebben we gestreefd naar reken kundige basis metingen.
Er zijn ook andere algemene metingen die zich voordoen bij Quantum Computing en die, vanuit een notatie perspectief, handig zijn om te worden uitgedrukt in termen van reken kundige basis metingen.
Als u werkt met Q# , worden de meest voorkomende maat eenheden die u kunt uitvoeren waarschijnlijk *Paulie metingen*, waarmee reken kundige basis metingen kunnen worden gebruikt voor metingen in andere bases en van pariteit tussen verschillende qubits.
In dergelijke gevallen is het gebruikelijk om de meting van een Pauli-operator te bespreken, in het algemeen een operator zoals $ X, Y, z $ of $ z \otimes z, x \otimes x, x \otimes Y enzovoort $ .

> [!TIP]
> In Q# worden Qubit-Opera tors van meerdere gebruikers doorgaans vertegenwoordigd door matrices van het type `Pauli[]` .
> Als $ u bijvoorbeeld X Z Y wilt weer geven \otimes \otimes $ , kunt u de matrix gebruiken `[PauliX, PauliZ, PauliY]` .

Het bespreken van metingen in termen van Pauli-Opera Tors is vooral gebruikelijk in het subveld van Quantum fout correctie.
In Q# volgen we een vergelijk bare Conventie. we bespreken nu deze alternatieve weer gave van metingen.

Voordat u meer informatie krijgt over hoe u een Pauli meting kunt zien, is het handig om te zien wat het meten van één Qubit in een quantum computer met de Quantum status is.
Stel dat er sprake $ is $ van een n-Qubit Quantum-status. vervolgens wordt een Qubit van de helft van de $ twee ^ n $ mogelijkheden waarvan de status mogelijk is, gemeten in.
Met andere woorden, de meting projecteert de Quantum status op een van de twee halve ruimtes.
We kunnen het beste bepalen hoe de meting wordt toegepast op deze intuition.

Om deze subruimten te kunnen identificeren, hebben we een taal nodig om ze te beschrijven.
Een van de manieren om de twee subruimten te beschrijven, is door ze op te geven via een matrix die net twee unieke eigenvalues heeft, die door de conventies worden beschouwd als $ \pm 1 $ .
Overweeg voor een eenvoudig voor beeld van het beschrijven van subruimten op deze manier $ Z $ :

$$
\begin{align}
  Z & = \begin{bmatrix} 1 & 0 \\\\ & -1 \end{bmatrix} .
\end{align}
$$

Door de diagonale elementen van de Pauli-Z-matrix te lezen $ $ , kunnen we zien dat $ Z $ twee eigenvectors, $ \ket { 0 } $ en $ \ket { 1 heeft } $ , met bijbehorende eigenvalues $ \pm 1 $ .
Als we de Qubit meten en `Zero` (overeenkomend met de status $ \ket { 0 } $ ), weten we dat de status van onze Qubit een $ + 1 $ eigenstate van de $ Z-operator is $ .
Op dezelfde manier `One` weten we dat de status van onze Qubit een $ $ eigenstate van $ Z is $ . Dit proces wordt in de taal van Pauli-metingen aangeduid als ' meten Pauli $ Z $ ' en is volledig gelijk aan het uitvoeren van een reken kundige basis meting.

Elke $ 2 \times 2 $ matrix die een unitary-trans formatie van Z is, $ $ voldoet ook aan deze criteria.
Dat wil zeggen dat we ook een matrix met $ = u ^ \dagger Z U $ , waarbij U een $ $ andere unitary-matrix is, kunt gebruiken om een matrix te geven die de twee uitkomsten van een meting in de $ \pm 1-eigenvectors definieert $ .
De notatie van Pauli metingen verwijst naar deze unitary-equivalentie door $ X-, Y-en Z- $ maat eenheden te identificeren als gelijkwaardige waarden die een Qubit zou kunnen hebben om informatie te verkrijgen van een.
Deze metingen worden hieronder vermeld voor het gemak.


|Pauli meting  | unitary-trans formatie  |
|-------------------|------------------------|
|$ $ Z |               $\boldone$             |
|$ $ X | $H               $                    |
|$ $ Y | $HS ^               {\dagger}$         |

Dat wil zeggen, ' meting $ Y $ ' is gelijk aan het Toep assen van $ HS ^ \dagger $ en het meten van de reken kracht, waarbij [`S`](xref:microsoft.quantum.intrinsic.s) een intrinsieke Quantum bewerking ook wel ' fase Gate ' wordt genoemd en kan worden gesimuleerd door de unitary-matrix

$$
\begin{align}
    S =\begin{bmatrix}
        1 & 0 \\\\ 0 & i \end{bmatrix} .
\end{align}
$$

Het is ook gelijk aan het Toep assen van $ HS ^ \dagger $ op de Quantum status vector en vervolgens $ Z $ , zodat de volgende bewerking overeenkomt met `Measure([PauliY], [q])` :

```Q#
operation MeasureY(qubit : Qubit) : Result {
    mutable result = Zero;
    within {
        H(q);
        Adjoint S(q);
    } apply {
        set result = M(q);
    }
    return result;
}
```

Vervolgens wordt de juiste status gevonden door terug te zetten naar de reken kundige basis, die bedragen om sh toe $ $ te passen op de Quantum status vector; in het bovenstaande code fragment wordt de trans formatie teruggeleid naar de reken kracht automatisch door het gebruik van het `within … apply` blok.

In Q# geven we het resultaat---dat wil zeggen dat de klassieke informatie die is geëxtraheerd uit interactie met de status---wordt gegeven met een `Result` waarde van $ j \in \\ { \texttt { nul } , \texttt { één } \\ } $ die aangeeft of het resultaat zich in de $ (-1) ^ j $ eigenspace van de Pauli-operator gemeten.


## <a name="multiple-qubit-measurements"></a>Metingen met meerdere Qubit

Metingen van Qubit Pauli-Opera tors worden op dezelfde manier gedefinieerd, zoals u kunt zien van:

$$
Z \otimes z = \begin{bmatrix} 1 & 0 0 0 & & \\\\  0 & -1 0 0 0 0 & & \\\\ & & -1 0 0 0 & \\\\ & & & 1 \end{bmatrix} .
$$

Daarom vormen de tensor-producten van twee Pauli- $ Z- $ Opera tors een matrix die bestaat uit twee spaties die bestaan uit $ + 1 $ en $ -1 $ eigenvalues.
Net als bij de single-Qubit geldt een halve spatie dat de helft van de toegankelijke vector ruimte behoort tot de $ + 1 $ eigenspace en de resterende helft tot de $ eigenspace-1 $ .
Over het algemeen is het eenvoudig om te zien uit de definitie van het tensor-product dat een tensor product van Pauli- $ Z- $ Opera tors en de identiteit dit ook volgt.
Bijvoorbeeld:

$$
\begin{align}
    \otimes \boldone Z =\begin{bmatrix}
        1 &  0 &  0 &  0 \\\\
        0 & 1 & 0 &\\\\
        0 &  0 & -1 &  0 \\\\
        0 &  0 &  0 & -1 \end{bmatrix} .
\end{align}
$$

Net als voorheen beschrijft elke unitary-trans formatie van dergelijke matrices ook twee halve ruimten die zijn gelabeld door $ \pm 1 $ eigenvalues.
Bijvoorbeeld $ x \otimes x = h \otimes h (z \otimes z) h \otimes h $  van de identiteit die $ Z = HXH $ .
Net als bij de één-qubite-case kunnen alle twee Qubit Pauli-metingen worden geschreven als $ U ^ \dagger (Z \otimes \id ) u $ voor $ 4 \times 4 $ unitary matrices $ u $ . De trans formaties in de volgende tabel worden opgesomd.

> [!NOTE]
>In de onderstaande tabel wordt swap gebruikt $ \operatorname { } $ om de matrix > aan te geven$$
> \begin{align}
>     \operatorname{WISSELEN } &=
>     \left( \begin { matrix}
>         1 & 0 & 0 & 0 \\\\
>         0 & 0 & 1 & 0 \\\\
>0 & 1 & 0 &\\\\
>matrix van 0 & 0 0 & & 1 > \end { } \right ) >     \end{align}
> $$
> wordt gebruikt om de intrinsieke bewerking te simuleren [`SWAP`](xref:microsoft.quantum.intrinsic) .

|Pauli meting     | unitary-trans formatie  |
|----------------------|------------------------|
|$ \otimes \boldone Z $ | $\boldone\otimes \boldone$|
|$ \otimes \boldone X $ | $ \otimes \boldone H $|
|$ \otimes \boldone Y $ | $ HS \dagger \otimes \boldone ^ $|
|$\boldone \otimes Z- $ | $ \operatorname { wisseling } $|
|$\boldone \otimes X $ | $ (H \otimes \boldone ) \operatorname { wisselen } $|
|$\boldone \otimes Y $ | $ (HS ^ \dagger \otimes \boldone ) \operatorname { wisselen } $|
|$Z \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } $|
|$X \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes \boldone ) $|
|$Y \otimes Z $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes \boldone ) $|
|$Z \otimes X $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes H) $|
|$X \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (h \otimes h) $|
|$Y \otimes X $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes H) $|
|$Z \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } ( \boldone \otimes HS ^ \dagger ) $|
|$X \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (H \otimes HS ^ \dagger ) $|
|$Y \otimes Y $ | $ \operatorname { CNOT } \_ { 10 } (HS ^ \dagger \otimes HS ^ \dagger ) $|

Hier wordt de [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) bewerking weer gegeven om de volgende reden.
Elke Pauli-meting die niet de matrix bevat, $ \boldone $ komt overeen met een unitary naar $ z \otimes z $ van de bovenstaande reden.
De eigenvalues van $ z \otimes z $ is alleen afhankelijk van de pariteit van de qubits die bestaan uit elke reken kundige basis vector, en de beheerde-not-bewerkingen dienen om deze pariteit te berekenen en op te slaan in de eerste bit.
Zodra de eerste bit wordt gemeten, kunnen we de identiteit van de resulterende halve ruimte herstellen, die overeenkomt met het meten van de Pauli-operator.

Een aanvullend Opmerking: Hoewel het mogelijk is om aan te nemen dat $ z \otimes z $ hetzelfde is als de opeenvolgende afmeting van $ z \otimes \mathbb { 1 } $ en vervolgens $ \mathbb { 1 } \otimes Z $ , zou deze veronderstelling onwaar zijn.
De reden hiervoor is dat $ bij \otimes het meten van z z $ project de Quantum status wordt omgezet in de $ + 1 $ $ -of-1- $ eigenstate van deze opera tors.
Door $ z \otimes \mathbb { 1 } $ te meten en vervolgens $ \mathbb { 1 } \otimes z $ projecteert u de Quantum status vector eerst op een halve spatie van $ Z \otimes \mathbb { 1 } $ en vervolgens op een halve spatie van $ \mathbb { 1 } \otimes Z $ . Omdat er vier reken kundige basis vectoren zijn, vermindert het uitvoeren van beide metingen de status naar een vierde spatie en vermindert deze in een enkele reken kundige basis vector.

## <a name="correlations-between-qubits"></a>Correlaties tussen qubits
Een andere manier om te kijken naar het meten van tensor-producten van Pauli-matrices, zoals $ X \otimes x $ of $ z \otimes z $ , is dat u met deze metingen de informatie kunt bekijken die is opgeslagen in de correlaties tussen de twee qubits.
Met $ X meten \otimes \id $ kunt u informatie bekijken die lokaal is opgeslagen in de eerste Qubit.
Hoewel beide soorten metingen even waardevol zijn voor Quantum Computing, licht de eerste maal de kracht van Quantum Computing.
In het geval van Quantum Computing is het vaak dat de informatie die u wilt leren, niet is opgeslagen in een enkele Qubit, maar niet lokaal is opgeslagen in alle qubits en daarom alleen door te kijken via een gemeen schappelijke meting (bijvoorbeeld $ Z \otimes z $ ).

In het geval van een fout correctie willen we vaak weten welke fout is opgetreden tijdens het leren over de status die we proberen te beveiligen.
Het [bit-Flip-code voorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) toont een voor beeld van hoe u dit kunt doen met behulp van maten als $ z \otimes z \otimes \id $ en $ \id \otimes z \otimes z $ . < --TODO: Wijzig dit in een koppeling naar de voor beelden van de browser zodra het code voorbeeld bit-Flip is ingeschakeld. -->

Wille keurige Pauli Opera Tors, zoals $ X \otimes Y \otimes Z, \otimes \boldone $ kunnen ook worden gemeten.
Al deze tensor-producten van Pauli-Opera tors hebben slechts twee eigenvalues $ \pm 1 $ en beide eigenspaces vormen een halve ruimte van de hele vector ruimte.
Daarom vallen ze samen met de hierboven vermelde vereisten.

In Q# retourneert deze metingen $ j $ als de meting resulteert in een resultaat in de eigenspace van het teken $ (-1) ^ j $ .
Het hebben van Pauli-metingen als ingebouwde functie in Q# is nuttig omdat het meten van dergelijke Opera tors lange ketens van besturings-en basis transformaties vereist om de diagonalizing $ U te beschrijven $ die nodig is om de bewerking uit te geven als een tensor product van $ Z $ en $ \id $ .
Doordat u kunt opgeven dat u een van deze vooraf gedefinieerde metingen wilt uitvoeren, hoeft u zich geen zorgen te maken over het transformeren van de basis, zodat een reken kundige basis meting de benodigde informatie bevat.
Q# Hiermee worden alle nood zakelijke trans formaties voor u automatisch verwerkt.
Zie de en-bewerkingen voor meer informatie [`Measure`](xref:microsoft.quantum.intrinsic.measure) [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) .

## <a name="the-no-cloning-theorem"></a>De theorema zonder klonen

De quantum informatie is krachtig.
Hierdoor kunnen we fantastische dingen doen, zoals factor nummers exponentieel sneller dan de best bekende klassieke algoritmen, of op efficiënte wijze simuleren van gecorreleerde elektroden systemen die klassieke kosten in de praktijk nodig hebben om nauw keurig te simuleren.
Er zijn echter beperkingen ten aanzien van de kracht van Quantum Computing.
Een dergelijke beperking wordt gegeven door de *theorema die niet klonen*.

De theorema zonder klonen is aptly met de naam.
Het klonen van generieke Quantum Staten door een quantum computer wordt niet toegestaan.
Het bewijs van de theorema is onduidelijker.
Hoewel een volledig bewijs van het no-klonen van theorema iets te technisch is voor onze bespreking, is de proef in het geval van geen extra hulp qubits binnen onze Scope (hulp qubits worden qubits gebruikt voor Scratch ruimte tijdens een berekening en worden ze eenvoudig gebruikt en beheerd in Q# , Zie [geleed qubits](xref:microsoft.quantum.guide.qubits#borrowed-qubits)).

Voor een dergelijke quantum computer moet de kloon bewerking worden beschreven in een unitary-matrix.
De meting is niet toegestaan omdat de Quantum status die we proberen te klonen, is beschadigd.
Voor het simuleren van de kloon bewerking willen we de unitary-matrix gebruiken om de eigenschap die $$
  U \ket { \psi } \ket { 0 } = \ket { \psi }\ket{\psi}
$$
voor elke status $ \ket { \psi } $ .
De eigenschap Linearity van matrix vermenigvuldiging impliceert dat voor elke tweede Quantum status $ \ket { \phi } $ ,

$$
\begin{align}
    U \left [ \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ] \ket { 0}
    &= \frac{ 1 } { \sqrt { 2 } } U \ket { \phi } \ket { 0}
      + \frac{1 } { \sqrt { 2 } } U \ket { \psi } \ket { 0 }\\\\
    &= \frac{ 1 } { \sqrt { 2 } } \left ( \ket { \phi } \ket { \phi }  +  \ket { \psi }\ket{\psi}
        \right) \\\\
    &\ne \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ) \otimes \left ( \frac { 1 } { \sqrt { 2 } } \left ( \ket { \phi } + \ket { \psi } \right ) \right ).
\end{align}
$$

Dit voorziet in de fundamentele Intuition achter het no-klonen theorema: elk apparaat dat een onbekende Quantum status kopieert, moet fouten veroorzaken op ten minste een van de statussen die worden gekopieerd.
Hoewel de sleutel veronderstelling dat de kloon van de gegevens in de invoer status lineair is, kan dit worden geschonden door de toevoeging en meting van de hulp qubits. dergelijke interacties lekken ook bij het verwerken van informatie over het systeem door middel van de meting statistieken en voor komen dat dergelijke gevallen precies worden gekloond.
Zie [voor meer informatie](xref:microsoft.quantum.more-information)over de theorema die u niet klonen.

Het niet-klonen van theorema is belang rijk voor de kwalitatieve kennis van Quantum Computing omdat als u de Quantum toestanden in de buurt zou kunnen klonen, dan krijgt u een Magical-mogelijkheid om te leren van Quantum Staten.
Het is ook mogelijk dat u het Heisenberg van vaunted onzekerheid schendt.
U kunt ook een optimale kloon gebruiken om één voor beeld van een complexe Quantum distributie te maken en alles te leren over die distributie, van slechts één voor beeld.
Dit is een manier om een munten te spie gelen en op de hoogte te houden en vervolgens een vriend te vertellen over het resultaat van de reactie "Ah de verdeling van die munten moet worden gebernoulli met $ p = 0.512643 \ ldots $ !"  Een dergelijke instructie zou niet-sensical zijn, omdat een stukje informatie (het resultaat van de kop) simpelweg de vele informatie die nodig is om de distributie te coderen zonder belang rijke eerdere informatie, niet kan leveren.
Op dezelfde manier kunnen we zonder voorafgaande informatie niet perfect een Quantum status klonen, net zoals we geen ensemble van deze munten kunnen voorbereiden zonder dat ze daar weten $ $ .

Informatie is niet gratis in Quantum Computing.
Elk Qubit dat wordt gemeten, geeft één stukje informatie en het theorema zonder klonen laat zien dat er geen beschik over is die kunnen worden misbruikt om de fundamentele berekenings verhouding te verkrijgen tussen informatie over het systeem en de verstoringen die erop worden opgeroepen.
