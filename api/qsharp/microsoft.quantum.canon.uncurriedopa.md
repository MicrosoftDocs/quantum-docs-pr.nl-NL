---
uid: Microsoft.Quantum.Canon.UncurriedOpA
title: De functie UncurriedOpA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `A` indicates that the operations are adjointable.
ms.openlocfilehash: feb5da771ee6cb6a750fa76f9ffd8f5a3e0b5734
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840057"
---
# <a name="uncurriedopa-function"></a><span data-ttu-id="5a1f2-102">De functie UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="5a1f2-102">UncurriedOpA function</span></span>

<span data-ttu-id="5a1f2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5a1f2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5a1f2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5a1f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5a1f2-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5a1f2-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="5a1f2-106">De aanpassings functie `A` geeft aan dat de bewerkingen adjointable zijn.</span><span class="sxs-lookup"><span data-stu-id="5a1f2-106">The modifier `A` indicates that the operations are adjointable.</span></span>

```qsharp
function UncurriedOpA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Adj))) : (('T, 'U) => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="5a1f2-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5a1f2-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj"></a><span data-ttu-id="5a1f2-108">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="5a1f2-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5a1f2-109">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="5a1f2-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj"></a><span data-ttu-id="5a1f2-110">Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="5a1f2-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="5a1f2-111">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="5a1f2-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5a1f2-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5a1f2-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5a1f2-113">T</span><span class="sxs-lookup"><span data-stu-id="5a1f2-113">'T</span></span>

<span data-ttu-id="5a1f2-114">Het type van het eerste argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="5a1f2-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="5a1f2-115">' U</span><span class="sxs-lookup"><span data-stu-id="5a1f2-115">'U</span></span>

<span data-ttu-id="5a1f2-116">Het type van het tweede argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="5a1f2-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a1f2-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5a1f2-117">See Also</span></span>

- [<span data-ttu-id="5a1f2-118">Micro soft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="5a1f2-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)