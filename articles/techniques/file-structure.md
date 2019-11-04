---
title: Inleiding tot het ontwikkelen van Quantum technieken | Microsoft Docs
description: Inleiding tot het ontwikkelen van Quantum technieken
author: QuantumWriter
ms.author: Christopher.Granade@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 702d23293a1c340ddd3d7032d0e05294345469b2
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442558"
---
# <a name="q-program-overview"></a>Q # programma overzicht

Q # is een schaal bare, op domeinen gebaseerde programmeer taal die specifiek is voor het gebruik van Quantum Computing. Q # is een Quantum-programmeer taal in die IT kan worden gebruikt om te beschrijven hoe instructies op Quantum machines worden uitgevoerd. De computers waarop het bereik kan worden toegepast, kunnen variëren van simulatoren tot echte kwantum-hardware. Q # is schaalbaar: het kan worden gebruikt voor het schrijven van eenvoudige demonstratie Programma's, zoals het teleporteren die worden uitgevoerd op een paar qubits, maar biedt ook ondersteuning voor het schrijven van grote, geavanceerde Program ma's, zoals simulaties van complexe moleculen die grote machines met miljoenen qubits nodig hebben. Hoewel grote fysieke machines zich nog steeds in de toekomst bevinden, staat Q # toe dat een programmeur nu complexe Quantum algoritmen kan Program meren. Wat meer is, Q # ondersteunt diverse taken zoals fout opsporing, profile ring, resource schatting en bepaalde speciale simulaties op een schaal bare manier. 

Vanuit een technisch perspectief kan een Quantum programma worden gezien als een bepaalde set klassieke functies die, indien aangeroepen, Quantum circuits genereren als neven effecten. Een belang rijk gevolg van deze weer gave is dat een programma dat is geschreven in Q # niet rechtstreeks model qubits is, maar in plaats daarvan beschrijft hoe een klassieke beheer computer communiceert met deze qubits.
Standaard worden met Q # geen Quantum toestanden of andere eigenschappen van Quantum-mechanismen gedefinieerd, maar wel direct via de actie van de verschillende subroutines die in de taal zijn gedefinieerd.
Bekijk bijvoorbeeld de status $ \ket{+} = \left (\ket{0} + \ket{1}\right)/\sqrt{2}$, zoals beschreven in de hand leiding over de [quantum computing-concepten](xref:microsoft.quantum.concepts.intro) .
Als u deze status wilt voorbereiden in Q #, gebruiken we de feiten die de qubits hebben geïnitialiseerd in $ \ket{0}$ status en dat $ \ket{+} = H\ket{0}$, waarbij $H $ de Hadamard-trans formatie is:

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0〉.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0〉 = |+〉, as we wanted.
}
```
## <a name="q-tranformations-of-quantum-states"></a>Q # tranformations van Quantum Staten

Het is belang rijk dat u bij het schrijven van het bovenstaande programma niet expliciet naar de status van Q # verwijst, maar in plaats daarvan hebt aangegeven hoe de status door ons programma is *getransformeerd* .
Net als bij de manier waarop een grafische arcerings programma een beschrijving van trans formaties naar elk hoek punt samenvoegt, accumuleert een Quantum programma in Q # trans formaties naar Quantum statussen.
Op deze manier kunnen we volledig neutraal over wat een Quantum staat, *zelfs op elke* doel computer, die verschillende interpretaties kan hebben, afhankelijk van de computer. 

Vanuit het perspectief van een Q #-programma is een Qubit een volledig dekkende verwijzing naar de interne structuur van een doel machine.
Een Q #-programma heeft geen mogelijkheid om introspect te gaan in de status van een Qubit, de weer gave op een doel machine of zelfs op dezelfde Qubit als andere Qubit die beschikbaar zijn voor het programma.
Een programma kan in plaats daarvan bewerkingen als `Measure` aanroepen om informatie uit een Qubit te leren en om bewerkingen zoals `X` en `H` aan te roepen om te reageren op de status van een Qubit.
Deze bewerkingen hebben geen intrinsieke definitie in de taal en worden alleen concreet gemaakt door de doel computer die wordt gebruikt om een bepaald Q #-programma uit te voeren.
Een Q #-programma recombineert deze bewerkingen, zoals gedefinieerd door een doel machine, om nieuwe bewerkingen op een hoger niveau te maken voor een snelle Quantum berekening.
Op deze manier maakt Q # het eenvoudig om de logische en hybride Quantum-algoritmen te kunnen uitdrukken, en is het ook algemeen wat betreft de structuur van een doel machine of Simulator.

## <a name="q-operations-and-functions"></a>Q # bewerkingen en functies

In concrete zin is een Q #-programma bestaande uit een of meer *bewerkingen*, een of meer *functies*en door de gebruiker gedefinieerde typen. Bewerkingen worden gebruikt om de trans formaties van de status van een Quantum machine te beschrijven en zijn de meest elementaire bouw stenen van Q #-Program ma's. Elke bewerking die is gedefinieerd in Q # kan vervolgens een wille keurig aantal andere bewerkingen aanroepen, met inbegrip van de ingebouwde *intrinsieke* bewerkingen die worden geïmplementeerd door een doel machine.
Bij compilatie wordt elke bewerking weer gegeven als een .NET-klassetype dat kan worden geleverd aan doel computers.

In tegens telling tot bewerkingen worden functies gebruikt om louter klassiek gedrag te beschrijven en geen effecten te hebben, behalve het berekenen van klassieke uitvoer waarden. Q # is een sterk getypeerde taal en wordt geleverd met een set ingebouwde primitieve typen, en biedt ondersteuning voor door de gebruiker gedefinieerde typen. 

In de rest van deze hand leiding wordt uitgelegd hoe u verschillende taal concepten en-constructies kunt gebruiken om te helpen bij het definiëren van complexe Quantum Programma's via de basis bouwstenen van bewerkingen, functies en typen. 

## <a name="structure-of-q-source-files"></a>Structuur van Q # bron bestanden

Een Q #-bron bestand bestaat mini maal uit een *naam ruimte declaratie*, waarmee een .net-naam ruimte wordt opgegeven die de definities in het bron bestand bevat.
Definities van andere Q #-bron bestanden en-bibliotheken kunnen worden opgenomen met behulp van de `open`-instructie.
Zo worden bijvoorbeeld de meeste Operations-basis poorten gedefinieerd in de naam ruimte <xref:microsoft.quantum.intrinsic>.
Om dit beschikbaar te maken voor onze code, `open` u de naam ruimte aan de bovenkant van elk bestand.

```qsharp
namespace Example {
    open Microsoft.Quantum.Intrinsic;

    // ...
}
```

Binnen een naam ruimte kan elk Q #-bron bestand een wille keurige combi natie van *bewerkingen*, *functies*en door de *gebruiker gedefinieerde typen*definiëren.
In de rest van deze sectie beschrijven we elk op zijn beurt en bieden we voor beelden van hoe ze in de praktijk kunnen worden gebruikt om nuttige Quantum Program ma's te maken.
