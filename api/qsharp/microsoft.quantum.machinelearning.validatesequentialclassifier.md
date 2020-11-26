---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Bewerking ValidateSequentialClassifier
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 5174085edbfd846e8f6649f33e325fd1979ae6a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196103"
---
# <a name="validatesequentialclassifier-operation"></a><span data-ttu-id="94ae5-102">Bewerking ValidateSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="94ae5-102">ValidateSequentialClassifier operation</span></span>

<span data-ttu-id="94ae5-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="94ae5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="94ae5-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="94ae5-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="94ae5-105">Hiermee wordt een bepaalde sequentiële classificatie gevalideerd op basis van een bepaalde set vooraf gelabelde voor beelden.</span><span class="sxs-lookup"><span data-stu-id="94ae5-105">Validates a given sequential classifier against a given set of pre-labeled samples.</span></span>

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a><span data-ttu-id="94ae5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="94ae5-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="94ae5-107">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="94ae5-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="94ae5-108">Het sequentiële model dat moet worden gevalideerd.</span><span class="sxs-lookup"><span data-stu-id="94ae5-108">The sequential model to be validated.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="94ae5-109">voor beelden: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="94ae5-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="94ae5-110">De voor beelden die moeten worden gebruikt om het opgegeven model te valideren.</span><span class="sxs-lookup"><span data-stu-id="94ae5-110">The samples to be used to validate the given model.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="94ae5-111">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="94ae5-111">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="94ae5-112">De benaderings tolerantie die moet worden gebruikt voor het coderen van elk voor beeld als invoer voor de sequentiële classificatie.</span><span class="sxs-lookup"><span data-stu-id="94ae5-112">The approximation tolerance to use in encoding each sample as an input to the sequential classifier.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="94ae5-113">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="94ae5-113">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="94ae5-114">Het aantal metingen dat moet worden gebruikt bij het classificeren van elk voor beeld.</span><span class="sxs-lookup"><span data-stu-id="94ae5-114">The number of measurements to use in classifying each sample.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="94ae5-115">validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="94ae5-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="94ae5-116">Het schema waarmee steek proeven worden getekend vanuit de validatieset.</span><span class="sxs-lookup"><span data-stu-id="94ae5-116">The schedule by which samples should be drawn from the validation set.</span></span>



## <a name="output--validationresults"></a><span data-ttu-id="94ae5-117">Uitvoer: [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span><span class="sxs-lookup"><span data-stu-id="94ae5-117">Output : [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)</span></span>

<span data-ttu-id="94ae5-118">De resultaten van de opgegeven validatie.</span><span class="sxs-lookup"><span data-stu-id="94ae5-118">The results of the given validation.</span></span>