---
uid: Microsoft.Quantum.Canon.DelayedCA
title: De functie DelayedCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedCA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: c44e3448c471f2a20f995d4546ee54f3affb726e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840555"
---
# <a name="delayedca-function"></a><span data-ttu-id="e2f2e-102">De functie DelayedCA</span><span class="sxs-lookup"><span data-stu-id="e2f2e-102">DelayedCA function</span></span>

<span data-ttu-id="e2f2e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e2f2e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e2f2e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e2f2e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e2f2e-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="e2f2e-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T) : (Unit => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="e2f2e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e2f2e-106">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="e2f2e-107">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="e2f2e-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e2f2e-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="e2f2e-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="e2f2e-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="e2f2e-109">arg : 'T</span></span>

<span data-ttu-id="e2f2e-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="e2f2e-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj--ctl"></a><span data-ttu-id="e2f2e-111">Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="e2f2e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e2f2e-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="e2f2e-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e2f2e-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e2f2e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e2f2e-114">T</span><span class="sxs-lookup"><span data-stu-id="e2f2e-114">'T</span></span>

<span data-ttu-id="e2f2e-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="e2f2e-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2f2e-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e2f2e-116">See Also</span></span>

- [<span data-ttu-id="e2f2e-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="e2f2e-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="e2f2e-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="e2f2e-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)