---
uid: Microsoft.Quantum.Logical.Or
title: Or-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 4a29b7684b28b904b43ccceb8e63280999690349
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848468"
---
# <a name="or-function"></a><span data-ttu-id="b6e3e-102">Or-functie</span><span class="sxs-lookup"><span data-stu-id="b6e3e-102">Or function</span></span>

<span data-ttu-id="b6e3e-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="b6e3e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="b6e3e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b6e3e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b6e3e-105">Retourneert de Booleaanse schei ding van twee waarden.</span><span class="sxs-lookup"><span data-stu-id="b6e3e-105">Returns the Boolean disjunction of two values.</span></span>

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="b6e3e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b6e3e-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="b6e3e-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b6e3e-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b6e3e-108">De eerste waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="b6e3e-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="b6e3e-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b6e3e-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b6e3e-110">De tweede waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="b6e3e-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b6e3e-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b6e3e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b6e3e-112">`true` Als en alleen als dat wel of het geval `a` `b` is `true` .</span><span class="sxs-lookup"><span data-stu-id="b6e3e-112">`true` if and only if either `a` or `b` are `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6e3e-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b6e3e-113">Remarks</span></span>

<span data-ttu-id="b6e3e-114">In tegens telling tot de `or` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="b6e3e-114">Unlike the `or` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="b6e3e-115">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="b6e3e-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a or b;
let x = Or(a, b);
```