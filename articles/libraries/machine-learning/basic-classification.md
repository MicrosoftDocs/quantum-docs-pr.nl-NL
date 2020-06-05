---
title: Basis classificatie met de Quantum Machine Learning-bibliotheek
description: 'Meer informatie over het uitvoeren van een Quantum sequentiële classificatie die is geschreven in Q # met de Quantum Machine Learning bibliotheek van de micro soft-QDK.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: 1d2538fd164c4c61c2712978d3b5c57b0eb766e6
ms.sourcegitcommit: 8d9d392bf5e114ae223e6f689ba80d25866ff586
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "84422169"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a><span data-ttu-id="bfcd4-103">Basis classificatie: gegevens classificeren met de QDK</span><span class="sxs-lookup"><span data-stu-id="bfcd4-103">Basic classification: Classify data with the QDK</span></span>

<span data-ttu-id="bfcd4-104">In deze Quick Start leert u hoe u een Quantum sequentiële classificatie kunt uitvoeren die is geschreven in Q # met de Quantum Machine Learning bibliotheek van de QDK.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-104">In this Quickstart, you will learn how to execute a quantum sequential classifier written in Q# using the Quantum Machine Learning library of the QDK.</span></span> 

<span data-ttu-id="bfcd4-105">In deze hand leiding wordt gebruikgemaakt van de halve maan gegevensset met behulp van een classificatie structuur die is gedefinieerd in Q #.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-105">In this guide we will use the half-moon dataset, using a classifier structure defined in Q#.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bfcd4-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="bfcd4-106">Prerequisites</span></span>

- <span data-ttu-id="bfcd4-107">De Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="bfcd4-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="bfcd4-108">Een Q #-project maken voor een [python-hostprogramma](xref:microsoft.quantum.install.python) of een [C#-hostprogramma](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="bfcd4-108">Create a Q# project for either a [Python host program](xref:microsoft.quantum.install.python) or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="host-program"></a><span data-ttu-id="bfcd4-109">Host-programma</span><span class="sxs-lookup"><span data-stu-id="bfcd4-109">Host program</span></span>

<span data-ttu-id="bfcd4-110">Uw hostprogramma bestaat uit drie delen:</span><span class="sxs-lookup"><span data-stu-id="bfcd4-110">Your host program consists of three parts:</span></span>

