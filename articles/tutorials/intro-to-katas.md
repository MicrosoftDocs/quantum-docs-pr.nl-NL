---
title: Algemene informatie over Quantum Katas
description: Lees meer over de katas (trainingsoefeningen) die worden geleverd bij de Microsoft Quantum Development Kit (QDK)
author: bradben
ms.author: bradben
ms.date: 06/02/2020
ms.topic: overview
uid: microsoft.quantum.overview.katas
no-loc:
- Q#
- $$v
ms.openlocfilehash: b2a3b25bf90109468f02c98c6c687befb83648bc
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869678"
---
# <a name="learn-quantum-computing-with-the-quantum-katas"></a>Kwantumcomputing leren met de Quantum Katas

[De Quantum Katas](https://github.com/Microsoft/QuantumKatas/) zijn open source, zelf studies en programmeer oefeningen gericht op het door geven van de elementen van Quantum Computing en Q# programmering.

## <a name="learning-by-doing"></a>Leren door te doen

De zelfstudies en oefeningen in dit project benadrukken het leren door te doen: ze bevatten programmeertaken die betrekking hebben op bepaalde onderwerpen en die variëren van zeer eenvoudig tot moeilijk. Voor elke taak moet u bepaalde code invullen. Voor de eerste taken is dat misschien maar één regel, terwijl u voor de daaropvolgende taken mogelijk een aanzienlijk codefragment moet maken.

Het Katas omvat het test raamwerk dat de oplossingen voor de taken heeft ingesteld, uitgevoerd en gevalideerd. Hierdoor kunt u onmiddellijk feedback krijgen over uw oplossing en kunt u uw aanpak indien nodig wijzigen als deze onjuist blijkt te zijn.

U kunt de Katas gebruiken voor het leren in uw omgeving van uw keuze:

* Jupyter-notebooks online in de Binder-omgeving
* Jupyter-notebooks die worden uitgevoerd op uw lokale computer
* Visual Studio
* Visual Studio Code

## <a name="what-can-i-learn-with-the-quantum-katas"></a>Wat kan ik leren met de Quantum Katas?

Verken de basis principes en fundamentals van Quantum Computing of dieper in Quantum algorithms and protocols. Het wordt aangeraden om dit leertraject zeker in het begin te volgen, om ervoor te zorgen dat u goed bekend bent met de basisconcepten van kwantumcomputing. Uiteraard kunt u bekende onderwerpen overslaan, zoals complexe wiskundige berekeningen, en de algoritmen in de gewenste volgorde doornemen.

### <a name="introduction-to-quantum-computing-concepts"></a>Concepten van kwantumcomputing

| Kata | Beschrijving |
|:-----|-------------|
|[Complexe wiskundige bewerkingen](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ComplexArithmetic)|In deze zelf studie wordt een deel van de wiskundige achtergrond uitgelegd dat vereist is voor het werken met Quantum Computing, zoals imaginaire en complexe getallen.|
|[Lineaire algebra](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/LinearAlgebra)|Lineaire algebra wordt gebruikt om Quantum statussen en bewerkingen in Quantum Computing aan te geven. In deze zelf studie worden de basis principes beschreven, waaronder matrices en vectoren.|
|[Het concept van een qubit](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/Qubit)|Meer informatie over qubits: een van de basis concepten van Quantum Computing. |
|[Kwantumpoorten met één qubit](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/SingleQubitGates)|In deze zelf studie wordt gequbiteerde Quantum-poorten, die fungeren als de bouw stenen van Quantum algoritmen en het transformeren van Quantum Qubit-Staten op verschillende manieren.|
|[Systemen met meerdere qubits](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitSystems)|In deze zelf studie introduceert u multi-Qubit systemen, hun representatie in wiskundige notatie en in Q# code en het concept van Entanglement.|
|[Multi-Qubit Quantum-Gates](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/MultiQubitGates)|In deze zelf studie wordt de zelf studie [Single-Qubit Quantum Gates](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/SingleQubitGates) beschreven en wordt gekeken naar het Toep assen van Quantum-poorten op multi-Qubit-systemen.|

### <a name="quantum-computing-fundamentals"></a>Basisprincipes van kwantumcomputing

| Kata | Beschrijving |
|:-----|-------------|
|[Kwantumpoorten herkennen](https://github.com/microsoft/QuantumKatas/tree/master/BasicGates)|Een reeks oefeningen die zijn ontworpen om u vertrouwd te raken met de eenvoudige Quantum Gates in Q# . Bevat oefeningen voor enkelvoudige Qubit-en multi-Qubit-Gates, adjoint en gecontroleerde poorten en hoe u Gates kunt gebruiken om de status van een Qubit te wijzigen.|
|[Kwantumsuperpositie maken](https://github.com/microsoft/QuantumKatas/tree/master/Superposition)|Gebruik deze oefeningen om vertrouwd te raken met het concept van superpositie en het Program meren in Q# . Bevat oefeningen voor Qubit-en multi-Qubit-Gates, Super position en datatransport besturing en recursie in Q# .|
|[Kwantumtoestanden onderscheiden met metingen](https://github.com/microsoft/QuantumKatas/tree/master/Measurements)|Los deze oefeningen op tijdens het leren over Quantum metingen en orthogonale en niet-orthogonale Staten. |
|[Gezamenlijke metingen](https://github.com/microsoft/QuantumKatas/tree/master/JointMeasurements)|Meer informatie over gezamenlijke pariteits metingen en hoe u de [meet](xref:microsoft.quantum.intrinsic.measure) bewerking kunt gebruiken om Quantum Staten te onderscheiden.|

### <a name="algorithms"></a>Algoritmen

| Kata | Beschrijving |
|:-----|-------------|
|[Kwantumteleportatie](https://github.com/microsoft/QuantumKatas/tree/master/Teleportation)|In deze Kata wordt gebruikgemaakt van Quantum Teleportation-een protocol waarmee een Quantum status kan worden gecommuniceerd met alleen klassieke communicatie en voorheen gedeelde Quantum Entanglement.|
|[Superdense codering](https://github.com/microsoft/QuantumKatas/tree/master/SuperdenseCoding)|De code ring van superzijdig is een protocol waarmee twee bits aan klassieke informatie kunnen worden verzonden door slechts één Qubit te verzenden met behulp van eerder gedeelde Quantum Entanglement.  |
|[Deutsch–Jozsa-algoritme](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringDeutschJozsaAlgorithm)|Dit algoritme is beroemde voor een van de eerste voor beelden van een Quantum algoritme die exponentieel sneller is dan een wille keurig deterministisch Klassieke algoritme.|
|[Algemene eigenschappen van zoekalgoritme van Grover ontdekken](https://github.com/microsoft/QuantumKatas/tree/master/tutorials/ExploringGroversAlgorithm)|Een geavanceerde Inleiding tot een van de meest beroemde-algoritmen in Quantum Computing. Het probleem van het vinden van een invoer naar een zwart vak (Oracle) dat een bepaalde uitvoer produceert, wordt opgelost. |
|[Zoekalgoritme van Grover implementeren](https://github.com/microsoft/QuantumKatas/tree/master/GroversAlgorithm)|Deze Kata Dives dieper op het zoek algoritme van Grover, en behandelt het schrijven van Oracle, het uitvoeren van de stappen van het algoritme en tot slot het samen zetten.|
|[Problemen oplossen met behulp van het algoritme van Grover: SAT](https://github.com/microsoft/QuantumKatas/tree/master/SolveSATWithGrover)|Een reeks oefeningen waarbij de algoritme van Grover wordt gebruikt om realistische problemen op te lossen, met behulp van [Booleaanse satisfiability-problemen](https://en.wikipedia.org/wiki/Boolean_satisfiability_problem) (SAT) als voor beeld.  |
|[Problemen oplossen met behulp van het algoritme van Grover: grafiek kleuren oplossen](https://github.com/microsoft/QuantumKatas/tree/master/GraphColoring)| Deze Kata gaat verder met het algoritme van Grover, deze tijd voor het oplossen van problemen met de [beperkings tevredenheid](https://en.wikipedia.org/wiki/Constraint_satisfaction_problem), het gebruik van een grafiek kleur probleem als voor beeld. |

### <a name="protocols-and-libraries"></a>Protocollen en bibliotheken

| Kata | Beschrijving |
|:-----|-------------|
|[BB84-protocol voor distributie van kwantumsleutels](https://github.com/microsoft/QuantumKatas/tree/master/KeyDistribution_BB84)|Meer informatie over en implementeren van een Quantum Key Distribution Protocol, [BB84](https://en.wikipedia.org/wiki/BB84), met behulp van qubits voor het uitwisselen van cryptografische sleutels. |
|[Bit-spie gelen fout bij het corrigeren van code](https://github.com/microsoft/QuantumKatas/tree/master/QEC_BitFlipCode)|Verken de Quantum-fout correctie met de eenvoudigste van de Quantum fout correctie (QEC)-codes-de code met drie Qubit bits spie gelen.|
|[Faseschatting](https://github.com/microsoft/QuantumKatas/blob/master/PhaseEstimation)|Fase schattings algoritmen zijn enkele van de meest fundamentele bouw stenen van Quantum Computing. Meer informatie over fase schatting met deze oefeningen die betrekking hebben op de Quantum fase-schatting en het voorbereiden en uitvoeren van fase-schattings routines in Q# .|
|[Quantum aritmetische: adders bouwen](https://github.com/microsoft/QuantumKatas/blob/master/RippleCarryAdder)|Een diep gaande reeks oefeningen waarmee [rimpels](https://en.wikipedia.org/wiki/Adder_(electronics)#Ripple-carry_adder) worden toegevoegd aan een quantum computer. Bouw een ' in-place ' Quantum adder, breid deze uit met een ander algoritme en bouw ten slotte een Quantum-subtrekker in plaats daarvan.   |

### <a name="entanglement-games"></a>Verstrengelingsgames

| Kata | Beschrijving |
|:-----|-------------|
|[CHSH-game](https://github.com/microsoft/QuantumKatas/tree/master/CHSHGame)|Verken de Quantum Entanglement met een implementatie van het [CHSH](https://en.wikipedia.org/wiki/CHSH_inequality) -spel. Dit niet- [lokale](https://en.wikipedia.org/wiki/Quantum_refereed_game) spel laat zien hoe Quantum Entanglement kan worden gebruikt om de kans te verg Roten dat de spelers groter worden dan wat zou kunnen zijn met een louter klassieke strategie.|
|[GHZ-game](https://github.com/microsoft/QuantumKatas/tree/master/GHZGame)|Het GIGAHERTZ-spel is een ander niet-lokaal spel, maar omvat drie spelers.|
|[Mermin-Peres Magic Square-game](https://github.com/microsoft/QuantumKatas/tree/master/MagicSquareGame)|Een reeks oefeningen waarmee [Quantum pseudo-telepathy](https://en.wikipedia.org/wiki/Quantum_pseudo-telepathy#The_Mermin%E2%80%93Peres_magic_square_game) wordt verkend om een Magic-kwadraat spel op te lossen.  |

## <a name="resources"></a>Resources

Bekijk de volledige serie met [Quantum Katas](https://github.com/microsoft/QuantumKatas)

[Voer de katas online uit](https://aka.ms/try-quantum-katas)
