---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: De functie TransformedOperationA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: eceba260e601b73bdfa2de6ea6ab146820b5c59a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204875"
---
# <a name="transformedoperationa-function"></a><span data-ttu-id="315a2-102">De functie TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="315a2-102">TransformedOperationA function</span></span>

<span data-ttu-id="315a2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="315a2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="315a2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="315a2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="315a2-105">Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.</span><span class="sxs-lookup"><span data-stu-id="315a2-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="315a2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="315a2-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="315a2-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="315a2-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="315a2-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="315a2-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="315a2-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="315a2-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="315a2-110">De bewerking die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="315a2-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-adj"></a><span data-ttu-id="315a2-111">Uitvoer: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="315a2-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="315a2-112">Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .</span><span class="sxs-lookup"><span data-stu-id="315a2-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="315a2-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="315a2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="315a2-114">T</span><span class="sxs-lookup"><span data-stu-id="315a2-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="315a2-115">' U</span><span class="sxs-lookup"><span data-stu-id="315a2-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="315a2-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="315a2-116">See Also</span></span>

- [<span data-ttu-id="315a2-117">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="315a2-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="315a2-118">Micro soft. Quantum. Canon. TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="315a2-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="315a2-119">Micro soft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="315a2-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="315a2-120">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="315a2-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="315a2-121">Micro soft. Quantum. Canon. samengesteld</span><span class="sxs-lookup"><span data-stu-id="315a2-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)