---
title: Pauli metingen | Microsoft Docs
description: Pauli metingen
author: QuantumWriter
uid: microsoft.quantum.concepts.pauli
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 7bea821be7e26e72f2860278486d35be676ca63d
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183706"
---
# <a name="pauli-measurements"></a>Pauli metingen

In de vorige discussies hebben we gestreefd naar reken kundige basis metingen.  Er zijn ook andere algemene metingen die zich voordoen bij Quantum Computing en die, vanuit een notatie perspectief, handig zijn om te worden gezien in termen van reken kundige basis metingen.  De meest voorkomende set van deze metingen zijn *Pauli-metingen*.  In dergelijke gevallen is het gebruikelijk om te discussiëren over het meten van een Pauli-operator, in het algemeen een operator zoals $X, Y, Z $ of $Z \otimes Z, X\otimes X, X\otimes Y $ enzovoort.  Het bespreken van metingen in termen van Pauli-Opera Tors is vooral gebruikelijk in het subveld van Quantum fout correctie. In Q # volgen we een vergelijk bare Conventie; We verklaren nu deze alternatieve weer gave van metingen.

Voordat u meer informatie krijgt over hoe u een Pauli meting kunt zien, is het handig om te zien wat het meten van één Qubit in een quantum computer met de Quantum status is.  Stel dat er een $n Quantum-status van $-Qubit is; vervolgens wordt een Qubit van de helft van de $2 ^ n $ mogelijkheden waarvan de status kan bestaan, onmiddellijk gemeten.  Met andere woorden, de meting projecteert de Quantum status op een van de twee halve ruimtes.  We kunnen de methode voor het meten van de meting nadenken.

Om deze subruimten te kunnen identificeren, hebben we een taal nodig om ze te beschrijven.  Een manier om dit te doen is door de twee subruimten te beschrijven door ze op te geven via een matrix die slechts twee unieke eigenvalues heeft, genomen door de Conventie $ \pm $1.  Het eenvoudigste voor beeld hiervan is:

$ $ Z = \begin{bmatrix} 1 & 0 \\\\ 0 &-1 \end{bmatrix}.
$$

De Pauli-$Z $ matrix heeft duidelijk twee eigenvectors $ \ket{0}$ en $ \ket{1}$ met eigenvalues $ \pm $1.  Als we de Qubit meten en $ \ket{0}$ hebben we in de eigenspace $ + $1 (de set van alle vectoren die zijn gevormd door de som van eigenvectors met alleen positieve of negatieve eigenvalues) van de operator en als we $ \ket meten{1}$ hebben we de $-$1 ei genspace van $Z $.  Dit proces wordt aangeduid met de taal van Pauli-metingen als ' meet Pauli $Z $ ' en is volledig gelijk aan het uitvoeren van een reken kundige basis meting.

Voor elke $2 \ Times $2-matrix die een unitary-trans formatie is van $Z $ voldoet ook aan deze criteria.  Dit wil zeggen dat we ook matrix $A = U ^ \dagger Z U $ voor elke unitary matrix $U $ kunnen overwegen om een matrix te geven waarin de twee resultaten van een meting in de $ \pm $1 eigenvectors worden gedefinieerd.  Met de notatie van Pauli metingen wordt dit aangegeven door $X, Y, Z $ metingen als gelijkwaardige waarden te identificeren die één zou kunnen doen om informatie te verkrijgen van een Qubit.  Deze metingen worden hieronder vermeld voor het gemak.

$ $ \begin{array}{| c | c |} \text{Pauli meting} & U\\\\ Z & \boldone\\\\ X & H\\\\ Y & HS ^ \dagger\\\\ \end{array} $ $

Dat wil zeggen dat het gebruik van deze taal ' Measure $Y $ ' gelijk is aan het Toep assen van $HS ^ \dagger $ en vervolgens wordt gemeten in de reken kracht, waarbij $S $ de zogenaamde fase-poort is die wordt verstrekt door

$ $ \begin{bmatrix}1 & 0\\\\ 0 & i\end {bmatrix}.
$$

