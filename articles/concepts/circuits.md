---
title: Kwantumcircuits
description: Meer informatie over het visueel weer geven van eenvoudige en complexe Quantum bewerkingen met Quantum circuit diagrammen.
author: QuantumWriter
uid: microsoft.quantum.concepts.circuits
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 8ba4648f1837065d15957a01ab4ca8dd2d490a42
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77905145"
---
# <a name="quantum-circuits"></a>Quantum circuits
Denk eens na over een ogen blik dat de unitary-trans formatie $ \Text{CNOT} _{01}(H\otimes 1) $.
Deze poort reeks is van fundamenteel belang voor Quantum Computing omdat hiermee een maximally Entangled-status van twee Qubit wordt gemaakt:

$ $ \mathrm{CNOT}_{01}(H\otimes 1) \ket{00} = \frac{1}{\sqrt{2}} \left (\ket{00} + \ket{11} \right), $ $

Bewerkingen met deze of meer complexiteit zijn alomtegenwoordige in Quantum-algoritmen en Quantum fout correctie, zodat het een uitstekende goed keuring vormt voor de visualisatie die een *Quantum diagram*wordt genoemd.
Het circuit diagram voor het voorbereiden van de Quantum status van deze maximally Entangled is:

<!--- ![](.\media\1.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![-circuit diagram voor een maximally Entangled-status van twee Qubit](~/media/Concepts1.png)

## <a name="quantum-circuit-diagram-conventions"></a>Conventies van Quantum circuit diagram
Deze visuele taal voor Quantum bewerkingen kan beter digestible zijn dan het schrijven van de equivalente matrix wanneer u de conventies voor het uitdrukken van een Quantum circuit begrijpt.
Deze conventies worden hieronder besproken.

In een circuit diagram geeft elke ononderbroken lijn een Qubit of meer in het algemeen een Qubit-REGI ster.
Per Conventie is de bovenste regel Qubit REGI ster $0 $ en de rest wordt opeenvolgend gelabeld. Het bovenstaande voor beeld wordt weer gegeven als een actie op twee qubits (of gelijkwaardige twee registers die uit één Qubit bestaan).
Poorten die aan een of meer Qubit-registers fungeren, worden aangeduid als een doos.
Bijvoorbeeld het symbool

<!--- ![](.\media\2.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![symbool voor een Hadamard-bewerking die wordt uitgevoerd op een single-Qubit-REGI ster](~/media/concepts_2.png)

is een [Hadamard](xref:microsoft.quantum.intrinsic.h) -bewerking die fungeert als een single-Qubit-REGI ster.

Quantum-Gates worden in chronologische volg orde gerangschikt met de meest linkse poort als de poort die voor het eerst op de qubits is toegepast.
Met andere woorden, als u de draden bijhoudt als het gaat om de Quantum status, halen de draden de Quantum status door elk van de poorten in het diagram van links naar rechts.
Dat wil zeggen 

<!--- ![](.\media\3.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![diagram van Quantum-Gates dat van links naar rechts wordt toegepast](~/media/concepts_3.png)

is de unitary matrix $CBA $.
Matrix vermenigvuldiging voldoet aan de tegenovergestelde Conventie: de meest rechtse matrix wordt eerst toegepast. In Quantum-circuit diagrammen wordt echter de meest linkse poort toegepast eerst.
Dit verschil kan in de loop van Verwar ring zijn, dus het is belang rijk dat u weet dat dit aanzienlijk verschil is tussen de lineaire algebraic notatie en Quantum circuit diagrammen.

## <a name="inputs-and-outputs-of-quantum-circuits"></a>Invoer en uitvoer van Quantum circuits
Alle voor gaande voor beelden hebben precies hetzelfde aantal bedradingen (qubits) in een Quantum poort gezien als het aantal draden van de Quantum poort.
Het kan eerst redelijk zijn dat quantum circuits meer of minder uitvoer hebben dan invoer in het algemeen.
Dit is echter onmogelijk, omdat alle Quantum bewerkingen, het opslaan van metingen, unitary en dus omkeerbaar zijn.
Als ze niet hetzelfde aantal uitvoer hebben als invoer, zouden ze niet omkeerbaar zouden zijn en dus niet unitary. Dit is een tegen strijdigheid.
Daarom moet elk vak dat in een circuit diagram wordt getekend, exact hetzelfde aantal draden hebben als het wordt afgesloten.

Multi-Qubit circuit diagrammen volgen vergelijk bare conventies voor enkelvoudige Qubit.
Een voor beeld hiervan is dat we een unitary-bewerking met twee Qubit definiëren $B $ (H S\otimes X) $ en het circuit gelijk geven aan

<!--- ![](.\media\4.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![circuit diagram van een unitary bewerking met twee qubits](~/media/concepts_4.png)

We kunnen ook $B $ weer geven als een actie voor een enkele twee Qubit-registratie in plaats van 2 1-Qubit registreert, afhankelijk van de context waarin het circuit wordt gebruikt. Misschien is de meest nuttige eigenschap van dergelijke abstracte circuit diagrammen dat ze gecompliceerde Quantum algoritmen op een hoog niveau mogen worden beschreven, zonder dat ze hoeven te compileren op basis poorten.
Dit betekent dat u een Intuition voor de gegevens stroom kunt verkrijgen voor een grote Quantum algoritme zonder dat u alle details hoeft te begrijpen van de manier waarop elk van de subroutines binnen het algoritme werkt.

## <a name="controlled-gates"></a>Bewaakte poorten
De andere constructie die is ingebouwd in multi-Qubit Quantum circuit diagrammen is Control.
De actie van een Quantum die wordt geïsoleerd als poort, heeft $ \Lambda (G) $, waarbij de waarde van één Qubit de toepassing van $G $, kan worden begrepen door te kijken naar het volgende voor beeld van een product status invoer $ \Lambda (G) (\alpha \ket{0} + \beta \ket{1}) \ket{\psi} = \alpha \ket{0} \ket{\psi} + \beta \ket{1} G\ket {\ psi} $.
Dat wil zeggen dat de bewaakte Gate $G $ toepast op het REGI ster met $ \psi $ als en alleen als het besturings element Qubit de waarde $1 $ heeft.
Over het algemeen beschrijven we dergelijke beheerde bewerkingen in circuit diagrammen als

<!--- ![](.\media\5.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![circuit diagram van een poort die afzonderlijk wordt gecontroleerd](~/media/concepts_5.png)

Hier geeft de zwarte cirkel de Quantum bit aan waarop de poort wordt gecontroleerd en een verticale bedrading de unitary die wordt toegepast wanneer het besturings element Qubit de waarde $1 $ heeft.
Voor de speciale gevallen waarin $G = X $ en $G = Z $, introduceren we de volgende notatie om de bewaakte versie van de poorten te beschrijven (Houd er rekening mee dat de Controlled-X-Gate de [$CNOT $ Gate](xref:microsoft.quantum.intrinsic.cnot)) is:

<!--- ![](.\media\6.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![-circuit diagram voor speciale gevallen van gecontroleerde poorten](~/media/concepts_6.png)

Q # biedt methoden voor het automatisch genereren van de bewaakte versie van een bewerking, waardoor de programmeur van de hand om deze bewerkingen te hoeven coderen. Hieronder ziet u een voor beeld van dit:

```qsharp
operation PrepareSuperposition(qubit : Qubit) : Unit
is Ctl { // Auto-generate the controlled specialization of the operation
    H(qubit);
}
```

## <a name="measurement-operator"></a>Meet operator
De resterende bewerking voor het visualiseren van circuit diagrammen is meting.
Meting neemt een Qubit-REGI ster, meet dit en voert het resultaat uit als klassieke informatie.
Een meting bewerking wordt aangeduid met een meter symbool en gaat altijd als invoer een Qubit-REGI ster (aangeduid met een ononderbroken lijn) en voert klassieke informatie uit (aangeduid met een dubbele lijn).
Met name een dergelijk subcircuit ziet er als volgt uit:

<!--- ![](.\media\7.svg) ---->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![-symbool dat een meting bewerking vertegenwoordigt](~/media/concepts_7.png)

Q # implementeert een [meet operator](xref:microsoft.quantum.intrinsic.measure) voor dit doel.
Zie de [sectie over metingen](xref:microsoft.quantum.libraries.standard.prelude#measurements) voor meer informatie.

Op dezelfde manier wordt het subcircuit

<!--- ![](.\media\8.svg) --->
<!-- Can't find a way to easily center this... probably an extension needed:  -->
![circuit diagram dat een gecontroleerde bewerking vertegenwoordigt](~/media/concepts_8.png)

geeft een klassieke, gecontroleerde poort, waarbij $G $ wordt toegepast op de waarde van het klassieke besturings element bit $1 $.

## <a name="teleportation-circuit-diagram"></a>Circuit diagram teleportatie
[Quantum-teleportie](xref:microsoft.quantum.techniques.puttingittogether) is misschien het beste Quantum algoritme voor het illustreren van deze onderdelen.
Quantum teleportie is een methode voor het verplaatsen van gegevens binnen een quantum computer (of zelfs tussen quantum computers in een Quantum netwerk) met behulp van entanglement en meting.
Het is interessant om een Quantum status te verplaatsen, de waarde in een bepaalde Qubit te zeggen van een Qubit naar een andere, zonder dat u weet wat de waarde van de Qubit is.
Dit is nodig om het protocol te laten werken volgens de wetten van Quantum-garages.
Het Quantum teleportal-circuit wordt hieronder gegeven. We bieden ook een geannoteerde versie van het circuit om te laten zien hoe het Quantum circuit kan worden gelezen.

<!--- ![](.\media\tp2.svg){ width=50% } --->
![Quantum Teleportation-circuit](~/media/concepts_tp2.png)
