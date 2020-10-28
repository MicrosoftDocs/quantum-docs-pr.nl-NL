---
uid: Microsoft.Quantum.Canon.DelayedC
title: De functie DelayedC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedC
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 7cfd77b0bb2d91c5a1c4bb5bc84e052421d733a9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704196"
---
# <a name="delayedc-function"></a><span data-ttu-id="5c271-102">De functie DelayedC</span><span class="sxs-lookup"><span data-stu-id="5c271-102">DelayedC function</span></span>

<span data-ttu-id="5c271-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5c271-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5c271-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5c271-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5c271-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="5c271-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedC<'T> (op : ('T => Unit is Ctl), arg : 'T) : (Unit => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="5c271-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5c271-106">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="5c271-107">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5c271-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5c271-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="5c271-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="5c271-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="5c271-109">arg : 'T</span></span>

<span data-ttu-id="5c271-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="5c271-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-ctl"></a><span data-ttu-id="5c271-111">Uitvoer: CTL [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5c271-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5c271-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="5c271-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5c271-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5c271-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5c271-114">T</span><span class="sxs-lookup"><span data-stu-id="5c271-114">'T</span></span>

<span data-ttu-id="5c271-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="5c271-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="5c271-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5c271-116">See Also</span></span>

- [<span data-ttu-id="5c271-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="5c271-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="5c271-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="5c271-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)