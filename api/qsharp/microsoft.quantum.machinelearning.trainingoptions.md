---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Door de gebruiker gedefinieerd TrainingOptions-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 280a3857aa7bc42f636a33f893d4f450e79b6a6a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196120"
---
# <a name="trainingoptions-user-defined-type"></a><span data-ttu-id="98063-102">Door de gebruiker gedefinieerd TrainingOptions-type</span><span class="sxs-lookup"><span data-stu-id="98063-102">TrainingOptions user defined type</span></span>

<span data-ttu-id="98063-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="98063-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="98063-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="98063-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="98063-105">Een verzameling opties die moeten worden gebruikt in de Quantum-classificaties voor de training.</span><span class="sxs-lookup"><span data-stu-id="98063-105">A collection of options to be used in training quantum classifiers.</span></span>

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a><span data-ttu-id="98063-106">Benoemde items</span><span class="sxs-lookup"><span data-stu-id="98063-106">Named Items</span></span>

### <a name="learningrate--double"></a><span data-ttu-id="98063-107">Leer tempo valt: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="98063-107">LearningRate : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="98063-108">Het leer tempo waarmee kleur overgangen moeten worden aangepast bij het bijwerken van model parameters tijdens de trainings stappen.</span><span class="sxs-lookup"><span data-stu-id="98063-108">The learning rate by which gradients should be rescaled when updating model parameters during training steps.</span></span>
### <a name="tolerance--double"></a><span data-ttu-id="98063-109">Tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="98063-109">Tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="98063-110">De aanpassings tolerantie die moet worden gebruikt bij het voorbereiden van voor beelden als Quantum status.</span><span class="sxs-lookup"><span data-stu-id="98063-110">The approximation tolerance to use when preparing samples as quantum states.</span></span>
### <a name="minibatchsize--int"></a><span data-ttu-id="98063-111">MinibatchSize: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="98063-111">MinibatchSize : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="98063-112">Het aantal voor beelden dat moet worden gebruikt in de minibatch van de training.</span><span class="sxs-lookup"><span data-stu-id="98063-112">The number of samples to use in each training minibatch.</span></span>
### <a name="nmeasurements--int"></a><span data-ttu-id="98063-113">NMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="98063-113">NMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="98063-114">Het aantal keer dat elk classificatie resultaat moet worden gemeten om de classificatie waarschijnlijkheid te schatten.</span><span class="sxs-lookup"><span data-stu-id="98063-114">The number of times to measure each classification result in order to estimate the classification probability.</span></span>
### <a name="maxepochs--int"></a><span data-ttu-id="98063-115">MaxEpochs: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="98063-115">MaxEpochs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="98063-116">Het maximum aantal epoches voor het trainen van elk model voor.</span><span class="sxs-lookup"><span data-stu-id="98063-116">The maximum number of epochs to train each model for.</span></span>
### <a name="maxstalls--int"></a><span data-ttu-id="98063-117">MaxStalls: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="98063-117">MaxStalls : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="98063-118">Het maximum aantal keren dat een trainings-epoche mag worden gestopt (ongeveer nul kleur overgang) voordat er een fout optreedt.</span><span class="sxs-lookup"><span data-stu-id="98063-118">The maximum number of times a training epoch is allowed to stall (approximately zero gradient) before failing.</span></span>
### <a name="stochasticrescalefactor--double"></a><span data-ttu-id="98063-119">StochasticRescaleFactor: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="98063-119">StochasticRescaleFactor : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="98063-120">De hoeveelheid voor het herschalen van gereduceerde modellen door voordat een update opnieuw wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="98063-120">The amount to rescale stalled models by before retrying an update.</span></span>
### <a name="scoringperiod--int"></a><span data-ttu-id="98063-121">ScoringPeriod: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="98063-121">ScoringPeriod : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="98063-122">Het aantal verloop stappen dat moet worden genomen tussen score punten.</span><span class="sxs-lookup"><span data-stu-id="98063-122">The number of gradient steps to be taken between scoring points.</span></span>
<span data-ttu-id="98063-123">Stel de beste nauw keurigheid in op 1.</span><span class="sxs-lookup"><span data-stu-id="98063-123">For best accuracy, set to 1.</span></span>
### <a name="verbosemessage--string---unit"></a><span data-ttu-id="98063-124">VerboseMessage: [teken reeks](xref:microsoft.quantum.lang-ref.string) -> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="98063-124">VerboseMessage : [String](xref:microsoft.quantum.lang-ref.string) -> [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="98063-125">Een functie die kan worden gebruikt om uitgebreide feedback te geven.</span><span class="sxs-lookup"><span data-stu-id="98063-125">A function that can be used to provide verbose feedback.</span></span>

## <a name="remarks"></a><span data-ttu-id="98063-126">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="98063-126">Remarks</span></span>

<span data-ttu-id="98063-127">Deze UDT mag niet direct worden gemaakt, maar moet in plaats daarvan worden opgegeven door @"microsoft.quantum.machinelearning.defaulttrainingoptions" de `w/` operator aan te roepen en vervolgens te gebruiken om verschillende standaard waarden te overschrijven.</span><span class="sxs-lookup"><span data-stu-id="98063-127">This UDT should not be created directly, but rather should be specified by calling @"microsoft.quantum.machinelearning.defaulttrainingoptions" and then using the `w/` operator to override different defaults.</span></span>

<span data-ttu-id="98063-128">Als u bijvoorbeeld 100.000 metingen en Maxi maal 8 trainings-epochen wilt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="98063-128">For example, to use 100,000 measurements and at most 8 training epochs:</span></span>

```Q#
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a><span data-ttu-id="98063-129">Referenties</span><span class="sxs-lookup"><span data-stu-id="98063-129">References</span></span>

- [<span data-ttu-id="98063-130">arXiv:1804.00633</span><span class="sxs-lookup"><span data-stu-id="98063-130">arXiv:1804.00633</span></span>](https://arxiv.org/abs/1804.00633)