- <span data-ttu-id="bfcd4-111">Laad de gegevensset en kies een set start-para meters voor uw model.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-111">Load the dataset and choose a set of starting parameters for your model.</span></span>
- <span data-ttu-id="bfcd4-112">Voer de training uit om de para meters en bias van het model te bepalen.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-112">Execute training to determine the parameters and bias of the model.</span></span>
- <span data-ttu-id="bfcd4-113">Valideer het model om de nauw keurigheid te bepalen</span><span class="sxs-lookup"><span data-stu-id="bfcd4-113">Validate the model to determine its accuracy</span></span>

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="bfcd4-114">Python met Visual Studio Code of de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="bfcd4-114">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

    <span data-ttu-id="bfcd4-115">Als u de ' Q #-classificatie van python wilt uitvoeren, slaat u de volgende code op als `host.py` .</span><span class="sxs-lookup"><span data-stu-id="bfcd4-115">To run your the Q# classifier from Python, save the following code as `host.py`.</span></span> <span data-ttu-id="bfcd4-116">Houd er rekening mee dat u ook het Q #-bestand nodig hebt `Training.qs` dat verderop in deze zelf studie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-116">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    <span data-ttu-id="bfcd4-117">U kunt vervolgens uw Python-hostprogramma uitvoeren vanaf de opdrachtregel:</span><span class="sxs-lookup"><span data-stu-id="bfcd4-117">You can then run your Python host program from the command line:</span></span>

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="bfcd4-118">C# met Visual Studio Code of de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="bfcd4-118">C# with Visual Studio Code or the Command Line</span></span>](#tab/tabid-csharp)

    <span data-ttu-id="bfcd4-119">Als u de ' Q #-classificatie van C# wilt uitvoeren, slaat u de volgende code op als `Host.cs` .</span><span class="sxs-lookup"><span data-stu-id="bfcd4-119">To run your the Q# classifier from C#, save the following code as `Host.cs`.</span></span> <span data-ttu-id="bfcd4-120">Houd er rekening mee dat u ook het Q #-bestand nodig hebt `Training.qs` dat verderop in deze zelf studie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-120">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="bfcd4-121">U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdrachtregel:</span><span class="sxs-lookup"><span data-stu-id="bfcd4-121">You can then run your C# host program from the command line:</span></span>

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[<span data-ttu-id="bfcd4-122">C# met Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="bfcd4-122">C# with Visual Studio 2019</span></span>](#tab/tabid-vs2019)

    <span data-ttu-id="bfcd4-123">Als u uw nieuwe Q #-programma van C# in Visual Studio wilt uitvoeren, wijzigt `Host.cs` u de volgende C#-code.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-123">To run your new Q# program from C# in Visual Studio, modify `Host.cs` to include the following C# code.</span></span> <span data-ttu-id="bfcd4-124">Houd er rekening mee dat u ook het Q #-bestand nodig hebt `Training.qs` dat verderop in deze zelf studie wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-124">Remember that you also need the Q# file `Training.qs` that is explained later in this tutorial.</span></span>

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    <span data-ttu-id="bfcd4-125">Druk vervolgens op F5 om het programma uit te voeren. Er worden nu nieuwe vensters weergegeven met de volgende resultaten:</span><span class="sxs-lookup"><span data-stu-id="bfcd4-125">Then press F5, the program will start execution and a new windows will pop-up with the following results:</span></span> 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a><span data-ttu-id="bfcd4-126">Q- \# classificeerder code</span><span class="sxs-lookup"><span data-stu-id="bfcd4-126">Q\# classifier code</span></span>

<span data-ttu-id="bfcd4-127">Nu gaan we kijken hoe de bewerkingen die worden aangeroepen door het hostprogramma worden gedefinieerd in Q #.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-127">Now let's see how the operations invoked by the host program are defined in Q#.</span></span>
<span data-ttu-id="bfcd4-128">We slaan de volgende code op in een bestand met de naam `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="bfcd4-128">We save the following code in a file named `Training.qs`.</span></span>

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

<span data-ttu-id="bfcd4-129">De belangrijkste functies en bewerkingen die zijn gedefinieerd in de bovenstaande code zijn:</span><span class="sxs-lookup"><span data-stu-id="bfcd4-129">The most important functions and operations defined in the code above are:</span></span>

- <span data-ttu-id="bfcd4-130">`ClassifierStructure() : ControlledRotation[]`: in deze functie hebben we de structuur van ons circuit model ingesteld door de lagen van de beheerde poorten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-130">`ClassifierStructure() : ControlledRotation[]` : in this function we set the structure of our circuit model by adding the layers of the controlled gates we consider.</span></span> <span data-ttu-id="bfcd4-131">Deze stap is vergelijkbaar met het declareren van lagen van neurons in een sequentief diep leer model.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-131">This step is analogous to the declaration of layers of neurons in a sequential deep learning model.</span></span>
- <span data-ttu-id="bfcd4-132">`TrainHalfMoonModel() : (Double[], Double)`: deze bewerking is het belangrijkste deel van de code en definieert de training.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-132">`TrainHalfMoonModel() : (Double[], Double)` : this operation is the core part of the code and defines the training.</span></span> <span data-ttu-id="bfcd4-133">Hier laden we de voor beelden uit de gegevensset die in de bibliotheek is opgenomen, stellen we de Hyper-para meters en de eerste para meters voor de training in en de training wordt gestart door de bewerking aan te roepen `TrainSequentialClassifier` die in de bibliotheek is opgenomen.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-133">Here we load the samples from the dataset included in the library, we set the hyper parameters and the initial parameters for the training and we start the training by calling the operation `TrainSequentialClassifier` included in the library.</span></span> <span data-ttu-id="bfcd4-134">De para meters en de bias die de classificatie bepalen, worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-134">It outputs the parameters and the bias that determine the classifier.</span></span>
- <span data-ttu-id="bfcd4-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: met deze bewerking wordt het validatie proces gedefinieerd om het model te evalueren.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-135">`ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : this operation defines the validation process to evaluate the model.</span></span> <span data-ttu-id="bfcd4-136">Hier laden we de voor beelden voor validatie, het aantal metingen per steek proef en de tolerantie.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-136">Here we load the samples for validation, the number of measurements per sample and the tolerance.</span></span> <span data-ttu-id="bfcd4-137">Hiermee wordt het aantal misclassificaties voor de gekozen batch van voor beelden voor validatie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-137">It outputs the number of misclassifications on the chosen batch of samples for validation.</span></span>

## <a name="next-steps"></a><span data-ttu-id="bfcd4-138">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="bfcd4-138">Next steps</span></span>

<span data-ttu-id="bfcd4-139">Eerst kunt u met de code spelen en een aantal para meters wijzigen om te zien hoe dit van invloed is op de training.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-139">First, you can play with the code and try to change some parameters to see how it affects the training.</span></span> <span data-ttu-id="bfcd4-140">Vervolgens kunt u in de volgende zelf studie [uw eigen classificatie ontwerpen](xref:microsoft.quantum.libraries.machine-learning.design). u leert hoe u de structuur van de classificatie definieert.</span><span class="sxs-lookup"><span data-stu-id="bfcd4-140">Then, in the next tutorial, [Design your own classifier](xref:microsoft.quantum.libraries.machine-learning.design),  you will learn how to define the structure of the classifier.</span></span>
