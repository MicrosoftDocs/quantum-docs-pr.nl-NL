---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Bewerking EstimateClassificationProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: c2b74bc55ad9005a8f52d05796e856f4f2fb62ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853943"
---
# <a name="estimateclassificationprobability-operation"></a><span data-ttu-id="95d6a-102">Bewerking EstimateClassificationProbability</span><span class="sxs-lookup"><span data-stu-id="95d6a-102">EstimateClassificationProbability operation</span></span>

<span data-ttu-id="95d6a-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="95d6a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="95d6a-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="95d6a-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="95d6a-105">Op basis van een voor beeld en een sequentiële classificatie schat de classificatie waarschijnlijkheid van het voor beeld door de uitvoer van de classificatie op basis van het opgegeven voor beeld herhaaldelijk te meten.</span><span class="sxs-lookup"><span data-stu-id="95d6a-105">Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.</span></span>

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a><span data-ttu-id="95d6a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="95d6a-106">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="95d6a-107">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="95d6a-107">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="95d6a-108">De tolerantie voor het coderen van het voor beeld in een status voorbereidings bewerking.</span><span class="sxs-lookup"><span data-stu-id="95d6a-108">The tolerance to allow in encoding the sample into a state preparation operation.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="95d6a-109">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="95d6a-109">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="95d6a-110">Het sequentiële model dat moet worden gebruikt om de classificatie waarschijnlijkheid voor het opgegeven voor beeld te schatten.</span><span class="sxs-lookup"><span data-stu-id="95d6a-110">The sequential model to be used to estimate the classification probability for the given sample.</span></span>


### <a name="sample--double"></a><span data-ttu-id="95d6a-111">voor beeld: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="95d6a-111">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="95d6a-112">De functie Vector voor het voor beeld dat moet worden geclassificeerd.</span><span class="sxs-lookup"><span data-stu-id="95d6a-112">The feature vector for the sample to be classified.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="95d6a-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="95d6a-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="95d6a-114">Het aantal metingen dat moet worden gebruikt bij het schatten van de classificatie waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="95d6a-114">The number of measurements to use in estimating the classification probability.</span></span>



## <a name="output--double"></a><span data-ttu-id="95d6a-115">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="95d6a-115">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="95d6a-116">Een schatting van de classificatie waarschijnlijkheid voor het gegeven voor beeld.</span><span class="sxs-lookup"><span data-stu-id="95d6a-116">An estimate of the classification probability for the given sample.</span></span>