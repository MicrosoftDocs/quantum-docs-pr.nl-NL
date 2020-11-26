---
uid: Microsoft.Quantum.Canon.TransformedOperationC
title: De functie TransformedOperationC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: TransformedOperationC
qsharp.summary: Given a function and an operation, returns a new operation whose input is transformed by the given function.
ms.openlocfilehash: 964576788bc80dd8920acdfb62d5d69a060e75f6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204858"
---
# <a name="transformedoperationc-function"></a><span data-ttu-id="93233-102">De functie TransformedOperationC</span><span class="sxs-lookup"><span data-stu-id="93233-102">TransformedOperationC function</span></span>

<span data-ttu-id="93233-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="93233-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="93233-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="93233-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="93233-105">Met een functie en een bewerking wordt een nieuwe bewerking geretourneerd waarvan de invoer wordt getransformeerd door de opgegeven functie.</span><span class="sxs-lookup"><span data-stu-id="93233-105">Given a function and an operation, returns a new operation whose input is transformed by the given function.</span></span>

```qsharp
function TransformedOperationC<'T, 'U> (fn : ('U -> 'T), op : ('T => Unit is Ctl)) : ('U => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="93233-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="93233-106">Input</span></span>

### <a name="fn--u---t"></a><span data-ttu-id="93233-107">FN: ' U-> '</span><span class="sxs-lookup"><span data-stu-id="93233-107">fn : 'U -> 'T</span></span>

<span data-ttu-id="93233-108">Een functie waarmee de gegeven invoer wordt getransformeerd in een formulier dat wordt verwacht door de bewerking.</span><span class="sxs-lookup"><span data-stu-id="93233-108">A function that transforms the given input into a form expected by the operation.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="93233-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="93233-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="93233-110">De bewerking die moet worden getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="93233-110">The operation to be transformed.</span></span>



## <a name="output--u--unit--is-ctl"></a><span data-ttu-id="93233-111">Uitvoer: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="93233-111">Output : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="93233-112">Een nieuwe bewerking tbat aanroepen `fn` met de invoer en geeft vervolgens de resulterende uitvoer door aan `op` .</span><span class="sxs-lookup"><span data-stu-id="93233-112">A new operation tbat calls `fn` with its input, then passes the resulting output to `op`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="93233-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="93233-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="93233-114">T</span><span class="sxs-lookup"><span data-stu-id="93233-114">'T</span></span>


### <a name="u"></a><span data-ttu-id="93233-115">' U</span><span class="sxs-lookup"><span data-stu-id="93233-115">'U</span></span>



## <a name="see-also"></a><span data-ttu-id="93233-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="93233-116">See Also</span></span>

- [<span data-ttu-id="93233-117">Micro soft. Quantum. Canon. TransformedOperation</span><span class="sxs-lookup"><span data-stu-id="93233-117">Microsoft.Quantum.Canon.TransformedOperation</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperation)
- [<span data-ttu-id="93233-118">Micro soft. Quantum. Canon. TransformedOperationA</span><span class="sxs-lookup"><span data-stu-id="93233-118">Microsoft.Quantum.Canon.TransformedOperationA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationA)
- [<span data-ttu-id="93233-119">Micro soft. Quantum. Canon. TransformedOperationCA</span><span class="sxs-lookup"><span data-stu-id="93233-119">Microsoft.Quantum.Canon.TransformedOperationCA</span></span>](xref:Microsoft.Quantum.Canon.TransformedOperationCA)
- [<span data-ttu-id="93233-120">Micro soft. Quantum. Canon. ApplyWithInputTransformation</span><span class="sxs-lookup"><span data-stu-id="93233-120">Microsoft.Quantum.Canon.ApplyWithInputTransformation</span></span>](xref:Microsoft.Quantum.Canon.ApplyWithInputTransformation)
- [<span data-ttu-id="93233-121">Micro soft. Quantum. Canon. samengesteld</span><span class="sxs-lookup"><span data-stu-id="93233-121">Microsoft.Quantum.Canon.Composed</span></span>](xref:Microsoft.Quantum.Canon.Composed)