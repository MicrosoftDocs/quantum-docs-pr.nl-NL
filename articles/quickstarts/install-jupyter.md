---
title: Ontwikkelen met Q#-Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 8a878e8f930f4b898f4de35751e4a39cc8716cec
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2020
ms.locfileid: "85884233"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="edd4a-102">Ontwikkelen met Q#-Jupyter Notebooks</span><span class="sxs-lookup"><span data-stu-id="edd4a-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="edd4a-103">Installeer de QDK voor het ontwikkelen van Q#-bewerkingen op Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="edd4a-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="edd4a-104">Met Jupyter Notebooks kunt u in-place codes uitvoeren naast instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="edd4a-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="edd4a-105">Deze omgeving is ideaal voor het schrijven van Q#-codes met ingesloten uitleg of interactieve zelfstudies over kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="edd4a-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="edd4a-106">Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.</span><span class="sxs-lookup"><span data-stu-id="edd4a-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

> [!NOTE]
> * <span data-ttu-id="edd4a-107">In Q#-Jupyter Notebooks kunt u alleen Q#-codes uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe hostprogramma's (zoals Python of C#-bestanden).</span><span class="sxs-lookup"><span data-stu-id="edd4a-107">In Q# Jupyter Notebooks, you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="edd4a-108">Deze omgeving is niet geschikt als u een extern, klassiek hostprogramma wilt combineren met het kwantumprogramma.</span><span class="sxs-lookup"><span data-stu-id="edd4a-108">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

## <a name="install-the-iq-jupyter-kernel"></a><span data-ttu-id="edd4a-109">De IQ # Jupyter-kernel installeren</span><span class="sxs-lookup"><span data-stu-id="edd4a-109">Install the IQ# Jupyter kernel</span></span>

