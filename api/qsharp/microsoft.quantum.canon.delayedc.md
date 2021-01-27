---
uid: Microsoft.Quantum.Canon.DelayedC
title: De functie DelayedC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: a1f2582668131816b774bf4a8b7476d9f1ee8cad
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840565"
---
# <a name="delayedc-function"></a><span data-ttu-id="f6feb-102">De functie DelayedC</span><span class="sxs-lookup"><span data-stu-id="f6feb-102">DelayedC function</span></span>

<span data-ttu-id="f6feb-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f6feb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f6feb-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f6feb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f6feb-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="f6feb-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="f6feb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f6feb-106">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="f6feb-107">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="f6feb-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f6feb-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="f6feb-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="f6feb-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="f6feb-109">arg : 'T</span></span>

<span data-ttu-id="f6feb-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="f6feb-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit--is-ctl"></a><span data-ttu-id="f6feb-111">Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="f6feb-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="f6feb-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="f6feb-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f6feb-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f6feb-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f6feb-114">T</span><span class="sxs-lookup"><span data-stu-id="f6feb-114">'T</span></span>

<span data-ttu-id="f6feb-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="f6feb-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="f6feb-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f6feb-116">See Also</span></span>

- [<span data-ttu-id="f6feb-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="f6feb-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="f6feb-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="f6feb-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)