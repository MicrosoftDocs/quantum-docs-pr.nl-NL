---
uid: Microsoft.Quantum.Canon.DelayedCA
title: De functie DelayedCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: fe2babb87d716185286b0864745f7ff6e637f8a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207004"
---
# <a name="delayedca-function"></a><span data-ttu-id="78a81-102">De functie DelayedCA</span><span class="sxs-lookup"><span data-stu-id="78a81-102">DelayedCA function</span></span>

<span data-ttu-id="78a81-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="78a81-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="78a81-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="78a81-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="78a81-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="78a81-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="78a81-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="78a81-106">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="78a81-107">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="78a81-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="78a81-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="78a81-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="78a81-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="78a81-109">arg : 'T</span></span>

<span data-ttu-id="78a81-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="78a81-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj--ctl"></a><span data-ttu-id="78a81-111">Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="78a81-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="78a81-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="78a81-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="78a81-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="78a81-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="78a81-114">T</span><span class="sxs-lookup"><span data-stu-id="78a81-114">'T</span></span>

<span data-ttu-id="78a81-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="78a81-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="78a81-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="78a81-116">See Also</span></span>

- [<span data-ttu-id="78a81-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="78a81-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="78a81-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="78a81-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)