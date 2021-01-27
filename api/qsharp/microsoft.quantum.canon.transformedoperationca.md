---
uid: Microsoft.Quantum.Canon.TransformedOperationCA
title: De functie TransformedOperationCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationCA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: bb39530ae28e17d07a6a5c2bb2d35f81be312d15
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840126"
---
# <a name="transformedoperationca-function"></a><span data-ttu-id="077ee-102">De functie TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="077ee-102">TransformedOperationCA function</span></span>

<span data-ttu-id="077ee-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="077ee-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="077ee-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="077ee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="077ee-105">Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.</span><span class="sxs-lookup"><span data-stu-id="077ee-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationCA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj + Ctl)) : ('U => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="077ee-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="077ee-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="077ee-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="077ee-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="077ee-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="077ee-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="077ee-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="077ee-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="077ee-110">De bewerking die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="077ee-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj--ctl"></a><span data-ttu-id="077ee-111">Output: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="077ee-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="077ee-112">Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .</span><span class="sxs-lookup"><span data-stu-id="077ee-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="077ee-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="077ee-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="077ee-114">T</span><span class="sxs-lookup"><span data-stu-id="077ee-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="077ee-115">' U</span><span class="sxs-lookup"><span data-stu-id="077ee-115">'U</span></span>



## <a name="example"></a><span data-ttu-id="077ee-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="077ee-116">Example</span></span>

<span data-ttu-id="077ee-117">Met de volgende aanroep wordt @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" een bewerking die is ontworpen voor invoer, omgezet @"Microsoft.Quantum.Arithmetic.BigEndian" in een bewerking die invoer van het type accepteert @"Microsoft.Quantum.Arithmetic.LittleEndian" :</span><span class="sxs-lookup"><span data-stu-id="077ee-117">The following call uses @"Microsoft.Quantum.Arithmetic.LittleEndianAsBigEndian" to transform an operation designed for @"Microsoft.Quantum.Arithmetic.BigEndian" inputs into an operation that accepts inputs of type @"Microsoft.Quantum.Arithmetic.LittleEndian":</span></span>

```qsharp
let leOp = TransformedOperation(LittleEndianAsBigEndian, ApplyXorInPlaceBE);
```

## <a name="see-also"></a><span data-ttu-id="077ee-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="077ee-118">See Also</span></span>

- [<span data-ttu-id="077ee-119">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="077ee-119">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="077ee-120">Micro soft. Quantum. Canon. TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="077ee-120">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="077ee-121">Micro soft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="077ee-121">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="077ee-122">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="077ee-122">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="077ee-123">Micro soft. Quantum. Canon. samengesteld</span><span class="sxs-lookup"><span data-stu-id="077ee-123">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)