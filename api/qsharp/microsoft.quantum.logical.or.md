---
uid: Microsoft.Quantum.Logical.Or
title: Or-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 7093d908696a8cfda6b5ef648f9dfafcfac97144
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197123"
---
# <a name="or-function"></a><span data-ttu-id="8791c-102">Or-functie</span><span class="sxs-lookup"><span data-stu-id="8791c-102">Or function</span></span>

<span data-ttu-id="8791c-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="8791c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="8791c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8791c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8791c-105">Retourneert de Booleaanse schei ding van twee waarden.</span><span class="sxs-lookup"><span data-stu-id="8791c-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="8791c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8791c-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="8791c-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8791c-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8791c-108">De eerste waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="8791c-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="8791c-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8791c-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8791c-110">De tweede waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="8791c-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="8791c-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="8791c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="8791c-112">`true` Als en alleen als dat wel of het geval `a` `b` is `true` .</span><span class="sxs-lookup"><span data-stu-id="8791c-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="8791c-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8791c-113">Remarks</span></span>

<span data-ttu-id="8791c-114">In tegens telling tot de `or` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="8791c-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="8791c-115">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="8791c-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a or b;
let x = Or(a, b);
```