---
uid: Microsoft.Quantum.Canon.DelayedA
title: De functie delayed
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 33ff4dab36a6c6e17b9496a623f70b814c9f2fed
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207068"
---
# <a name="delayeda-function"></a><span data-ttu-id="820ed-102">De functie delayed</span><span class="sxs-lookup"><span data-stu-id="820ed-102">DelayedA function</span></span>

<span data-ttu-id="820ed-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="820ed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="820ed-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="820ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="820ed-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="820ed-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="820ed-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="820ed-106">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="820ed-107">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="820ed-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="820ed-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="820ed-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="820ed-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="820ed-109">arg : 'T</span></span>

<span data-ttu-id="820ed-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="820ed-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj"></a><span data-ttu-id="820ed-111">Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="820ed-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="820ed-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="820ed-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="820ed-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="820ed-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="820ed-114">T</span><span class="sxs-lookup"><span data-stu-id="820ed-114">'T</span></span>

<span data-ttu-id="820ed-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="820ed-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="820ed-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="820ed-116">See Also</span></span>

- [<span data-ttu-id="820ed-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="820ed-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="820ed-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="820ed-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)