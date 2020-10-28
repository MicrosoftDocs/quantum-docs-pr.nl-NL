---
uid: Microsoft.Quantum.Canon.CurriedOp
title: De functie CurriedOp
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: 13bc3e195d8a4ba26b726f96e4dc6b83da43c3e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704284"
---
# <a name="curriedop-function"></a><span data-ttu-id="c7340-102">De functie CurriedOp</span><span class="sxs-lookup"><span data-stu-id="c7340-102">CurriedOp function</span></span>

<span data-ttu-id="c7340-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c7340-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c7340-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c7340-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c7340-105">Retourneert een Curried-versie van een bewerking op twee invoer.</span><span class="sxs-lookup"><span data-stu-id="c7340-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="c7340-106">Op basis van een bewerking met twee invoer, past deze functie de isomorphism $f van Curry (x, y) \equiv f (x) (y) $ om een bewerking te retour neren van één invoer waarmee een bewerking van één invoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c7340-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="c7340-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c7340-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="c7340-108">op: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7340-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c7340-109">Een bewerking waarvan de invoer een paar is.</span><span class="sxs-lookup"><span data-stu-id="c7340-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="c7340-110">Uitvoer: niet-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c7340-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c7340-111">Een bewerking die het eerste element van een paar accepteert en een bewerking retourneert die de invoer accepteert van het tweede element van de invoer van de oorspronkelijke bewerking.</span><span class="sxs-lookup"><span data-stu-id="c7340-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c7340-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c7340-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c7340-113">T</span><span class="sxs-lookup"><span data-stu-id="c7340-113">'T</span></span>

<span data-ttu-id="c7340-114">Het type van het eerste onderdeel van een functie die op paren is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c7340-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="c7340-115">' U</span><span class="sxs-lookup"><span data-stu-id="c7340-115">'U</span></span>

<span data-ttu-id="c7340-116">Het type van het tweede onderdeel van een functie die op paren is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c7340-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7340-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c7340-117">Remarks</span></span>

<span data-ttu-id="c7340-118">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="c7340-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```