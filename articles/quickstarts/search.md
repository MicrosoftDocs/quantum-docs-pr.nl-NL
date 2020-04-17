---
title: Algoritme van Grover uitvoeren in Q# - Quantum Development Kit
description: U gaat een Q#-project maken waarin het algoritme van Grover wordt gedemonstreerd, een van de bekendste kwantumalgoritmen.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 0e64fcd56929fa33397c45bf1b2e99bf687eca6f
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2020
ms.locfileid: "77906947"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a>Quickstart: Zoekalgoritme van Grover implementeren in Q#

In deze quickstart leert u hoe u het zoekalgoritme van Grover kunt bouwen en uitvoeren om het doorzoeken van ongestructureerde gegevens te versnellen.  Het zoekalgoritme van Grover is een van de populairste algoritmen voor kwantumcomputing en deze relatief kleine Q#-implementatie geeft u een beeld van enkele van de voordelen van het programmeren van kwantumoplossingen met de high-level Q#-programmeertaal voor het voorstellen van kwantumalgoritmen.  Aan het einde van de quickstart ziet u dat in een lijst met ongeordende vermeldingen een bepaalde tekenreeks wordt gevonden in een fractie van de tijd die nodig zou zijn om de hele lijst op een klassieke computer te doorzoeken.

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

1. Gebruik de Quantum Development Kit om [een nieuw Q#-project](xref:microsoft.quantum.howto.createproject) met de naam `Grover` te maken in de ontwikkelomgeving van uw keuze.

1. Voeg de volgende code toe aan het bestand `Operations.qs` in uw nieuwe project:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-40":::

1. Als u de lijst wilt definiëren om te doorzoeken, maakt u een nieuw bestand `Reflections.qs` en plakt u daar de volgende code in:

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    Met de bewerking `ReflectAboutMarked` wordt de marked input gedefinieerd die u zoekt: de reeks van afwisselend nullen en enen. In dit voorbeeld wordt de marked input in code vastgelegd en kan deze worden uitgebreid om te zoeken naar andere invoer of worden gegeneraliseerd voor willekeurige invoer.

1. Vervolgens voert u het nieuwe Q#-programma uit om het item te vinden dat is gemarkeerd door `ReflectAboutMarked`.

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python met Visual Studio Code of de opdrachtregel](#tab/tabid-python)

    Als u uw nieuwe Q#-programma wilt uitvoeren vanuit Python, slaat u de volgende code op als `host.py`:

    :::code language="python" source="~/quantum/samples/algorithms/simple-grover/host.py" range="9-14":::

    U kunt vervolgens uw Python-hostprogramma uitvoeren vanaf de opdrachtregel:

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# met Visual Studio Code of de opdrachtregel](#tab/tabid-csharp)

    Als u uw nieuwe Q#-programma wilt uitvoeren vanuit C#, wijzigt u `Driver.cs` om de volgende C#-code toe te voegen:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdrachtregel:

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# met Visual Studio 2019](#tab/tabid-vs2019)

    Als u uw nieuwe Q#-programma wilt uitvoeren vanuit C# in Visual Studio, wijzigt u `Driver.cs` om de volgende C#-code toe te voegen:

    :::code language="csharp" source="~/quantum/samples/algorithms/simple-grover/Host.cs" range="4-23":::

    Druk vervolgens op F5 om het programma uit te voeren. Er worden nu nieuwe vensters weergegeven met de volgende resultaten: 

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```
    ***

    De bewerking `ReflectAboutMarked` wordt slechts vier keer aangeroepen, maar uw Q#-programma heeft de invoer '01010' toch gevonden tussen $2^{5} = $32 mogelijke invoerwaarden.

## <a name="next-steps"></a>Volgende stappen

Als deze quickstart een succes was, kunt u de onderstaande informatiebronnen bekijken voor meer informatie over het schrijven van uw eigen kwantumtoepassingen met Q#:

- [Terug naar de handleiding Aan de slag met de Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)
- Probeer een meer algemeen [voorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) van het zoekalgoritme van Grover
- [Meer informatie over het zoekalgoritme van Grover met de Quantum Katas](xref:microsoft.quantum.overview.katas)
- Lees meer over [amplitudeversterking](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), de techniek van kwantumcomputing die de basis vormt van het zoekalgoritme van Grover
- [Concepten van kwantumcomputing](xref:microsoft.quantum.concepts.intro)
- [Voorbeelden Quantum Development Kit](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
