---
title: Ontwikkelen met Q#-Jupyter-notebooks
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b80d95a160b5f46c1132d3428ba32ad6dcd5656e
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630335"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="064f0-102">Ontwikkelen met Q#-Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="064f0-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="064f0-103">Installeer de QDK voor het ontwikkelen van Q #-bewerkingen op Q # Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="064f0-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="064f0-104">Met Jupyter-notebooks kunt u uitvoering in-place code uitvoeren naast instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="064f0-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="064f0-105">Deze omgeving is ideaal voor het schrijven van Q #-code met Inge sloten zelf studies voor uitleg of Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="064f0-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="064f0-106">Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.</span><span class="sxs-lookup"><span data-stu-id="064f0-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="064f0-107">IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="064f0-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="064f0-108">In Q # Jupyter-notebooks kunt u alleen Q # code uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe host-Program ma's (zoals python of C#-bestanden).</span><span class="sxs-lookup"><span data-stu-id="064f0-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="064f0-109">Deze omgeving is niet geschikt als u een extern klassiek host-programma wilt combi neren met het Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="064f0-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="064f0-110">Vereisten</span><span class="sxs-lookup"><span data-stu-id="064f0-110">Prerequisites</span></span>

    - <span data-ttu-id="064f0-111">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="064f0-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="064f0-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="064f0-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="064f0-113">.NET Core SDK 3,1</span><span class="sxs-lookup"><span data-stu-id="064f0-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="064f0-114">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="064f0-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > <span data-ttu-id="064f0-115">Als er tijdens de stap een fout optreedt `dotnet iqsharp install` , opent u een nieuw terminal venster en probeert u het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="064f0-115">If you get an error during the `dotnet iqsharp install` step, open a new terminal window and try again.</span></span>
    > <span data-ttu-id="064f0-116">Als dit nog steeds niet werkt, probeert u het geïnstalleerde `dotnet-iqsharp` hulp programma (in Windows) te vinden en uit te `dotnet-iqsharp.exe` voeren:</span><span class="sxs-lookup"><span data-stu-id="064f0-116">If this still doesn't work, try locating the installed `dotnet-iqsharp` tool (on Windows, `dotnet-iqsharp.exe`) and running:</span></span>
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > <span data-ttu-id="064f0-117">waar `/path/to/dotnet-iqsharp` moet worden vervangen door het absolute pad naar het `dotnet-iqsharp` hulp programma in het bestands systeem.</span><span class="sxs-lookup"><span data-stu-id="064f0-117">where `/path/to/dotnet-iqsharp` should be replaced by the absolute path to the `dotnet-iqsharp` tool in your file system.</span></span>
    > <span data-ttu-id="064f0-118">Normaal gesp roken wordt dit onder `.dotnet/tools` in uw gebruikersprofielmap.</span><span class="sxs-lookup"><span data-stu-id="064f0-118">Typically this will be under `.dotnet/tools` in your user profile folder.</span></span>

1. <span data-ttu-id="064f0-119">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="064f0-119">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="064f0-120">Voer de volgende opdracht uit om de Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="064f0-120">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="064f0-121">Als u de Jupyter Notebook wilt openen, kopieert en plakt u de URL die u hebt ontvangen van de opdracht regel in uw browser.</span><span class="sxs-lookup"><span data-stu-id="064f0-121">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="064f0-122">Maak een Jupyter Notebook met een Q #-kernel en voeg de volgende code toe aan de eerste notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="064f0-122">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="064f0-123">Voer deze cel van het Notebook uit:</span><span class="sxs-lookup"><span data-stu-id="064f0-123">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook cel met Q # code](~/media/install-guide-jupyter.png)

        <span data-ttu-id="064f0-125">U ziet `SayHello` in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="064f0-125">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="064f0-126">Wanneer in Jupyter Notebook wordt uitgevoerd, wordt de Q #-code gecompileerd en de notitie blok voert de naam van de bewaarde bewerking (en) uit.</span><span class="sxs-lookup"><span data-stu-id="064f0-126">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="064f0-127">Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de `%simulate` opdracht:</span><span class="sxs-lookup"><span data-stu-id="064f0-127">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook cel met% simulatie Magic](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="064f0-129">Het bericht wordt afgedrukt op het scherm samen met het resultaat van de bewerking die u hebt aangeroepen (hier zien we de lege tuple omdat de `()` bewerking alleen een `Unit` type retourneert).</span><span class="sxs-lookup"><span data-stu-id="064f0-129">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="064f0-130">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="064f0-130">Next steps</span></span>

<span data-ttu-id="064f0-131">Nu u de QDK voor Q # Jupyter-notebooks hebt geïnstalleerd, kunt u [uw eerste Quantum programma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren door uw Q #-code rechtstreeks in de Jupyter notebook omgeving te schrijven.</span><span class="sxs-lookup"><span data-stu-id="064f0-131">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="064f0-132">Voor meer voor beelden van wat u kunt doen met Q # Jupyter-notebooks, gaat u naar:</span><span class="sxs-lookup"><span data-stu-id="064f0-132">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="064f0-133">[Inleiding tot Q # en Jupyter notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="064f0-133">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="064f0-134">Er wordt een Q #-Jupyter Notebook weer gegeven waarin wordt uitgelegd hoe u Q # in deze omgeving kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="064f0-134">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="064f0-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), een open-source verzameling zelf studies en reeksen programmeer oefeningen in de vorm van Q # Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="064f0-135">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="064f0-136">De [Quantum Katas zelf studie notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) zijn een goed uitgangs punt.</span><span class="sxs-lookup"><span data-stu-id="064f0-136">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="064f0-137">De Quantum Katas is gericht op het aanwijzen van de elementen van Quantum Computing en Q #-programmering tegelijk.</span><span class="sxs-lookup"><span data-stu-id="064f0-137">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="064f0-138">Ze zijn een uitstekend voor beeld van wat voor soort inhoud u kunt maken met Q # Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="064f0-138">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
