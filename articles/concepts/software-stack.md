---
title: Software stack | Microsoft Docs
description: Software stack
author: QuantumWriter
uid: microsoft.quantum.concepts.software-stack
ms.author: nawiebe@microsoft.com
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: f97dfacf6cde5fa92e1f368efaae36554a5c944d
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2019
ms.locfileid: "73184726"
---
# <a name="software-stack-for-quantum-computing"></a>Software stack voor Quantum Computing
Normaal gesp roken wordt een computer voor één apparaat gebruikt, maar moderne computer omgevingen zijn veel complexer en Geavanceerd. De toepassing waarmee u communiceert, verloopt doorgaans op meerdere lagen software die de uitvoering van de toepassing naar het hardwareniveau bieden. Deze software lagen zijn nodig om de ontwikkeling van een toepassings oplossing uit de onderliggende complexiteit van het volledige computer systeem te abstracten. Als een ontwikkelaar heeft gedenkd over bus, cache architecturen, communicatie protocollen en meer tijdens het schrijven van een eenvoudige smartphone-app, zou de taak veel ingewik kelder worden.  Het concept van een *software stack* is ontwikkeld in klassieke computing om deze problemen op te lossen.  Lenen van het klassieke concept is een software stack ook een belang rijk onderdeel van de visie achter Quantum Computing met Q #.

## <a name="conventional-stack"></a>Conventionele stack
Het belangrijkste idee achter een software stack is recursie.  Het bestaat uit verschillende geneste lagen van interfaces waarmee de details van de lagere niveaus van het apparaat van de ontwikkelaar worden opgebouwd.  Een veelgebruikte software stack omvat bijvoorbeeld het uitvoeren van ASP.NET (een programmeer taal), op SQL Server (een relationele Database Management System), die wordt uitgevoerd boven op Internet Information Services (een webserver), die wordt uitgevoerd op Windows Server (een besturings systeem), dat de computerhardware verstuurt.  Door te kijken naar software als een hiërarchie, kan de ene software schrijven in ASP.NET zonder dat ze de details op laag niveau van alle bijbehorende software moeten begrijpen.

## <a name="quantum-stack"></a>Quantum stack

De software stack in quantum computing is niet anders in principe en werkt in de praktijk op een lager niveau dan traditionele stacks.  Hoe ziet een Quantum stack eruit?  Een quantum computer is geen vervanging voor traditionele (ook wel klassieke) computers genoemd.  In feite zullen quantum computers vrijwel zeker samen werken met klassieke computers voor het oplossen van reken problemen.  Dit veroorzaakt deel uit de kwets bare Quantum gegevens.  Quantum gegevens zijn zo kwetsbaar dat als u deze zelfs bekijkt, de informatie die wordt waargenomen, bijna zeker beschadigd is.  Quantum computers moeten daarom worden ontworpen met een Quantum fout correctie, zodat de interacties van de fysieke omgeving niet per ongeluk de informatie en berekening kunnen beschadigen. Daarom is een natuurlijk doel voor Q # een fout gecorrigeerde quantum computer (ook wel een *fout tolerante* quantum computer genoemd) die een lijst met Quantum instructies (Gates of poort bewerkingen genoemd) accepteert en die instructies toepast op de Quantum gegevens die in het bestand zijn opgeslagen.  Houd er rekening mee dat als het aantal qubits-en Gate-bewerkingen in een Quantum algoritme of programma klein genoeg is, de fout correctie mogelijk niet absoluut nood zakelijk is.  Naarmate het aantal qubits-en poort bewerkingen groeit, is het beter om de software-stack en Q # te bouwen aan aptly en efficiënt fouten te corrigeren en schaal bare, fout tolerante Quantum Computing in te scha kelen.

