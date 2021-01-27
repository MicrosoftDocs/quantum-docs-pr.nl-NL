---
uid: Microsoft.Quantum.Canon.Delayed
title: Vertraagde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 40fcc7d0a178fdb18437b4d6c96542db593347b4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840587"
---
# <a name="delayed-function"></a><span data-ttu-id="5bc73-102">Vertraagde functie</span><span class="sxs-lookup"><span data-stu-id="5bc73-102">Delayed function</span></span>

<span data-ttu-id="5bc73-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5bc73-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5bc73-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5bc73-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5bc73-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="5bc73-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="5bc73-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5bc73-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="5bc73-107">op: 'T> ' U</span><span class="sxs-lookup"><span data-stu-id="5bc73-107">op : 'T => 'U</span></span> 

<span data-ttu-id="5bc73-108">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="5bc73-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="5bc73-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="5bc73-109">arg : 'T</span></span>

<span data-ttu-id="5bc73-110">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="5bc73-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="5bc73-111">Output: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="5bc73-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="5bc73-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="5bc73-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5bc73-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5bc73-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5bc73-114">T</span><span class="sxs-lookup"><span data-stu-id="5bc73-114">'T</span></span>

<span data-ttu-id="5bc73-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="5bc73-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="5bc73-116">' U</span><span class="sxs-lookup"><span data-stu-id="5bc73-116">'U</span></span>

<span data-ttu-id="5bc73-117">Het retour type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="5bc73-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bc73-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5bc73-118">See Also</span></span>

- [<span data-ttu-id="5bc73-119">Micro soft. Quantum. Canon. DelayedC</span><span class="sxs-lookup"><span data-stu-id="5bc73-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="5bc73-120">Micro soft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="5bc73-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="5bc73-121">Micro soft. Quantum. Canon. DelayedCA</span><span class="sxs-lookup"><span data-stu-id="5bc73-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="5bc73-122">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="5bc73-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)