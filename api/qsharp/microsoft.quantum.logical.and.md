---
uid: Microsoft.Quantum.Logical.And
title: En-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 6c405bdb4182cc7f32bd04952dec25a974c03445
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849231"
---
# <a name="and-function"></a><span data-ttu-id="84bbf-102">En-functie</span><span class="sxs-lookup"><span data-stu-id="84bbf-102">And function</span></span>

<span data-ttu-id="84bbf-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="84bbf-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="84bbf-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="84bbf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="84bbf-105">Retourneert de Booleaanse combi natie van twee waarden.</span><span class="sxs-lookup"><span data-stu-id="84bbf-105">Returns the Boolean conjunction of two values.</span></span>

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="84bbf-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="84bbf-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="84bbf-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="84bbf-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="84bbf-108">De eerste waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="84bbf-108">The first value to be considered.</span></span>


### <a name="b--bool"></a><span data-ttu-id="84bbf-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="84bbf-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="84bbf-110">De tweede waarde die moet worden overwogen.</span><span class="sxs-lookup"><span data-stu-id="84bbf-110">The second value to be considered.</span></span>



## <a name="output--bool"></a><span data-ttu-id="84bbf-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="84bbf-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="84bbf-112">`true` Als en alleen als `a` en `b` beide `true` .</span><span class="sxs-lookup"><span data-stu-id="84bbf-112">`true` if and only if `a` and `b` are both `true`.</span></span>

## <a name="remarks"></a><span data-ttu-id="84bbf-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="84bbf-113">Remarks</span></span>

<span data-ttu-id="84bbf-114">In tegens telling tot de `and` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="84bbf-114">Unlike the `and` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="84bbf-115">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="84bbf-115">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = a and b;
let x = And(a, b);
```