---
title: Intrinsieke bewerkingen en functies in de QDK
description: Meer informatie over de intrinsieke bewerkingen en functies in de QDK, waaronder klassieke functies en unitary, rotatie-en meet bewerkingen.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.prelude
no-loc:
- Q#
- $$v
ms.openlocfilehash: dd507d0c644ae711a5e5a1dff9156f571cb0fa92
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833550"
---
# <a name="the-prelude"></a>De prelude #

De Q# compiler en de doel computers die deel uitmaken van de Quantum Development Kit bieden een reeks ingebouwde functies en bewerkingen die kunnen worden gebruikt bij het schrijven van Quantum Program ma's in Q# .

## <a name="intrinsic-operations-and-functions"></a>Intrinsieke bewerkingen en functies ##

De intrinsieke bewerkingen die in de standaard bibliotheek zijn gedefinieerd, vallen ongeveer in een van de volgende categorieën:

- Essentiële klassieke functies die zijn verzameld in de <xref:microsoft.quantum.core> naam ruimte.
- Bewerkingen voor unitaries die bestaan uit [Clifford en $T $ Gates](xref:microsoft.quantum.concepts.qubit).
- Bewerkingen die betrekking hebben op rotaties over verschillende Opera tors.
- Bewerkingen geïmplementeerd metingen.

Omdat de Clifford + $T $ Gate-set is ingesteld op [Universal](xref:microsoft.quantum.concepts.multiple-qubits) voor Quantum Computing, zijn deze bewerkingen voldoende om een Quantum algoritme te implementeren in negligibly kleine fout.
Door draaiing te bieden, Q# kan de programmeur binnen de single Qubit unitary-en CNOT-poort bibliotheek werken. Deze bibliotheek is veel gemakkelijker te zien, omdat het niet vereist is dat de programmeur rechtstreeks de Clifford + $T $ decompileren en omdat er zeer efficiënte methoden bestaan voor het samen stellen van één Qubit unitaries in Clifford en $T $ Gates (Zie [hier](xref:microsoft.quantum.more-information) voor meer informatie).

Waar mogelijk, de bewerkingen die zijn gedefinieerd in de prelude die op qubits zijn toegestaan voor het Toep assen van de `Controlled` Variant, zodat de doel computer de juiste ontleding uitvoert.

Veel van de functies en bewerkingen die in dit gedeelte van de prelude zijn gedefinieerd, bevinden zich in de @"microsoft.quantum.intrinsic" naam ruimte, zodat Q# de meeste bron bestanden een instructie hebben die `open Microsoft.Quantum.Intrinsic;` direct volgt op de oorspronkelijke naam ruimte declaratie.
De <xref:microsoft.quantum.core> naam ruimte wordt automatisch geopend, zodat functies zoals <xref:microsoft.quantum.core.length> kan worden gebruikt zonder een `open` instructie.

### <a name="common-single-qubit-unitary-operations"></a>Algemene single-Qubit unitary-bewerkingen ###

