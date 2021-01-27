---
uid: Microsoft.Quantum.Canon.ApplyWithInputTransformationA
title: Bewerking ApplyWithInputTransformationA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithInputTransformationA
qsharp.summary: Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.
ms.openlocfilehash: 3ab07f301f310e3ec380981bdb53201fc74bd289
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841127"
---
# <a name="applywithinputtransformationa-operation"></a><span data-ttu-id="aef74-102">Bewerking ApplyWithInputTransformationA</span><span class="sxs-lookup"><span data-stu-id="aef74-102">ApplyWithInputTransformationA operation</span></span>

<span data-ttu-id="aef74-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aef74-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aef74-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aef74-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aef74-105">Op basis van een bewerking waarbij een invoer wordt geaccepteerd, wordt met een functie die een uitvoer die compatibel is met die bewerking, en een invoer naar die functie, de bewerking toegepast met behulp van de functie om de invoer te transformeren naar een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="aef74-105">Given an operation that accepts some input, a function that returns an output compatible with that operation, and an input to that function, applies the operation using the function to transform the input to a form expected by the operation.</span></span>

```qsharp
operation ApplyWithInputTransformationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj), input : 'U) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="aef74-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="aef74-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="aef74-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="aef74-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="aef74-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="aef74-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="aef74-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="aef74-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="aef74-110">De bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="aef74-110">The operation to be applied.</span></span>


### <a name="input--u"></a><span data-ttu-id="aef74-111">invoer: ' U</span><span class="sxs-lookup"><span data-stu-id="aef74-111">input : 'U</span></span>

<span data-ttu-id="aef74-112">Een invoer voor de functie.</span><span class="sxs-lookup"><span data-stu-id="aef74-112">An input to the function.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aef74-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aef74-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="aef74-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="aef74-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aef74-115">T</span><span class="sxs-lookup"><span data-stu-id="aef74-115">'T</span></span>


### <a name="u"></a><span data-ttu-id="aef74-116">' U</span><span class="sxs-lookup"><span data-stu-id="aef74-116">'U</span></span>



## <a name="example"></a><span data-ttu-id="aef74-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="aef74-117">Example</span></span>

<span data-ttu-id="aef74-118">De volgende aanroep gebruikt @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" om een bewerking die is ontworpen voor invoer, toe @"Microsoft.Quantum.Arithmetic.BigEndian" te passen op een invoer van het type @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="aef74-118">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to apply an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs to an input of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
ApplyWithInputTransformation(LittleEndianAsBigEndian, ApplyXorInPlaceBE, LittleEndian(qubits));
```

## <a name="see-also"></a><span data-ttu-id="aef74-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="aef74-119">See Also</span></span>

- [<span data-ttu-id="aef74-120">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="aef74-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="aef74-121">Micro soft. Quantum. Canon. ApplyWithInputTransformationC</span><span class="sxs-lookup"><span data-stu-id="aef74-121">Microsoft.Quantum.Canon.ApplyWithInputTransformationC</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationC)
- [<span data-ttu-id="aef74-122">Micro soft. Quantum. Canon. ApplyWithInputTransformationCA</span><span class="sxs-lookup"><span data-stu-id="aef74-122">Microsoft.Quantum.Canon.ApplyWithInputTransformationCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformationCA)
- [<span data-ttu-id="aef74-123">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="aef74-123">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)