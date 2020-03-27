---
title: Pauli metingen
description: Meer informatie over het werken met single-en multi-Qubit Pauli-meet bewerkingen.
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 08babbcb0d6c6c4d83622489bc4ecc811e64829a
ms.sourcegitcommit: a0e50c5f07841b99204c068cf5b5ec8ed087ffea
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/26/2020
ms.locfileid: "80320869"
---
# <a name="pauli-measurements"></a>Pauli metingen

In de vorige discussies hebben we gestreefd naar reken kundige basis metingen.
Er zijn ook andere algemene metingen die zich voordoen bij Quantum Computing en die, vanuit een notatie perspectief, handig zijn om te worden uitgedrukt in termen van reken kundige basis metingen.
Terwijl u met Q # werkt, zijn de meest voorkomende maat eenheden die u in de hand hebt, waarschijnlijk *Paulie metingen*, waarmee reken kundige basis metingen kunnen worden gemeten in andere bases en van de pariteit tussen verschillende qubits.
In dergelijke gevallen is het gebruikelijk om de meting van een Pauli-operator te bespreken, in het algemeen een operator zoals $X, Y, Z $ of $Z \otimes Z, X\otimes X, X\otimes Y $, enzovoort.

> [!TIP]
> In Q # worden Opera tors met meerdere Qubit Pauli doorgaans vertegenwoordigd door matrices van het type `Pauli[]`.
> Als u bijvoorbeeld $X \otimes Z \otimes Y $ wilt weer geven, kunt u de matrix `[PauliX, PauliZ, PauliY]`gebruiken.

Het bespreken van metingen in termen van Pauli-Opera Tors is vooral gebruikelijk in het subveld van Quantum fout correctie.
In Q # volgen we een vergelijk bare Conventie; We verklaren nu deze alternatieve weer gave van metingen.

Voordat u meer informatie krijgt over hoe u een Pauli meting kunt zien, is het handig om te zien wat het meten van één Qubit in een quantum computer met de Quantum status is.
Stel dat er een $n Quantum-status van $-Qubit is; vervolgens wordt een Qubit van de helft van de $2 ^ n $ mogelijkheden waarvan de status kan bestaan, onmiddellijk gemeten.
Met andere woorden, de meting projecteert de Quantum status op een van de twee halve ruimtes.
We kunnen het beste bepalen hoe de meting wordt toegepast op deze intuition.

Om deze subruimten te kunnen identificeren, hebben we een taal nodig om ze te beschrijven.
Een van de manieren om de twee subruimten te beschrijven, is door deze op te geven via een matrix die slechts twee unieke eigenvalues heeft, genomen door de Conventie $ \pm $1.
Voor een eenvoudig voor beeld van het beschrijven van subruimten op deze manier kunt u $Z $:

$ $ \begin{align} Z & = \begin{bmatrix} 1 & 0 \\\\ 0 &-1 \end{bmatrix}.
\end{align} $ $

Door de diagonale elementen van de Pauli-$Z $ matrix te lezen, kunnen we zien dat $Z $ twee eigenvectors heeft, $ \ket{0}$ en $ \ket{1}$, met bijbehorende eigenvalues $ \pm $1.
Als we de Qubit meten en `Zero` verkrijgen (overeenkomend met de status $ \ket{0}$), weten we dat de status van onze Qubit een $ + $1-eigenstate van de operator $Z $ is.
En als we `One`verkrijgen, weet u dat de status van onze Qubit een $-$1-eigenstate van $Z $ is.
Dit proces wordt aangeduid met de taal van Pauli-metingen als ' meet Pauli $Z $ ' en is volledig gelijk aan het uitvoeren van een reken kundige basis meting.

Elke $2 \ Times $2-matrix die een unitary-trans formatie is van $Z $ voldoet ook aan deze criteria.
Dat wil zeggen dat we ook een matrix $A = U ^ \dagger Z U $ gebruiken, waarbij $U $ een andere unitary-matrix is, om een matrix te geven waarin de twee resultaten van een meting in de $ \pm $1 eigenvectors worden gedefinieerd.
De notatie van Pauli metingen verwijst naar deze unitary-equivalentie door $X, Y, Z $ metingen als gelijkwaardige waarden te identificeren die een kan doen om informatie te verkrijgen van een Qubit.
Deze metingen worden hieronder vermeld voor het gemak.


|Pauli meting  |Unitary-trans formatie  |
|-------------------|------------------------|
| $Z $               | $ \boldone $             |
| $X $               | $H $                    |
| $Y $               | $HS ^ {\dagger} $         |