### <a name="error-correction"></a>Fout correctie
Voor fout correctie moet een snelle en betrouw bare klassieke computer in overleg met de quantum computer worden uitgevoerd om fouten te corrigeren zoals ze worden weer gegeven in de Quantum berekening.  In de praktijk moeten onderdelen, zoals veld-Programmeer bare Gate arrays (Fpga's) of snelle Cryogenic-processors, nodig zijn om de fouten sneller te identificeren en te corrigeren dan ze in de quantum computer in natuurlijke richting oplopen.  Als gevolg hiervan is een quantum computer een hybride computer die bestaat uit verschillende reken apparaten die over een breed scala van Tempe raturen beschikken.  Daarom is het veel handiger om te denken over het Program meren van een quantum computer via de lens van een software stack, omdat er veel hardware-en software lagen (klassiek en Quantum) nodig zijn om de implementatie van een quantum te verzorgen algoritme op een quantum computer.

### <a name="quantum-conceptual-stack"></a>Quantum conceptuele stack
Hieronder ziet u een conceptuele stack die de functionele stroom van factor 8704143553785700723 in een quantum computer omgeving illustreert:

![Software stack](~/media/concepts_stack.png)

### <a name="specification-and-algorithm"></a>Specificatie en algoritme
Er zijn verschillende algemene fasen voor het Program meren van een dergelijke Quantum berekening.  De eerste en weliswaar meest uitdagende fase geeft u het probleem op dat één wil oplossen.  In dit geval is het probleem het getal 8704143553785700723 te vermenigvuldigen met een product van twee priem cijfers.  De volgende stap omvat het ontwerpen van een algoritme voor het oplossen van dit verwerkings probleem.  In dit geval kan het beroemde Quantum Factory-algoritme van Shor worden gebruikt om de factoren te vinden.  Dit algoritme wordt uitgedrukt in Q # en vervolgens wordt een reeks Quantum bewerkingen uitgevoerd die kunnen worden uitgevoerd op een computer met een ideale fout-Free Quantum.  

### <a name="physical-gates"></a>Fysieke Gates
In dit voor beeld wordt ervan uitgegaan dat er een fout vrije quantum computer is, zodat de volgende stap de door Q # uitgelichte bewerkingen uitvoert en deze vertaalt met behulp van sjablonen die zijn opgegeven door de Quantum fout correctie methode die is gekozen in fysieke poorten die de basis-hardware kan worden uitgevoerd.  Dit proces omvat het vervangen van elke logische Qubit die wordt beschreven in het vorige model met een host van fysieke qubits die worden gebruikt voor het opslaan en beveiligen van de informatie binnen één Qubit op een redundante manier die lokale fouten op het fysieke niveau kan voor komen. qubits lang genoeg om dergelijke fouten te detecteren en te corrigeren.  Net zoals de logische qubits die wordt beschreven door de Q #-code moet worden vervangen door veel fysieke qubits, op dezelfde manier moet elke Quantum-poort die in de uitvoer wordt beschreven, worden vertaald naar een reeks fysieke poorten die op de fysieke qubits handelen.  Daarom is de uitvoer van Q # zelden het uiteindelijke doel voor Quantum Computing en zijn er verdere abstractie niveaus nodig om de code op hardware in een Oblivious te kunnen uitvoeren.

### <a name="control-computer"></a>Beheer computer
De fysieke poort reeks wordt vervolgens geladen in een gewone computer die deze instructies verzendt naar een beheer computer die rechtstreeks interfaces met de quantum computer doorgeeft.  Deze laag in de software stack wordt vaak verwerkt door experimentele controle software, zoals [QCoDeS](http://qcodes.github.io/Qcodes/).

### <a name="interface-computer"></a>Interface computer
De laatste stap in dit proces is dat de interface computer eerst de poorten moet streamen die nodig zijn voor een snelle controle computer. De Fast Control-computer past vervolgens de benodigde spanningen (vaak pulsen genoemd) toe om de vereiste poorten op qubits te implementeren. Dit moet worden gedaan bij het corrigeren van fouten die worden waargenomen door middel van een Quantum fout correctie.  Cryogenic Fpga's of andere exotische hardware kan nodig zijn om deze stappen uit te voeren binnen de strikte tijd vereisten die zijn opgelegd door de snelheid waarmee fouten worden weer gegeven op de quantum computer.  De doel taal op dit niveau is vaak [VHDL](https://en.wikipedia.org/wiki/VHDL), wat een unieke manier moet bedenken die wordt gebruikt in het bovenste uiteinde van de stack om een beschrijving van een Quantum algoritme te parseren.

### <a name="the-q-quantum-programming-language"></a>De ' Q # Quantum-programmeer taal
Het doel van Q # is om een eenvoudige taal te bieden waarmee ontwikkel aars code kunnen schrijven die gericht is op een schat aan Quantum Computing platformen en interface met de tussenliggende lagen van software die tussen de gebruiker en het Quantum apparaat staan.  De taal vereenvoudigt dit door het begrip van een software stack te maken en veel van de details van de onderliggende quantum computer samen te stellen, terwijl er C#nog andere niveaus van de stack beschikbaar zijn, zodat deze de benodigde vertalingen van Q #-code naar fundamentele bewerkingen.  Zo kan de ontwikkelaar zich richten op wat ze het beste doen: algoritmen ontwerpen en problemen oplossen.
