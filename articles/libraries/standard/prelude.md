---
title: Intrinsieke bewerkingen en functies in de QDK
description: Meer informatie over de intrinsieke bewerkingen en functies in de QDK, waaronder klassieke functies en unitary, rotatie-en meet bewerkingen.
author: QuantumWriter
uid: microsoft.quantum.libraries.standard.prelude
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: b1c26c632f36b6c254d940a89b13638f7592ab80
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907202"
---
# <a name="the-prelude"></a>De prelude #

De Q #-compiler en de doel computers die deel uitmaken van de Quantum Development Kit bieden een aantal ingebouwde functies en bewerkingen die kunnen worden gebruikt bij het schrijven van Quantum Program ma's in Q #.

## <a name="intrinsic-operations-and-functions"></a>Intrinsieke bewerkingen en functies ##

De intrinsieke bewerkingen die in de standaard bibliotheek zijn gedefinieerd, vallen ongeveer in een van de volgende categorieën:

- Essentiële klassieke functies die zijn verzameld in de naam ruimte van <xref:microsoft.quantum.core>.
- Bewerkingen voor unitaries die bestaan uit [Clifford en $T $ Gates](xref:microsoft.quantum.concepts.qubit).
- Bewerkingen die betrekking hebben op rotaties over verschillende Opera tors.
- Bewerkingen geïmplementeerd metingen.

Omdat de Clifford + $T $ Gate-set is ingesteld op [Universal](xref:microsoft.quantum.concepts.multiple-qubits) voor Quantum Computing, zijn deze bewerkingen voldoende om een Quantum algoritme te implementeren in negligibly kleine fout.
Door ook rotaties op te geven, kan met Q # de programmeur binnen de single Qubit unitary-en CNOT-poort bibliotheek werken. Deze bibliotheek is veel gemakkelijker te zien, omdat het niet vereist is dat de programmeur rechtstreeks de Clifford + $T $ decompileren en omdat er zeer efficiënte methoden bestaan voor het samen stellen van één Qubit unitaries in Clifford en $T $ Gates (Zie [hier](xref:microsoft.quantum.more-information) voor meer informatie).

Waar mogelijk, de bewerkingen die zijn gedefinieerd in de prelude die op qubits zijn toegestaan voor het Toep assen van de `Controlled` variant, zodat de doel computer de juiste ontleding uitvoert.

Veel van de functies en bewerkingen die in dit gedeelte van de prelude zijn gedefinieerd, bevinden zich in de naam ruimte @"microsoft.quantum.intrinsic", zodat de meeste Q #-bron bestanden een `open Microsoft.Quantum.Intrinsic;`-instructie hebben die direct volgt op de oorspronkelijke naam ruimte declaratie.
De naam ruimte van de <xref:microsoft.quantum.core> wordt automatisch geopend, zodat functies zoals <xref:microsoft.quantum.core.length> kunnen worden gebruikt zonder een `open`-instructie.

### <a name="common-single-qubit-unitary-operations"></a>Algemene single-Qubit unitary-bewerkingen ###

De prelude definieert ook veel veelvoorkomende [bewerkingen met één Qubit](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).
Al deze bewerkingen staan zowel de `Controlled` als `Adjoint` functors toe.

#### <a name="pauli-operators"></a>Pauli-Opera tors ####

Met de <xref:microsoft.quantum.intrinsic.x> bewerking wordt de operator Pauli $X $ geïmplementeerd.
Dit wordt soms ook wel de `NOT`-poort genoemd.
Het bevat handtekening `(Qubit => Unit is Adj + Ctl)`.
Dit komt overeen met de unitary met één Qubit:

\begin{Equation} \begin{bmatrix} 0 & 1 \\\\% controle: dit maakt momenteel gebruik van de quadwhack hack.
1 & 0 \end{bmatrix} \end{Equation}

Met de <xref:microsoft.quantum.intrinsic.y> bewerking wordt de operator Pauli $Y $ geïmplementeerd.
Het bevat handtekening `(Qubit => Unit is Adj + Ctl)`.
Dit komt overeen met de unitary met één Qubit:

