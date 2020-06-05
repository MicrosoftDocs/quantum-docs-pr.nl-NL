---
title: Algoritme van Grover uitvoeren in Q# - Quantum Development Kit
description: U gaat een Q#-project maken waarin het algoritme van Grover wordt gedemonstreerd, een van de bekendste kwantumalgoritmen.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 9e4c53b4d5159cf07f0654603c1d477ad09eb7c6
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327404"
---
# <a name="tutorial-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="cae98-103">Zelfstudie: Zoekalgoritme van Grover implementeren in Q\#</span><span class="sxs-lookup"><span data-stu-id="cae98-103">Tutorial: Implement Grover's search algorithm in Q\#</span></span>

<span data-ttu-id="cae98-104">In deze zelfstudie leert u hoe u het zoekalgoritme van Grover kunt bouwen en uitvoeren om het doorzoeken van niet-gestructureerde gegevens te versnellen.</span><span class="sxs-lookup"><span data-stu-id="cae98-104">In this tutorial, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="cae98-105">Het zoekalgoritme van Grover is een van de populairste algoritmen voor kwantumcomputing en deze relatief kleine Q#-implementatie geeft u een beeld van enkele van de voordelen van het programmeren van kwantumoplossingen met de high-level Q#-programmeertaal voor het voorstellen van kwantumalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="cae98-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="cae98-106">Aan het einde van de quickstart ziet u dat in een lijst met ongeordende vermeldingen een bepaalde tekenreeks wordt gevonden in een fractie van de tijd die nodig zou zijn om de hele lijst op een klassieke computer te doorzoeken.</span><span class="sxs-lookup"><span data-stu-id="cae98-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of unordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="cae98-107">Het algoritme van Grover doorzoekt een lijst met ongestructureerde gegevens op specifieke items.</span><span class="sxs-lookup"><span data-stu-id="cae98-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="cae98-108">Het algoritme kan bijvoorbeeld deze vraag beantwoorden: Is deze kaart uit een spel kaarten een hartenaas?</span><span class="sxs-lookup"><span data-stu-id="cae98-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="cae98-109">De labeling van het specifieke item wordt _marked input_ genoemd.</span><span class="sxs-lookup"><span data-stu-id="cae98-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="cae98-110">Als een kwantumcomputer het zoekalgoritme van Grover gebruikt, heeft deze zoekopdracht gegarandeerd minder stappen nodig dan het aantal items in de lijst die u doorzoekt, iets wat geen enkel klassiek algoritme kan.</span><span class="sxs-lookup"><span data-stu-id="cae98-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="cae98-111">Deze hogere snelheid is verwaarloosbaar in het geval van een spel kaarten, maar in lijsten met miljoenen of miljarden items, is de tijdswinst aanzienlijk.</span><span class="sxs-lookup"><span data-stu-id="cae98-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="cae98-112">U kunt met slechts een paar regels code het zoekalgoritme van Grover bouwen.</span><span class="sxs-lookup"><span data-stu-id="cae98-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cae98-113">Vereisten</span><span class="sxs-lookup"><span data-stu-id="cae98-113">Prerequisites</span></span>