<span data-ttu-id="edd4a-110">IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="edd4a-110">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="edd4a-111">Installeren met behulp van Conda (aanbevolen)</span><span class="sxs-lookup"><span data-stu-id="edd4a-111">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="edd4a-112">Installeer [Miniconda](https://docs.conda.io/en/latest/miniconda.html) of [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="edd4a-112">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span>

1. <span data-ttu-id="edd4a-113">Open een Anaconda-prompt.</span><span class="sxs-lookup"><span data-stu-id="edd4a-113">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="edd4a-114">Of, als u liever PowerShell of pwsh gebruikt: open een shell, voer `conda init powershell` uit, sluit de shell en open deze vervolgens opnieuw.</span><span class="sxs-lookup"><span data-stu-id="edd4a-114">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="edd4a-115">Maak en activeer een nieuwe Conda-omgeving met de naam `qsharp-env` met de vereiste pakketten (inclusief Jupyter Notebook en IQ#) door de volgende opdrachten uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="edd4a-115">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="edd4a-116">Voer `python -c "import qsharp"` uit via dezelfde terminal om de installatie te controleren, en vul de lokale pakketcache met alle vereiste QDK-onderdelen.</span><span class="sxs-lookup"><span data-stu-id="edd4a-116">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-advanced"></a>[<span data-ttu-id="edd4a-117">Installeren met behulp van .NET CLI (geavanceerd)</span><span class="sxs-lookup"><span data-stu-id="edd4a-117">Install using .NET CLI (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="edd4a-118">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="edd4a-118">Prerequisites:</span></span>

    - <span data-ttu-id="edd4a-119">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="edd4a-119">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="edd4a-120">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="edd4a-120">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="edd4a-121">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="edd4a-121">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="edd4a-122">Installeer het `Microsoft.Quantum.IQSharp`-pakket.</span><span class="sxs-lookup"><span data-stu-id="edd4a-122">Install the `Microsoft.Quantum.IQSharp` package.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="edd4a-123">Als er tijdens de `dotnet iqsharp install`-stap een fout optreedt, moet u een nieuw terminalvenster openen en het nogmaals proberen.</span><span class="sxs-lookup"><span data-stu-id="edd4a-123">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="edd4a-124">Als het daarna nog steeds niet werkt, zoekt u het geïnstalleerde `dotnet-iqsharp`-hulpprogramma (in Windows, `dotnet-iqsharp.exe`) en voert u dit uit:</span><span class="sxs-lookup"><span data-stu-id="edd4a-124">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="edd4a-125">waarbij `/path/to/dotnet-iqsharp` moet worden vervangen door het absolute pad naar het `dotnet-iqsharp`-hulpprogramma in uw bestandssysteem.</span><span class="sxs-lookup"><span data-stu-id="edd4a-125">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="edd4a-126">Dit is meestal bij `.dotnet/tools` in de map van uw gebruikersprofiel.</span><span class="sxs-lookup"><span data-stu-id="edd4a-126">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="edd4a-127">Dat is alles.</span><span class="sxs-lookup"><span data-stu-id="edd4a-127">That's it!</span></span> <span data-ttu-id="edd4a-128">U beschikt nu over de IQ#-kernel voor Jupyter, die de kernfunctionaliteit biedt voor het compileren en uitvoeren van Q#-bewerkingen vanuit Q# Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="edd4a-128">You now have the IQ# kernel for Jupyter, which provides the core functionality for compiling and executing Q# operations from Q# Jupyter Notebooks.</span></span>

## <a name="create-your-first-q-notebook"></a><span data-ttu-id="edd4a-129">Uw eerste Q#-notebook maken</span><span class="sxs-lookup"><span data-stu-id="edd4a-129">Create your first Q# notebook</span></span>

<span data-ttu-id="edd4a-130">Nu bent u klaar om de installatie van uw Q# Jupyter Notebook te controleren door een eenvoudige Q#-bewerking te schrijven en uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="edd4a-130">Now you are ready to verify your Q# Jupyter Notebook installation by writing and executing a simple Q# operation.</span></span>

1. <span data-ttu-id="edd4a-131">Voer vanuit de omgeving die u hebt gemaakt tijdens de installatie (dat is de Conda-omgeving die u hebt gemaakt, of de Python-omgeving waarin u Jupyter hebt geïnstalleerd), het volgende programma uit om de Jupyter Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="edd4a-131">From the environment you created during installation (i.e., either the conda environment you created, or the Python environment where you installed Jupyter), run the following command to start the Jupyter Notebook server:</span></span>

    ```
    jupyter notebook
    ```

    - <span data-ttu-id="edd4a-132">Als Jupyter Notebook niet automatisch wordt geopend in de browser, kopieert en plakt u de URL die u van de opdrachtregel hebt ontvangen, in de browser.</span><span class="sxs-lookup"><span data-stu-id="edd4a-132">If the Jupyter Notebook doesn't open automatically in your browser, copy and paste the URL provided by the command line into your browser.</span></span>

1. <span data-ttu-id="edd4a-133">Kies Nieuw → Q# om een Jupyter Notebook met een Q#-kernel te maken, en voeg de volgende code toe aan de eerste notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="edd4a-133">Choose "New" → "Q#" to create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. <span data-ttu-id="edd4a-134">Voer deze cel van het Notebook uit:</span><span class="sxs-lookup"><span data-stu-id="edd4a-134">Run this cell of the notebook:</span></span>

    ![Cel met Q#-code in een Jupyter Notebook](~/media/install-guide-jupyter.png)

    <span data-ttu-id="edd4a-136">U ziet `SampleQuantumRandomNumberGenerator` in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="edd4a-136">You should see `SampleQuantumRandomNumberGenerator` in the output of the cell.</span></span> <span data-ttu-id="edd4a-137">Als u de Q#-code uitvoert in een Jupyter Notebook, wordt de Q#-code gecompileerd en zijn de namen van alle gevonden bewerkingen te zien in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="edd4a-137">When running in Jupyter Notebook, the Q# code is compiled, and the cell outputs the name of any operations that it finds.</span></span>

1. <span data-ttu-id="edd4a-138">Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de opdracht `%simulate`:</span><span class="sxs-lookup"><span data-stu-id="edd4a-138">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

    ![Cel met %simulate magic in een Jupyter Notebook](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="edd4a-140">U ziet nu het resultaat van de bewerking die u hebt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="edd4a-140">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="edd4a-141">In dit geval ziet u `Zero` of `One` op het scherm, omdat met de bewerking een willekeurig resultaat is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="edd4a-141">In this case, because your operation generates a random result, you will see either `Zero` or `One` printed on the screen.</span></span> <span data-ttu-id="edd4a-142">Als u de cel herhaaldelijk uitvoert, ziet u elk resultaat ongeveer de helft van de tijd.</span><span class="sxs-lookup"><span data-stu-id="edd4a-142">If you execute the cell repeatedly, you should see each result approximately half the time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="edd4a-143">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="edd4a-143">Next steps</span></span>

<span data-ttu-id="edd4a-144">Nu u de QDK voor Q#-Jupyter Notebooks hebt geïnstalleerd, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren door Q#-code rechtstreeks in de Jupyter Notebook-omgeving te schrijven.</span><span class="sxs-lookup"><span data-stu-id="edd4a-144">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="edd4a-145">Ga voor meer voorbeelden van wat u kunt doen met Q#-Jupyter Notebooks naar:</span><span class="sxs-lookup"><span data-stu-id="edd4a-145">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>

- <span data-ttu-id="edd4a-146">[Inleiding tot Q# en Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="edd4a-146">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="edd4a-147">Hier vindt u een Q#-Jupyter Notebook dat meer details biedt over hoe u Q# kunt gebruiken in de Jupyter-omgeving.</span><span class="sxs-lookup"><span data-stu-id="edd4a-147">There you will find a Q# Jupyter Notebook that provides more details on how to use Q# in the Jupyter environment.</span></span>
- <span data-ttu-id="edd4a-148">[Quantum Katas](xref:microsoft.quantum.overview.katas), een open-source verzameling van zelfstudies die u in uw eigen tempo kunt uitvoeren, evenals programmeeroefeningen in de vorm van Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="edd4a-148">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="edd4a-149">De [Quantum Katas-notebooks voor zelfstudie](https://github.com/microsoft/QuantumKatas#tutorial-topics) zijn een goed beginpunt.</span><span class="sxs-lookup"><span data-stu-id="edd4a-149">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="edd4a-150">In de Quantum Katas leert u meer over de verschillende elementen van kwantumcomputing en Q#-programmering.</span><span class="sxs-lookup"><span data-stu-id="edd4a-150">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="edd4a-151">Ze zijn een uitstekend voorbeeld van wat voor soort inhoud u kunt maken met Q#-Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="edd4a-151">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
