---
title: Wat zijn Q# en de QDK?
description: Lees hier meer over Q#, een programmeertaal van Microsoft voor het ontwikkelen van toepassingen voor kwantumcomputers en een cruciaal onderdeel van de Quantum Development Kit van Microsoft
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.qsharp
ms.openlocfilehash: a4bf21887e34ac85f75e5e0b9a033138464fd09d
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2020
ms.locfileid: "77906998"
---
# <a name="what-are-q-and-the-qdk"></a>Wat zijn Q# en de QDK?

Q# is een programmeertaal met functies die speciaal zijn ontworpen voor gebruik in kwantumcomputing.
Als belangrijk onderdeel van de Quantum Development Kit van Microsoft biedt Q# kwantumprogrammeurs een framework waarmee ze zich kunnen concentreren op de algoritmen zonder dat ze zich zorgen hoeven te maken over technische details zoals het optimaliseren van de gate-sequence of de fysieke implementatie van een kwantumcomputer.

De QDK omvat een verscheidenheid aan hulpprogramma's, waarmee ontwikkelaars alles hebben dat nodig is om kwantumprogramma's te schrijven.
Naast de Q#-taal omvat de QDK:
* de *Q#-bibliotheken*, waarmee ontwikkelaars gelijk aan de slag kunnen om echte kwantumtoepassingen te maken
* verschillende *doelmachines* waarop Q#-programma's kunnen worden uitgevoerd. Dit zijn onder andere tools voor resource-inschatting en simulatoren voor grotere kwantumprogramma's, evenals een volledige kwantumsimulator, die zich als een ruisvrije kwantumcomputer gedraagt. Deze laatste is zeer nuttig bij het experimenteren met ideeën, foutopsporing van programma's en leren over kwantumfysica, maar alleen efficiënt voor programma's met relatief weinig qubits. We kijken ernaar uit dat we in de toekomst hardware voor kwantumcomputing als doelmachines beschikbaar kunnen maken.
* *hulpprogramma's* om het gebruik van Q# zo naadloos mogelijk te maken, zoals uitbreidingen voor Visual Studio en VS Code en pakketten voor gebruik met Python en Jupyter Notebook.
* *API-documentatie* om Q# te combineren met klassieke host-talen zoals Python en C#

Toepassingen die zijn ontwikkeld met de Quantum Development Kit van Microsoft bestaan doorgaans uit twee delen:
1. Een of meer kwantumalgoritmen, geïmplementeerd met behulp van de kwantumprogrammeertaal Q# en aangeroepen door het klassieke host-programma. Deze bestaan uit: 
    - Q#-bewerkingen: subroutines met kwantumbewerkingen, en 
    - Q#-functies: klassieke subroutines die worden gebruikt binnen het kwantumalgoritme.
2. Een klassiek programma, geïmplementeerd in een klassieke programmeertaal als Python of C#, dat als het belangrijkste toegangspunt fungeert en Q#-bewerkingen aanroept om een kwantumalgoritme uit te voeren.

## <a name="write-quantum-programs-not-quantum-circuits"></a>Kwantumprogramma's schrijven, geen kwantumcircuits

In het begintijdperk van de kwantumcomputing werden algoritmen gevisualiseerd als schema's, vergelijkbaar met circuitschema's in klassieke computing.
Hoewel het circuitmodel jarenlang nuttig is geweest in het onderzoek naar kwantumcomputing, zijn we bij Microsoft van mening dat kwantumcircuits nog maar het begin zijn voor ontwikkelaars en dat ze kwantumalgoritmen en -toepassingen kunnen ontwikkelen met Q#.
Bij het ontwikkelen van de Q#-taal hebben we rekening gehouden met wat we hebben geleerd in tientallen jaren ontwikkeling van klassieke software om kwantumontwikkelaars te voorzien van een high-level taal die specifiek is gericht op kwantumcomputing.

## <a name="how-does-q-work"></a>Hoe werkt Q#?

De programmeertaal Q# biedt een intuïtieve set met typen, bewerkingen en logische expressies voor het ontwikkelen van algoritmen zonder dat u rekening hoeft te houden met de interne logica van de kwantumcomputer.

