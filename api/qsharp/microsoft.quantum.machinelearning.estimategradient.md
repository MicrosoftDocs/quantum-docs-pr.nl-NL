---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Bewerking EstimateGradient
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 38edcb67e7dcc5d2e971fb507a792937774a702c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844383"
---
# <a name="estimategradient-operation"></a><span data-ttu-id="c2a3a-102">Bewerking EstimateGradient</span><span class="sxs-lookup"><span data-stu-id="c2a3a-102">EstimateGradient operation</span></span>

<span data-ttu-id="c2a3a-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c2a3a-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="c2a3a-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c2a3a-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="c2a3a-105">Maakt een schatting van de cursus verloop voor een sequentiële classificatie in een bepaald model en voor een gegeven gecodeerde invoer.</span><span class="sxs-lookup"><span data-stu-id="c2a3a-105">Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.</span></span>

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a><span data-ttu-id="c2a3a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c2a3a-106">Input</span></span>

### <a name="model--sequentialmodel"></a><span data-ttu-id="c2a3a-107">model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span><span class="sxs-lookup"><span data-stu-id="c2a3a-107">model : [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)</span></span>

<span data-ttu-id="c2a3a-108">Het sequentiële model waarvan het verloop moet worden geschat.</span><span class="sxs-lookup"><span data-stu-id="c2a3a-108">The sequential model whose gradient is to be estimated.</span></span>


### <a name="encodedinput--stategenerator"></a><span data-ttu-id="c2a3a-109">encodedInput: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span><span class="sxs-lookup"><span data-stu-id="c2a3a-109">encodedInput : [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)</span></span>

<span data-ttu-id="c2a3a-110">Een invoer van de sequentiële classificatie, gecodeerd in een status voorbereidings bewerking.</span><span class="sxs-lookup"><span data-stu-id="c2a3a-110">An input to the sequential classifier, encoded into a state preparation operation.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="c2a3a-111">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c2a3a-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c2a3a-112">Het aantal metingen dat moet worden gebruikt bij het schatten van de kleur overgang.</span><span class="sxs-lookup"><span data-stu-id="c2a3a-112">The number of measurements to use in estimating the gradient.</span></span>



## <a name="output--double"></a><span data-ttu-id="c2a3a-113">Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c2a3a-113">Output : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c2a3a-114">Een schatting van de verloop tijd van de training bij de gegeven para meters voor invoer en model.</span><span class="sxs-lookup"><span data-stu-id="c2a3a-114">An estimate of the training gradient at the given input and model parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2a3a-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c2a3a-115">Remarks</span></span>

<span data-ttu-id="c2a3a-116">Deze bewerking maakt gebruik van een Hadamard-test en de para meter Shift-techniek om de kleur overgang te schatten.</span><span class="sxs-lookup"><span data-stu-id="c2a3a-116">This operation uses a Hadamard test and the parameter shift technique together to estimate the gradient.</span></span>