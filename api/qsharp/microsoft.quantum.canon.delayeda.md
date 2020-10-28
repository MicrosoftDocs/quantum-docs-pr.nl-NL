---
uid: Microsoft.Quantum.Canon.DelayedA
title: De functie delayed
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayedA
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 11c11cdd75d80d6324666ef56930f7a522121826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704213"
---
# <a name="delayeda-function"></a><span data-ttu-id="f0b82-102">De functie delayed</span><span class="sxs-lookup"><span data-stu-id="f0b82-102">DelayedA function</span></span>

<span data-ttu-id="f0b82-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f0b82-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f0b82-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0b82-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0b82-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="f0b82-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function DelayedA<'T> (op : ('T => Unit is Adj), arg : 'T) : (Unit => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="f0b82-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f0b82-106">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="f0b82-107">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="f0b82-107">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="f0b82-108">Een bewerking die moet worden toegepast als gevolg van het Toep assen van de retour waarde</span><span class="sxs-lookup"><span data-stu-id="f0b82-108">An operation to be applied as a result of applying return value</span></span>


### <a name="arg--t"></a><span data-ttu-id="f0b82-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="f0b82-109">arg : 'T</span></span>

<span data-ttu-id="f0b82-110">De invoer waarop de bewerking `op` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="f0b82-110">The input to which the operation `op` is applied.</span></span>



## <a name="output--unit--unit-adj"></a><span data-ttu-id="f0b82-111">Output: [eenheids](xref:microsoft.quantum.lang-ref.unit) => [eenheid](xref:microsoft.quantum.lang-ref.unit) correctie</span><span class="sxs-lookup"><span data-stu-id="f0b82-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="f0b82-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="f0b82-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f0b82-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f0b82-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f0b82-114">T</span><span class="sxs-lookup"><span data-stu-id="f0b82-114">'T</span></span>

<span data-ttu-id="f0b82-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="f0b82-115">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0b82-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f0b82-116">See Also</span></span>

- [<span data-ttu-id="f0b82-117">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="f0b82-117">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)
- [<span data-ttu-id="f0b82-118">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="f0b82-118">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)