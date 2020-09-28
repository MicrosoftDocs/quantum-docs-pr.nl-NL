---
title: Ontwikkelen met Q# en Python
description: Meer informatie over hoe u een Q#-toepassing maakt met Python.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: f6a2a7d1888cfe458fa3989a27d71fcdeed0f01f
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834156"
---
# <a name="develop-with-no-locq-and-python"></a><span data-ttu-id="80f0e-103">Ontwikkelen met Q# en Python</span><span class="sxs-lookup"><span data-stu-id="80f0e-103">Develop with Q# and Python</span></span>

<span data-ttu-id="80f0e-104">Installeer de QDK om Python-hostprogramma's te ontwikkelen waarmee Q#-bewerkingen kunnen worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="80f0e-104">Install the QDK to develop Python host programs to call Q# operations.</span></span>

## <a name="install-the-qsharp-python-package"></a><span data-ttu-id="80f0e-105">Het Python-pakket voor `qsharp` installeren</span><span class="sxs-lookup"><span data-stu-id="80f0e-105">Install the `qsharp` Python package</span></span>

### <a name="install-using-conda-recommended"></a>[<span data-ttu-id="80f0e-106">Installeren met behulp van Conda (aanbevolen)</span><span class="sxs-lookup"><span data-stu-id="80f0e-106">Install using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="80f0e-107">Installeer [Miniconda](https://docs.conda.io/en/latest/miniconda.html) of [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span><span class="sxs-lookup"><span data-stu-id="80f0e-107">Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/individual#Downloads).</span></span> <span data-ttu-id="80f0e-108">**Opmerking:** 64-bits installatie vereist.</span><span class="sxs-lookup"><span data-stu-id="80f0e-108">**Note:** 64-bit installation required.</span></span>

1. <span data-ttu-id="80f0e-109">Open een Anaconda-prompt.</span><span class="sxs-lookup"><span data-stu-id="80f0e-109">Open an Anaconda Prompt.</span></span>

   - <span data-ttu-id="80f0e-110">Of, als u liever PowerShell of pwsh gebruikt: open een shell, voer `conda init powershell` uit, sluit de shell en open deze vervolgens opnieuw.</span><span class="sxs-lookup"><span data-stu-id="80f0e-110">Or, if you prefer to use PowerShell or pwsh: open a shell, run `conda init powershell`, then close and re-open the shell.</span></span>

