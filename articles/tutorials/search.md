---
title: Zoek algoritme van de Grover uitvoeren in de Q# Quantum Development Kit
description: Bouw een Q# project dat het algoritme van Grover toont, een van de canonieke Quantum algoritmen.
author: cgranade
ms.author: chgranad
ms.date: 10/19/2019
ms.topic: tutorial
uid: microsoft.quantum.quickstarts.search
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5e0398338ff710decc0f3038c07c9b7d39514195
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856637"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a>Zelfstudie: Zoekalgoritme van Grover implementeren in Q\#

In deze zelfstudie leert u hoe u het zoekalgoritme van Grover kunt bouwen en uitvoeren om het doorzoeken van niet-gestructureerde gegevens te versnellen.  De zoek functie van Grover is een van de populairste Quantum Computing-algoritmen, en met deze relatief kleine Q# implementatie krijgt u een beeld van de voor delen van het Program meren van Quantum oplossingen met een Quantum-programmeer taal op hoog niveau voor het weggeven van Q# Quantum algoritmen.  Aan het einde van de quickstart ziet u dat in een lijst met ongeordende vermeldingen een bepaalde tekenreeks wordt gevonden in een fractie van de tijd die nodig zou zijn om de hele lijst op een klassieke computer te doorzoeken.

Het algoritme van Grover doorzoekt een lijst met ongestructureerde gegevens op specifieke items. Het algoritme kan bijvoorbeeld deze vraag beantwoorden: Is deze kaart uit een spel kaarten een hartenaas? De labeling van het specifieke item wordt _marked input_ genoemd.

Als een kwantumcomputer het zoekalgoritme van Grover gebruikt, heeft deze zoekopdracht gegarandeerd minder stappen nodig dan het aantal items in de lijst die u doorzoekt, iets wat geen enkel klassiek algoritme kan. Deze hogere snelheid is verwaarloosbaar in het geval van een spel kaarten, maar in lijsten met miljoenen of miljarden items, is de tijdswinst aanzienlijk.

U kunt met slechts een paar regels code het zoekalgoritme van Grover bouwen.

## <a name="prerequisites"></a>Vereisten

- De Microsoft [Quantum Development Kit][install].

## <a name="what-does-grovers-search-algorithm-do"></a>Wat doet het zoekalgoritme van Grover?

Het algoritme van Grover vraagt of een item in een lijst het item is dat we zoeken. Hiervoor wordt een kwantumsuperpositie samengesteld van de indexen van de lijst met elke coëfficiënt, of waarschijnlijkheidsamplitude, waarmee de waarschijnlijkheid wordt aangegeven dat die specifieke index de index is die u zoekt.

De kern van het algoritme bestaat uit twee stappen die de coëfficiënt van de gezochte index incrementeel ophogen, totdat de waarschijnlijkheidsamplitude van die coëfficiënt één benadert.

Het aantal incrementele ophogingen is minder dan het aantal items in de lijst. Dit is de reden waarom het zoekalgoritme van Grover minder stappen nodig heeft voor de zoekopdracht dan een klassiek algoritme.

![Functioneel diagram van het zoekalgoritme van Grover](~/media/grover.png)

## <a name="write-the-code"></a>De code schrijven

1. [Maak een nieuw Q# project voor de toepassing](xref:microsoft.quantum.install.standalone)met behulp van de Quantum Development Kit. Titel van het project `Grover`.

1. Voeg de volgende code toe aan het bestand `Program.qs` in uw nieuwe project:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. Als u de lijst wilt definiëren om te doorzoeken, maakt u een nieuw bestand `Reflections.qs` en plakt u daar de volgende code in:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    Met de bewerking `ReflectAboutMarked` wordt de marked input gedefinieerd die u zoekt: de reeks van afwisselend nullen en enen. In dit voorbeeld wordt de marked input in code vastgelegd en kan deze worden uitgebreid om te zoeken naar andere invoer of worden gegeneraliseerd voor willekeurige invoer.

1. Voer vervolgens het nieuwe Q# programma uit om het item te vinden dat is gemarkeerd door `ReflectAboutMarked` .

### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>Q# toepassingen met Visual Studio of Visual Studio code

De bewerking of functie die is gemarkeerd met het `@EntryPoint()` kenmerk op een Simulator-of resource-Estimator wordt uitgevoerd, afhankelijk van de project configuratie en opdracht regel opties.

Druk in Visual Studio op CTRL + F5 om het script uit te voeren.

Bouw in VS Code `Program.qs` voor de eerste keer door het onderstaande in de terminal in te voeren:

```Command line
dotnet build
```

Voor nieuwe uitvoeringen is het niet nodig om de build opnieuw te doen. Typ de volgende opdracht en druk op enter om hem uit te voeren:

```Command line
dotnet run --no-build
```

U ziet het volgende bericht in de terminal:

```
operations.qs:
This operation applies Grover's algorithm to search all possible inputs to an operation to find a particular marked state.
Usage:
operations.qs [options] [command]

--n-qubits <n-qubits> (REQUIRED)
-s, --simulator <simulator>         The name of the simulator to use.
--version                           Show version information
-?, -h, --help                      Show help and usage information
Commands:
```

Dit komt omdat u niet het aantal qubits hebt opgegeven dat u wilde gebruiken. de terminal toont u de opdrachten die beschikbaar zijn voor het uitvoer bare programma. Als we 5 qubits willen gebruiken, moeten we het volgende typen:

```Command line
dotnet run --n-qubits 5
```

Als u op enter drukt, ziet u de volgende uitvoer:

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a>Volgende stappen

Als u deze zelf studie hebt, raadpleegt u een aantal van de onderstaande bronnen voor meer informatie over hoe u kunt gebruiken Q# om uw eigen Quantum toepassingen te schrijven:

- [Terug naar de handleiding Aan de slag met de Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)
- Probeer een meer algemeen [voorbeeld](https://github.com/microsoft/Quantum/tree/main/samples/algorithms/database-search) van het zoekalgoritme van Grover
- [Meer informatie over het zoekalgoritme van Grover met de Quantum Katas](xref:microsoft.quantum.overview.katas)
- Lees meer over [amplitudeversterking][amplitude-amplification], de techniek van kwantumcomputing die de basis vormt van het zoekalgoritme van Grover
- [Concepten van kwantumcomputing](xref:microsoft.quantum.concepts.intro)
- [Voorbeelden Quantum Development Kit](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