Het is ook gelijk aan het Toep assen van $HS ^ \dagger $ aan de Quantum status vector en vervolgens $Z $.  De juiste status zou worden gevonden door terug te gaan naar de reken kundige basis, die bedragen om $SH $ toe te passen op de Quantum status vector.

## <a name="q-outcome-classical-information-obtained-from-quantum-state"></a>Q # resultaat, klassieke informatie verkregen van Quantum status
In Q # zeggen we dat het resultaat, dat wil zeggen, de klassieke informatie die is geëxtraheerd uit interactie met de status, is $j $, die zich in de set $\{0, 1\}$ bevindt in de $ (-1) ^ j $ eigenspace van de Pauli-operator gemeten.

Metingen van Qubit Pauli-Opera tors worden op dezelfde manier gedefinieerd, zoals u kunt zien van:

$ $ Z\otimes Z = \begin{bmatrix}1 & 0 & 0 & 0\\\\ 0 &-1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 & 1 \ end {bmatrix}.
$$

Daarom vormen de tensor-producten van twee Pauli-$Z $-Opera tors een matrix die bestaat uit twee ruimten die bestaan uit $ + $1 en $-$1 eigenvalues.  Net als bij de single-Qubit geldt dat beide een halve ruimte betekenen dat de helft van de toegankelijke vector ruimte behoort tot de $ + $1 eigenspace en de resterende helft naar $-$1 eigenspace.  Over het algemeen is het eenvoudig om te zien uit de definitie van het tensor-product dat een tensor product van Pauli $ $Z-Opera tors en de identiteit hiervan in de hand heeft.  Bijvoorbeeld:

$ $ Z\otimes\boldone = \begin{bmatrix} 1 & 0 & 0 & 0\\\\ 0 & 1 & 0 & 0\\\\ 0 & 0 &-1 & 0\\\\ 0 & 0 & 0 &-1 \ end {bmatrix}.
$$

Net als voorheen beschrijft elke unitary-trans formatie van dergelijke matrices ook twee halve ruimten die zijn gelabeld met $ \pm $1 eigenvalues.  Bijvoorbeeld $X \otimes X = H\otimes H (Z\otimes Z) H\otimes H $ van de identiteit die $Z = HXH $.  Net als bij het Qubit-geval kunnen alle twee Qubit Pauli-metingen worden geschreven als $U ^ \dagger (Z\otimes \id) U $ voor $4 \ Times $4 unitary-matrices $U $.  De trans formaties in de volgende tabel worden opgesomd, waar we de swap-Gate voor het gemak van qubits $0 $ en $1 $: $ \operatorname{SWAP} = \operatorname{CNOT}\_{01}\operatorname{CNOT}\_{10}\operatorname{ CNOT}\_{01}$:

$ $ \begin{array}{| c | c |} \text{Pauli meting} & U\\\\ \hline Z\otimes \boldone & \boldone\otimes \boldone\\\\ X\otimes \boldone & H\otimes \boldone\\\\ Y\otimes \boldone & HS ^ \dagger\ otimes \boldone\\\\ \boldone \otimes Z & \operatorname{SWAP}\\\\ \boldone \otimes X & (H\otimes \boldone) \operatorname{SWAP}\\\\ \boldone \otimes Y & (HS ^ \dagger\otimes \boldone) \ operator {SWAP}\\\\ Z\otimes Z & \operatorname{CNOT}\_{10}\\\\ X\otimes Z & \operatorname{CNOT}\_{10}(H\otimes \boldone)\\\\ Y\otimes Z & \ operator {CNOT}\_{10}(HS ^ \dagger\otimes \boldone)\\\\ Z\otimes X & \operatorname{CNOT}\_{10}(\boldone\otimes H)\\\\ X\otimes X & \operatorname{CNOT}\_@no__t _31_ (H\otimes H)\\\\ Y\otimes X & \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes H)\\\\ Z\otimes Y & \operatorname{CNOT}\_{10}(\boldone \otimes HS ^ \dagger)\\\\ X\otimes Y & \operatorname{CNOT}\_{10}(H\otimes HS ^ \dagger)\\\\ Y\otimes Y & \operatorname{CNOT}\_{10}(HS ^ \dagger\otimes HS ^ \dagger)\\\\ \end{array} $ $