\begin{Equation} \begin{bmatrix} 0 &-i \\\\% controle: dit maakt momenteel gebruik van de quadwhack hack.
Ik & 0 \end{bmatrix} \end{Equation}

Met de <xref:microsoft.quantum.intrinsic.z> bewerking wordt de operator Pauli $Z $ geïmplementeerd.
Het bevat handtekening `(Qubit => Unit is Adj + Ctl)`.
Dit komt overeen met de unitary met één Qubit:

\begin{Equation} \begin{bmatrix} 1 & 0 \\\\% controle: dit maakt momenteel gebruik van de quadwhack hack.
0 &-1 \end{bmatrix} \end{Equation}

Hieronder ziet u de trans formaties die zijn toegewezen aan de [Bloch-bol](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) (de rotatieas in elke case is rood gemarkeerd):

![Pauli-bewerkingen die zijn toegewezen aan de Bloch-bol](~/media/prelude_pauliBloch.png)

Het is belang rijk te weten dat het Toep assen van dezelfde Pauli-Gate twee maal op dezelfde Qubit de bewerking annuleert (omdat u nu een volledige draaiing van 2π (360 °) over het Opper vlak naar de Bloch-bol hebt uitgevoerd, waardoor er op het begin punt weer een bericht binnenkomt. Dit brengt ons de volgende identiteit:

$ $ X ^ 2 = Y ^ 2 = Z ^ 2 = \boldone $ $

Dit kan worden visualised op de Bloch-bol:

![XX = I](~/media/prelude_blochIdentity.png)

#### <a name="other-single-qubit-cliffords"></a>Andere single-Qubit Cliffords ####

Met de <xref:microsoft.quantum.intrinsic.h>-bewerking wordt de Hadamard-poort geïmplementeerd.
Hiermee worden de Pauli $X $ en $Z $ assen van de doel-Qubit verwisseld, zodat $H \ket{0} = \ket{+} \mathrel{: =} (\ket{0} + \ket{1})/\sqrt{2}$ en $H \ket{+} = \ket{0}$.
Het bevat hand tekeningen `(Qubit => Unit is Adj + Ctl)`en komt overeen met de single-Qubit unitary:

\begin{Equation} \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\\\% controle: dit maakt momenteel gebruik van de quadwhack hack.
1 &-1 \end{bmatrix} \end{Equation}

De Hadamard-Gate is bijzonder belang rijk, omdat deze kan worden gebruikt om een super positie te maken van de $ \ket{0}$ en $ \ket{1}$ States. In de weer gave van de Bloch-bol is het het gemakkelijkst om dit te zien als een rotatie van $ \ket{\psi} $ rond de x-as met $ \pi $ radialen ($ 180 ^ \circ $), gevolgd door een (rechtsom) draaiing rond de y-as met $ \ pi/2 $ radialen ($ 90 ^ \circ $):

![Bewerking Hadamard is toegewezen aan de Bloch-bol](~/media/prelude_hadamardBloch.png)

Met de <xref:microsoft.quantum.intrinsic.s> bewerking wordt de Phase-Gate geïmplementeerd $S $.
Dit is de matrix wortel van de Pauli $Z $-bewerking.
Dat wil zeggen $S ^ 2 = Z $.
Het bevat hand tekeningen `(Qubit => Unit is Adj + Ctl)`en komt overeen met de single-Qubit unitary:

\begin{Equation} \begin{bmatrix} 1 & 0 \\\\% controle: dit maakt momenteel gebruik van de quadwhack hack.
0 & \end{bmatrix} \end{Equation}

#### <a name="rotations"></a>Rotaties ####

Naast de bovenstaande Pauli-en Clifford-bewerkingen biedt Q # prelude diverse manieren om draaiingen uit te drukken.
Zoals beschreven in [Single-Qubit bewerkingen](xref:microsoft.quantum.concepts.qubit#single-qubit-operations), is de mogelijkheid om te draaien essentieel voor Quantum algoritmen.

We beginnen met het aanroepen van een bewerking met één Qubit met de $H $ en $T $ Gates, waarbij $H $ de Hadamard-bewerking is, en waarbij \begin{Equation} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\\\% controle: dit maakt momenteel gebruik van de Quad back Swagger hack.
0 & e ^ {i \pi/4} \end{bmatrix} \end{Equation} dit is de vierkantswortel van de <xref:microsoft.quantum.intrinsic.s> bewerking, zoals $T ^ 2 = S $.
De $T $ Gate wordt geïmplementeerd door de <xref:microsoft.quantum.intrinsic.t> bewerking en heeft hand tekening `(Qubit => Unit is Adj + Ctl)`, waarmee wordt aangegeven dat het een unitary-bewerking is op één Qubit.

Hoewel dit in principe voldoende is om een wille keurige bewerking met één Qubit te beschrijven, hebben verschillende doel machines mogelijk een efficiëntere weer gave voor rotaties over Pauli-Opera Tors, zodat de prelude een aantal manieren heeft om te convienently deze draaiing uitdrukken.
De meeste basis hiervan is de <xref:microsoft.quantum.intrinsic.r> bewerking, die een rotatie rond een opgegeven Pauli-as implementeert, \begin{Equation} R (\sigma, \phi) \mathrel{: =} \exp (-i \phi \sigma/2), \end{Equation} waarbij $ \sigma $ een Pauli-operator is, $ \phi $ is een hoek en waarbij $ \exp $ de matrix exponentieel aangeeft.
Er zijn hand tekeningen `((Pauli, Double, Qubit) => Unit is Adj + Ctl)`, waarbij de eerste twee delen van de invoer de klassieke argumenten $ \sigma $ en $ \phi $ bevatten die nodig zijn om de unitary-operator $R (\sigma, \phi) $ op te geven.
We kunnen $ \sigma $ en $ \phi $ deels Toep assen om een bewerking te verkrijgen waarvan het type van een single-Qubit unitary is.
`R(PauliZ, PI() / 4, _)` heeft bijvoorbeeld het type `(Qubit => Unit is Adj + Ctl)`.

> [!NOTE]
> De <xref:microsoft.quantum.intrinsic.r>-bewerking deelt de invoer hoek met 2 en vermenigvuldigt deze met-1.
> Voor $Z $ rotations betekent dit dat de $ \ket{0}$ eigenstate wordt geroteerd door $-\phi/$2 en de $ \ket{1}$ eigenstate wordt geroteerd door $ \phi/$2, zodat de $ \ket-{1}$ eigenstate wordt geroteerd door $ \phi $ ten opzichte van $ \ket{0}$ eigenstate.
>
> Dit betekent met name dat `T` en `R(PauliZ, PI() / 8, _)` alleen van een irrelevante [globale fase](xref:microsoft.quantum.glossary#global-phase)verschillen.
> Daarom wordt $T $ ook wel de $ \frac{\pi}-{8}$-Gate genoemd.
>
> Houd er ook rekening mee dat draait rond `PauliI` gewoon een globale fase van $ \phi/$2 toepast. Hoewel deze fasen niet van belang zijn, zoals in [de conceptuele documenten](xref:microsoft.quantum.concepts.qubit)is gevoerd, zijn ze relevant voor beheerde `PauliI` draaiingen.

Binnen Quantum-algoritmen is het vaak handig om rotaties als dyadic fracties te expresseren, zodat $ \phi = \pi k/2 ^ n $ voor sommige $k \in \mathbb{Z} $ en $n \in \mathbb{N} $.
Met de <xref:microsoft.quantum.intrinsic.rfrac> bewerking wordt een rotatie rond een opgegeven Pauli-as geïmplementeerd met deze Conventie.
Dit verschilt van <xref:microsoft.quantum.intrinsic.r> in de draai hoek wordt opgegeven als twee invoer van het type `Int`, geïnterpreteerd als een dyadic-Fractie.
`RFrac` heeft daarom hand tekening `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)`.
Het implementeert de single-Qubit unitary $ \exp (i \pi k \sigma/2 ^ n) $, waarbij $ \sigma $ de Pauli matrix is die overeenkomt met het eerste argument, $k $ het tweede argument is en $n $ het derde argument is.
`RFrac(_,k,n,_)` is hetzelfde als `R(_,-πk/2^n,_)`; Houd er rekening mee dat de hoek de *negatieve* waarde van de Fractie.

De <xref:microsoft.quantum.intrinsic.rx>-bewerking implementeert een rotatie rond de Pauli $X $ as.
Het bevat handtekening `((Double, Qubit) => Unit is Adj + Ctl)`.
`Rx(_, _)` is hetzelfde als `R(PauliX, _, _)`.

De <xref:microsoft.quantum.intrinsic.ry>-bewerking implementeert een rotatie rond de Pauli $Y $ as.
Het bevat handtekening `((Double, Qubit) => Unit is Adj + Ctl)`.
`Ry(_, _)` is hetzelfde als `R(PauliY,_ , _)`.

De <xref:microsoft.quantum.intrinsic.rz>-bewerking implementeert een rotatie rond de Pauli $Z $ as.
Het bevat handtekening `((Double, Qubit) => Unit is Adj + Ctl)`.
`Rz(_, _)` is hetzelfde als `R(PauliZ, _, _)`.

Met de <xref:microsoft.quantum.intrinsic.r1> bewerking wordt een rotatie geïmplementeerd met de opgegeven hoeveelheid rond $ \ket{1}$, de $-$1 eigenstate van $Z $.
Het bevat handtekening `((Double, Qubit) => Unit is Adj + Ctl)`.
`R1(phi,_)` is hetzelfde als `R(PauliZ,phi,_)` gevolgd door `R(PauliI,-phi,_)`.

Met de <xref:microsoft.quantum.intrinsic.r1frac> bewerking wordt een gedeeltelijke draaiing geïmplementeerd met de opgegeven hoeveelheid rond de Z = 1 eigenstate.
Het bevat handtekening `((Int,Int, Qubit) => Unit is Adj + Ctl)`.
`R1Frac(k,n,_)` is hetzelfde als `RFrac(PauliZ,-k.n+1,_)` gevolgd door `RFrac(PauliI,k,n+1,_)`.

Hieronder ziet u een voor beeld van een rotatie bewerking (rond de Pauli $Z $ as, in dit geval) die is toegewezen aan de Bloch-bol:

![Rotatie bewerking die is toegewezen aan de Bloch-bol](~/media/prelude_rotationBloch.png)

#### <a name="multi-qubit-operations"></a>Multi-Qubit bewerkingen ####

Naast de bovenstaande bewerkingen met één Qubit definieert de prelude ook enkele multi-Qubit bewerkingen.

Eerst voert de <xref:microsoft.quantum.intrinsic.cnot> bewerking een standaard Controlled-`NOT` Gate, \begin{Equation} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \\\\ 0 & 0 & 1 & 0 \end{bmatrix}.
\end{Equation} heeft een handtekening `((Qubit, Qubit) => Unit is Adj + Ctl)`, die aangeeft dat $ \operatorname{CNOT} $ unitarily op twee afzonderlijke qubits.
`CNOT(q1, q2)` is hetzelfde als `(Controlled X)([q1], q2)`.
Omdat de `Controlled` functor in staat is om op een REGI ster te beheren, gebruiken we de matrix letterlijke waarde `[q1]` om aan te geven dat we alleen het ene besturings element willen.

Met de <xref:microsoft.quantum.intrinsic.ccnot> bewerking wordt een niet-Gate met dubbele controle uitgevoerd, ook wel bekend als de Toffoli-poort.
Het bevat handtekening `((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)`.
`CCNOT(q1, q2, q3)` is hetzelfde als `(Controlled X)([q1, q2], q3)`.

Met de <xref:microsoft.quantum.intrinsic.swap> bewerking worden de Quantum statussen van twee qubits gewisseld.
Dat wil zeggen, implementeert de unitary-matrix \begin{Equation} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{bmatrix}.
\end{Equation} heeft een handtekening `((Qubit, Qubit) => Unit is Adj + Ctl)`.
`SWAP(q1,q2)` komt overeen met `CNOT(q1, q2)` gevolgd door `CNOT(q2, q1)` en `CNOT(q1, q2)`.

> [!NOTE]
> De SWAP-Gate is *niet* hetzelfde als het opnieuw rangschikken van de elementen van een variabele met het type `Qubit[]`.
> Het Toep assen van `SWAP(q1, q2)` veroorzaakt een wijziging in de status van de qubits waarnaar wordt verwezen door `q1` en `q2`, terwijl `let swappedRegister = [q2, q1];` alleen invloed heeft op de manier waarop we verwijzen naar die qubits.
> Bovendien kan `(Controlled SWAP)([q0], (q1, q2))` toestaan dat `SWAP` voor waarden in de staat van een derde Qubit, die we niet kunnen vertegenwoordigen door elementen opnieuw te rangschikken.
> De Controlled-SWAP-Gate, ook wel bekend als de Fredkin-poort, is krachtig genoeg om alle klassieke berekeningen uit te sluiten.

Ten slotte biedt de prelude twee bewerkingen voor het weer geven van exponenten van de Pauli Opera tors van meerdere Qubit.
De <xref:microsoft.quantum.intrinsic.exp> bewerking voert een rotatie uit op basis van een tensor product van Pauli-matrices, zoals vertegenwoordigd door de multi-Qubit unitary \begin{Equation} \operatorname{Exp} (\vec{\sigma}, \phi) \mathrel{: =} \exp\left (i \phi \ sigma_0 \otimes \ sigma_1 \otimes \cdots \otimes \ sigma_n \right), \end{Equation} waarbij $ \vec{\sigma} = (\ sigma_0, \ sigma_1, \dots, \ sigma_n) $ is een opeenvolging van single-Qubit Pauli-Opera tors en, waarbij $ \phi $ een hoek is.
De `Exp` rotatie vertegenwoordigt $ \vec{\sigma} $ als een matrix met `Pauli` elementen, zodat de hand tekening `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)`heeft.

De <xref:microsoft.quantum.intrinsic.expfrac>-bewerking voert dezelfde draaiing uit met behulp van de dyadic-fractie notatie die hierboven wordt beschreven.
Het bevat handtekening `((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)`.

> [!WARNING]
> Exponentieel van het tensor product van Pauli-Opera tors zijn niet hetzelfde als tensor-producten van de exponenten van Pauli-Opera tors.
> Dat wil zeggen, $e ^ {i (Z \otimes Z) \phi} \ne e ^ {i Z \phi} \otimes e ^ {i Z \phi} $.

### <a name="measurements"></a>Metingen ###

Bij het meten moet de + 1-eigenvalue van de operator worden gemeten, overeenkomt met een `Zero` resultaat en de eigenvalue-1 tot een `One` resultaat.

> [!NOTE]
> Hoewel deze Conventie mogelijk oneven lijkt, heeft deze twee zeer goede voor delen.
> Eerst moet het resultaat $ \ket{0}$ worden geobserveerd door de `Result` waarde `Zero`, terwijl $ \ket{1}$ overeenkomt met `One`.
> Ten tweede kunnen we schrijven dat de eigenvalue $ \lambda $ die overeenkomt met een resultaat $r $ $ \lambda = (-1) ^ r $ is.

Meting bewerkingen ondersteunen noch de `Adjoint` noch de `Controlled` functor.

Met de <xref:microsoft.quantum.intrinsic.measure> bewerking wordt een gemeen schappelijke meting uitgevoerd van een of meer qubits in het opgegeven product van Pauli-Opera tors.
Als de matrix Pauli en Qubit verschillende lengten hebben, mislukt de bewerking.
`Measure` heeft hand tekening `((Pauli[], Qubit[]) => Result)`.

Houd er rekening mee dat een gezamenlijke meting niet hetzelfde is als het meten van elk Qubit afzonderlijk.
Bekijk bijvoorbeeld de status $ \ket{11} = \ket{1} \otimes \ket{1} = X\otimes X \ket{00}$.
Voor het meten van $Z _0 $ en $Z _1 $ elke afzonderlijke, krijgen we de resultaten $r _0 = $1 en $r _1 = $1.
Meten $Z _0 Z_1 $, krijgen we echter het enige resultaat $r _ {\textrm{joint}} = $0, die aangeeft dat de paren van $ \ket{11}$ positief is.
Plaats een andere $ (-1) ^ {r_0 + r_1} = (-1) ^ r_ {\textrm{joint}}) $.
Omdat we de pariteit van deze meting *alleen* kunnen zien, worden alle gegevens van de Quantum die worden weer gegeven in de superpositie tussen de 2 2-Qubit-statussen van positieve pariteit, $ \ket{00}$ en $ \ket{11}$, bewaard.
Deze eigenschap is op een later tijdstip essentieel, omdat de fout correctie wordt besproken.

Voor het gemak biedt de prelude ook twee andere bewerkingen voor het meten van qubits.
Ten eerste, omdat het uitvoeren van metingen met één Qubit heel gebruikelijk is, definieert de prelude een steno voor deze aanvraag.
De <xref:microsoft.quantum.intrinsic.m> bewerking meet de Pauli $Z $-operator op één Qubit en heeft hand tekening `(Qubit => Result)`.
`M(q)` is gelijk aan `Measure([PauliZ], [q])`.

De <xref:microsoft.quantum.measurement.multim> meet de Pauli $Z $-operator *afzonderlijk* op elke matrix van qubits en retourneert de *matrix* van `Result` waarden die zijn verkregen voor elke qubit.
In sommige gevallen kan dit worden geoptimaliseerd. Deze heeft hand tekening (`Qubit[] => Result[])`.
`MultiM(qs)` is gelijk aan:

```qsharp
mutable rs = new Result[Length(qs)];
for (index in 0..Length(qs)-1)
{
    set rs[index] = M(qs[index]);
}
return rs;
```

## <a name="extension-functions-and-operations"></a>Uitbreidings functies en-bewerkingen ##

Daarnaast definieert de prelude een uitgebreide set wiskundige en type conversie functies op .NET-niveau voor gebruik binnen Q #-code.
Zo definieert de <xref:microsoft.quantum.extensions.math> naam ruimte nuttige bewerkingen, zoals <xref:microsoft.quantum.extensions.math.sin> en <xref:microsoft.quantum.extensions.math.log>.
De implementatie van de Quantum Development Kit maakt gebruik van de klassieke .NET-basis klassen bibliotheek en kan daarom een extra communicatie tussen Quantum Program ma's en hun klassieke Stuur Programma's tot stand brengen.
Hoewel dit geen probleem voor een lokale Simulator voordoet, kan dit een prestatie probleem zijn bij het gebruik van een externe Simulator of een echte hardware als doel computer.
Op die manier kan een individuele doel computer deze invloed op de prestaties beperken door deze bewerkingen te overschrijven met versies die efficiënter zijn voor dat specifieke systeem.

### <a name="math"></a>Kundig ###

De naam ruimte <xref:microsoft.quantum.extensions.math> biedt veel nuttige functies uit de [`System.Math` klasse](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1)van de .net-basis klasse.
Deze functies kunnen op dezelfde manier worden gebruikt als andere Q #-functies:

```qsharp
open Microsoft.Quantum.Math;
// ...
let y = Sin(theta);
```

Wanneer een statische .NET-methode is overbelast op basis van het type van de argumenten, wordt de bijbehorende Q #-functie vermeld met een achtervoegsel dat het type invoer aangeeft:

```qsharp
let x = AbsI(-3); // x : Int = 3
let y = AbsD(-PI()); // y : Double = 3.1415...
```


### <a name="bitwise-operations"></a>Bitsgewijze bewerkingen ###

Ten slotte biedt de <xref:microsoft.quantum.extensions.bitwise> naam ruimte verschillende handige functies voor het bewerken van gehele getallen via bitsgewijze Opera tors.
<xref:microsoft.quantum.extensions.bitwise.parity> retourneert bijvoorbeeld de bitsgewijze pariteit van een geheel getal als een geheel getal.
