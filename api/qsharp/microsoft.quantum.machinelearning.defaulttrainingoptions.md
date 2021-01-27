---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: De functie DefaultTrainingOptions
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855996"
---
# <a name="defaulttrainingoptions-function"></a><span data-ttu-id="d373f-102">De functie DefaultTrainingOptions</span><span class="sxs-lookup"><span data-stu-id="d373f-102">DefaultTrainingOptions function</span></span>

<span data-ttu-id="d373f-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d373f-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="d373f-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="d373f-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="d373f-105">Retourneert een standaardset opties voor opleidings classificaties.</span><span class="sxs-lookup"><span data-stu-id="d373f-105">Returns a default set of options for training classifiers.</span></span>

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a><span data-ttu-id="d373f-106">Uitvoer: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span><span class="sxs-lookup"><span data-stu-id="d373f-106">Output : [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)</span></span>

<span data-ttu-id="d373f-107">Een redelijk aantal standaard opleidings opties voor het gebruik van classificaties voor trainingen.</span><span class="sxs-lookup"><span data-stu-id="d373f-107">A reasonable set of default training options for use when training classifiers.</span></span>

## <a name="example"></a><span data-ttu-id="d373f-108">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d373f-108">Example</span></span>

<span data-ttu-id="d373f-109">Als u de standaard opties wilt gebruiken, maar met extra metingen, gebruikt u de `w/` operator:</span><span class="sxs-lookup"><span data-stu-id="d373f-109">To use the default options, but with additional measurements, use the `w/` operator:</span></span>

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```