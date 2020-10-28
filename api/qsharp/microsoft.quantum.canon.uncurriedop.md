---
uid: Microsoft.Quantum.Canon.UncurriedOp
title: De functie UncurriedOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: UncurriedOp
qsharp.summary: Given a function which returns operations, returns a new operation which takes both inputs as a tuple.
ms.openlocfilehash: 359c0b2a9dd56445fb39fadc6580809dd9fbf628
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703725"
---
# <a name="uncurriedop-function"></a><span data-ttu-id="9dee0-102">De functie UncurriedOp</span><span class="sxs-lookup"><span data-stu-id="9dee0-102">UncurriedOp function</span></span>

<span data-ttu-id="9dee0-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9dee0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9dee0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9dee0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9dee0-105">Op basis van een functie die bewerkingen retourneert, retourneert een nieuwe bewerking waarbij beide invoer als een tuple worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="9dee0-105">Given a function which returns operations, returns a new operation which takes both inputs as a tuple.</span></span>

```qsharp
function UncurriedOp<'T, 'U> (curriedOp : ('T -> ('U => Unit))) : (('T, 'U) => Unit)
```


## <a name="input"></a><span data-ttu-id="9dee0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9dee0-106">Input</span></span>

### <a name="curriedop--t---u--unit"></a><span data-ttu-id="9dee0-107">curriedOp: 'T-> ' U =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9dee0-107">curriedOp : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="9dee0-108">Een functie waarmee bewerkingen worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="9dee0-108">A function which returns operations.</span></span>



## <a name="output--tu--unit"></a><span data-ttu-id="9dee0-109">Output: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9dee0-109">Output : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="9dee0-110">Een nieuwe bewerking `op` , die `op(t, u)` gelijk is aan `(curriedOp(t))(u)` .</span><span class="sxs-lookup"><span data-stu-id="9dee0-110">A new operation `op` such that `op(t, u)` is equivalent to `(curriedOp(t))(u)`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9dee0-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9dee0-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9dee0-112">T</span><span class="sxs-lookup"><span data-stu-id="9dee0-112">'T</span></span>

<span data-ttu-id="9dee0-113">Het type van de eerste invoer voor een Curried-bewerking.</span><span class="sxs-lookup"><span data-stu-id="9dee0-113">The type of the first input to a curried operation.</span></span>
### <a name="u"></a><span data-ttu-id="9dee0-114">' U</span><span class="sxs-lookup"><span data-stu-id="9dee0-114">'U</span></span>

<span data-ttu-id="9dee0-115">Het type van de tweede invoer voor een Curried-bewerking.</span><span class="sxs-lookup"><span data-stu-id="9dee0-115">The type of the second input to a curried operation.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dee0-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9dee0-116">See Also</span></span>

- [<span data-ttu-id="9dee0-117">Micro soft. Quantum. Canon. UncurriedOpC</span><span class="sxs-lookup"><span data-stu-id="9dee0-117">Microsoft.Quantum.Canon.UncurriedOpC</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpC)
- [<span data-ttu-id="9dee0-118">Micro soft. Quantum. Canon. UncurriedOpA</span><span class="sxs-lookup"><span data-stu-id="9dee0-118">Microsoft.Quantum.Canon.UncurriedOpA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpA)
- [<span data-ttu-id="9dee0-119">Micro soft. Quantum. Canon. UncurriedOpCA</span><span class="sxs-lookup"><span data-stu-id="9dee0-119">Microsoft.Quantum.Canon.UncurriedOpCA</span></span>](xref:Microsoft.Quantum.Canon.UncurriedOpCA)