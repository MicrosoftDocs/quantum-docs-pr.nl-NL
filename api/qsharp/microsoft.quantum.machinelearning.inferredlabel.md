---
uid: Microsoft.Quantum.MachineLearning.InferredLabel
title: De functie InferredLabel
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: InferredLabel
qsharp.summary: Given a of classification probability and a bias, returns the label inferred from that probability.
ms.openlocfilehash: 1d6edec94f731fe96da797f0c3d77e6eba565149
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708016"
---
# <a name="inferredlabel-function"></a><span data-ttu-id="89f92-102">De functie InferredLabel</span><span class="sxs-lookup"><span data-stu-id="89f92-102">InferredLabel function</span></span>

<span data-ttu-id="89f92-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="89f92-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="89f92-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="89f92-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="89f92-105">Als gevolg van een classificatie waarschijnlijkheid en een bias, retourneert het label afgeleid van die kans.</span><span class="sxs-lookup"><span data-stu-id="89f92-105">Given a of classification probability and a bias, returns the label inferred from that probability.</span></span>

```qsharp
function InferredLabel (bias : Double, probability : Double) : Int
```


## <a name="input"></a><span data-ttu-id="89f92-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="89f92-106">Input</span></span>

### <a name="bias--double"></a><span data-ttu-id="89f92-107">afwijking: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="89f92-107">bias : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="89f92-108">De afwijking tussen twee klassen, meestal het resultaat van het trainen van een classificatie.</span><span class="sxs-lookup"><span data-stu-id="89f92-108">The bias between two classes, typically the result of training a classifier.</span></span>


### <a name="probability--double"></a><span data-ttu-id="89f92-109">waarschijnlijkheid: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="89f92-109">probability : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="89f92-110">Een classificatie waarschijnlijkheid voor een bepaald voor beeld, wat vaak het resultaat is van het schatten van de classificatie frequentie.</span><span class="sxs-lookup"><span data-stu-id="89f92-110">A classification probabilities for a particular sample, typically resulting from estimating its classification frequency.</span></span>



## <a name="output--int"></a><span data-ttu-id="89f92-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="89f92-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="89f92-112">Het label is afgeleid van de gegeven classificatie waarschijnlijkheid.</span><span class="sxs-lookup"><span data-stu-id="89f92-112">The label inferred from the given classification probability.</span></span>