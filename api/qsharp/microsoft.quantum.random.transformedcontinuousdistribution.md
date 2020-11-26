---
uid: Microsoft.Quantum.Random.TransformedContinuousDistribution
title: De functie TransformedContinuousDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: TransformedContinuousDistribution
qsharp.summary: Given a continuous distribution, returns a new distribution that transforms the original by a given function.
ms.openlocfilehash: b317eaaa0ff0180ea5d240464c96d1c6b59c9c70
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226261"
---
# <a name="transformedcontinuousdistribution-function"></a><span data-ttu-id="8144c-102">De functie TransformedContinuousDistribution</span><span class="sxs-lookup"><span data-stu-id="8144c-102">TransformedContinuousDistribution function</span></span>

<span data-ttu-id="8144c-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="8144c-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="8144c-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="8144c-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="8144c-105">Op basis van een continue distributie retourneert een nieuwe distributie waarmee het origineel door een bepaalde functie wordt getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="8144c-105">Given a continuous distribution, returns a new distribution that transforms the original by a given function.</span></span>

```qsharp
function TransformedContinuousDistribution (transform : (Double -> Double), distribution : Microsoft.Quantum.Random.ContinuousDistribution) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="8144c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8144c-106">Input</span></span>

### <a name="transform--double---double"></a><span data-ttu-id="8144c-107">transformeren: [dubbele](xref:microsoft.quantum.lang-ref.double) -> [dubbele precisie](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8144c-107">transform : [Double](xref:microsoft.quantum.lang-ref.double) -> [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8144c-108">Een functie waarmee de variates van de oorspronkelijke distributie wordt getransformeerd naar de getransformeerde distributie.</span><span class="sxs-lookup"><span data-stu-id="8144c-108">A function that transforms variates of the original distribution to the transformed distribution.</span></span>


### <a name="distribution--continuousdistribution"></a><span data-ttu-id="8144c-109">distributie: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="8144c-109">distribution : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="8144c-110">De oorspronkelijke verdeling die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="8144c-110">The original distribution to be transformed.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="8144c-111">Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="8144c-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="8144c-112">Een nieuwe distributie gerelateerd aan `distribution` de trans formatie die wordt gegeven door `transform` .</span><span class="sxs-lookup"><span data-stu-id="8144c-112">A new distribution related to `distribution` by the transformation given by `transform`.</span></span>