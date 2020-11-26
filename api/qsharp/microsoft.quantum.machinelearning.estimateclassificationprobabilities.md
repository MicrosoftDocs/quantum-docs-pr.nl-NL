---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Bewerking EstimateClassificationProbabilities
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 1cd56f6a6483b00afb168f8d84301e73eae9af65
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211896"
---
# <a name="estimateclassificationprobabilities-operation"></a><span data-ttu-id="977d7-102">Bewerking EstimateClassificationProbabilities</span><span class="sxs-lookup"><span data-stu-id="977d7-102">EstimateClassificationProbabilities operation</span></span>

<span data-ttu-id="977d7-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="977d7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="977d7-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="977d7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="977d7-105">Op basis van een reeks voor beelden en een sequentiële classificatie schat de classificatie waarschijnlijkheid van deze voor beelden door herhaaldelijk de uitvoer van de classificatie voor elk voor beeld te meten.</span><span class="sxs-lookup"><span data-stu-id="977d7-105">Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.</span></span>

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="977d7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="977d7-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="977d7-107">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="977d7-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="977d7-108">De tolerantie voor het coderen van het voor beeld in een status voorbereidings bewerking.</span><span class="sxs-lookup"><span data-stu-id="977d7-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="977d7-109">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="977d7-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="977d7-110">Het sequentiële model dat moet worden gebruikt om de classificatie kansen voor de opgegeven steek proeven te schatten.</span><span class="sxs-lookup"><span data-stu-id="977d7-110">The sequential model to be used to estimate the classification probabilities for the given samples.</span></span>


### <a name="samples--double"></a><span data-ttu-id="977d7-111">voor beelden: [Double](xref:microsoft.quantum.lang-ref.double)[] []</span><span class="sxs-lookup"><span data-stu-id="977d7-111">samples : [Double](xref:microsoft.quantum.lang-ref.double)[][]</span></span>

<span data-ttu-id="977d7-112">Een matrix met functie vectoren voor elk voor beeld dat moet worden geclassificeerd.</span><span class="sxs-lookup"><span data-stu-id="977d7-112">An array of feature vectors for each sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="977d7-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="977d7-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="977d7-114">Het aantal metingen dat moet worden gebruikt bij het schatten van de classificatie waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="977d7-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="977d7-115">Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="977d7-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="977d7-116">Een matrix met schattingen van de classificatie waarschijnlijkheid van elk gegeven voor beeld.</span><span class="sxs-lookup"><span data-stu-id="977d7-116">An array of estimates of the classification probability for each given sample.</span></span>