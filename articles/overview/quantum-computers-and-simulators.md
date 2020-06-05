---
title: Kwantumcomputers en kwantumsimulators
description: Meer informatie over kwantumhardware, kwantumsimulators en hoe kwantumbewerkingen werken.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.simulators
ms.openlocfilehash: 2f5345504ba31211c97493e78af1563d575881e4
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327744"
---
# <a name="quantum-computers-and-quantum-simulators"></a>Kwantumcomputers en kwantumsimulators

De ontwikkeling van de kwantumcomputer bevindt zich nog in het beginstadium. De hardware en het onderhoud zijn duur en de meeste systemen bevinden zich in universiteiten en onderzoekslaboratoria. De technologie gaat echter vooruit en sommige systemen zijn (beperkt) vrij toegankelijk.

Kwantumsimulators zijn softwareprogramma's die worden uitgevoerd op klassieke computers en die het mogelijk maken om kwantumprogramma's uit te voeren en te testen in een omgeving die voorspelt hoe qubits op verschillende bewerkingen reageren.

## <a name="quantum-hardware"></a>Kwantumhardware

Een kwantumcomputer bestaat uit drie hoofdonderdelen: een deel dat de qubits bevat, een methode voor het overbrengen van signalen naar de qubits, en een klassieke computer voor het uitvoeren van een programma en het verzenden van instructies.

- Het kwantummateriaal dat voor qubits wordt gebruikt, is kwetsbaar en zeer gevoelig voor storingen uit de omgeving. Voor sommige methoden van qubitopslag wordt de eenheid die de qubits bevat, gekoeld tot een temperatuur vlak boven het absolute nulpunt om de coherentie te maximaliseren. Bij andere typen systemen die qubits bevatten, wordt gebruikgemaakt van een vacuümkamer om trillingen te minimaliseren en de qubits te stabiliseren.  
- Signalen kunnen naar de qubits worden verzonden met behulp van diverse methoden, waaronder microgolven, lasers en spanningsverschillen.

Het bedienen van kwantumcomputers kent een groot aantal uitdagingen. Foutcorrectie in kwantumcomputers vormt een aanzienlijk probleem en het opschalen (toevoegen van meer qubits) verhoogt het aantal fouten dat optreedt. Vanwege deze beperkingen is een kwantum-pc voor op het bureau nog toekomstmuziek; een commercieel interessante kwantumcomputer in een laboratorium is echter dichterbij.

## <a name="quantum-simulators"></a>Kwantumsimulators

Met de kwantumsimulators die op klassieke computers worden uitgevoerd, kunt u het uitvoeren van kwantumalgoritmen op een kwantumsysteem simuleren.  De Quantum Development Kit (QDK) van Microsoft bevat een volledige vectorsimulator en tevens andere gespecialiseerde kwantumsimulators.

## <a name="topological-qubit"></a>Topologische qubit

Microsoft is bezig met de ontwikkeling van een kwantumcomputer op basis van topologische qubits. Een topologische qubit zal minder worden beïnvloed door veranderingen van de omgeving, waardoor de vereiste mate van externe foutcorrectie zal afnemen.

Topologische qubits zijn stabieler en beter bestand tegen omgevingsruis, wat betekent dat ze makkelijker kunnen worden geschaald en langer betrouwbaar blijven.

## <a name="microsoft-and-quantum-hardware-partnerships"></a>Partnerschappen van Microsoft en kwantumhardware

Microsoft is partnerschappen aangegaan met IonQ, Honeywell en QCI, fabrikanten van kwantumhardware, om in de toekomst kwantumcomputers toegankelijk te maken voor ontwikkelaars. Ontwikkelaars die gebruikmaken van het Azure Quantum-platform kunnen de Quantum Development Kit (QDK) van Microsoft en Q# gebruiken om kwantumprogramma's te schrijven en deze op afstand uit te voeren.

## <a name="quantum-computations"></a>Kwantumberekeningen

Het uitvoeren van berekeningen op een kwantum computer of kwantumsimulator verloopt volgens een eenvoudig proces:

- Toegang tot de qubits
- Initialiseren van de qubits tot de gewenste toestand
- Bewerkingen uitvoeren om de toestanden van de qubits te transformeren
- Meten van de nieuwe toestanden van de qubits

Het initialiseren en transformeren van qubits wordt uitgevoerd met behulp van **kwantumbewerkingen** (ook wel kwantumpoorten genoemd). Kwantumbewerkingen zijn vergelijkbaar met logische bewerkingen in het klassieke computing, zoals AND, OR, NOT en XOR. Een bewerking kan heel eenvoudig zijn, bijvoorbeeld het omkeren van de toestand van een qubit van 1 naar 0. Het kan ook ingewikkelder zijn, zoals het verstrengelen van een paar qubits of het gebruik van meerdere bewerkingen in serie om de kans te beïnvloeden dat een qubit in superpositie ineenstort (naar een van beide toestanden).

> [!NOTE] 
> De [Q#-bibliotheken](xref:microsoft.quantum.libraries) bieden ingebouwde bewerkingen waarmee complexe combinaties van kwantumbewerkingen op een lager niveau worden gedefinieerd. U kunt de bewerkingen uit de bibliotheek gebruiken om qubits te transformeren en om complexe, door de gebruiker gedefinieerde bewerkingen te creëren.  

Als de uitkomst van de berekening wordt gemeten, hebben we een antwoord, maar voor sommige kwantumalgoritmen is dat niet noodzakelijkerwijs het juiste antwoord. Omdat de uitkomst van bepaalde kwantumalgoritmen is gebaseerd op de waarschijnlijkheid die is geconfigureerd door de kwantumbewerkingen, worden deze berekeningen meerdere keren uitgevoerd om een kansverdeling te krijgen en de nauwkeurigheid van de uitkomsten te verfijnen.  Zekerheid dat een bewerking een correct antwoord retourneert, wordt wel kwantumverificatie genoemd en vormt een aanzienlijke uitdaging voor de kwantumcomputing.

## <a name="summary"></a>Samenvatting

Kwantumcomputing kent een aantal van dezelfde concepten als het klassieke computing, maar verschilt op enkele punten. Enkele principes:

- Kwantumhardware is kostbaar en kwetsbaar om mee te werken, dus er worden kwantumsimulators gebruikt om programma's te schrijven en te testen.
- Zowel klassieke als kwantumcomputers gebruiken logische bewerkingen (of poorten) om berekeningen voor te bereiden.
- Kwantumberekeningen retourneren waarschijnlijkheden.

De vooruitgang in de kwantumhardware en -techniek is snel aan het veranderen. Hier ziet u slechts een paar voorbeelden van de [huidige ontwikkelingen](https://phys.org/search/?search=quantum+computer&s=0).

## <a name="next-steps"></a>Volgende stappen

[Wat wordt verstaan onder de Q#-programmeertaal en de QDK?](xref:microsoft.quantum.overview.q-sharp)
