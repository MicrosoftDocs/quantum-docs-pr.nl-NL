---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: De functie UncurriedOpC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 05df99dce8b167f32078ce256748647ceb94d0fe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851991"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="87191-102">De functie UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="87191-102">UncurriedOpC function</span></span>

<span data-ttu-id="87191-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="87191-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="87191-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="87191-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="87191-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="87191-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="87191-106">De aanpassings functie `C` geeft aan dat de bewerkingen kunnen worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="87191-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="87191-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="87191-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="87191-108">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="87191-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="87191-109">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="87191-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-ctl"></a><span data-ttu-id="87191-110">Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="87191-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="87191-111">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="87191-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="87191-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="87191-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="87191-113">T</span><span class="sxs-lookup"><span data-stu-id="87191-113">'T</span></span>

<span data-ttu-id="87191-114">Het type van het eerste argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="87191-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="87191-115">' U</span><span class="sxs-lookup"><span data-stu-id="87191-115">'U</span></span>

<span data-ttu-id="87191-116">Het type van het tweede argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="87191-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="87191-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="87191-117">See Also</span></span>

- [<span data-ttu-id="87191-118">Micro soft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="87191-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)