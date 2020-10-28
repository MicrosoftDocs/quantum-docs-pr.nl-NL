---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationCA
title: Bewerking ApplyWithInputTransformationCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationCA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: c80ce0887a202a60de81c2d12fa95ce1eab59058
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704549"
---
# <a name="applywithinputtransformationca-operation"></a><span data-ttu-id="a6f17-102">Bewerking ApplyWithInputTransformationCA</span><span class="sxs-lookup"><span data-stu-id="a6f17-102">ApplyWithInputTransformationCA operation</span></span>

<span data-ttu-id="a6f17-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a6f17-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a6f17-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a6f17-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a6f17-105">Op basis van een bewerking waarbij een invoer wordt geaccepteerd, wordt met een functie die een uitvoer die compatibel is met die bewerking, en een invoer naar die functie, de bewerking toegepast met behulp van de functie om de invoer te transformeren naar een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="a6f17-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="a6f17-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a6f17-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="a6f17-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="a6f17-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="a6f17-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="a6f17-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="a6f17-109">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="a6f17-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a6f17-110">De bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a6f17-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="a6f17-111">invoer: ' U</span><span class="sxs-lookup"><span data-stu-id="a6f17-111">input : 'U</span></span>

<span data-ttu-id="a6f17-112">Een invoer voor de functie.</span><span class="sxs-lookup"><span data-stu-id="a6f17-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a6f17-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a6f17-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a6f17-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a6f17-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a6f17-115">T</span><span class="sxs-lookup"><span data-stu-id="a6f17-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="a6f17-116">' U</span><span class="sxs-lookup"><span data-stu-id="a6f17-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="a6f17-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a6f17-117">See Also</span></span>

- [<span data-ttu-id="a6f17-118">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="a6f17-118">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="a6f17-119">Micro soft. Quantum. Canon. ApplyWithInputTransformationA</span><span class="sxs-lookup"><span data-stu-id="a6f17-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationA)
- [<span data-ttu-id="a6f17-120">Micro soft. Quantum. Canon. ApplyWithInputTransformationC</span><span class="sxs-lookup"><span data-stu-id="a6f17-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="a6f17-121">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="a6f17-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)