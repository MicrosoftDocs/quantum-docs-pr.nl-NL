---
uid: Microsoft.Quantum.Canon.DelayedA
title: De functie delayed
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: e53279bd3ddc5fa8bc0c862f998b273a9e17a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840606"
---
# <a name="delayeda-function"></a><span data-ttu-id="d60c2-102">De functie delayed</span><span class="sxs-lookup"><span data-stu-id="d60c2-102">DelayedA function</span></span>

<span data-ttu-id="d60c2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d60c2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d60c2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d60c2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d60c2-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="d60c2-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="d60c2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d60c2-106">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="d60c2-107">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="d60c2-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d60c2-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="d60c2-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="d60c2-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="d60c2-109">arg : 'T</span></span>

<span data-ttu-id="d60c2-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="d60c2-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-adj"></a><span data-ttu-id="d60c2-111">Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="d60c2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d60c2-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="d60c2-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d60c2-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d60c2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d60c2-114">T</span><span class="sxs-lookup"><span data-stu-id="d60c2-114">'T</span></span>

<span data-ttu-id="d60c2-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="d60c2-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="d60c2-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d60c2-116">See Also</span></span>

- [<span data-ttu-id="d60c2-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="d60c2-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="d60c2-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="d60c2-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)