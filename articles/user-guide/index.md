---
title: Q#-gebruikershandleiding
description: Overzicht van het doel en de inhoud van de gebruikershandleiding
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: 979e468cc743bd9125eaba0b71f794977c914447
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231754"
---
# <a name="the-no-locq-user-guide"></a>Q#-gebruikershandleiding

Welkom bij de Q#-gebruikershandleiding. 

In de verschillende onderwerpen van deze handleiding introduceren we een aantal basisbeginselen voor het ontwikkelen van kwantumprogramma's met Q#.

We verwijzen naar de [Q#-taalhandleiding](xref:microsoft.quantum.qsharp.index) voor een volledige specificatie en documentatie van de Q#-kwantumcomputertaal. 

## <a name="user-guide-contents"></a>Inhoud van de gebruikershandleiding

- [Q#-programma's](xref:microsoft.quantum.guide.programs): Een korte inleiding tot kwantumprogramma's in Q#. 

- [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs): beschrijft hoe een Q#-programma wordt uitgevoerd, en biedt een overzicht van de verschillende manieren waarop u het programma kunt aanroepen: vanuit de opdrachtregel, in Q# Jupyter Notebooks, of vanuit een klassiek hostprogramma dat in Python of een .NET-taal is geschreven.

- [Testen en foutopsporing](xref:microsoft.quantum.guide.testingdebugging): hierin wordt een aantal technieken uitgelegd om ervoor te zorgen dat uw code doet wat die moet doen. 
    Als gevolg van de algemene matheid van kwantuminformatie, kunnen er voor het opsporen van fouten in een kwantumprogramma gespecialiseerde technieken nodig zijn. 
    Gelukkig ondersteunt Q# veel van de klassieke foutopsporingstechnieken waarmee programmeurs bekend zijn, evenals technieken die kwantumspecifiek zijn. Deze omvatten het maken en uitvoeren van eenheidstests in Q#, het insluiten van *asserties* voor waarden en waarschijnlijkheden in uw code en de `Dump`-functies die de statussen van de doelmachines uitvoeren. 
    De laatste kunnen worden gebruikt in onze volledige simulator om fouten in bepaalde berekeningen op te sporen door kwantumlimieten te introduceren, bijvoorbeeld de [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).

### <a name="quantum-simulators-and-resource-estimators"></a>Kwantumsimulators en resourceschattingen

- [Kwantumsimulatoren en hosttoepassingen](xref:microsoft.quantum.machines): Een overzicht van de verschillende beschikbare simulatoren, evenals hoe hostprogramma's en doelmachines samenwerken om Q#-programma's uit te voeren.

- [Volledige statussimulator](xref:microsoft.quantum.machines.full-state-simulator): de doelcomputer die de volledige kwantumstatus simuleert. Handig voor het volledig uitvoeren of debuggen van kleinere programma's (minder dan een paar dozijn qubits)

- [Resoureschattingen](xref:microsoft.quantum.machines.resources-estimator): maakt een schatting van het aantal benodigde resources om een bepaald exemplaar uit te voeren van een Q#-bewerking in een kwantumcomputer.

- [Traceersimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Voert een kwantumprogramma uit zonder de toestand van een kwantumcomputer daadwerkelijk te simuleren en kan daarom kwantumprogramma's simuleren die duizenden qubits gebruiken. Handig om klassieke code binnen een kwantumprogramma te debuggen en om in te schatten hoeveel resources zijn vereist.

- [Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator): een kwantumsimulator voor speciale doeleinden die kan worden gebruikt met miljoenen qubits, maar alleen voor programma's met een beperkte set kwantumbewerkingen (X, CNOT en multi-controlled X).

### <a name="quick-reference-pages"></a>Snelzoekpagina's

- [IQ# Magic-opdrachten](xref:microsoft.quantum.guide.quickref.iqsharp): Snelzoekpagina voor IQ# Magic-opdrachten binnen Q# Jupyter Notebooks.
