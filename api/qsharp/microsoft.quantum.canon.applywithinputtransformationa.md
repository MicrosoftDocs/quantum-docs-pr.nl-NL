---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationA
title: Bewerking ApplyWithInputTransformationA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: b72c131691e08b4bd32b7faf9265aad6c52b7fde
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704557"
---
# <a name="applywithinputtransformationa-operation"></a><span data-ttu-id="76c9c-102">Bewerking ApplyWithInputTransformationA</span><span class="sxs-lookup"><span data-stu-id="76c9c-102">ApplyWithInputTransformationA operation</span></span>

<span data-ttu-id="76c9c-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="76c9c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="76c9c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="76c9c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="76c9c-105">Op basis van een bewerking waarbij een invoer wordt geaccepteerd, wordt met een functie die een uitvoer die compatibel is met die bewerking, en een invoer naar die functie, de bewerking toegepast met behulp van de functie om de invoer te transformeren naar een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="76c9c-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj), input : 'U) : Unit
```


## <a name="input"></a><span data-ttu-id="76c9c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="76c9c-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="76c9c-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="76c9c-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="76c9c-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="76c9c-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="76c9c-109">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="76c9c-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="76c9c-110">De bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="76c9c-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="76c9c-111">invoer: ' U</span><span class="sxs-lookup"><span data-stu-id="76c9c-111">input : 'U</span></span>

<span data-ttu-id="76c9c-112">Een invoer voor de functie.</span><span class="sxs-lookup"><span data-stu-id="76c9c-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="76c9c-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="76c9c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="76c9c-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="76c9c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="76c9c-115">T</span><span class="sxs-lookup"><span data-stu-id="76c9c-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="76c9c-116">' U</span><span class="sxs-lookup"><span data-stu-id="76c9c-116">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="76c9c-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="76c9c-117">See Also</span></span>

- [<span data-ttu-id="76c9c-118">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="76c9c-118">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="76c9c-119">Micro soft. Quantum. Canon. ApplyWithInputTransformationC</span><span class="sxs-lookup"><span data-stu-id="76c9c-119">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="76c9c-120">Micro soft. Quantum. Canon. ApplyWithInputTransformationCA</span><span class="sxs-lookup"><span data-stu-id="76c9c-120">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="76c9c-121">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="76c9c-121">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)