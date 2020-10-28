---
title: Uw eigen classificatie ontwerpen met de QDK
description: Leer de basis concepten van het ontwerpen van circuit modellen voor de classificatie van het Quantum circuit Basic.
author: geduardo
ms.author: v-edsanc
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: 221479e616ff7a03c4ac20e0062125660314e95b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691153"
---
# <a name="design-your-own-classifier"></a><span data-ttu-id="83b5a-103">Uw eigen classificatie ontwerpen</span><span class="sxs-lookup"><span data-stu-id="83b5a-103">Design your own classifier</span></span>

<span data-ttu-id="83b5a-104">In deze hand leiding leert u de basis concepten achter het ontwerp van circuit modellen voor de gecentreerde Quantum-circuit classificatie.</span><span class="sxs-lookup"><span data-stu-id="83b5a-104">In this guide you will learn the basic concepts behind the design of circuit models for the quantum circuit centric classifier.</span></span>

<span data-ttu-id="83b5a-105">Net als bij klassiek diep leren is er geen algemene regel voor het kiezen van een specifieke architectuur.</span><span class="sxs-lookup"><span data-stu-id="83b5a-105">As in classical deep learning, there is no general rule for choosing a specific architecture.</span></span> <span data-ttu-id="83b5a-106">Afhankelijk van het probleem zullen sommige architecturen beter zijn dan andere.</span><span class="sxs-lookup"><span data-stu-id="83b5a-106">Depending on the problem some architectures will perform better than others.</span></span> <span data-ttu-id="83b5a-107">Er zijn echter enkele concepten die nuttig kunnen zijn bij het ontwerpen van het circuit:</span><span class="sxs-lookup"><span data-stu-id="83b5a-107">But, there are some concepts that might be useful when designing the circuit:</span></span>

- <span data-ttu-id="83b5a-108">Een groot aantal para meters is een flexibeler model, dat mogelijk geschikt is voor het tekenen van gecompliceerde classificatie grenzen, maar dat ook vatbaarer is voor overmontage.</span><span class="sxs-lookup"><span data-stu-id="83b5a-108">A large number of parameters implies a more flexible model, which may be suitable to draw complicated classification boundaries but which may also be more susceptible to overfitting.</span></span>

- <span data-ttu-id="83b5a-109">Entangling-poorten tussen qubits zijn essentieel voor het vastleggen van de correlaties tussen de Quantum functies.</span><span class="sxs-lookup"><span data-stu-id="83b5a-109">Entangling gates between qubits are essential to capture the correlations between the quantum features.</span></span>

## <a name="how-to-build-a-classifier-with-q"></a><span data-ttu-id="83b5a-110">Een classificatie bouwen met Q\#</span><span class="sxs-lookup"><span data-stu-id="83b5a-110">How to build a classifier with Q\#</span></span>

<span data-ttu-id="83b5a-111">Voor het bouwen van een classificatie gaan we parametrized beheerde rotaties in ons circuit model samen voegen.</span><span class="sxs-lookup"><span data-stu-id="83b5a-111">To build a classifier we are going to concatenate parametrized controlled rotations in our circuit model.</span></span> <span data-ttu-id="83b5a-112">Hiervoor kunnen we het type gebruiken dat is [`ControlledRotation`](xref:Microsoft.Quantum.MachineLearning.ControlledRotation) gedefinieerd in de Quantum machine learning-bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="83b5a-112">To do it we can use the type [`ControlledRotation`](xref:Microsoft.Quantum.MachineLearning.ControlledRotation) defined in the Quantum Machine Learning library.</span></span> <span data-ttu-id="83b5a-113">Dit type accepteert vier argumenten die bepalen: de index van de doel-Qubit, de matrix van de indexen van het besturings element qubits, de rotatieas en de index van de bijbehorende para meter in de matrix met para meters waarmee het model wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="83b5a-113">This type accepts four arguments that determine: the index of the target qubit, the array of indices of the control qubits, the axis of rotation, and index of the associated parameter in the array of parameters defining the model.</span></span>

<span data-ttu-id="83b5a-114">Laten we een voor beeld zien van een classificatie.</span><span class="sxs-lookup"><span data-stu-id="83b5a-114">Let's see an example of a classifier.</span></span> <span data-ttu-id="83b5a-115">In het voor [beeld van halve maan](https://github.com/microsoft/Quantum/tree/main/samples/machine-learning/half-moons)kunnen we de volgende classificatie vinden die in het bestand is gedefinieerd `Training.qs` .</span><span class="sxs-lookup"><span data-stu-id="83b5a-115">In the [half-moons sample](https://github.com/microsoft/Quantum/tree/main/samples/machine-learning/half-moons), we can find the following classifier defined in the file `Training.qs`.</span></span>

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

