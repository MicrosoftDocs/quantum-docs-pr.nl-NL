---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: De functie UncurriedOpC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: f3e5ecf3f7df0393dfbb948f064c27505f04cfcf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703713"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="5069e-102">De functie UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="5069e-102">UncurriedOpC function</span></span>

<span data-ttu-id="5069e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5069e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5069e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5069e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5069e-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5069e-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="5069e-106">De aanpassings functie `C` geeft aan dat de bewerkingen kunnen worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="5069e-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="5069e-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="5069e-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl"></a><span data-ttu-id="5069e-108">curriedOp: 'T-> ' U => CTL van de [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5069e-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5069e-109">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="5069e-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl"></a><span data-ttu-id="5069e-110">Output: ('T, ' U) => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5069e-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="5069e-111">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="5069e-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5069e-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5069e-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5069e-113">T</span><span class="sxs-lookup"><span data-stu-id="5069e-113">'T</span></span>

<span data-ttu-id="5069e-114">Het type van het eerste argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="5069e-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="5069e-115">' U</span><span class="sxs-lookup"><span data-stu-id="5069e-115">'U</span></span>

<span data-ttu-id="5069e-116">Het type van het tweede argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="5069e-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="5069e-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5069e-117">See Also</span></span>

- [<span data-ttu-id="5069e-118">Micro soft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="5069e-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)