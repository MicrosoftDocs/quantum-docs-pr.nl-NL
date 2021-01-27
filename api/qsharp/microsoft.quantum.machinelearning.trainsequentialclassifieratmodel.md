---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Bewerking TrainSequentialClassifierAtModel
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: 4164c190cb19b6d3ea74d9803a77d2b19607279b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857162"
---
# <a name="trainsequentialclassifieratmodel-operation"></a><span data-ttu-id="001e3-102">Bewerking TrainSequentialClassifierAtModel</span><span class="sxs-lookup"><span data-stu-id="001e3-102">TrainSequentialClassifierAtModel operation</span></span>

<span data-ttu-id="001e3-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="001e3-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="001e3-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="001e3-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="001e3-105">Gezien de structuur van een sequentiële classificatie, traint de classificatie op een bepaald gelabelde Trainingsset, beginnend bij een bepaald model.</span><span class="sxs-lookup"><span data-stu-id="001e3-105">Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.</span></span>

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a><span data-ttu-id="001e3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="001e3-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="001e3-107">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="001e3-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="001e3-108">Het sequentiële model dat moet worden gebruikt als uitgangs punt voor training.</span><span class="sxs-lookup"><span data-stu-id="001e3-108">The sequential model to be used as a starting point for training.</span></span>


### <a name="samples--labeledsample"></a><span data-ttu-id="001e3-109">voor beelden: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span><span class="sxs-lookup"><span data-stu-id="001e3-109">samples : [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]</span></span>

<span data-ttu-id="001e3-110">Een set gelabelde trainings gegevens die worden gebruikt voor het uitvoeren van training.</span><span class="sxs-lookup"><span data-stu-id="001e3-110">A set of labeled training data that will be used to perform training.</span></span>


### <a name="options--trainingoptions"></a><span data-ttu-id="001e3-111">opties: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="001e3-111">options : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="001e3-112">De configuratie die moet worden gebruikt bij het trainen; Zie @"microsoft.quantum.machinelearning.trainingoptions" en @"microsoft.quantum.machinelearning.defaulttrainingoptions" voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="001e3-112">Configuration to be used when training; see @"microsoft.quantum.machinelearning.trainingoptions" and @"microsoft.quantum.machinelearning.defaulttrainingoptions" for more details.</span></span>


### <a name="trainingschedule--samplingschedule"></a><span data-ttu-id="001e3-113">trainingSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="001e3-113">trainingSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="001e3-114">Een steekproef schema dat moet worden gebruikt bij het selecteren van voor beelden uit de trainings gegevens tijdens de trainings stappen.</span><span class="sxs-lookup"><span data-stu-id="001e3-114">A sampling schedule to use when selecting samples from the training data during training steps.</span></span>


### <a name="validationschedule--samplingschedule"></a><span data-ttu-id="001e3-115">validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span><span class="sxs-lookup"><span data-stu-id="001e3-115">validationSchedule : [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)</span></span>

<span data-ttu-id="001e3-116">Een steekproef schema dat moet worden gebruikt bij het selecteren van steek proeven uit de opleidings gegevens wanneer wordt geselecteerd welk begin punt heeft geresulteerd in de beste classificatie Score.</span><span class="sxs-lookup"><span data-stu-id="001e3-116">A sampling schedule to use when selecting samples from the training data when selecting which start point resulted in the best classifier score.</span></span>



## <a name="output--sequentialmodelint"></a><span data-ttu-id="001e3-117">Uitvoer: ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="001e3-117">Output : ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

- <span data-ttu-id="001e3-118">Een parameterisering van de gegeven classificatie en een afwijking tussen de twee klassen, samen met het beste resultaat van elk van de opgegeven begin punten.</span><span class="sxs-lookup"><span data-stu-id="001e3-118">A parameterization of the given classifier and a bias between the two classes, together corresponding to the best result from each of the given start points.</span></span>
- <span data-ttu-id="001e3-119">Het aantal missers dat bij het beste classificatie model is waargenomen.</span><span class="sxs-lookup"><span data-stu-id="001e3-119">The number of misses observed at the best classifier model.</span></span>

## <a name="see-also"></a><span data-ttu-id="001e3-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="001e3-120">See Also</span></span>

- [<span data-ttu-id="001e3-121">Micro soft. Quantum. MachineLearning. TrainSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="001e3-121">Microsoft.Quantum.MachineLearning.TrainSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [<span data-ttu-id="001e3-122">Micro soft. Quantum. MachineLearning. ValidateSequentialClassifier</span><span class="sxs-lookup"><span data-stu-id="001e3-122">Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier</span></span>](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)