1. <span data-ttu-id="80f0e-111">Maak en activeer een nieuwe Conda-omgeving met de naam `qsharp-env` met de vereiste pakketten (inclusief Jupyter Notebook en IQ#) door de volgende opdrachten uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="80f0e-111">Create and activate a new conda environment named `qsharp-env` with the required packages (including Jupyter Notebook and IQ#) by running the following commands:</span></span>

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. <span data-ttu-id="80f0e-112">Voer `python -c "import qsharp"` uit via dezelfde terminal om de installatie te controleren, en vul de lokale pakketcache met alle vereiste QDK-onderdelen.</span><span class="sxs-lookup"><span data-stu-id="80f0e-112">Run `python -c "import qsharp"` from the same terminal to verify your installation and populate your local package cache with all required QDK components.</span></span>

### <a name="install-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="80f0e-113">Installeren met behulp van .NET CLI en PIP (geavanceerd)</span><span class="sxs-lookup"><span data-stu-id="80f0e-113">Install using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="80f0e-114">Vereisten:</span><span class="sxs-lookup"><span data-stu-id="80f0e-114">Prerequisites:</span></span>

    - <span data-ttu-id="80f0e-115">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="80f0e-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="80f0e-116">Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="80f0e-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="80f0e-117">.NET Core SDK 3.1</span><span class="sxs-lookup"><span data-stu-id="80f0e-117">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. <span data-ttu-id="80f0e-118">Installeer het `qsharp`-pakket, een Python-pakket dat interoperabiliteit mogelijk maakt tussen Q# en Python.</span><span class="sxs-lookup"><span data-stu-id="80f0e-118">Install the `qsharp` package, a Python package that enables interop between Q# and Python.</span></span>

    ```
    pip install qsharp
    ```

1. <span data-ttu-id="80f0e-119">Installeer IQ#, een kernel die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en uitvoeren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="80f0e-119">Install IQ#, a kernel used by Jupyter and Python that provides the core functionality for compiling and running Q# operations.</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="80f0e-120">Als er tijdens de `dotnet iqsharp install`-stap een fout optreedt, moet u een nieuw terminalvenster openen en het nogmaals proberen.</span><span class="sxs-lookup"><span data-stu-id="80f0e-120">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="80f0e-121">Als het daarna nog steeds niet werkt, zoekt u het geïnstalleerde `dotnet-iqsharp`-hulpprogramma (in Windows, `dotnet-iqsharp.exe`) en voert u dit uit:</span><span class="sxs-lookup"><span data-stu-id="80f0e-121">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="80f0e-122">waarbij `/path/to/dotnet-iqsharp` moet worden vervangen door het absolute pad naar het `dotnet-iqsharp`-hulpprogramma in uw bestandssysteem.</span><span class="sxs-lookup"><span data-stu-id="80f0e-122">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="80f0e-123">Dit is meestal bij `.dotnet/tools` in de map van uw gebruikersprofiel.</span><span class="sxs-lookup"><span data-stu-id="80f0e-123">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>
    
***

<span data-ttu-id="80f0e-124">Dat is alles.</span><span class="sxs-lookup"><span data-stu-id="80f0e-124">That's it!</span></span> <span data-ttu-id="80f0e-125">U beschikt nu over het Python-pakket met `qsharp` en de IQ#-kernel voor Jupyter, die de kernfunctionaliteit biedt voor het compileren en uitvoeren van Q#-bewerkingen vanuit Python, en u in staat stelt Q# Jupyter Notebooks te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="80f0e-125">You now have both the `qsharp` Python package and the IQ# kernel for Jupyter, which provide the core functionality for compiling and running Q# operations from Python and allows you to use Q# Jupyter Notebooks.</span></span>

## <a name="choose-your-ide"></a><span data-ttu-id="80f0e-126">Uw IDE kiezen</span><span class="sxs-lookup"><span data-stu-id="80f0e-126">Choose your IDE</span></span>

<span data-ttu-id="80f0e-127">Hoewel u Q# met Python in elke IDE kunt gebruiken, raden we u ten zeerste aan om de IDE van Visual Studio Code (VS Code) voor uw Q# + Python-toepassingen te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="80f0e-127">While you can use Q# with Python in any IDE, we highly recommend using Visual Studio Code (VS Code) IDE for your Q# + Python applications.</span></span> <span data-ttu-id="80f0e-128">Met de QDK Visual Studio Code-extensie krijgt u toegang tot uitgebreidere functies, zoals waarschuwingen, markeren van syntaxis, projectsjablonen, en meer.</span><span class="sxs-lookup"><span data-stu-id="80f0e-128">With the QDK Visual Studio Code extension you gain access to richer functionality such as warnings, syntax highlighting, project templates, and more.</span></span>

<span data-ttu-id="80f0e-129">Ga als volgt te werk als u VS Code wilt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="80f0e-129">If you would like to use VS Code:</span></span>

- <span data-ttu-id="80f0e-130">Installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).</span><span class="sxs-lookup"><span data-stu-id="80f0e-130">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
- <span data-ttu-id="80f0e-131">Installeer de [QDK-extensie voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="80f0e-131">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="80f0e-132">Als u een andere editor wilt gebruiken, helpen bovenstaande instructies u om aan de slag te gaan.</span><span class="sxs-lookup"><span data-stu-id="80f0e-132">If you would like to use a different editor, the instructions above have you all set.</span></span>

## <a name="write-your-first-no-locq-program"></a><span data-ttu-id="80f0e-133">Uw eerste Q#-programma schrijven</span><span class="sxs-lookup"><span data-stu-id="80f0e-133">Write your first Q# program</span></span>

<span data-ttu-id="80f0e-134">Nu bent u klaar om de installatie van het Python-pakket voor `qsharp` te controleren door een eenvoudig Q#-programma te schrijven en uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="80f0e-134">Now you are ready to verify your `qsharp` Python package installation by writing and running a simple Q# program.</span></span>

1. <span data-ttu-id="80f0e-135">Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en de volgende code toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="80f0e-135">Create a minimal Q# operation by creating a file called `Operation.qs` and adding the following code to it:</span></span>

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. <span data-ttu-id="80f0e-136">Maak in dezelfde map als `Operation.qs` een Python-programma met de naam `host.py`, om de Q# `SampleQuantumRandomNumberGenerator()`-bewerking te simuleren:</span><span class="sxs-lookup"><span data-stu-id="80f0e-136">In the same folder as `Operation.qs`, create a Python program called `host.py` to simulate the Q# `SampleQuantumRandomNumberGenerator()` operation:</span></span>

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. <span data-ttu-id="80f0e-137">Voer vanuit de omgeving die u hebt gemaakt tijdens de installatie (dat is de Conda- of Python-omgeving waarin u `qsharp` hebt geïnstalleerd), het volgende programma uit:</span><span class="sxs-lookup"><span data-stu-id="80f0e-137">From the environment you created during installation (i.e., the conda or Python environment where you installed `qsharp`), run the program:</span></span>

    ```
    python host.py
    ```

1. <span data-ttu-id="80f0e-138">U ziet nu het resultaat van de bewerking die u hebt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="80f0e-138">You should see the result of the operation you invoked.</span></span> <span data-ttu-id="80f0e-139">In dit geval ziet u `0` of `1` op het scherm, omdat met de bewerking een willekeurig resultaat is gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="80f0e-139">In this case, because your operation generates a random result, you will see either `0` or `1` printed on the screen.</span></span> <span data-ttu-id="80f0e-140">Als u het programma herhaaldelijk uitvoert, ziet u elk resultaat ongeveer de helft van de tijd.</span><span class="sxs-lookup"><span data-stu-id="80f0e-140">If you run the program repeatedly, you should see each result approximately half the time.</span></span>

> [!NOTE]
> * <span data-ttu-id="80f0e-141">De Python-code is een regulier Python-programma.</span><span class="sxs-lookup"><span data-stu-id="80f0e-141">The Python code is just a normal Python program.</span></span> <span data-ttu-id="80f0e-142">U kunt een willekeurige Python-omgeving gebruiken, inclusief Jupyter Notebooks op basis van Python, om het Python-programma te schrijven en Q#-bewerkingen aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="80f0e-142">You can use any Python environment, including Python-based Jupyter Notebooks, to write the Python program and call Q# operations.</span></span> <span data-ttu-id="80f0e-143">Met het Python-programma kunnen Q#-bewerkingen worden geïmporteerd uit elk .qs-bestand dat zich in dezelfde map bevindt als de Python-code.</span><span class="sxs-lookup"><span data-stu-id="80f0e-143">The Python program can import Q# operations from any .qs files located in the same folder as the Python code itself.</span></span>

## <a name="next-steps"></a><span data-ttu-id="80f0e-144">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="80f0e-144">Next steps</span></span>

<span data-ttu-id="80f0e-145">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u deze zelfstudie volgen en [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="80f0e-145">Now that you have tested the Quantum Development Kit in your preferred environment, you can follow this tutorial to write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
