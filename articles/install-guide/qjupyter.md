---
title: 'Ontwikkelen met Q # Jupyter-notebooks'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 3302a9bd0652b2dea86b844058bf8303ee7a4a7f
ms.sourcegitcommit: c85c1b439807ac576d3a11aadca307d57b059673
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "83551036"
---
# <a name="develop-with-q-jupyter-notebooks"></a><span data-ttu-id="2f739-102">Ontwikkelen met Q # Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="2f739-102">Develop with Q# Jupyter notebooks</span></span>

<span data-ttu-id="2f739-103">Installeer de QDK voor het ontwikkelen van Q #-bewerkingen op Q # Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="2f739-103">Install the QDK for developing Q# operations on Q# Jupyter Notebooks.</span></span>

<span data-ttu-id="2f739-104">Met Jupyter-notebooks kunt u uitvoering in-place code uitvoeren naast instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="2f739-104">Jupyter Notebooks allow in-place code execution alongside instructions, notes, and other content.</span></span> <span data-ttu-id="2f739-105">Deze omgeving is ideaal voor het schrijven van Q #-code met Inge sloten zelf studies voor uitleg of Quantum Computing.</span><span class="sxs-lookup"><span data-stu-id="2f739-105">This environment is ideal for writing Q# code with embedded explanations or quantum computing interactive tutorials.</span></span> <span data-ttu-id="2f739-106">Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.</span><span class="sxs-lookup"><span data-stu-id="2f739-106">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="2f739-107">IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="2f739-107">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>

> [!NOTE]
> * <span data-ttu-id="2f739-108">In Q # Jupyter-notebooks kunt u alleen Q # code uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe host-Program ma's (zoals python of C#-bestanden).</span><span class="sxs-lookup"><span data-stu-id="2f739-108">In Q# Jupyter Notebooks you can only run Q# code, and the operations cannot be called from external host programs (e.g. Python or C# files).</span></span> <span data-ttu-id="2f739-109">Deze omgeving is niet geschikt als u een extern klassiek host-programma wilt combi neren met het Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="2f739-109">This environment is not appropriate if your goal is to combine an external classical host program with the quantum program.</span></span>

1. <span data-ttu-id="2f739-110">Vereisten</span><span class="sxs-lookup"><span data-stu-id="2f739-110">Pre-requisites</span></span>

    - <span data-ttu-id="2f739-111">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="2f739-111">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="2f739-112">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="2f739-112">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="2f739-113">.NET Core SDK 3,1</span><span class="sxs-lookup"><span data-stu-id="2f739-113">.NET Core SDK 3.1</span></span>](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. <span data-ttu-id="2f739-114">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="2f739-114">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="2f739-115">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="2f739-115">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="2f739-116">Voer de volgende opdracht uit om de Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="2f739-116">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="2f739-117">Als u het Jupyter-notebook wilt openen en de URL wilt plakken die u hebt ontvangen van de opdracht regel in uw browser.</span><span class="sxs-lookup"><span data-stu-id="2f739-117">To open the Jupyter notebook copy and paste the URL provided by the command line into your browser.</span></span>

    - <span data-ttu-id="2f739-118">Maak een Jupyter Notebook met een Q#-kernel en voeg de volgende code toe aan de eerste Notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="2f739-118">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="2f739-119">Voer deze cel van het Notebook uit:</span><span class="sxs-lookup"><span data-stu-id="2f739-119">Run this cell of the notebook:</span></span>

        ![Cel met Q#-code in een Jupyter-notebook](~/media/install-guide-jupyter.png)

        <span data-ttu-id="2f739-121">U ziet `SayHello` in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="2f739-121">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="2f739-122">Wanneer u werkt met Jupyter Notebook, wordt de Q#-code gecompileerd en wordt de naam van de gevonden bewerking(en) geretourneerd in de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="2f739-122">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="2f739-123">Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de `%simulate` opdracht:</span><span class="sxs-lookup"><span data-stu-id="2f739-123">In a new cell, execute the operation you just created (in a simulator) by using the `%simulate` command:</span></span>

        ![Cel met %simulate magic in een Jupyter-notebook](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="2f739-125">Het bericht wordt afgedrukt op het scherm samen met het resultaat van de bewerking die u hebt aangeroepen (hier zien we de lege tuple omdat de `()` bewerking alleen een `Unit` type retourneert).</span><span class="sxs-lookup"><span data-stu-id="2f739-125">You should see the message printed on the screen along with the result of the operation you invoked (here, we see the empty tuple `()` because our operation simply returns a `Unit` type).</span></span>

## <a name="next-steps"></a><span data-ttu-id="2f739-126">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="2f739-126">Next steps</span></span>

<span data-ttu-id="2f739-127">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="2f739-127">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