- <span data-ttu-id="cae98-114">De Microsoft [Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="cae98-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="cae98-115">Wat doet het zoekalgoritme van Grover?</span><span class="sxs-lookup"><span data-stu-id="cae98-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="cae98-116">Het algoritme van Grover vraagt of een item in een lijst het item is dat we zoeken.</span><span class="sxs-lookup"><span data-stu-id="cae98-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="cae98-117">Hiervoor wordt een kwantumsuperpositie samengesteld van de indexen van de lijst met elke coëfficiënt, of waarschijnlijkheidsamplitude, waarmee de waarschijnlijkheid wordt aangegeven dat die specifieke index de index is die u zoekt.</span><span class="sxs-lookup"><span data-stu-id="cae98-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="cae98-118">De kern van het algoritme bestaat uit twee stappen die de coëfficiënt van de gezochte index incrementeel ophogen, totdat de waarschijnlijkheidsamplitude van die coëfficiënt één benadert.</span><span class="sxs-lookup"><span data-stu-id="cae98-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="cae98-119">Het aantal incrementele ophogingen is minder dan het aantal items in de lijst.</span><span class="sxs-lookup"><span data-stu-id="cae98-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="cae98-120">Dit is de reden waarom het zoekalgoritme van Grover minder stappen nodig heeft voor de zoekopdracht dan een klassiek algoritme.</span><span class="sxs-lookup"><span data-stu-id="cae98-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Functioneel diagram van het zoekalgoritme van Grover](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="cae98-122">De code schrijven</span><span class="sxs-lookup"><span data-stu-id="cae98-122">Write the code</span></span>

1. <span data-ttu-id="cae98-123">Maak met de Quantum Development Kit [een nieuw Q#-project voor de opdrachtregeltoepassing](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="cae98-123">Using the Quantum Development Kit, [create a new Q# project for the command line application](xref:microsoft.quantum.install.standalone).</span></span> <span data-ttu-id="cae98-124">Titel van het project `Grover`.</span><span class="sxs-lookup"><span data-stu-id="cae98-124">Title the project `Grover`.</span></span>

1. <span data-ttu-id="cae98-125">Voeg de volgende code toe aan het bestand `Program.qs` in uw nieuwe project:</span><span class="sxs-lookup"><span data-stu-id="cae98-125">Add the following code to the `Program.qs` file in your new project:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs" range="4-41":::

1. <span data-ttu-id="cae98-126">Als u de lijst wilt definiëren om te doorzoeken, maakt u een nieuw bestand `Reflections.qs` en plakt u daar de volgende code in:</span><span class="sxs-lookup"><span data-stu-id="cae98-126">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    :::code language="qsharp" source="~/quantum/samples/algorithms/simple-grover/Reflections.qs" range="4-70":::

    <span data-ttu-id="cae98-127">Met de bewerking `ReflectAboutMarked` wordt de marked input gedefinieerd die u zoekt: de reeks van afwisselend nullen en enen.</span><span class="sxs-lookup"><span data-stu-id="cae98-127">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="cae98-128">In dit voorbeeld wordt de marked input in code vastgelegd en kan deze worden uitgebreid om te zoeken naar andere invoer of worden gegeneraliseerd voor willekeurige invoer.</span><span class="sxs-lookup"><span data-stu-id="cae98-128">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="cae98-129">Vervolgens voert u het nieuwe Q#-programma uit om het item te vinden dat is gemarkeerd door `ReflectAboutMarked`.</span><span class="sxs-lookup"><span data-stu-id="cae98-129">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a><span data-ttu-id="cae98-130">Q#-opdrachtregeltoepassingen met Visual Studio of Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="cae98-130">Q# command line applications with Visual Studio or Visual Studio Code</span></span>

<span data-ttu-id="cae98-131">Het uitvoerbare bestand voert de bewerking of functie met het kenmerk `@EntryPoint()` uit in een simulator of resourceschatter, afhankelijk van de projectconfiguratie en opdrachtregelopties.</span><span class="sxs-lookup"><span data-stu-id="cae98-131">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

<span data-ttu-id="cae98-132">Druk in Visual Studio op Ctrl + F5 om het script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="cae98-132">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="cae98-133">Bouw in VS Code `Program.qs` voor de eerste keer door het onderstaande in de terminal in te voeren:</span><span class="sxs-lookup"><span data-stu-id="cae98-133">In VS Code, build the `Program.qs` the first time by typing the below in the terminal:</span></span>

```Command line
dotnet build
```

<span data-ttu-id="cae98-134">Voor nieuwe uitvoeringen is het niet nodig om de build opnieuw te doen.</span><span class="sxs-lookup"><span data-stu-id="cae98-134">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="cae98-135">Typ de volgende opdracht en druk op enter om hem uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="cae98-135">To run it, type the following command and press enter:</span></span>

```Command line
dotnet run --no-build
```

<span data-ttu-id="cae98-136">U ziet het volgende bericht in de terminal:</span><span class="sxs-lookup"><span data-stu-id="cae98-136">You should see the following message displayed in the terminal:</span></span>

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

<span data-ttu-id="cae98-137">Dit komt omdat u niet het aantal qubits hebt opgegeven dat u wilt gebruiken. Daarom zegt de terminal welke opdrachten beschikbaar zijn voor het uitvoerbare bestand.</span><span class="sxs-lookup"><span data-stu-id="cae98-137">This is because you didn't specify the number of qubits you wanted to use, so the terminal tells you the commands available for the executable.</span></span> <span data-ttu-id="cae98-138">Als u 5 qubits wilt gebruiken, typt u:</span><span class="sxs-lookup"><span data-stu-id="cae98-138">If we want to use 5 qubits we should type:</span></span>

```Command line
dotnet run --n-qubits 5
```

<span data-ttu-id="cae98-139">Als u op enter drukt, ziet u de volgende uitvoer:</span><span class="sxs-lookup"><span data-stu-id="cae98-139">Pressing enter you should see the following output:</span></span>

```
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
Reflecting about marked state...
[Zero,One,Zero,One,Zero]
```

## <a name="next-steps"></a><span data-ttu-id="cae98-140">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="cae98-140">Next steps</span></span>

<span data-ttu-id="cae98-141">Als deze zelfstudie een succes was, kunt u de onderstaande informatiebronnen bekijken voor meer informatie over het schrijven van uw eigen kwantumtoepassingen met Q#:</span><span class="sxs-lookup"><span data-stu-id="cae98-141">If you enjoyed this tutorial, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="cae98-142">Terug naar de handleiding Aan de slag met de Microsoft Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="cae98-142">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="cae98-143">Probeer een meer algemeen [voorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) van het zoekalgoritme van Grover</span><span class="sxs-lookup"><span data-stu-id="cae98-143">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="cae98-144">Meer informatie over het zoekalgoritme van Grover met de Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="cae98-144">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="cae98-145">Lees meer over [amplitudeversterking][amplitude-amplification], de techniek van kwantumcomputing die de basis vormt van het zoekalgoritme van Grover</span><span class="sxs-lookup"><span data-stu-id="cae98-145">Read more about [Amplitude amplification][amplitude-amplification], the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="cae98-146">Concepten van kwantumcomputing</span><span class="sxs-lookup"><span data-stu-id="cae98-146">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="cae98-147">Voorbeelden Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="cae98-147">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
[amplitude-amplification]: xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification
