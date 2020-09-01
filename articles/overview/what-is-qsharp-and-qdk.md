---
title: Wat wordt verstaan onder de Q#-programmeertaal en de QDK?
description: Meer informatie over de Microsoft Quantum Development Kit, de Q#-programmeertaal en hoe u kwantumprogramma's kunt maken.
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.q-sharp
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5db574b0380ffa1616cb3959d84925854df4e321
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863777"
---
# <a name="what-are-the-no-locq-programming-language-and-qdk"></a>Wat wordt verstaan onder de Q#-programmeertaal en de QDK?

Q# is de opensource-programmeertaal van Microsoft voor het ontwikkelen en uitvoeren van kwantumalgoritmen. Deze maakt deel uit van de Quantum Development Kit (QDK), met onder meer [Q#-bibliotheken](xref:microsoft.quantum.libraries), [kwantumsimulators](xref:microsoft.quantum.machines), [extensies voor andere programmeeromgevingen](xref:microsoft.quantum.install) en [API-documentatie](xref:microsoft.quantum.standardlibsintro). Naast de Standard Q#-bibliotheek bevat de QDK ook scheikunde-, machine learning- en numerieke bibliotheken.

Als programmeertaal bevat Q# bekende elementen uit Python, C# en F#, en ondersteunt het een eenvoudig proceduremodel voor het schrijven van programma's met lussen, if/then-instructies en veelvoorkomende gegevenstypen. De taal introduceert tevens nieuwe, kwantumspecifieke gegevensstructuren en bewerkingen.

## <a name="what-can-i-do-with-the-qdk"></a>Wat kan ik met de QDK doen?

De QDK is een volledige Development Kit voor Q# die u kunt gebruiken met gangbare hulpprogramma's en talen om kwantumtoepassingen te ontwikkelen die u in verschillende omgevingen kunt uitvoeren. Q#-programma's kunnen worden uitgevoerd als een consoletoepassing, via Jupyter Notebooks, of gebruikmaken van een Python- of .NET-hostprogramma.

### <a name="develop-in-common-tools-and-environments"></a>Ontwikkelen in veelgebruikte tools en omgevingen

Integreer uw kwantumontwikkeling met [Visual Studio, Visual Studio Code](xref:microsoft.quantum.install.standalone) en [Jupyter Notebooks](xref:microsoft.quantum.install.jupyter). Gebruik de ingebouwde API's voor het koppelen van uw programma's met [Python](xref:microsoft.quantum.install.python)- en [.NET](xref:microsoft.quantum.install.cs)-hostprogramma's.

### <a name="try-quantum-operations-and-domain-specific-libraries"></a>Kwantumbewerkingen en domeinspecifieke bibliotheken uitproberen

Schrijf en test kwantumalgoritmen voor het verkennen van superpositie, verstrengeling en andere kwantumbewerkingen. Met de Q#-bibliotheken kunt u complexe kwantumbewerkingen uitvoeren zonder dat u bewerkingsreeksen op laag niveau hoeft te ontwerpen.

### <a name="run-programs-in-simulators"></a>Programma's uitvoeren in simulators

Voer uw kwantumprogramma's uit in een volledige kwantumsimulator, een Toffoli-simulator met beperkt bereik of test uw Q#-code in verschillende resourceschattingen. 

## <a name="where-can-i-learn-more"></a>Waar vind ik meer informatie?

|||
| ---- | ---- |
| **Ik ben niet bekend met kwantumcomputing** | Bekijk een aantal basisbeginselen uit de kwantumfysica en kwantumcomputing in [Basisconcepten](xref:microsoft.quantum.overview.understanding).|
| **Ik wil me verder verdiepen in de Q#-taal** | Maak kennis met typen, expressies, variabelen en de kwantumprogrammastructuur in de [Q#-gebruikers handleiding](xref:microsoft.quantum.guide).|
| **Ik wil alleen maar kwantumprogramma's schrijven** | Stel uw Q#-omgeving in en begin met het schrijven van kwantumprogramma's in [QuickStarts](xref:microsoft.quantum.install).|

## <a name="how-does-no-locq-work"></a>Hoe werkt Q#?

Een Q#-programma kan worden gecompileerd in een zelfstandige toepassing of worden aangeroepen door een hostprogramma dat in Python of een .NET-taal is geschreven.

Wanneer u het programma compileert en uitvoert, wordt er een exemplaar van de kwantumsimulator gemaakt en de Q#-code hieraan doorgegeven. De simulator gebruikt de Q#-code voor het maken van qubits (simulaties van kwantumdeeltjes) en het toepassen van transformaties om hun toestand te wijzigen. De resultaten van de kwantumbewerkingen in de simulator worden vervolgens teruggestuurd naar het programma.  

Het isoleren van de Q#-code in de simulator zorgt ervoor dat de algoritmen de wetten van kwantumfysica volgen en op de juiste wijze op kwantumcomputers kunnen worden uitgevoerd.

![qsharp-code-flow](~/media/qsharp-code-flow.png)

## <a name="how-do-i-use-the-qdk"></a>Hoe kan ik de QDK gebruiken?

Alles wat u nodig hebt om Q#-programma's te schrijven en uit te voeren, inclusief de Q#-compiler, de Q#-bibliotheken en de kwantumsimulators, kan worden geïnstalleerd op uw lokale computer en hierop worden uitgevoerd. Na verloop van tijd kunt u uw Q#-programma's op afstand uitvoeren op een echte kwantumcomputer, maar tot die tijd leveren de kwantumsimulators die met de QDK worden meegeleverd, nauwkeurige en betrouwbare resultaten.

- Het ontwikkelen van [Q#-toepassingen](xref:microsoft.quantum.install.standalone) is de snelste manier om aan de slag te gaan.

- Voer zelfstandige [Jupyter-notebooks uit met IQ#](xref:microsoft.quantum.install.jupyter), een Jupyter-extensie voor het compileren, simuleren en visualiseren van Q#-programma's.

- Als u bekend bent met [Python](xref:microsoft.quantum.install.python), kunt u dit gebruiken als een hostprogrammeerplatform om aan de slag te gaan. Python wordt niet alleen veelvuldig gebruikt door ontwikkelaars, maar ook door wetenschappers, onderzoekers en docenten.

- Als u al ervaring hebt met [C#, F# of VB.NET](xref:microsoft.quantum.install.cs) en bekend bent met de Visual Studio-ontwikkelomgeving, hoeft u slechts enkele extensies aan Visual Studio toe te voegen om het voor te bereiden voor Q#.  

## <a name="summary"></a>Samenvatting

Q# is een opensource-programmeertaal voor het ontwikkelen van kwantumprogramma's. Q# bevat bibliotheken waarmee u complexe kwantumbewerkingen kunt maken, en kwantumsimulators om uw programma's nauwkeurig uit te voeren en te testen. Q#-programma's kunnen worden uitgevoerd als zelfstandige apps of worden aangeroepen vanuit een Python- of .NET-hostprogramma, en kunnen worden geschreven, uitgevoerd en getest vanaf uw lokale computer.

## <a name="next-steps"></a>Volgende stappen

[Lineaire algebra voor kwantumcomputing](xref:microsoft.quantum.overview.algebra)
