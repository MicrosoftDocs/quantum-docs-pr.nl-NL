---
uid: Microsoft.Quantum.Canon.TransformedOperationA
title: De functie TransformedOperationA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationA
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 349424a102dba7354bbaa65fffdc2b5d506a3b91
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703766"
---
# <a name="transformedoperationa-function"></a><span data-ttu-id="cd0e4-102">De functie TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="cd0e4-102">TransformedOperationA function</span></span>

<span data-ttu-id="cd0e4-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cd0e4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cd0e4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cd0e4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cd0e4-105">Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.</span><span class="sxs-lookup"><span data-stu-id="cd0e4-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationA<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Adj)) : ('U => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="cd0e4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cd0e4-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="cd0e4-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="cd0e4-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="cd0e4-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="cd0e4-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="cd0e4-109">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="cd0e4-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="cd0e4-110">De bewerking die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="cd0e4-110">The operation to be transformed.</span></span>



## <a name="output--u--unit-adj"></a><span data-ttu-id="cd0e4-111">Output: ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="cd0e4-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="cd0e4-112">Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .</span><span class="sxs-lookup"><span data-stu-id="cd0e4-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cd0e4-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="cd0e4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cd0e4-114">T</span><span class="sxs-lookup"><span data-stu-id="cd0e4-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="cd0e4-115">' U</span><span class="sxs-lookup"><span data-stu-id="cd0e4-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="cd0e4-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cd0e4-116">See Also</span></span>

- [<span data-ttu-id="cd0e4-117">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="cd0e4-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="cd0e4-118">Micro soft. Quantum. Canon. TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="cd0e4-118">Microsoft.Quantum.Canon.TransformedOperationC</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationC)
- [<span data-ttu-id="cd0e4-119">Micro soft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="cd0e4-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="cd0e4-120">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="cd0e4-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="cd0e4-121">Micro soft. Quantum. Canon. samengesteld</span><span class="sxs-lookup"><span data-stu-id="cd0e4-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)