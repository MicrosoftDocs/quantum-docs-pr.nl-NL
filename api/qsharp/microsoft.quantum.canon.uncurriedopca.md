---
uid: Microsoft.Quantum.Canon.UncurriedOpCA
title: De functie UncurriedOpCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOpCA
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple. The modifier `CA` indicates that the operations are controllable and adjointable.
ms.openlocfilehash: 6a0f2e1b345d0ba3ac5c779c5dc2bfffaf659a0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703712"
---
# <a name="uncurriedopca-function"></a><span data-ttu-id="d650a-102">De functie UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="d650a-102">UncurriedOpCA function</span></span>

<span data-ttu-id="d650a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d650a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d650a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d650a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d650a-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d650a-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>
<span data-ttu-id="d650a-106">De aanpassings functie `CA` geeft aan dat de bewerkingen kunnen worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="d650a-106">The modifier `CA` indicates that the operations are controllable and adjointable.</span></span>

```qsharp
function UncurriedOpCA<'T, 'U> (curriedOp : ('T -> ('U => Unit is Ctl + Adj))) : (('T, 'U) => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="d650a-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="d650a-107">Input</span></span>

### <a name="curriedop--t---u--unit-ctl--adj"></a><span data-ttu-id="d650a-108">curriedOp: 'T-> ' U => [Unit](xref:microsoft.quantum.lang-ref.unit) CTL + ADJ</span><span class="sxs-lookup"><span data-stu-id="d650a-108">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="d650a-109">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d650a-109">A function which returns operations.</span></span>



## <a name="output--tu--unit-ctl--adj"></a><span data-ttu-id="d650a-110">Output: ('T, ' U) => van CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) en correctie</span><span class="sxs-lookup"><span data-stu-id="d650a-110">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="d650a-111">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="d650a-111">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d650a-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d650a-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d650a-113">T</span><span class="sxs-lookup"><span data-stu-id="d650a-113">'T</span></span>

<span data-ttu-id="d650a-114">Het type van het eerste argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="d650a-114">The type of the first argument of a curried function.</span></span>
### <a name="u"></a><span data-ttu-id="d650a-115">' U</span><span class="sxs-lookup"><span data-stu-id="d650a-115">'U</span></span>

<span data-ttu-id="d650a-116">Het type van het tweede argument van een Curried-functie.</span><span class="sxs-lookup"><span data-stu-id="d650a-116">The type of the second argument of a curried function.</span></span>

## <a name="see-also"></a><span data-ttu-id="d650a-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d650a-117">See Also</span></span>

- [<span data-ttu-id="d650a-118">Micro soft. Quantum. Canon. UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="d650a-118">Microsoft.Quantum.Canon.UncurriedOp</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOp)