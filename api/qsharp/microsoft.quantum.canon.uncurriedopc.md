---
uid: Microsoft.Quantum.Canon.UncurriedOpC
title: De functie UncurriedOpC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpC
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `C` indicates that the operations are controllable.
ms.openlocfilehash: 35be5425fcd76eae9e0a6fde6a689a5db00da52f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204586"
---
# <a name="uncurriedopc-function"></a><span data-ttu-id="0f70d-102">De functie UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="0f70d-102">UncurriedOpC function</span></span>

<span data-ttu-id="0f70d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0f70d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0f70d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0f70d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0f70d-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0f70d-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="0f70d-106">De aanpassings functie `C` geeft aan dat de bewerkingen kunnen worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="0f70d-106">The modifier `C` indicates that the operations are controllable.</span></span>

```qsharp
function UncurriedOpC<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl))) : (('T, 'U) => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="0f70d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="0f70d-107">Input</span></span>

### <a name="curriedop--t---u--unit--is-ctl"></a><span data-ttu-id="0f70d-108">curriedOp: 'T-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="0f70d-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="0f70d-109">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="0f70d-109">A function which returns operations.</span></span>



## <a name="output--tu--unit--is-ctl"></a><span data-ttu-id="0f70d-110">Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="0f70d-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="0f70d-111">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="0f70d-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0f70d-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="0f70d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0f70d-113">T</span><span class="sxs-lookup"><span data-stu-id="0f70d-113">'T</span></span>

<span data-ttu-id="0f70d-114">Het type van het eerste argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="0f70d-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="0f70d-115">' U</span><span class="sxs-lookup"><span data-stu-id="0f70d-115">'U</span></span>

<span data-ttu-id="0f70d-116">Het type van het tweede argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="0f70d-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f70d-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0f70d-117">See Also</span></span>

- [<span data-ttu-id="0f70d-118">Micro soft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="0f70d-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)