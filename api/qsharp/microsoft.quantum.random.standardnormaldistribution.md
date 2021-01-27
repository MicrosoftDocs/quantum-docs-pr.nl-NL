---
uid: Microsoft.Quantum.Random.StandardNormalDistribution
title: De functie StandardNormalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: StandardNormalDistribution
qsharp.summary: Returns a normal distribution with mean 0 and variance 1.
ms.openlocfilehash: e1776339655c33516f7b3d156f1b377a0c74d250
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857802"
---
# <a name="standardnormaldistribution-function"></a><span data-ttu-id="55801-102">De functie StandardNormalDistribution</span><span class="sxs-lookup"><span data-stu-id="55801-102">StandardNormalDistribution function</span></span>

<span data-ttu-id="55801-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="55801-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="55801-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="55801-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="55801-105">Retourneert een normale verdeling met gemiddelde 0 en variantie 1.</span><span class="sxs-lookup"><span data-stu-id="55801-105">Returns a normal distribution with mean 0 and variance 1.</span></span>

```qsharp
function StandardNormalDistribution () : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="output--continuousdistribution"></a><span data-ttu-id="55801-106">Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="55801-106">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>



## <a name="example"></a><span data-ttu-id="55801-107">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="55801-107">Example</span></span>

<span data-ttu-id="55801-108">In het volgende voor beeld worden tien voor beelden van de normale standaard distributie getekend:</span><span class="sxs-lookup"><span data-stu-id="55801-108">The following draws 10 samples from the standard normal distribution:</span></span>

```qsharp
let samples = DrawMany((StandardNormalDistribution())::Sample, 10, ());
```

## <a name="see-also"></a><span data-ttu-id="55801-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="55801-109">See Also</span></span>

- [<span data-ttu-id="55801-110">Micro soft. Quantum. wille keurig. NormalDistribution</span><span class="sxs-lookup"><span data-stu-id="55801-110">Microsoft.Quantum.Random.NormalDistribution</span></span>](xref:Microsoft.Quantum.Random.NormalDistribution)