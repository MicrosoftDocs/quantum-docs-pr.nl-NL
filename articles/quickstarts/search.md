---
title: Algoritme van Grover uitvoeren in Q# - Quantum Development Kit
description: U gaat een Q#-project maken waarin het algoritme van Grover wordt gedemonstreerd, een van de bekendste kwantumalgoritmen.
author: cgranade
ms.author: chgranad@microsoft.com
ms.date: 10/19/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.search
ms.openlocfilehash: 75028a1dc29abe5fbea2e789d896563f3d6331c9
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443933"
---
# <a name="quickstart-implement-grovers-search-algorithm-in-q"></a><span data-ttu-id="a462a-103">Quickstart: Zoekalgoritme van Grover implementeren in Q#</span><span class="sxs-lookup"><span data-stu-id="a462a-103">Quickstart: Implement Grover's search algorithm in Q#</span></span>

<span data-ttu-id="a462a-104">In deze quickstart leert u hoe u het zoekalgoritme van Grover kunt bouwen en uitvoeren om het doorzoeken van ongestructureerde gegevens te versnellen.</span><span class="sxs-lookup"><span data-stu-id="a462a-104">In this Quickstart, you can learn how to build and run Grover search to speed up the search of unstructured data.</span></span>  <span data-ttu-id="a462a-105">Het zoekalgoritme van Grover is een van de populairste algoritmen voor kwantumcomputing en deze relatief kleine Q#-implementatie geeft u een beeld van enkele van de voordelen van het programmeren van kwantumoplossingen met de high-level Q#-programmeertaal voor het voorstellen van kwantumalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="a462a-105">Grover's search is one of the most popular quantum computing algorithms, and this relatively small Q# implementation gives you a sense of some of the advantages of programming quantum solutions with a high-level Q# quantum programming language to express quantum algorithms.</span></span>  <span data-ttu-id="a462a-106">Aan het einde van de quickstart ziet u dat in een lijst met ongeordende vermeldingen een bepaalde tekenreeks wordt gevonden in een fractie van de tijd die nodig zou zijn om de hele lijst op een klassieke computer te doorzoeken.</span><span class="sxs-lookup"><span data-stu-id="a462a-106">At the end of the guide, you will see the simulation output demonstrates successfully finding a specific string among a list of onordered entries in a fraction of the time it would take to search the whole list on a classical computer.</span></span>

<span data-ttu-id="a462a-107">Het algoritme van Grover doorzoekt een lijst met ongestructureerde gegevens op specifieke items.</span><span class="sxs-lookup"><span data-stu-id="a462a-107">Grover's algorithm searches a list of unstructured data for specific items.</span></span> <span data-ttu-id="a462a-108">Het algoritme kan bijvoorbeeld deze vraag beantwoorden: Is deze kaart uit een spel kaarten een hartenaas?</span><span class="sxs-lookup"><span data-stu-id="a462a-108">For example, it can answer the question: Is this card drawn from a pack of cards an ace of hearts?</span></span> <span data-ttu-id="a462a-109">De labeling van het specifieke item wordt _marked input_ genoemd.</span><span class="sxs-lookup"><span data-stu-id="a462a-109">The labeling of the specific item is called _marked input_.</span></span>

<span data-ttu-id="a462a-110">Als een kwantumcomputer het zoekalgoritme van Grover gebruikt, heeft deze zoekopdracht gegarandeerd minder stappen nodig dan het aantal items in de lijst die u doorzoekt, iets wat geen enkel klassiek algoritme kan.</span><span class="sxs-lookup"><span data-stu-id="a462a-110">Using Grover's search algorithm, a quantum computer is guaranteed to run this search in fewer steps than the number of items in the list that you're searching — something no classical algorithm can do.</span></span> <span data-ttu-id="a462a-111">Deze hogere snelheid is verwaarloosbaar in het geval van een spel kaarten, maar in lijsten met miljoenen of miljarden items, is de tijdswinst aanzienlijk.</span><span class="sxs-lookup"><span data-stu-id="a462a-111">The increased speed in the case of a pack of cards is negligible; however, in lists containing millions or billions of items, it becomes significant.</span></span>

<span data-ttu-id="a462a-112">U kunt met slechts een paar regels code het zoekalgoritme van Grover bouwen.</span><span class="sxs-lookup"><span data-stu-id="a462a-112">You can build Grover's search algorithm with just a few lines of code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a462a-113">Vereisten</span><span class="sxs-lookup"><span data-stu-id="a462a-113">Prerequisites</span></span>

- <span data-ttu-id="a462a-114">De Microsoft [Quantum Development Kit][install].</span><span class="sxs-lookup"><span data-stu-id="a462a-114">The Microsoft [Quantum Development Kit][install].</span></span>

