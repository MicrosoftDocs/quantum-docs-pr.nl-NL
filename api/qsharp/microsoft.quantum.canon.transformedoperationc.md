---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: De functie TransformedOperationC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 9475c5a1cc3b7e14c56c301749311a72e15f71e0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852033"
---
# <a name="transformedoperationc-function"></a><span data-ttu-id="bdc77-102">De functie TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="bdc77-102">TransformedOperationC function</span></span>

<span data-ttu-id="bdc77-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bdc77-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bdc77-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bdc77-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bdc77-105">Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.</span><span class="sxs-lookup"><span data-stu-id="bdc77-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="bdc77-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bdc77-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="bdc77-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="bdc77-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="bdc77-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="bdc77-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="bdc77-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="bdc77-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="bdc77-110">De bewerking die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="bdc77-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-ctl"></a><span data-ttu-id="bdc77-111">Uitvoer: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="bdc77-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="bdc77-112">Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .</span><span class="sxs-lookup"><span data-stu-id="bdc77-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bdc77-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="bdc77-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bdc77-114">T</span><span class="sxs-lookup"><span data-stu-id="bdc77-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="bdc77-115">' U</span><span class="sxs-lookup"><span data-stu-id="bdc77-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="bdc77-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="bdc77-116">Example</span></span>

<span data-ttu-id="bdc77-117">Met de volgende aanroep wordt @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" een bewerking die is ontworpen voor invoer, omgezet @"Microsoft.Quantum.Arithmetic.BigEndian" in een bewerking die invoer van het type accepteert @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="bdc77-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="bdc77-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bdc77-118">See Also</span></span>

- [<span data-ttu-id="bdc77-119">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="bdc77-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="bdc77-120">Micro soft. Quantum. Canon. TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="bdc77-120">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="bdc77-121">Micro soft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="bdc77-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="bdc77-122">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="bdc77-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="bdc77-123">Micro soft. Quantum. Canon. samengesteld</span><span class="sxs-lookup"><span data-stu-id="bdc77-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)