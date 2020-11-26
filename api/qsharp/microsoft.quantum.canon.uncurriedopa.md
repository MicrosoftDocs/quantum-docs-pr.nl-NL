---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: De functie UncurriedOpA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: e535d017d2665ddb76e5f422e18b8656c73171c6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204620"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="71860-102">De functie UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="71860-102">UncurriedOpA function</span></span>

<span data-ttu-id="71860-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="71860-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="71860-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71860-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71860-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71860-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="71860-106">De aanpassings functie `A` geeft aan dat de bewerkingen adjointable zijn.</span><span class="sxs-lookup"><span data-stu-id="71860-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="71860-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="71860-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="71860-108">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="71860-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="71860-109">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="71860-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj"></a><span data-ttu-id="71860-110">Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="71860-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="71860-111">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="71860-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="71860-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="71860-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="71860-113">T</span><span class="sxs-lookup"><span data-stu-id="71860-113">'T</span></span>

<span data-ttu-id="71860-114">Het type van het eerste argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="71860-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="71860-115">' U</span><span class="sxs-lookup"><span data-stu-id="71860-115">'U</span></span>

<span data-ttu-id="71860-116">Het type van het tweede argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="71860-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="71860-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="71860-117">See Also</span></span>

- [<span data-ttu-id="71860-118">Micro soft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="71860-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)