---
title: Wat is Q#?
description: Lees hier meer over Q#, een programmeertaal van Microsoft voor het ontwikkelen van toepassingen voor kwantumcomputers
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: e04228ff62092a15c529297bd56b9ee48399f4a5
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443950"
---
# <a name="what-is-q"></a>Wat is Q#?

Q# is een programmeertaal met functies die specifiek zijn voor kwantumcomputing. Met Q# beschikken kwantumprogrammeurs over een framework waarmee ze zich kunnen concentreren op de algoritmen zonder dat ze zich zorgen hoeven te maken over technische details zoals het optimaliseren van de gate-sequence of de fysieke implementatie van een kwantumcomputer.

De programmeertaal Q# biedt een intuïtieve set met typen, bewerkingen en logische expressies voor het ontwikkelen van algoritmen zonder dat u rekening hoeft te houden met de interne logica van de kwantumcomputer.

## <a name="code-algorithms"></a>Algoritmen coderen

In het begintijdperk van de kwantumcomputing werden algoritmen gevisualiseerd als schema's, vergelijkbaar met circuitschema's in klassieke computing.  Hoewel het circuitmodel gedurende een groot aantal jaren heel nuttig is geweest in het onderzoek naar kwantumcomputing, hier bij Microsoft, zijn we van mening dat kwantumcircuits nog maar het begin zijn voor ontwikkelaars en dat ze kwantumalgoritmen en -toepassingen kunnen ontwikkelen met Q#. Bij het bouwen van de Q#-taal hebben we rekening gehouden met wat we hebben geleerd in tientallen jaren ontwikkeling van klassieke software om kwantumontwikkelaars te voorzien van een high-level taal die specifiek is gericht op kwantumcomputing.


## <a name="how-does-q-work"></a>Hoe werkt Q#?

Een van de fundamentele bouwstenen van Q# is het `Qubit`-type, dat niet kan worden gekopieerd en ook niet rechtstreeks toegankelijk is, net als een echte qubit. In plaats daarvan kunnen we deze meten en het resultaat van de meting opslaan in een `Result`-variabele; een Q#-type dat twee mogelijke waarden kan aannemen: `Zero` en `One`. Constructies zoals deze garanderen dat algoritmen altijd de wetten van de kwantumfysica respecteren en correct kunnen worden uitgevoerd op kwantumcomputers of simulators.

Q# bevat ook functies van klassieke logica zoals voorwaarden of lussen, met een aantal nuanceringen om ervoor te zorgen dat alle kwantumregels worden nageleefd. Zo moeten kwantumbewerkingen bijvoorbeeld omkeerbaar zijn. Dit dwingt enkele beperkingen af voor de manier waarop lussen worden uitgevoerd.

Programma's geschreven in Q# zijn vaak gekoppeld aan een hostprogramma dat is geschreven in C# of Python, waarmee klassieke code en kwantumcode op een handige manier kunnen worden geordend. Naast de ondersteuning van .NET-talen zoals C# en Python biedt de QDK ondersteuning voor Jupyter-notebooks met de Jupyter-kernel IQ#.

## <a name="use-q-to-learn-quantum-computing"></a>Kwantumcomputing leren met Q#

Tot nu toe was kennis van het circuitmodel nodig om te leren werken met kwantumcomputing, teneinde de algoritmen te begrijpen in de vorm van geordende reeksen kwantum-gates en metingen. Met Q# kunt u een ander traject volgen: kwantumcomputing leren door kwantumprogramma's te schrijven.

## <a name="use-q-to-design-quantum-algorithms"></a>Q# gebruiken om kwantumalgoritmen te ontwerpen

Er zijn steeds meer bibliotheken en door de gebruiker gedefinieerde typen beschikbaar voor Q# waarmee u hulpprogramma's en functies kunt implementeren om zo geavanceerde kwantumalgoritmen te maken. Stel dat u de twee qubits q1 en q2 moet verstrengelen. In plaats van afzonderlijk de benodigde gates toe te passen om dit te realiseren, kunt u de al ingebouwde bewerking `PrepareEntangledState([q1], [q2])` gebruiken.

## <a name="use-q-to-estimate-quantum-resources"></a>Q# gebruiken om een schatting te maken van kwantumbronnen

U kunt de uitvoering van uw Q#-programma simuleren met behulp van de full-state kwantumsimulator die wordt geleverd bij de Quantum Development Kit (QDK).  De QDK biedt ook bronschattingen die u inzicht geven in de prestaties van Q#-programma's die te groot zijn om te worden uitgevoerd op een simulator.  Dit is zeer nuttig voor ontwerpers van algoritmen omdat ze hun programma's kunnen afstemmen op het gebruik van minder bronnen (bijvoorbeeld minder qubits waarop minder bewerkingen worden uitgevoerd), om te worden uitgevoerd op oudere kwantumhardware op kleinere schaal.   

## <a name="use-q-to-validate-hardware-performance"></a>Q# gebruiken om de prestaties van hardware te valideren

Het mooie van Q# is dat een programma maar eenmaal hoeft te worden geschreven en kan worden uitgevoerd op kwantumsimulators voor foutopsporing, en op verschillende hardware voor kwantumcomputers kan worden uitgevoerd.  Benchmarkprogramma's die zijn geschreven in Q# kunnen worden uitgevoerd voor het valideren van de prestaties van hardware en het vergelijken van resultaten wanneer kwantumcomputers zich ontwikkelen en er nieuwe kwantumcomputers beschikbaar komen.  

## <a name="next-steps"></a>Volgende stappen

* [Hoe kan ik kwantumcomputing leren?](xref:microsoft.quantum.overview.learn)
* [Aan de slag met de Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)
