---
uid: Microsoft.Quantum.Canon.CurriedOp
title: De functie CurriedOp
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 6c1917d6f1ee69cb29fed1ab173106af1e206533
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216622"
---
# <a name="curriedop-function"></a><span data-ttu-id="c7fe0-102">De functie CurriedOp</span><span class="sxs-lookup"><span data-stu-id="c7fe0-102">CurriedOp function</span></span>

<span data-ttu-id="c7fe0-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c7fe0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c7fe0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c7fe0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c7fe0-105">Retourneert een Curried-versie van een bewerking op twee invoer.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="c7fe0-106">Op basis van een bewerking met twee invoer, past deze functie de isomorphism $f van Curry (x, y) \equiv f (x) (y) $ om een bewerking te retour neren van één invoer waarmee een bewerking van één invoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="c7fe0-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c7fe0-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="c7fe0-108">op: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7fe0-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c7fe0-109">Een bewerking waarvan de invoer een paar is.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="c7fe0-110">Uitvoer: niet-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7fe0-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c7fe0-111">Een bewerking die het eerste element van een paar accepteert en een bewerking retourneert die de invoer accepteert van het tweede element van de invoer van de oorspronkelijke bewerking.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c7fe0-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c7fe0-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c7fe0-113">T</span><span class="sxs-lookup"><span data-stu-id="c7fe0-113">'T</span></span>

<span data-ttu-id="c7fe0-114">Het type van het eerste onderdeel van een functie die op paren is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="c7fe0-115">' U</span><span class="sxs-lookup"><span data-stu-id="c7fe0-115">'U</span></span>

<span data-ttu-id="c7fe0-116">Het type van het tweede onderdeel van een functie die op paren is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c7fe0-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7fe0-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c7fe0-117">Remarks</span></span>

<span data-ttu-id="c7fe0-118">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="c7fe0-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```