De prelude definieert ook veel veelvoorkomende [bewerkingen met één Qubit](xref:microsoft.quantum.concepts.qubit#single-qubit-operations).
Voor al deze bewerkingen zijn zowel de `Controlled` als- `Adjoint` functors toegestaan.

#### <a name="pauli-operators"></a>Pauli-Opera tors ####

Met de <xref:microsoft.quantum.intrinsic.x> bewerking wordt de Pauli $X $-operator geïmplementeerd.
Dit wordt soms ook wel de `NOT` poort genoemd.
Deze heeft hand tekening `(Qubit => Unit is Adj + Ctl)` .
Dit komt overeen met de unitary met één Qubit:

\begin{Equation} \begin{bmatrix} 0 & 1 \\ \\ % controle: dit maakt momenteel gebruik van de quadwhack hack.
1 & 0 \end{bmatrix} \end{Equation}

Met de <xref:microsoft.quantum.intrinsic.y> bewerking wordt de Pauli $Y $-operator geïmplementeerd.
Deze heeft hand tekening `(Qubit => Unit is Adj + Ctl)` .
Dit komt overeen met de unitary met één Qubit:

\begin{Equation} \begin{bmatrix} 0 &-i \\ \\ % controle: dit maakt momenteel gebruik van de quadwhack hack.
Ik & 0 \end{bmatrix} \end{Equation}

Met de <xref:microsoft.quantum.intrinsic.z> bewerking wordt de Pauli $Z $-operator geïmplementeerd.
Deze heeft hand tekening `(Qubit => Unit is Adj + Ctl)` .
Dit komt overeen met de unitary met één Qubit:

\begin{Equation} \begin{bmatrix} 1 & 0 \\ \\ % controle: dit maakt momenteel gebruik van de quadwhack hack.
0 &-1 \end{bmatrix} \end{Equation}

Hieronder ziet u de trans formaties die zijn toegewezen aan de [Bloch-bol](xref:microsoft.quantum.concepts.qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere) (de rotatieas in elke case is rood gemarkeerd):

![Pauli-bewerkingen die zijn toegewezen aan de Bloch-bol](~/media/prelude_pauliBloch.png)

Het is belang rijk te weten dat het Toep assen van dezelfde Pauli-Gate twee maal op dezelfde Qubit de bewerking annuleert (omdat u nu een volledige draaiing van 2π (360 °) over het Opper vlak naar de Bloch-bol hebt uitgevoerd, waardoor er op het begin punt weer een bericht binnenkomt. Dit brengt ons de volgende identiteit:

$ $ X ^ 2 = Y ^ 2 = Z ^ 2 = \boldone $ $

Dit kan worden visualised op de Bloch-bol:

![XX = I](~/media/prelude_blochIdentity.png)

#### <a name="other-single-qubit-cliffords"></a>Andere single-Qubit Cliffords ####

Met de <xref:microsoft.quantum.intrinsic.h> bewerking wordt de Hadamard-Gate geïmplementeerd.
Hiermee worden de Pauli $X $ en $Z $ assen van de doel-Qubit verwisseld, zodat $H \ket {0} = \ket{+} \mathrel{: =} (\ket {0} + \ket {1} )/\sqrt {2} $ en $H \ket{+} = \ket {0} $.
Het heeft hand tekening `(Qubit => Unit is Adj + Ctl)` en komt overeen met de single-Qubit unitary:

\begin{Equation} \frac {1} {\sqrt {2} } \begin{bmatrix} 1 & 1 \\ \\ % controle: dit maakt momenteel gebruik van de quadwhack hack.
1 &-1 \end{bmatrix} \end{Equation}

De Hadamard-poort is met name belang rijk, omdat deze kan worden gebruikt voor het maken van een super positie van $ \ket {0} $ en $ \ket {1} $ States. In de weer gave van de Bloch-bol is het het gemakkelijkst om dit te zien als een rotatie van $ \ket{\psi} $ rond de x-as met $ \pi $ radialen ($ 180 ^ \circ $), gevolgd door een (rechtsom) draaiing rond de y-as met $ \ pi/2 $ radialen ($ 90 ^ \circ $):

![Bewerking Hadamard is toegewezen aan de Bloch-bol](~/media/prelude_hadamardBloch.png)

Met deze <xref:microsoft.quantum.intrinsic.s> bewerking wordt de Phase-gate $S $ geïmplementeerd.
Dit is de matrix wortel van de Pauli $Z $-bewerking.
Dat wil zeggen $S ^ 2 = Z $.
Het heeft hand tekening `(Qubit => Unit is Adj + Ctl)` en komt overeen met de single-Qubit unitary:

\begin{Equation} \begin{bmatrix} 1 & 0 \\ \\ % controle: dit maakt momenteel gebruik van de quadwhack hack.
0 & \end{bmatrix} \end{Equation}

#### <a name="rotations"></a>Rouleringen ####

Naast de bovenstaande Pauli-en Clifford-bewerkingen biedt de Q# prelude diverse manieren om draaiingen uit te drukken.
Zoals beschreven in [Single-Qubit bewerkingen](xref:microsoft.quantum.concepts.qubit#single-qubit-operations), is de mogelijkheid om te draaien essentieel voor Quantum algoritmen.

We beginnen met het opnieuw aanroepen van een bewerking met één Qubit met de $H $ en $T $ Gates, waarbij $H $ de Hadamard-bewerking is, en waarbij \begin{Equation} T \mathrel{: =} \begin{bmatrix} 1 & 0 \\ \\ % controle: dit maakt momenteel gebruik van de Quad back Swagger hack.
0 & e ^ {i \pi/4} \end{bmatrix} \end{Equation} dit is de vierkantswortel van de <xref:microsoft.quantum.intrinsic.s> bewerking, bijvoorbeeld $T ^ 2 = S $.
De $T $ Gate wordt geïmplementeerd door de <xref:microsoft.quantum.intrinsic.t> bewerking en heeft hand tekening `(Qubit => Unit is Adj + Ctl)` , wat aangeeft dat het een unitary-bewerking is op een enkele Qubit.

Hoewel dit in principe voldoende is om een wille keurige bewerking met één Qubit te beschrijven, hebben verschillende doel machines mogelijk een efficiëntere weer gave voor rotaties over Pauli-Opera Tors, zodat de prelude een aantal manieren bevat om dergelijke draaiingen te convienentlyen.
De meest algemene van deze is de <xref:microsoft.quantum.intrinsic.r> bewerking, die een rotatie rond een opgegeven Pauli-as implementeert, \Begin{Equation} R (\sigma, \phi) \mathrel{: =} \exp (-i \phi \sigma/2), \end{Equation} waarbij $ \sigma $ een Pauli-operator is, $ \phi $ is een hoek en waarbij $ \exp $ de matrix exponentiële aangeeft.
Het heeft hand tekening `((Pauli, Double, Qubit) => Unit is Adj + Ctl)` , waarbij de eerste twee delen van de invoer de klassieke argumenten $ \sigma $ en $ \phi $ bevatten die nodig zijn om de unitary-operator op te geven $R (\sigma, \phi) $.
We kunnen $ \sigma $ en $ \phi $ deels Toep assen om een bewerking te verkrijgen waarvan het type van een single-Qubit unitary is.
Bijvoorbeeld, is van het `R(PauliZ, PI() / 4, _)` type `(Qubit => Unit is Adj + Ctl)` .

> [!NOTE]
> De <xref:microsoft.quantum.intrinsic.r> bewerking deelt de invoer hoek met 2 en vermenigvuldigt deze met-1.
> Voor $Z $ rotations betekent dit dat $ \ket {0} $ eigenstate wordt geroteerd door $-\phi/$2 en dat $ \ket {1} $ eigenstate wordt geroteerd door $ \phi/$2, zodat $ \ket {1} $ eigenstate wordt geroteerd door $ \phi $ ten opzichte van $ \ket {0} $ eigenstate.
>
> Dit betekent met name dat `T` en `R(PauliZ, PI() / 8, _)` anders alleen door een irrelevante [globale fase](xref:microsoft.quantum.glossary#global-phase).
> Daarom wordt $T $ ook wel de $ \frac{\pi} {8} $-Gate genoemd.
>
> Houd er ook rekening mee dat draait om `PauliI` simpelweg een globale fase van $ \phi/$2 toe te staan. Hoewel deze fasen niet van belang zijn, zoals in [de conceptuele documenten](xref:microsoft.quantum.concepts.qubit)is gevoerd, zijn ze relevant voor beheerde `PauliI` draaiingen.

Binnen Quantum-algoritmen is het vaak handig om rotaties als dyadic fracties te expresseren, zodat $ \phi = \pi k/2 ^ n $ voor sommige $k \in \mathbb{Z} $ en $n \in \mathbb{N} $.
<xref:microsoft.quantum.intrinsic.rfrac>Met deze bewerking wordt een rotatie rond een opgegeven Pauli-as met deze Conventie geïmplementeerd.
Het verschil <xref:microsoft.quantum.intrinsic.r> is dat de draai hoek wordt opgegeven als twee invoer typen `Int` , geïnterpreteerd als een dyadic Fractie.
Daarom `RFrac` heeft hand tekening `((Pauli, Int, Int, Qubit) => Unit is Adj + Ctl)` .
Het implementeert de single-Qubit unitary $ \exp (i \pi k \sigma/2 ^ n) $, waarbij $ \sigma $ de Pauli matrix is die overeenkomt met het eerste argument, $k $ het tweede argument is en $n $ het derde argument is.
`RFrac(_,k,n,_)` is hetzelfde als `R(_,-πk/2^n,_)` . Houd er rekening mee dat de hoek de *negatieve* waarde van de Fractie.

Met de <xref:microsoft.quantum.intrinsic.rx> bewerking wordt een draaiing rond de Pauli $X $ as geïmplementeerd.
Deze heeft hand tekening `((Double, Qubit) => Unit is Adj + Ctl)` .
`Rx(_, _)` is hetzelfde als `R(PauliX, _, _)` .

Met de <xref:microsoft.quantum.intrinsic.ry> bewerking wordt een draaiing rond de Pauli $Y $ as geïmplementeerd.
Deze heeft hand tekening `((Double, Qubit) => Unit is Adj + Ctl)` .
`Ry(_, _)` is hetzelfde als `R(PauliY,_ , _)` .

Met de <xref:microsoft.quantum.intrinsic.rz> bewerking wordt een draaiing rond de Pauli $Z $ as geïmplementeerd.
Deze heeft hand tekening `((Double, Qubit) => Unit is Adj + Ctl)` .
`Rz(_, _)` is hetzelfde als `R(PauliZ, _, _)` .

<xref:microsoft.quantum.intrinsic.r1>Met de bewerking wordt een rotatie geïmplementeerd met de opgegeven hoeveelheid rond $ \ket {1} $, de $-$1 eigenstate van $Z $.
Deze heeft hand tekening `((Double, Qubit) => Unit is Adj + Ctl)` .
`R1(phi,_)` is hetzelfde als `R(PauliZ,phi,_)` gevolgd door `R(PauliI,-phi,_)` .

<xref:microsoft.quantum.intrinsic.r1frac>Met de bewerking wordt een gedeeltelijke draaiing geïmplementeerd met de opgegeven hoeveelheid rond de Z = 1 eigenstate.
Deze heeft hand tekening `((Int,Int, Qubit) => Unit is Adj + Ctl)` .
`R1Frac(k,n,_)` is hetzelfde als `RFrac(PauliZ,-k.n+1,_)` gevolgd door `RFrac(PauliI,k,n+1,_)` .

Hieronder ziet u een voor beeld van een rotatie bewerking (rond de Pauli $Z $ as, in dit geval) die is toegewezen aan de Bloch-bol:

![Rotatie bewerking die is toegewezen aan de Bloch-bol](~/media/prelude_rotationBloch.png)

#### <a name="multi-qubit-operations"></a>Multi-Qubit bewerkingen ####

Naast de bovenstaande bewerkingen met één Qubit definieert de prelude ook enkele multi-Qubit bewerkingen.

Ten eerste <xref:microsoft.quantum.intrinsic.cnot> voert de bewerking een standaard Controlled- `NOT` Gate, \begin{Equation} \operatorname{CNOT} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \\ \\ 0 & 0 & 1 & 0 \end{bmatrix}.
\end{Equation} heeft een hand tekening, waarmee wordt aangegeven `((Qubit, Qubit) => Unit is Adj + Ctl)` dat $ \operatorname{CNOT} $ unitarily op twee afzonderlijke qubits.
`CNOT(q1, q2)` is hetzelfde als `(Controlled X)([q1], q2)` .
Omdat de `Controlled` functor voor het beheren van een REGI ster toestaat, gebruiken we de matrix letterlijke waarde `[q1]` om aan te geven dat we alleen het ene besturings element willen.

Met de <xref:microsoft.quantum.intrinsic.ccnot> bewerking wordt een niet-Gate met dubbele controle uitgevoerd, ook wel bekend als de Toffoli-poort.
Deze heeft hand tekening `((Qubit, Qubit, Qubit) => Unit is Adj + Ctl)` .
`CCNOT(q1, q2, q3)` is hetzelfde als `(Controlled X)([q1, q2], q3)` .

<xref:microsoft.quantum.intrinsic.swap>Met deze bewerking worden de Quantum statussen van twee qubits gewisseld.
Dat wil zeggen, implementeert de unitary-matrix \begin{Equation} \operatorname{SWAP} \mathrel{: =} \begin{bmatrix} 1 & 0 & 0 & 0 \\ \\ 0 & 0 & 1 & 0 \\ \\ 0 & 1 & 0 & 0 \\ \\ 0 & 0 & 0 & 1 \end{bmatrix}.
\end{Equation} heeft een hand tekening `((Qubit, Qubit) => Unit is Adj + Ctl)` .
`SWAP(q1,q2)` is gelijk aan `CNOT(q1, q2)` gevolgd door `CNOT(q2, q1)` en vervolgens `CNOT(q1, q2)` .

> [!NOTE]
> De SWAP-Gate is *niet* hetzelfde als de elementen van een variabele met type `Qubit[]` .
> Met Toep assen `SWAP(q1, q2)` wordt een wijziging in de status van de qubits waarnaar `q1` wordt verwezen door en `q2` , en `let swappedRegister = [q2, q1];` is alleen van invloed op de manier waarop we verwijzen naar die qubits.
> Daarnaast kan `(Controlled SWAP)([q0], (q1, q2))` `SWAP` de status van een derde Qubit worden opgegeven, wat niet kan worden aangegeven door elementen opnieuw te rangschikken.
> De Controlled-SWAP-Gate, ook wel bekend als de Fredkin-poort, is krachtig genoeg om alle klassieke berekeningen uit te sluiten.

Ten slotte biedt de prelude twee bewerkingen voor het weer geven van exponenten van de Pauli Opera tors van meerdere Qubit.
De <xref:microsoft.quantum.intrinsic.exp> bewerking voert een rotatie uit op basis van een tensor-product van Pauli-matrices, zoals vertegenwoordigd door de multi-Qubit unitary \Begin{Equation} \operatorname{exp} (\vec{\sigma}, \phi) \mathrel{: =} \exp\left (i \phi \ sigma_0 \otimes \ sigma_1 \otimes \cdots \otimes \ sigma_n \right), \end{Equation} waarbij $ \vec{\sigma} = (\ sigma_0, \ sigma_1, \dots, \ sigma_n) $ is een opeenvolging van single-Qubit Pauli-Opera tors en, waarbij $ \phi $ een hoek is.
De `Exp` rotatie vertegenwoordigt $ \vec{\sigma} $ als een matrix met `Pauli` elementen, zodat het een hand tekening heeft `((Pauli[], Double, Qubit[]) => Unit is Adj + Ctl)` .

De <xref:microsoft.quantum.intrinsic.expfrac> bewerking voert dezelfde draaiing uit met behulp van de dyadic-fractie notatie die hierboven wordt beschreven.
Deze heeft hand tekening `((Pauli[], Int, Int, Qubit[]) => Unit is Adj + Ctl)` .

> [!WARNING]
> Exponentieel van het tensor product van Pauli-Opera tors zijn niet hetzelfde als tensor-producten van de exponenten van Pauli-Opera tors.
> Dat wil zeggen, $e ^ {i (Z \otimes Z) \phi} \ne e ^ {i Z \phi} \otimes e ^ {i Z \phi} $.

### <a name="measurements"></a>Metingen ###

Bij het meten moet de + 1-eigenvalue van de operator worden gemeten, overeenkomt met een `Zero` resultaat en de eigenvalue-1 tot een `One` resultaat.

> [!NOTE]
> Hoewel deze Conventie mogelijk oneven lijkt, heeft deze twee zeer goede voor delen.
> Ten eerste, waarbij het resultaat $ \ket {0} $ wordt weer gegeven door de `Result` waarde `Zero` , terwijl $ \ket {1} $ overeenkomt met `One` .
> Ten tweede kunnen we schrijven dat de eigenvalue $ \lambda $ die overeenkomt met een resultaat $r $ $ \lambda = (-1) ^ r $ is.

Meting bewerkingen ondersteunen noch de `Adjoint` `Controlled` functor.

Met deze <xref:microsoft.quantum.intrinsic.measure> bewerking wordt een gemeen schappelijke meting uitgevoerd van een of meer qubits in het opgegeven product van Pauli-Opera tors.
Als de matrix Pauli en Qubit verschillende lengten hebben, mislukt de bewerking.
`Measure` heeft hand tekening `((Pauli[], Qubit[]) => Result)` .

Houd er rekening mee dat een gezamenlijke meting niet hetzelfde is als het meten van elk Qubit afzonderlijk.
Bekijk bijvoorbeeld de status $ \ket {11} = \ket {1} \otimes \Ket {1} = X\otimes X \ket {00} $.
Voor het meten van $Z _0 $ en $Z _1 $ elke afzonderlijke, krijgen we de resultaten $r _0 = $1 en $r _1 = $1.
Meten $Z _0 Z_1 $, krijgen we echter het enige resultaat $r _ {\textrm{joint}} = $0, waarmee wordt aangegeven dat de paren van $ \ket {11} $ positief zijn.
Plaats een andere $ (-1) ^ {r_0 + r_1} = (-1) ^ r_ {\textrm{joint}}) $.
Omdat we de pariteit van deze meting *alleen* leren kennen, blijven de Quantum gegevens die worden weer gegeven in de superpositie tussen de 2 2-Qubit statussen van positieve pariteit, $ \ket {00} $ en $ \ket {11} $, behouden.
Deze eigenschap is op een later tijdstip essentieel, omdat de fout correctie wordt besproken.

Voor het gemak biedt de prelude ook twee andere bewerkingen voor het meten van qubits.
Ten eerste, omdat het uitvoeren van metingen met één Qubit heel gebruikelijk is, definieert de prelude een steno voor deze aanvraag.
De <xref:microsoft.quantum.intrinsic.m> bewerking meet de Pauli $Z $-operator op één Qubit en heeft hand tekening `(Qubit => Result)` .
`M(q)` is gelijk aan `Measure([PauliZ], [q])` .

De <xref:microsoft.quantum.measurement.multim> meet de Pauli $Z $-operator *afzonderlijk* op elk van een matrix van qubits en retourneert de *matrix* met waarden die zijn `Result` verkregen voor elke qubit.
In sommige gevallen kan dit worden geoptimaliseerd. Deze heeft hand tekening ( `Qubit[] => Result[])` .
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

Daarnaast definieert de prelude een uitgebreide set wiskundige en type conversie functies op .NET-niveau voor gebruik in Q# code.
Zo <xref:microsoft.quantum.math> definieert de naam ruimte nuttige bewerkingen zoals <xref:microsoft.quantum.math.sin> en <xref:microsoft.quantum.math.log> .
De implementatie van de Quantum Development Kit maakt gebruik van de klassieke .NET-basis klassen bibliotheek en kan daarom een extra communicatie tussen Quantum Program ma's en hun klassieke Stuur Programma's tot stand brengen.
Hoewel dit geen probleem voor een lokale Simulator voordoet, kan dit een prestatie probleem zijn bij het gebruik van een externe Simulator of een echte hardware als doel computer.
Op die manier kan een individuele doel computer deze invloed op de prestaties beperken door deze bewerkingen te overschrijven met versies die efficiënter zijn voor dat specifieke systeem.

### <a name="math"></a>Berekeningen ###

De <xref:microsoft.quantum.math> naam ruimte biedt veel nuttige functies van de [ `System.Math` klasse](https://docs.microsoft.com/dotnet/api/system.math?view=netframework-4.7.1&preserve-view=true)van de .net-basis klasse-bibliotheek.
Deze functies kunnen op dezelfde manier worden gebruikt als andere Q# functies:

```qsharp
open Microsoft.Quantum.Math;
// ...
let y = Sin(theta);
```

Wanneer een statische methode van .NET is overbelast op basis van het type van de argumenten, wordt de bijbehorende Q# functie vermeld met een achtervoegsel dat het type invoer aangeeft:

```qsharp
let x = AbsI(-3); // x : Int = 3
let y = AbsD(-PI()); // y : Double = 3.1415...
```


### <a name="bitwise-operations"></a>Bitsgewijze bewerkingen ###

Ten slotte <xref:microsoft.quantum.bitwise> biedt de naam ruimte verschillende handige functies voor het bewerken van gehele getallen via bitsgewijze Opera tors.
<xref:microsoft.quantum.bitwise.parity>Retourneert bijvoorbeeld de bitsgewijze pariteit van een geheel getal als een ander geheel getal.