Dat wil zeggen, het gebruik van deze taal, ' Measure $Y $ ' is gelijk aan het Toep assen van $HS ^ \dagger $ en meet vervolgens in de berekening, waarbij [`S`](xref:microsoft.quantum.intrinsic.s) een intrinsieke Quantum bewerking is die ook wel ' Phase-Gate ' wordt genoemd en kan worden gesimuleerd door de unitary-matrix

$ $ \begin{align} S = \begin{bmatrix} 1 & 0 \\\\ 0 & \end{bmatrix}.
\end{align} $ $

Het is ook gelijk aan het Toep assen van $HS ^ \dagger $ aan de Quantum status vector en vervolgens het meten van $Z $, zodat de volgende bewerking gelijk is aan `Measure([PauliY], [q])`:

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

De juiste status zou worden gevonden door terug te gaan naar de reken kundige basis, die bedragen om $SH $ toe te passen op de Quantum status vector. in het bovenstaande code fragment wordt de trans formatie teruggeleid naar de reken kracht automatisch verwerkt door het gebruik van het `within … apply` blok.

In Q # zeggen we het resultaat---dat wil zeggen dat de klassieke informatie die is geëxtraheerd uit interactie met de status---wordt gegeven door een `Result` waarde $j \in \\{\texttt{Zero}, \texttt{One}\\} $ die aangeeft of het resultaat zich in $ (-1) ^ j $ eigenspace van de Pauli-operator gemeten.


## <a name="multiple-qubit-measurements"></a>Metingen met meerdere Qubit

Metingen van Qubit Pauli-Opera tors worden op dezelfde manier gedefinieerd, zoals u kunt zien van:

$ $ Z\otimes Z = \begin{bmatrix}1 & 0 & 0 & 0\\\\ 0 &-1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 & 1 \ end {bmatrix}.
$$

Daarom vormen de tensor-producten van twee Pauli-$Z $-Opera tors een matrix die bestaat uit twee ruimten die bestaan uit $ + $1 en $-$1 eigenvalues.
Net als bij de single-Qubit geldt dat beide een halve ruimte betekenen dat de helft van de toegankelijke vector ruimte behoort tot de $ + $1 eigenspace en de resterende helft naar $-$1 eigenspace.
Over het algemeen is het eenvoudig om te zien uit de definitie van het tensor-product dat een tensor product van Pauli $ $Z-Opera tors en de identiteit hiervan in de hand heeft.
Bijvoorbeeld:

$ $ \begin{align} Z \otimes \boldone = \begin{bmatrix} 1 & 0 & 0 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 &-1 & 0 \\\\ 0 & 0 & 0 &-1 \end{bmatrix}.
\end{align} $ $

Net als voorheen beschrijft elke unitary-trans formatie van dergelijke matrices ook twee halve ruimten die zijn gelabeld met $ \pm $1 eigenvalues.
Bijvoorbeeld $X \otimes X = H\otimes H (Z\otimes Z) H\otimes H $ van de identiteit die $Z = HXH $.
Net als bij het Qubit-geval kunnen alle twee Qubit Pauli-metingen worden geschreven als $U ^ \dagger (Z\otimes \id) U $ voor $4 \ Times $4 unitary-matrices $U $. De trans formaties in de volgende tabel worden opgesomd.

> [!NOTE]
> In de onderstaande tabel gebruiken we $ \operatorname{SWAP} $ om aan te geven dat de matrix $ $ \begin{align} \operatorname{SWAP} & = \left (\begin{matrix} 1 & 0 & 0 & 0 \\\\ 0 & 0 & 1 & 0 \\\\ 0 & 1 & 0 & 0 \\\\ 0 & 0 & 0 & 1 \end{matrix}\right) \end{align} $ $, waarmee de intrinsieke bewerking [`SWAP`](xref:microsoft.quantum.intrinsic)wordt gesimuleerd.

|Pauli meting     |Unitary-trans formatie  |
|----------------------|------------------------|
| $Z \otimes \boldone $ | $ \boldone \otimes \boldone $ |
| $Z \otimes \boldone $ | $ \boldone\otimes \boldone $ |
| $X \otimes \boldone $ | $H \otimes \boldone $ |
| $Y \otimes \boldone $ | $HS ^ \dagger\otimes \boldone $ |
| $ \boldone \otimes Z $ | $ \operatorname{SWAP} $ |
| $ \boldone \otimes X $ | $ (H\otimes \boldone) \operatorname{SWAP} $ |
| $ \boldone \otimes Y $ | $ (HS ^ \dagger\otimes \boldone) \operatorname{SWAP} $ |
| $Z \otimes Z $ | $ \operatorname{CNOT}\_{10}$ |
| $X \otimes Z $ | $ \operatorname{CNOT}\_{10}(H\otimes \boldone) $ |
| $Y \otimes Z $ | $ \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes \boldone) $ |
| $Z \otimes X $ | $ \operatorname{CNOT}\_{10}(\boldone\otimes H) $ |
| $X \otimes X $ | $ \operatorname{CNOT}\_{10}(H\otimes H) $ |
| $Y \otimes X $ | $ \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes H) $ |
| $Z \otimes Y $ | $ \operatorname{CNOT}\_{10}(\boldone \otimes HS ^ \dagger) $ |
| $X \otimes Y $ | $ \operatorname{CNOT}\_{10}(H\otimes HS \dagger) $ |
| $Y \otimes Y $ | $ \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes HS ^ \dagger) $ |

