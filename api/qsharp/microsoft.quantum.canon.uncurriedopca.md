---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: De functie UncurriedOpCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 910d8a3006a2f217888b791e479e10f9f1a6965e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840044"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="8283d-102">De functie UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="8283d-102">UncurriedOpCA function</span></span>

<span data-ttu-id="8283d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8283d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8283d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8283d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8283d-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8283d-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="8283d-106">De aanpassings functie `CA` geeft aan dat de bewerkingen kunnen worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="8283d-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="8283d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="8283d-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-adj--ctl"></a><span data-ttu-id="8283d-108">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="8283d-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8283d-109">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="8283d-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-adj--ctl"></a><span data-ttu-id="8283d-110">Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8283d-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8283d-111">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="8283d-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8283d-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8283d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8283d-113">T</span><span class="sxs-lookup"><span data-stu-id="8283d-113">'T</span></span>

<span data-ttu-id="8283d-114">Het type van het eerste argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="8283d-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="8283d-115">' U</span><span class="sxs-lookup"><span data-stu-id="8283d-115">'U</span></span>

<span data-ttu-id="8283d-116">Het type van het tweede argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="8283d-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="8283d-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8283d-117">See Also</span></span>

- [<span data-ttu-id="8283d-118">Micro soft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="8283d-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)