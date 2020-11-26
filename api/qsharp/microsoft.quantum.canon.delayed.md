---
uid: Microsoft.Quantum.Canon.Delayed
title: Vertraagde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delayed
qsharp.summary: Returns an operation that applies given operation with given argument.
ms.openlocfilehash: 863c63d0c1a50339e9d5b9fbe4729932b2706f32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216452"
---
# <a name="delayed-function"></a><span data-ttu-id="33826-102">Vertraagde functie</span><span class="sxs-lookup"><span data-stu-id="33826-102">Delayed function</span></span>

<span data-ttu-id="33826-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="33826-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="33826-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="33826-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="33826-105">Retourneert een bewerking die een opgegeven bewerking toepast op het opgegeven argument.</span><span class="sxs-lookup"><span data-stu-id="33826-105">Returns an operation that applies given operation with given argument.</span></span>

```qsharp
function Delayed<'T, 'U> (op : ('T => 'U), arg : 'T) : (Unit => 'U)
```


## <a name="input"></a><span data-ttu-id="33826-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="33826-106">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="33826-107">op: 'T> ' U</span><span class="sxs-lookup"><span data-stu-id="33826-107">op : 'T => 'U</span></span> 

<span data-ttu-id="33826-108">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="33826-108">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="33826-109">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="33826-109">arg : 'T</span></span>

<span data-ttu-id="33826-110">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="33826-110">The input to which the operation is applied.</span></span>



## <a name="output--unit--u"></a><span data-ttu-id="33826-111">Output: [Unit](xref:microsoft.quantum.lang-ref.unit) => ' U</span><span class="sxs-lookup"><span data-stu-id="33826-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit) => 'U</span></span> 

<span data-ttu-id="33826-112">Een nieuwe bewerking die van toepassing is op `op` invoer `arg`</span><span class="sxs-lookup"><span data-stu-id="33826-112">A new operation which applies `op` with input `arg`</span></span>

## <a name="type-parameters"></a><span data-ttu-id="33826-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="33826-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="33826-114">T</span><span class="sxs-lookup"><span data-stu-id="33826-114">'T</span></span>

<span data-ttu-id="33826-115">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="33826-115">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="33826-116">' U</span><span class="sxs-lookup"><span data-stu-id="33826-116">'U</span></span>

<span data-ttu-id="33826-117">Het retour type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="33826-117">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="33826-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="33826-118">See Also</span></span>

- [<span data-ttu-id="33826-119">Micro soft. Quantum. Canon. DelayedC</span><span class="sxs-lookup"><span data-stu-id="33826-119">Microsoft.Quantum.Canon.DelayedC</span></span>](xref:Microsoft.Quantum.Canon.DelayedC)
- [<span data-ttu-id="33826-120">Micro soft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="33826-120">Microsoft.Quantum.Canon.DelayedA</span></span>](xref:Microsoft.Quantum.Canon.DelayedA)
- [<span data-ttu-id="33826-121">Micro soft. Quantum. Canon. DelayedCA</span><span class="sxs-lookup"><span data-stu-id="33826-121">Microsoft.Quantum.Canon.DelayedCA</span></span>](xref:Microsoft.Quantum.Canon.DelayedCA)
- [<span data-ttu-id="33826-122">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="33826-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)