## <a name="what-does-grovers-search-algorithm-do"></a><span data-ttu-id="a462a-115">Wat doet het zoekalgoritme van Grover?</span><span class="sxs-lookup"><span data-stu-id="a462a-115">What does Grover's search algorithm do?</span></span>

<span data-ttu-id="a462a-116">Het algoritme van Grover vraagt of een item in een lijst het item is dat we zoeken.</span><span class="sxs-lookup"><span data-stu-id="a462a-116">Grover's algorithm asks whether an item in a list is the one we are searching for.</span></span> <span data-ttu-id="a462a-117">Hiervoor wordt een kwantumsuperpositie samengesteld van de indexen van de lijst met elke coëfficiënt, of waarschijnlijkheidsamplitude, waarmee de waarschijnlijkheid wordt aangegeven dat die specifieke index de index is die u zoekt.</span><span class="sxs-lookup"><span data-stu-id="a462a-117">It does this by constructing a quantum superposition of the indexes of the list with each coefficient, or probability amplitude, representing the probability of that specific index being the one you are looking for.</span></span>

<span data-ttu-id="a462a-118">De kern van het algoritme bestaat uit twee stappen die de coëfficiënt van de gezochte index incrementeel ophogen, totdat de waarschijnlijkheidsamplitude van die coëfficiënt één benadert.</span><span class="sxs-lookup"><span data-stu-id="a462a-118">At the heart of the algorithm are two steps that incrementally boost the coefficient of the index that we are looking for, until the probability amplitude of that coefficient approaches one.</span></span>

<span data-ttu-id="a462a-119">Het aantal incrementele ophogingen is minder dan het aantal items in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a462a-119">The number of incremental boosts is fewer than the number of items in the list.</span></span> <span data-ttu-id="a462a-120">Dit is de reden waarom het zoekalgoritme van Grover minder stappen nodig heeft voor de zoekopdracht dan een klassiek algoritme.</span><span class="sxs-lookup"><span data-stu-id="a462a-120">This is why Grover's search algorithm performs the search in fewer steps than any classical algorithm.</span></span>

![Functioneel diagram van het zoekalgoritme van Grover](~/media/grover.png)

## <a name="write-the-code"></a><span data-ttu-id="a462a-122">De code schrijven</span><span class="sxs-lookup"><span data-stu-id="a462a-122">Write the code</span></span>

