---
title: Ontwikkelen met Q#-Jupyter-notebooks
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 9117794d6cf6f05fa34e05c21fad8977d0e76505
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577817"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="8efda-102">Ontwikkelen met Q#-Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="8efda-102">Develop with Q# Jupyter Notebooks</span></span>

<span data-ttu-id="8efda-103">Installeer de QDK voor het ontwikkelen van Q #-bewerkingen op Q # Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="8efda-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="8efda-104">Met Jupyter-notebooks kunt u uitvoering in-place code uitvoeren naast instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="8efda-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="8efda-105">Deze omgeving is ideaal voor het schrijven van Q #-code met Inge sloten zelf studies voor uitleg of Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="8efda-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="8efda-106">Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.</span><span class="sxs-lookup"><span data-stu-id="8efda-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="8efda-107">IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="8efda-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="8efda-108">In Q # Jupyter-notebooks kunt u alleen Q # code uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe host-Program ma's (zoals python of C#-bestanden).</span><span class="sxs-lookup"><span data-stu-id="8efda-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="8efda-109">Deze omgeving is niet geschikt als u een extern klassiek host-programma wilt combi neren met het Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="8efda-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="8efda-110">Vereisten</span><span class="sxs-lookup"><span data-stu-id="8efda-110">Pre-requisites</span></span>

    - <span data-ttu-id="8efda-111">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="8efda-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="8efda-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="8efda-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="8efda-113">.NET Core SDK 3,1</span><span class="sxs-lookup"><span data-stu-id="8efda-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="8efda-114">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="8efda-114">Install the `iqsharp` package</span></span>

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="8efda-115">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="8efda-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="8efda-116">Voer de volgende opdracht uit om de Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="8efda-116">Run the following command to start the notebook server:</span></span>

        ```
        jupyter notebook
        ```

    - <span data-ttu-id="8efda-117">Als u de Jupyter Notebook wilt openen, kopieert en plakt u de URL die u hebt ontvangen van de opdracht regel in uw browser.</span><span class="sxs-lookup"><span data-stu-id="8efda-117">To open the Jupyter Notebook, copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="8efda-118">Maak een Jupyter Notebook met een Q #-kernel en voeg de volgende code toe aan de eerste notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="8efda-118">Create a Jupyter Notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="8efda-119">Voer deze cel van het Notebook uit:</span><span class="sxs-lookup"><span data-stu-id="8efda-119">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook cel met Q # code](~/media/install-guide-jupyter.png)

        <span data-ttu-id="8efda-121">U ziet `SayHello` in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="8efda-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="8efda-122">Wanneer in Jupyter Notebook wordt uitgevoerd, wordt de Q #-code gecompileerd en de notitie blok voert de naam van de bewaarde bewerking (en) uit.</span><span class="sxs-lookup"><span data-stu-id="8efda-122">When running in Jupyter Notebook, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="8efda-123">Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de `%simulate` opdracht:</span><span class="sxs-lookup"><span data-stu-id="8efda-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Jupyter Notebook cel met% simulatie Magic](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="8efda-125">Het bericht wordt afgedrukt op het scherm samen met het resultaat van de bewerking die u hebt aangeroepen (hier zien we de lege tuple omdat de `()` bewerking alleen een `Unit` type retourneert).</span><span class="sxs-lookup"><span data-stu-id="8efda-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="8efda-126">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="8efda-126">Next steps</span></span>

<span data-ttu-id="8efda-127">Nu u de QDK voor Q # Jupyter-notebooks hebt geïnstalleerd, kunt u [uw eerste Quantum programma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren door uw Q #-code rechtstreeks in de Jupyter notebook omgeving te schrijven.</span><span class="sxs-lookup"><span data-stu-id="8efda-127">Now that you have installed the QDK for Q# Jupyter Notebooks, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng) by writing your Q# code directly within the Jupyter Notebook environment.</span></span>

<span data-ttu-id="8efda-128">Voor meer voor beelden van wat u kunt doen met Q # Jupyter-notebooks, gaat u naar:</span><span class="sxs-lookup"><span data-stu-id="8efda-128">For more examples of what you can do with Q# Jupyter Notebooks, please take a look at:</span></span>
- <span data-ttu-id="8efda-129">[Inleiding tot Q # en Jupyter notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span><span class="sxs-lookup"><span data-stu-id="8efda-129">[Intro to Q# and Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/).</span></span> <span data-ttu-id="8efda-130">Er wordt een Q #-Jupyter Notebook weer gegeven waarin wordt uitgelegd hoe u Q # in deze omgeving kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8efda-130">There you will find a Q# Jupyter Notebook that shows how to use Q# in this environment.</span></span>
- <span data-ttu-id="8efda-131">[Quantum Katas](xref:microsoft.quantum.overview.katas), een open-source verzameling zelf studies en reeksen programmeer oefeningen in de vorm van Q # Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="8efda-131">[Quantum Katas](xref:microsoft.quantum.overview.katas), an open-source collection of self-paced tutorials and sets of programming exercises in the form of Q# Jupyter Notebooks.</span></span> <span data-ttu-id="8efda-132">De [Quantum Katas zelf studie notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) zijn een goed uitgangs punt.</span><span class="sxs-lookup"><span data-stu-id="8efda-132">The [Quantum Katas tutorial notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) are a good starting point.</span></span> <span data-ttu-id="8efda-133">De Quantum Katas is gericht op het aanwijzen van de elementen van Quantum Computing en Q #-programmering tegelijk.</span><span class="sxs-lookup"><span data-stu-id="8efda-133">The Quantum Katas are aimed at teaching you elements of quantum computing and Q# programming at the same time.</span></span> <span data-ttu-id="8efda-134">Ze zijn een uitstekend voor beeld van wat voor soort inhoud u kunt maken met Q # Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="8efda-134">They're an excellent example of what kind of content you can create with Q# Jupyter Notebooks.</span></span>