Hier wordt de poort $ \operatorname{CNOT}\_{10}$ weer gegeven om de volgende reden.  Elke Pauli-meting die geen $ \boldone $-matrix bevat, is gelijk aan een unitary om \otimes Z $ te $Z door de bovenstaande reden.  De eigenvalues van $Z \otimes Z $ is alleen afhankelijk van de pariteit van de qubits die bestaat uit elke reken kundige basis vector en de Controlled-not-bewerkingen die in deze lijst worden weer gegeven, dienen om deze pariteit te berekenen en op te slaan in de eerste bit.  Zodra de eerste bit wordt gemeten, kunnen we de identiteit van de resulterende halve ruimte herstellen die overeenkomt met het meten van de Pauli-operator.

Een aanvullend bericht, terwijl het kan voor komen dat de meting $Z \otimes Z $ hetzelfde is als de meet $Z \otimes \id $ en vervolgens $ \id \otimes Z $, zou deze veronderstelling onwaar zijn.  Het meten van $Z \otimes Z $ projecteert de Quantum status in de $ + $1-of $-$1-eigenstate van deze opera tors.  Meting $Z \otimes \id $ en vervolgens $ \id \otimes Z $ projecteert de Quantum State vector eerst op een halve ruimte van $Z \otimes $ en vervolgens op een halve spatie van $ \id \id Z $.  Omdat er vier reken kundige basis vectoren zijn, vermindert het uitvoeren van beide metingen de status naar een vierde spatie en vermindert deze in een enkele reken kundige basis vector.


## <a name="correlations-between-qubits"></a>Correlaties tussen qubits
Een andere manier om te kijken naar het meten van tensor-producten van Paulis, zoals $X \otimes X $ of $Z \otimes Z $, is dat met deze metingen u de informatie kunt bekijken die is opgeslagen in de correlaties tussen de twee qubits.  Door $X \otimes \id $ te meten, kunt u zien welke gegevens lokaal zijn opgeslagen in de eerste Qubit.  Hoewel beide soorten metingen even waardevol zijn voor Quantum Computing, licht de eerste maal de kracht van Quantum Computing. Het blijkt dat in Quantum Computing vaak de informatie die u wenst te leren, niet is opgeslagen in een enkele Qubit, maar niet lokaal is opgeslagen in alle qubits, en alleen door een gemeen schappelijke meting te bekijken met $Z \otimes Z $, worden deze gegevens merkt.

Wille keurige Pauli-Opera tors zoals $X \otimes Y \otimes Z \otimes \boldone $ kunnen ook worden gemeten.  Al deze tensor-producten van Pauli-Opera tors hebben slechts twee eigenvalues $ \pm $1 en beide eigenspaces vormen een halve ruimte van de hele vector ruimte.  Daarom vallen ze samen met de hierboven vermelde vereisten.

In Q # retourneert deze metingen $j $ als de meting resulteert in een resultaat in de eigenspace van Sign $ (-1) ^ j $.  Als een ingebouwde functie in Q # is nuttig, omdat het meten van deze opera tors lange ketens van beheerde-en basis transformaties vereist om de diagonalizing $U $-Gate te beschrijven die nodig is om de bewerking uit te geven als een tensor-product van $Z $ en $ \id $.  Door simpelweg in te stellen dat u een van deze vooraf gedefinieerde metingen wilt uitvoeren, hoeft u zich geen zorgen te maken over de manier waarop u uw basis kunt transformeren, zodat een reken kundige basis meting de benodigde informatie bevat.  Q # Hiermee worden alle nood zakelijke trans formaties automatisch voor u verwerkt. Zie [Q # Library Reference voor Pauli-metingen](/qsharp/api/canon/microsoft.quantum.canon.measurepaulis)

## <a name="the-no-cloning-theorem"></a>De theorema zonder klonen
De quantum informatie is krachtig.  Hierdoor kunnen we fantastische dingen doen, zoals factor nummers exponentieel sneller dan de best bekende klassieke algoritmen, of op efficiënte wijze simuleren van gecorreleerde elektroden systemen die klassieke kosten in de praktijk nodig hebben om nauw keurig te simuleren.  Er zijn echter beperkingen ten aanzien van de kracht van Quantum Computing.  Een dergelijke beperking wordt gegeven door de *theorema die niet klonen*.

