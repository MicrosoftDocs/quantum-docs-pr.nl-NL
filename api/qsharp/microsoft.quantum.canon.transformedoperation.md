---
uid: Microsoft.Quantum.Canon.TransformedOperation
title: De functie TransformedOperation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperation
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: d8c2f52290ce89d0a8ff138ba25f6b2e5e0516d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703767"
---
# <a name="transformedoperation-function"></a><span data-ttu-id="52e6b-102">De functie TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="52e6b-102">TransformedOperation function</span></span>

<span data-ttu-id="52e6b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="52e6b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="52e6b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="52e6b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="52e6b-105">Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.</span><span class="sxs-lookup"><span data-stu-id="52e6b-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperation<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit)) : ('U => Unit)
```


## <a name="input"></a><span data-ttu-id="52e6b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="52e6b-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="52e6b-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="52e6b-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="52e6b-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="52e6b-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="52e6b-109">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52e6b-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="52e6b-110">De bewerking die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="52e6b-110">The operation to be transformed.</span></span>



## <a name="output--u--unit"></a><span data-ttu-id="52e6b-111">Uitvoer: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52e6b-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="52e6b-112">Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .</span><span class="sxs-lookup"><span data-stu-id="52e6b-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="52e6b-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="52e6b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="52e6b-114">T</span><span class="sxs-lookup"><span data-stu-id="52e6b-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="52e6b-115">' U</span><span class="sxs-lookup"><span data-stu-id="52e6b-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="52e6b-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="52e6b-116">See Also</span></span>

- [<span data-ttu-id="52e6b-117">Micro soft. Quantum. Canon. TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="52e6b-117">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="52e6b-118">Micro soft. Quantum. Canon. TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="52e6b-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="52e6b-119">Micro soft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="52e6b-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="52e6b-120">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="52e6b-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="52e6b-121">Micro soft. Quantum. Canon. samengesteld</span><span class="sxs-lookup"><span data-stu-id="52e6b-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)