1. <span data-ttu-id="a462a-123">Gebruik de Quantum Development Kit om [een nieuw Q#-project](xref:microsoft.quantum.howto.createproject) met de naam `Grover` te maken in de ontwikkelomgeving van uw keuze.</span><span class="sxs-lookup"><span data-stu-id="a462a-123">Using the Quantum Development Kit, [create a new Q# project](xref:microsoft.quantum.howto.createproject) called `Grover`, in your development environment of choice.</span></span>

1. <span data-ttu-id="a462a-124">Voeg de volgende code toe aan het bestand `Operations.qs` in uw nieuwe project:</span><span class="sxs-lookup"><span data-stu-id="a462a-124">Add the following code to the `Operations.qs` file in your new project:</span></span>

    [!code-qsharp[](~/quantum/samples/algorithms/simple-grover/SimpleGrover.qs?highlight=5,27)]

1. <span data-ttu-id="a462a-125">Als u de lijst wilt definiëren om te doorzoeken, maakt u een nieuw bestand `Reflections.qs` en plakt u daar de volgende code in:</span><span class="sxs-lookup"><span data-stu-id="a462a-125">To define the list that we're searching, create a new file `Reflections.qs`, and paste in the following code:</span></span>

    [!code-qsharp[](~/quantum/samples/algorithms/simple-grover/Reflections.qs)]

    <span data-ttu-id="a462a-126">Met de bewerking `ReflectAboutMarked` wordt de marked input gedefinieerd die u zoekt: de reeks van afwisselend nullen en enen.</span><span class="sxs-lookup"><span data-stu-id="a462a-126">The `ReflectAboutMarked` operation defines the marked input that you are searching for: the string of alternating zeros and ones.</span></span> <span data-ttu-id="a462a-127">In dit voorbeeld wordt de marked input in code vastgelegd en kan deze worden uitgebreid om te zoeken naar andere invoer of worden gegeneraliseerd voor willekeurige invoer.</span><span class="sxs-lookup"><span data-stu-id="a462a-127">This sample hard-codes the marked input, and can be extended to search for different inputs or generalized for any input.</span></span>

1. <span data-ttu-id="a462a-128">Vervolgens voert u het nieuwe Q#-programma uit om het item te vinden dat is gemarkeerd door `ReflectAboutMarked`.</span><span class="sxs-lookup"><span data-stu-id="a462a-128">Next, run your new Q# program to find the item marked by `ReflectAboutMarked`.</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-linetabtabid-python"></a>[<span data-ttu-id="a462a-129">Python met Visual Studio Code of de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="a462a-129">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="a462a-130">Als u uw nieuwe Q#-programma wilt uitvoeren vanuit Python, slaat u de volgende code op als `host.py`:</span><span class="sxs-lookup"><span data-stu-id="a462a-130">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

    [!code-python[](~/quantum/samples/algorithms/simple-grover/host.py)]

    <span data-ttu-id="a462a-131">U kunt vervolgens uw Python-hostprogramma uitvoeren vanaf de opdrachtregel:</span><span class="sxs-lookup"><span data-stu-id="a462a-131">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    [0, 1, 0, 1, 0]
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-linetabtabid-csharp"></a>[<span data-ttu-id="a462a-132">C# met Visual Studio Code of de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="a462a-132">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="a462a-133">Als u uw nieuwe Q#-programma wilt uitvoeren vanuit C#, wijzigt u `Driver.cs` om de volgende C#-code toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="a462a-133">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

    [!code-csharp[](~/quantum/samples/algorithms/simple-grover/Host.cs)]

    <span data-ttu-id="a462a-134">U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdrachtregel:</span><span class="sxs-lookup"><span data-stu-id="a462a-134">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Reflecting about marked state...
    Result: [Zero,One,Zero,One,Zero]

    Press any key to continue...
    ```

    ### <a name="c-with-visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="a462a-135">C# met Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="a462a-135">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="a462a-136">Als u uw nieuwe Q#-programma wilt uitvoeren vanuit C# in Visual Studio, wijzigt u `Driver.cs` om de volgende C#-code toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="a462a-136">To run your new Q# program from C# in Visual Studio, modify `Driver.cs` to include the following C# code:</span></span>

    [!code-csharp[](~/quantum/samples/algorithms/simple-grover/Host.cs)]

    <span data-ttu-id="a462a-137">Druk vervolgens op F5 om het programma uit te voeren. Er worden nu nieuwe vensters weergegeven met de volgende resultaten:</span><span class="sxs-lookup"><span data-stu-id="a462a-137">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

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

    <span data-ttu-id="a462a-138">De bewerking `ReflectAboutMarked` wordt slechts vier keer aangeroepen, maar uw Q#-programma heeft de invoer '01010' toch gevonden tussen $2^{5} = $32 mogelijke invoerwaarden.</span><span class="sxs-lookup"><span data-stu-id="a462a-138">The `ReflectAboutMarked` operation is called only four times, but your Q# program was able to find the "01010" input amongst $2^{5} = 32$ possible inputs!</span></span>

## <a name="next-steps"></a><span data-ttu-id="a462a-139">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="a462a-139">Next steps</span></span>

<span data-ttu-id="a462a-140">Als deze quickstart een succes was, kunt u de onderstaande informatiebronnen bekijken voor meer informatie over het schrijven van uw eigen kwantumtoepassingen met Q#:</span><span class="sxs-lookup"><span data-stu-id="a462a-140">If you enjoyed this quickstart, check out some of the resources below to learn more about how you can use Q# to write your own quantum applications:</span></span>

- [<span data-ttu-id="a462a-141">Terug naar de handleiding Aan de slag met de Microsoft Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="a462a-141">Back to the Getting Started with QDK guide</span></span>](xref:microsoft.quantum.welcome)
- <span data-ttu-id="a462a-142">Probeer een meer algemeen [voorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search) van het zoekalgoritme van Grover</span><span class="sxs-lookup"><span data-stu-id="a462a-142">Try a more general Grover's search algorithm [sample](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/database-search)</span></span>
- [<span data-ttu-id="a462a-143">Meer informatie over het zoekalgoritme van Grover met de Quantum Katas</span><span class="sxs-lookup"><span data-stu-id="a462a-143">Learn more about Grover's search with the Quantum Katas</span></span>](xref:microsoft.quantum.overview.katas)
- <span data-ttu-id="a462a-144">Lees meer over [amplitudeversterking](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), de techniek van kwantumcomputing die de basis vormt van het zoekalgoritme van Grover</span><span class="sxs-lookup"><span data-stu-id="a462a-144">Read more about [Amplitude amplification](xref:microsoft.quantum.libraries.standard.algorithms#amplitude-amplification), the quantum computing technique behind Grover's search algorithm</span></span>
- [<span data-ttu-id="a462a-145">Concepten van kwantumcomputing</span><span class="sxs-lookup"><span data-stu-id="a462a-145">Quantum computing concepts</span></span>](xref:microsoft.quantum.concepts.intro)
- [<span data-ttu-id="a462a-146">Voorbeelden Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="a462a-146">Quantum Development Kit Samples</span></span>](https://docs.microsoft.com/samples/browse/?products=qdk)

<!-- LINKS -->

[install]: xref:microsoft.quantum.install
