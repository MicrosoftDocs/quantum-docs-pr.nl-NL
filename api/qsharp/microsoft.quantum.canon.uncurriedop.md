---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: De functie UncurriedOp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: cad508f166d4af805cb98cd21a0260d9babb6a4c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204637"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="5cdf5-102">De functie UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="5cdf5-102">UncurriedOp function</span></span>

<span data-ttu-id="5cdf5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5cdf5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5cdf5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5cdf5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5cdf5-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5cdf5-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="5cdf5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5cdf5-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="5cdf5-107">curriedOp: 'T-> ' U =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5cdf5-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5cdf5-108">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="5cdf5-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="5cdf5-109">Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5cdf5-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5cdf5-110">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="5cdf5-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5cdf5-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5cdf5-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5cdf5-112">T</span><span class="sxs-lookup"><span data-stu-id="5cdf5-112">'T</span></span>

<span data-ttu-id="5cdf5-113">Het type van de eerste invoer voor een Curried-bewerking.</span><span class="sxs-lookup"><span data-stu-id="5cdf5-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="5cdf5-114">' U</span><span class="sxs-lookup"><span data-stu-id="5cdf5-114">'U</span></span>

<span data-ttu-id="5cdf5-115">Het type van de tweede invoer voor een Curried-bewerking.</span><span class="sxs-lookup"><span data-stu-id="5cdf5-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="5cdf5-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5cdf5-116">See Also</span></span>

- [<span data-ttu-id="5cdf5-117">Micro soft. Quantum. Canon. UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="5cdf5-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="5cdf5-118">Micro soft. Quantum. Canon. UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="5cdf5-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="5cdf5-119">Micro soft. Quantum. Canon. UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="5cdf5-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)