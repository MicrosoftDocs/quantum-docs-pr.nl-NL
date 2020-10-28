---
uid: Microsoft.Quantum.Logical.Or
title: Or-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 98a416229386461b241d087b7ae95f078f8be70a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706516"
---
# <a name="or-function"></a><span data-ttu-id="12873-102">Or-functie</span><span class="sxs-lookup"><span data-stu-id="12873-102">Or function</span></span>

<span data-ttu-id="12873-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="12873-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="12873-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12873-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12873-105">Retourneert de Booleaanse schei ding van twee waarden.</span><span class="sxs-lookup"><span data-stu-id="12873-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="12873-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="12873-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="12873-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="12873-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="12873-108">De eerste waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="12873-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="12873-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="12873-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="12873-110">De tweede waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="12873-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="12873-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="12873-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="12873-112">`true` Als en alleen als dat wel of het geval `a` `b` is `true` .</span><span class="sxs-lookup"><span data-stu-id="12873-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="12873-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="12873-113">Remarks</span></span>

<span data-ttu-id="12873-114">In tegens telling tot de `or` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="12873-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="12873-115">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="12873-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a or b;
let x = Or(a, b);
```