Hier wordt de [`CNOT`](xref:microsoft.quantum.intrinsic.cnot) -bewerking weer gegeven om de volgende reden.
Elke Pauli-meting die geen $ \boldone $-matrix bevat, is gelijk aan een unitary om \otimes Z $ te $Z door de bovenstaande reden.
De eigenvalues van $Z \otimes Z $ is alleen afhankelijk van de pariteit van de qubits die elke reken kundige basis vector vormt, en de beheerde-not-bewerkingen dienen om deze pariteit te berekenen en op te slaan in de eerste bit.
Zodra de eerste bit wordt gemeten, kunnen we de identiteit van de resulterende halve ruimte herstellen, die overeenkomt met het meten van de Pauli-operator.

Een aanvullend Opmerking: Hoewel het mogelijk is om te voor komen dat de meting $Z \otimes Z $ hetzelfde is als het sequentieel meten van $Z \otimes \mathbb{1}$ en vervolgens $ \mathbb{1} \otimes Z $, is deze veronderstelling onwaar.
Het meten van $Z \otimes Z $ projecteert de Quantum status in de $ + $1-of $-$1-eigenstate van deze opera tors.
Meting $Z \otimes \mathbb{1}$ en vervolgens $ \mathbb{1} \otimes Z $ projecteert de Quantum status vector eerst op een halve ruimte van $Z \otimes \mathbb{1}$ en vervolgens op een halve spatie van $ \mathbb{1} \otimes Z $.
Omdat er vier reken kundige basis vectoren zijn, vermindert het uitvoeren van beide metingen de status naar een vierde spatie en vermindert deze in een enkele reken kundige basis vector.

## <a name="correlations-between-qubits"></a>Correlaties tussen qubits
Een andere manier om te kijken naar het meten van tensor-producten van Pauli-matrices zoals $X \otimes X $ of $Z \otimes Z $ is dat u met deze metingen informatie kunt bekijken die is opgeslagen in de correlaties tussen de twee qubits.
Door $X \otimes \id $ te meten, kunt u zien welke gegevens lokaal zijn opgeslagen in de eerste Qubit.
Hoewel beide soorten metingen even waardevol zijn voor Quantum Computing, licht de eerste maal de kracht van Quantum Computing.
In het geval van Quantum Computing is het vaak dat de informatie die u wilt leren, niet is opgeslagen in een enkele Qubit, maar niet lokaal is opgeslagen in alle qubits, en daarom alleen door een gemeen schappelijke meting te bekijken (bijvoorbeeld $Z \otimes Z $). de gegevens worden manifest.

In het geval van een fout correctie willen we vaak weten welke fout is opgetreden tijdens het leren over de status die we proberen te beveiligen.
Het [bit-Flip-code voorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/error-correction/bit-flip-code) toont een voor beeld van hoe u dit kunt doen met behulp van maten als $Z \otimes Z \otimes \id $ en $ \Id \otimes Z \otimes z $.
<!-- TODO: change this to a link to the samples browser as soon as the bit-flip code sample is on-boarded. -->

Wille keurige Pauli-Opera tors zoals $X \otimes Y \otimes Z \otimes \boldone $ kunnen ook worden gemeten.
Al deze tensor-producten van Pauli-Opera tors hebben slechts twee eigenvalues $ \pm $1 en beide eigenspaces vormen een halve ruimte van de hele vector ruimte.
Daarom vallen ze samen met de hierboven vermelde vereisten.

In Q # retourneert deze metingen $j $ als de meting resulteert in een resultaat in de eigenspace van Sign $ (-1) ^ j $.
Het gebruik van Pauli-metingen als een ingebouwde functie in Q # is nuttig omdat het meten van dergelijke Opera tors lange ketens van besturings-en basis transformaties vereist om de diagonalizing $U $-Gate te beschrijven die nodig is om de bewerking uit te geven als een tensor product van $Z $ en $ \id $.
Doordat u kunt opgeven dat u een van deze vooraf gedefinieerde metingen wilt uitvoeren, hoeft u zich geen zorgen te maken over het transformeren van de basis, zodat een reken kundige basis meting de benodigde informatie bevat.
Q # Hiermee worden alle nood zakelijke trans formaties automatisch voor u verwerkt.
Zie voor meer informatie de bewerkingen [`Measure`](xref:microsoft.quantum.intrinsic.measure) en [`MeasurePaulis`](xref:microsoft.quantum.measurement.measurepaulis) .