De theorema zonder klonen is aptly met de naam.
Het klonen van generieke Quantum Staten door een quantum computer wordt niet toegestaan.
Het bewijs van de theorema is onduidelijker.
Hoewel een volledig bewijs van het no-klonen van theorema een beetje te technisch is voor onze bespreking, is het bewijs van de theorema in het geval dat de quantum computer in kwestie geen extra ancilla qubits heeft binnen onze Scope (ancilla qubits worden qubits gebruikt voor een nieuwe ruimte tijdens een berekening en kan eenvoudig worden gebruikt en beheerd in Q #, zie <xref:microsoft.quantum.techniques.qubits>).
Voor een dergelijke quantum computer moet de kloon bewerking een unitary matrix zijn. De meting is niet toegestaan omdat de Quantum status die we proberen te klonen, is beschadigd. De unitary-matrix die we willen hebben, moet de eigenschap hebben die $ $ U \ket{\psi} \ket{0} = \ket{\psi} \ket{\psi}, $ $ voor elke status $ \ket{\psi} $.
De eigenschap Linearity van matrix vermenigvuldiging impliceert dat voor elke tweede Quantum status $ \ket{\phi} $,

\begin{align} & U\left [\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right] \ket{0}= \frac{1}{\sqrt{2}} U\ket {\ Phi} \ Ket{0}+ \frac{1}{\sqrt{2}} U\ket {\ psi} \ Ket{0}@no__ t_9_ \\ & \qquad\qquad = \frac{1}{\sqrt{2}} \left (\ket{\phi}\ket{\phi} + \ket{\psi}\ket{\psi}\right)\\\\ & \qquad\qquad\ne \left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \ rechts) \right) \otimes\left (\frac{1}{\sqrt{2}} \left (\ket{\phi} + \ket{\psi} \right) \right).
\end{align}

Dit voorziet in de fundamentele Intuition achter het no-klonen theorema: elk apparaat dat een onbekende Quantum status kopieert, moet fouten veroorzaken op ten minste een van de statussen die worden gekopieerd.  Hoewel de sleutel veronderstelling dat de klooner lineair op de invoer status optreedt, kan worden geschonden door de toevoeging van ancilla en meting van de ancilla-qubits, worden ook gegevens over het systeem door middel van de meting statistieken gelekt en wordt voor komen dat in dergelijke gevallen is het precies klonen.  Zie [voor meer informatie](xref:microsoft.quantum.more-information)over de theorema die u niet klonen.

Het niet-klonen van theorema is belang rijk voor de kwalitatieve kennis van Quantum Computing omdat als u de Quantum toestanden in de buurt zou kunnen klonen, dan krijgt u een Magical-mogelijkheid om te leren van Quantum Staten.  Het is ook mogelijk dat u het Heisenberg van vaunted onzekerheid schendt.  U kunt ook een optimale kloon gebruiken om één voor beeld van een complexe Quantum distributie te maken en alles te leren over die distributie, van slechts één voor beeld.  Dit is een manier om een munten te spie gelen en op de hoogte te houden en vervolgens een vriend te vertellen over het resultaat van de reactie "Ah de verdeling van die munten moet worden gebernoulli met $p = 0.512643 \ ldots $!"  Een dergelijke instructie zou niet-sensical zijn, omdat een stukje informatie (het resultaat van de kop) simpelweg de vele informatie die nodig is om de distributie te coderen zonder belang rijke eerdere informatie, niet kan leveren.  Op dezelfde manier kunnen we zonder voorafgaande informatie een Quantum staat niet op dezelfde manier klonen als we geen ensemble van deze munten voors bereiden zonder te weten $p $.

Informatie is niet gratis in Quantum Computing.  Elk Qubit dat wordt gemeten, geeft één stukje informatie en het theorema zonder klonen laat zien dat er geen beschik over is die kunnen worden misbruikt om de fundamentele berekenings verhouding te verkrijgen tussen informatie over het systeem en de verstoringen die erop worden opgeroepen.