<span data-ttu-id="83b5a-116">Wat we hier definiëren, is een functie die een matrix van `ControlledRotation` elementen retourneert, samen met een matrix met para meters en een bias definieert onze [`SequentialModel`](xref:Microsoft.Quantum.MachineLearning.SequentialModel) .</span><span class="sxs-lookup"><span data-stu-id="83b5a-116">What we are defining here is a function that returns an array of `ControlledRotation` elements, that together with an array of parameters and a bias will define our [`SequentialModel`](xref:Microsoft.Quantum.MachineLearning.SequentialModel).</span></span> <span data-ttu-id="83b5a-117">Dit type is fundamenteel in de Quantum Machine Learning-bibliotheek en definieert de classificatie.</span><span class="sxs-lookup"><span data-stu-id="83b5a-117">This type is fundamental in the Quantum Machine Learning library and defines the classifier.</span></span> <span data-ttu-id="83b5a-118">Het circuit dat is gedefinieerd in de bovenstaande functie maakt deel uit van een classificatie waarin elk voor beeld van de gegevensset twee functies bevat.</span><span class="sxs-lookup"><span data-stu-id="83b5a-118">The circuit defined in the function above is part of a classifier in which each sample of the dataset contains two features.</span></span> <span data-ttu-id="83b5a-119">Daarom hebben we slechts twee qubits nodig.</span><span class="sxs-lookup"><span data-stu-id="83b5a-119">Therefore we only need two qubits.</span></span> <span data-ttu-id="83b5a-120">De grafische weer gave van het circuit is:</span><span class="sxs-lookup"><span data-stu-id="83b5a-120">The graphical representation of the circuit is:</span></span>

 ![Voor beeld van circuit model](~/media/circuit_model_1.PNG)

<span data-ttu-id="83b5a-122">Houd er rekening mee dat de bewerkingen van de Quantum Machine Learning bibliotheek de laatste Qubit van het REGI ster meten om de classificatie kansen te schatten.</span><span class="sxs-lookup"><span data-stu-id="83b5a-122">Note that by default the operations of the Quantum Machine Learning library measure the last qubit of the register to estimate the classification probabilities.</span></span> <span data-ttu-id="83b5a-123">Houd rekening met dit feit bij het ontwerpen van uw circuit.</span><span class="sxs-lookup"><span data-stu-id="83b5a-123">You should keep in mind this fact when designing your circuit.</span></span>

## <a name="use-the-library-functions-to-write-layers-of-gates"></a><span data-ttu-id="83b5a-124">De functies van de bibliotheek gebruiken om lagen van poorten te schrijven</span><span class="sxs-lookup"><span data-stu-id="83b5a-124">Use the library functions to write layers of gates</span></span>

<span data-ttu-id="83b5a-125">Stel dat er een gegevensset met 784-functies per exemplaar is, zoals installatie kopieën van 28 × 28 pixels, zoals de MNIST-gegevensset.</span><span class="sxs-lookup"><span data-stu-id="83b5a-125">Suppose we have a dataset with 784 features per instance, e.g. images of 28×28 pixels like the MNIST dataset.</span></span> <span data-ttu-id="83b5a-126">In dit geval wordt de breedte van het circuit groot genoeg zodat elke afzonderlijke Gate een mogelijke, maar niet-praktische taak wordt.</span><span class="sxs-lookup"><span data-stu-id="83b5a-126">In this case, the width of the circuit becomes large enough so that writing by hand each individual gate becomes a possible but impractical task.</span></span> <span data-ttu-id="83b5a-127">Daarom biedt de Quantum Machine Learning bibliotheek een set hulpprogram ma's waarmee automatisch lagen van parametrized-rotaties kunnen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="83b5a-127">This is why the Quantum Machine Learning library provides a set of tools to automatically generate layers of parametrized rotations.</span></span> <span data-ttu-id="83b5a-128">De functie [`LocalRotationsLayer`](xref:Microsoft.Quantum.MachineLearning.LocalRotationsLayer) retourneert bijvoorbeeld een matrix met onbeheerde rotaties met één Qubit langs een bepaalde as, met één rotatie voor elke qubit in de kassa, elk parametrized met een andere model parameter.</span><span class="sxs-lookup"><span data-stu-id="83b5a-128">For instance, the function [`LocalRotationsLayer`](xref:Microsoft.Quantum.MachineLearning.LocalRotationsLayer) returns an array of uncontrolled single-qubit rotations along a given axis, with one rotation for each qubit in the register, each parametrized by a different model parameter.</span></span> <span data-ttu-id="83b5a-129">`LocalRotationsLayer(4, X)`Retourneert bijvoorbeeld de volgende set Gates:</span><span class="sxs-lookup"><span data-stu-id="83b5a-129">For example, `LocalRotationsLayer(4, X)` returns the following set of gates:</span></span>

 ![Laag lokale draaiingen](~/media/local_rotations_layer.PNG)

<span data-ttu-id="83b5a-131">We raden u aan de [API-verwijzing van de Quantum machine learning Library](xref:Microsoft.Quantum.MachineLearning) te verkennen om alle hulpprogram ma's te ontdekken die beschikbaar zijn om het circuit ontwerp te stroom lijnen.</span><span class="sxs-lookup"><span data-stu-id="83b5a-131">We recommend you explore the [API reference of the Quantum Machine Learning library](xref:Microsoft.Quantum.MachineLearning) to discover all the tools available to streamline the circuit design.</span></span>

## <a name="next-steps"></a><span data-ttu-id="83b5a-132">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="83b5a-132">Next steps</span></span>

 <span data-ttu-id="83b5a-133">Probeer verschillende structuren in de voor beelden van de voor beelden.</span><span class="sxs-lookup"><span data-stu-id="83b5a-133">Try different structures in the examples provided by the samples.</span></span> <span data-ttu-id="83b5a-134">Ziet u eventuele wijzigingen in de prestaties van het model?</span><span class="sxs-lookup"><span data-stu-id="83b5a-134">Do you see any changes in the performance of the model?</span></span> <span data-ttu-id="83b5a-135">In de volgende zelf studie [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load) leert u hoe u gegevens sets kunt laden om nieuwe architecturen van classificaties te verkennen.</span><span class="sxs-lookup"><span data-stu-id="83b5a-135">In the next tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load), you will learn how to load datasets to try and explore new architectures of classifiers.</span></span>