## <a name="the-no-cloning-theorem"></a>De theorema zonder klonen

De quantum informatie is krachtig.
Hierdoor kunnen we fantastische dingen doen, zoals factor nummers exponentieel sneller dan de best bekende klassieke algoritmen, of op efficiënte wijze simuleren van gecorreleerde elektroden systemen die klassieke kosten in de praktijk nodig hebben om nauw keurig te simuleren.
Er zijn echter beperkingen ten aanzien van de kracht van Quantum Computing.
Een dergelijke beperking wordt gegeven door de *theorema die niet klonen*.

De theorema zonder klonen is aptly met de naam.
Het klonen van generieke Quantum Staten door een quantum computer wordt niet toegestaan.
Het bewijs van de theorema is onduidelijker.
Hoewel een volledig bewijs van het no-klonen van theorema iets te technisch is voor onze bespreking, is de proef in het geval van geen extra hulp qubits binnen onze Scope (hulp qubits worden qubits gebruikt voor Scratch ruimte tijdens een berekening en kunnen ze eenvoudig worden gebruikt en beheerd in Q #, zie <xref:microsoft.quantum.techniques.qubits>).

Voor een dergelijke quantum computer moet de kloon bewerking worden beschreven in een unitary-matrix.
De meting is niet toegestaan omdat de Quantum status die we proberen te klonen, is beschadigd.
Voor het simuleren van de kloon bewerking willen we de unitary-matrix gebruiken om de eigenschap te hebben die $ $ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi} $ $ voor een wille keurige status $ \ket{\psi} $.
De eigenschap Linearity van matrix vermenigvuldiging impliceert dat voor elke tweede Quantum status $ \ket{\phi} $,

$ $ \begin{align} U \left [\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right] \ket{0} & = \frac{1}{\sqrt{2}} U\ket {\ Phi} \ Ket{0} + \frac{1}{\sqrt{2}} U\ket {\ psi} \ Ket{0} \\\\ & = \frac{1}{\sqrt{2}} \left (\ket{\phi} \ket{\phi} + \ket{\psi} \ket{\psi} \right) \\\\ & \ne \left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right) \otimes \ Left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right).
\end{align} $ $

Dit voorziet in de fundamentele Intuition achter het no-klonen theorema: elk apparaat dat een onbekende Quantum status kopieert, moet fouten veroorzaken op ten minste een van de statussen die worden gekopieerd.
Hoewel de sleutel veronderstelling dat de klooner lineair op de invoer status optreedt, kan worden geschonden door de toevoeging en meting van de hulp qubits, wordt ook informatie over het systeem door middel van de meting statistieken gerapporteerd en wordt voor komen dat er exacte in dergelijke gevallen klonen.
Zie [voor meer informatie](xref:microsoft.quantum.more-information)over de theorema die u niet klonen.

Het niet-klonen van theorema is belang rijk voor de kwalitatieve kennis van Quantum Computing omdat als u de Quantum toestanden in de buurt zou kunnen klonen, dan krijgt u een Magical-mogelijkheid om te leren van Quantum Staten.
Het is ook mogelijk dat u het Heisenberg van vaunted onzekerheid schendt.
U kunt ook een optimale kloon gebruiken om één voor beeld van een complexe Quantum distributie te maken en alles te leren over die distributie, van slechts één voor beeld.
Dit is een manier om een munten te spie gelen en op de hoogte te houden en vervolgens een vriend te vertellen over het resultaat van de reactie "Ah de verdeling van die munten moet worden gebernoulli met $p = 0.512643 \ ldots $!"  Een dergelijke instructie zou niet-sensical zijn, omdat een stukje informatie (het resultaat van de kop) simpelweg de vele informatie die nodig is om de distributie te coderen zonder belang rijke eerdere informatie, niet kan leveren.
Op dezelfde manier kunnen we zonder voorafgaande informatie een Quantum staat niet op dezelfde manier klonen als we geen ensemble van deze munten voors bereiden zonder te weten $p $.

Informatie is niet gratis in Quantum Computing.
Elk Qubit dat wordt gemeten, geeft één stukje informatie en het theorema zonder klonen laat zien dat er geen beschik over is die kunnen worden misbruikt om de fundamentele berekenings verhouding te verkrijgen tussen informatie over het systeem en de verstoringen die erop worden opgeroepen.
