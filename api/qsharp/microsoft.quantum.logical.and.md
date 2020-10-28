---
uid: Microsoft.Quantum.Logical.And
title: En-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: cc81f650216c4db219a79c4fe89a42447a4e95b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707061"
---
# <a name="and-function"></a><span data-ttu-id="6768d-102">En-functie</span><span class="sxs-lookup"><span data-stu-id="6768d-102">And function</span></span>

<span data-ttu-id="6768d-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="6768d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="6768d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6768d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6768d-105">Retourneert de Booleaanse combi natie van twee waarden.</span><span class="sxs-lookup"><span data-stu-id="6768d-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="6768d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6768d-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="6768d-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6768d-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6768d-108">De eerste waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="6768d-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="6768d-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6768d-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6768d-110">De tweede waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="6768d-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="6768d-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="6768d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="6768d-112">`true` Als en alleen als `a` en `b` beide `true` .</span><span class="sxs-lookup"><span data-stu-id="6768d-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6768d-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6768d-113">Remarks</span></span>

<span data-ttu-id="6768d-114">In tegens telling tot de `and` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="6768d-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="6768d-115">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="6768d-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = a and b;
let x = And(a, b);
```