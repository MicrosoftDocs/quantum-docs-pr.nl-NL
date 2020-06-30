---
title: Ontwikkelen met Q#-Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274052"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="3bc96-102">Ontwikkelen met Q#-Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="3bc96-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="3bc96-103">Installeer de QDK voor het ontwikkelen van Q#-bewerkingen op Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="3bc96-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="3bc96-104">Met Jupyter Notebooks kunt u in-place codes uitvoeren naast instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="3bc96-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="3bc96-105">Deze omgeving is ideaal voor het schrijven van Q#-codes met ingesloten uitleg of interactieve zelfstudies over kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="3bc96-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="3bc96-106">Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.</span><span class="sxs-lookup"><span data-stu-id="3bc96-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="3bc96-107">IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="3bc96-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="3bc96-108">In Q#-Jupyter Notebooks kunt u alleen Q#-codes uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe hostprogramma's (zoals Python of C#-bestanden).</span><span class="sxs-lookup"><span data-stu-id="3bc96-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="3bc96-109">Deze omgeving is niet geschikt als u een extern, klassiek hostprogramma wilt combineren met het kwantumprogramma.</span><span class="sxs-lookup"><span data-stu-id="3bc96-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="3bc96-110">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3bc96-110">Prerequisites</span></span>

    - <span data-ttu-id="3bc96-111">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="3bc96-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="3bc96-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="3bc96-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="3bc96-113">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="3bc96-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="3bc96-114">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="3bc96-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="3bc96-115">Als er tijdens de `dotnet iqsharp install`-stap een fout optreedt, moet u een nieuw terminalvenster openen en het nogmaals proberen.</span><span class="sxs-lookup"><span data-stu-id="3bc96-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="3bc96-116">Als het daarna nog steeds niet werkt, zoekt u het geïnstalleerde `dotnet-iqsharp`-hulpprogramma (in Windows, `dotnet-iqsharp.exe`) en voert u dit uit:</span><span class="sxs-lookup"><span data-stu-id="3bc96-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="3bc96-117">waarbij `/path/to/dotnet-iqsharp` moet worden vervangen door het absolute pad naar het `dotnet-iqsharp`-hulpprogramma in uw bestandssysteem.</span><span class="sxs-lookup"><span data-stu-id="3bc96-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="3bc96-118">Dit is meestal bij `.dotnet/tools` in de map van uw gebruikersprofiel.</span><span class="sxs-lookup"><span data-stu-id="3bc96-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="3bc96-119">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="3bc96-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="3bc96-120">Voer de volgende opdracht uit om de Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="3bc96-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="3bc96-121">Als u de Jupyter Notebook wilt openen, kopieert en plakt u de URL die u van de opdrachtregel hebt ontvangen in uw browser.</span><span class="sxs-lookup"><span data-stu-id="3bc96-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="3bc96-122">Maak een Jupyter Notebook met een Q#-kernel en voeg de volgende code toe aan de eerste notebookcel:</span><span class="sxs-lookup"><span data-stu-id="3bc96-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="3bc96-123">Voer deze cel van het Notebook uit:</span><span class="sxs-lookup"><span data-stu-id="3bc96-123">Run this cell of the notebook:</span></span>

        ![Cel met Q#-code in een Jupyter Notebook](~/media/install-guide-jupyter.png)

        <span data-ttu-id="3bc96-125">U ziet `SayHello` in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="3bc96-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="3bc96-126">Als u de Q#-code uitvoert in een Jupyter Notebook, wordt de Q#-code gecompileerd en wordt de naam van de gevonden bewerking(en) door het notebook uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="3bc96-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="3bc96-127">Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de opdracht `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="3bc96-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Cel met %simulate magic in een Jupyter Notebook](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="3bc96-129">Het bericht wordt nu op het scherm weergegeven, samen met het resultaat van de bewerking die u hebt aangeroepen (in dit geval een lege tuple `()`, omdat onze bewerking een `Unit`-type oplevert).</span><span class="sxs-lookup"><span data-stu-id="3bc96-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="3bc96-130">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="3bc96-130">Next steps</span></span>

<span data-ttu-id="3bc96-131">Nu u de QDK voor Q#-Jupyter Notebooks hebt geïnstalleerd, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren door uw Q#-code rechtstreeks in de Jupyter Notebook-omgeving te schrijven.</span><span class="sxs-lookup"><span data-stu-id="3bc96-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="3bc96-132">Ga voor meer voorbeelden van wat u kunt doen met Q#-Jupyter Notebooks naar:</span><span class="sxs-lookup"><span data-stu-id="3bc96-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="3bc96-133">[Inleiding tot Q# en Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="3bc96-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="3bc96-134">Daar vindt u een Q#-Jupyter Notebook waarin wordt getoond hoe u Q# in deze omgeving kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3bc96-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="3bc96-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), een open-source verzameling van zelfstudies die u in uw eigen tempo kunt uitvoeren, evenals programmeeroefeningen in de vorm van Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="3bc96-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="3bc96-136">De [Quantum Katas-notebooks voor zelfstudie](https://github.com/microsoft/QuantumKatas#tutorial-topics) zijn een goed beginpunt.</span><span class="sxs-lookup"><span data-stu-id="3bc96-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="3bc96-137">In de Quantum Katas leert u meer over de verschillende elementen van kwantumcomputing en Q#-programmering.</span><span class="sxs-lookup"><span data-stu-id="3bc96-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="3bc96-138">Ze zijn een uitstekend voorbeeld van wat voor soort inhoud u kunt maken met Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="3bc96-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
