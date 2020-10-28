---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingEpoch
title: _RunSingleTrainingEpoch bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingEpoch
qsharp.summary: Perform one epoch of sequential classifier training on a subset of data samples.
ms.openlocfilehash: 2b4f629eac0bd8e60bd4d86077521c60085d4809
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706949"
---
# <a name="_runsingletrainingepoch-operation"></a><span data-ttu-id="39a34-102">_RunSingleTrainingEpoch bewerking</span><span class="sxs-lookup"><span data-stu-id="39a34-102">_RunSingleTrainingEpoch operation</span></span>

<span data-ttu-id="39a34-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="39a34-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="39a34-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="39a34-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="39a34-105">Voer één epoche uit van opeenvolgende classificatie trainingen op een subset van gegevens voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="39a34-105">Perform one epoch of sequential classifier training on a subset of data samples.</span></span>

```qsharp
operation _RunSingleTrainingEpoch (encodedSamples : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, periodScore : Int, options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel, nPreviousBestMisses : Int) : (Int, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a><span data-ttu-id="39a34-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="39a34-106">Input</span></span>

### <a name="encodedsamples--labeledsamplestategenerator"></a><span data-ttu-id="39a34-107">encodedSamples: ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []</span><span class="sxs-lookup"><span data-stu-id="39a34-107">encodedSamples : ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator))[]</span></span>




### <a name="schedule--samplingschedule"></a><span data-ttu-id="39a34-108">planning: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="39a34-108">schedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>




### <a name="periodscore--int"></a><span data-ttu-id="39a34-109">periodScore: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39a34-109">periodScore : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39a34-110">Het aantal verloop stappen dat moet worden genomen tussen score punten.</span><span class="sxs-lookup"><span data-stu-id="39a34-110">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="39a34-111">Stel de beste nauw keurigheid in op 1.</span><span class="sxs-lookup"><span data-stu-id="39a34-111">For best accuracy, set to 1.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="39a34-112">opties: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="39a34-112">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="39a34-113">Opties die moeten worden gebruikt in de training.</span><span class="sxs-lookup"><span data-stu-id="39a34-113">Options to be used in training.</span></span>


### <a name="model--sequentialmodel"></a><span data-ttu-id="39a34-114">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="39a34-114">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="39a34-115">Het sequentiële model dat moet worden getraind.</span><span class="sxs-lookup"><span data-stu-id="39a34-115">The sequential model to be trained.</span></span>


### <a name="npreviousbestmisses--int"></a><span data-ttu-id="39a34-116">nPreviousBestMisses: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39a34-116">nPreviousBestMisses : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39a34-117">Het beste aantal misclassificaties dat in eerdere epochen wordt waargenomen.</span><span class="sxs-lookup"><span data-stu-id="39a34-117">The best number of misclassifications observed in previous epochs.</span></span>



## <a name="output--intsequentialmodel"></a><span data-ttu-id="39a34-118">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span><span class="sxs-lookup"><span data-stu-id="39a34-118">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))</span></span>

- <span data-ttu-id="39a34-119">Het kleinste aantal misclassificaties dat door deze epoche wordt waargenomen.</span><span class="sxs-lookup"><span data-stu-id="39a34-119">The smallest number of misclassifications observed through to this epoch.</span></span>
- <span data-ttu-id="39a34-120">Het nieuwe best sequentiële model is gevonden.</span><span class="sxs-lookup"><span data-stu-id="39a34-120">The new best sequential model found.</span></span>