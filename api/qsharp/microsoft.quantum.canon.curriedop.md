---
uid: Microsoft.Quantum.Canon.CurriedOp
title: De functie CurriedOp
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CurriedOp
qsharp.summary: >-
  Returns a curried version of an operation on two inputs.

  That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.
ms.openlocfilehash: f811347d65a6460690163e9df631979c906bd89f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840767"
---
# <a name="curriedop-function"></a><span data-ttu-id="d326d-102">De functie CurriedOp</span><span class="sxs-lookup"><span data-stu-id="d326d-102">CurriedOp function</span></span>

<span data-ttu-id="d326d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d326d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d326d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d326d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d326d-105">Retourneert een Curried-versie van een bewerking op twee invoer.</span><span class="sxs-lookup"><span data-stu-id="d326d-105">Returns a curried version of an operation on two inputs.</span></span>

<span data-ttu-id="d326d-106">Op basis van een bewerking met twee invoer, past deze functie de isomorphism $f van Curry (x, y) \equiv f (x) (y) $ om een bewerking te retour neren van één invoer waarmee een bewerking van één invoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="d326d-106">That is, given an operation with two inputs, this function applies Curry's isomorphism $f(x, y) \equiv f(x)(y)$ to return an operation of one input which returns an operation of one input.</span></span>

```qsharp
function CurriedOp<'T, 'U> (op : (('T, 'U) => Unit)) : ('T -> ('U => Unit))
```


## <a name="input"></a><span data-ttu-id="d326d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="d326d-107">Input</span></span>

### <a name="op--tu--unit"></a><span data-ttu-id="d326d-108">op: ('T, ' U) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d326d-108">op : ('T,'U) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d326d-109">Een bewerking waarvan de invoer een paar is.</span><span class="sxs-lookup"><span data-stu-id="d326d-109">An operation whose input is a pair.</span></span>



## <a name="output--t---u--unit"></a><span data-ttu-id="d326d-110">Uitvoer: niet-> ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d326d-110">Output : 'T -> 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d326d-111">Een bewerking die het eerste element van een paar accepteert en een bewerking retourneert die de invoer accepteert van het tweede element van de invoer van de oorspronkelijke bewerking.</span><span class="sxs-lookup"><span data-stu-id="d326d-111">An operation which accepts the first element of a pair and returns an operation which accepts as its input the second element of the original operation's input.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d326d-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d326d-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d326d-113">T</span><span class="sxs-lookup"><span data-stu-id="d326d-113">'T</span></span>

<span data-ttu-id="d326d-114">Het type van het eerste onderdeel van een functie die op paren is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d326d-114">The type of the first component of a function defined on pairs.</span></span>
### <a name="u"></a><span data-ttu-id="d326d-115">' U</span><span class="sxs-lookup"><span data-stu-id="d326d-115">'U</span></span>

<span data-ttu-id="d326d-116">Het type van het tweede onderdeel van een functie die op paren is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="d326d-116">The type of the second component of a function defined on pairs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d326d-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d326d-117">Remarks</span></span>

<span data-ttu-id="d326d-118">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="d326d-118">The following are equivalent:</span></span>

```qsharp
op(x, y);

let curried = CurriedOp(op);
let partial = curried(x);
partial(y);
```