Een van de fundamentele bouwstenen van Q# is het `Qubit`-type, dat niet kan worden gekopieerd en ook niet rechtstreeks toegankelijk is, net als een echte qubit.
In plaats daarvan kunnen we deze meten en het resultaat van de meting opslaan in een `Result`-variabele; een Q#-type dat twee mogelijke waarden kan aannemen: `Zero` en `One`.
Constructies zoals deze garanderen dat algoritmen altijd de wetten van de kwantumfysica respecteren en correct kunnen worden uitgevoerd op kwantumcomputers of simulators.

Q# bevat ook functies van klassieke logica zoals voorwaarden en lussen, met een aantal nuanceringen om ervoor te zorgen dat alle kwantumregels worden nageleefd.
U kunt bijvoorbeeld de manier beperken waarop lussen worden uitgevoerd om ervoor te zorgen dat quantumbewerkingen niet worden aangeroepen binnen functies die alleen deterministische klassieke subroutines kunnen bevatten.

Programma's geschreven in Q# zijn vaak gekoppeld aan een hostprogramma dat is geschreven in C# of Python, waarmee klassieke code en kwantumcode op een handige manier kunnen worden geordend.
Naast de ondersteuning van talen zoals C# en Python biedt de QDK ondersteuning voor Jupyter-notebooks met de Jupyter-kernel IQ#.

## <a name="what-can-i-use-q-for"></a>Waar kan ik Q# voor gebruiken?

### <a name="use-q-to-learn-quantum-computing"></a>Kwantumcomputing leren met Q#

Tot nu toe was kennis van het circuitmodel nodig om te leren werken met kwantumcomputing, teneinde de algoritmen te begrijpen in de vorm van geordende reeksen kwantum-gates en metingen. Met Q# kunt u een ander traject volgen: kwantumcomputing leren door kwantumprogramma's te schrijven.

### <a name="use-q-to-design-quantum-algorithms"></a>Q# gebruiken om kwantumalgoritmen te ontwerpen

Er zijn steeds meer bibliotheken en door de gebruiker gedefinieerde typen beschikbaar voor Q# waarmee u hulpprogramma's en functies kunt implementeren om zo geavanceerde kwantumalgoritmen te maken. Stel dat u de twee qubits q1 en q2 moet verstrengelen. In plaats van afzonderlijk de benodigde gates toe te passen om dit te realiseren, kunt u de al ingebouwde bewerking `PrepareEntangledState([q1], [q2])` gebruiken.

### <a name="use-q-to-estimate-quantum-resources"></a>Q# gebruiken om een schatting te maken van kwantumbronnen

U kunt de uitvoering van uw Q#-programma simuleren met behulp van de full-state kwantumsimulator die wordt geleverd bij de Quantum Development Kit (QDK).  De QDK biedt ook bronschattingen die u inzicht geven in de prestaties van Q#-programma's die te groot zijn om te worden uitgevoerd op een simulator.  Dit is zeer nuttig voor ontwerpers van algoritmen omdat ze hun programma's kunnen afstemmen op het gebruik van minder bronnen (bijvoorbeeld minder qubits waarop minder bewerkingen worden uitgevoerd), om te worden uitgevoerd op oudere kwantumhardware op kleinere schaal.

### <a name="use-q-to-validate-hardware-performance"></a>Q# gebruiken om de prestaties van hardware te valideren

Het mooie van Q# is dat een programma maar eenmaal hoeft te worden geschreven en vervolgens zowel kan worden uitgevoerd op kwantumsimulators voor foutopsporing, als op verschillende hardware voor kwantumcomputers.  Benchmarkprogramma's die zijn geschreven in Q# kunnen worden uitgevoerd voor het valideren van de prestaties van hardware en het vergelijken van resultaten wanneer kwantumcomputers zich ontwikkelen en er nieuwe kwantumcomputers beschikbaar komen.  

## <a name="next-steps"></a>Volgende stappen

* [Waar leer ik meer over kwantumcomputing?](xref:microsoft.quantum.overview.learn)
* [Get started with the Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome) (Aan de slag met de Microsoft Quantum Development Kit)
