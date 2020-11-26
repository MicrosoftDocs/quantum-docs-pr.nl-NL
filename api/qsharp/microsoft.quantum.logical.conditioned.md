---
uid: Microsoft.Quantum.Logical.Conditioned
title: Voorwaarde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: c0f55d4db95ad1f0d2b7f291cbc6ba8ae704cb81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198483"
---
# <a name="conditioned-function"></a><span data-ttu-id="95fc5-102">Voorwaarde functie</span><span class="sxs-lookup"><span data-stu-id="95fc5-102">Conditioned function</span></span>

<span data-ttu-id="95fc5-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="95fc5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="95fc5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="95fc5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="95fc5-105">Retourneert een van twee waarden, afhankelijk van de waarde van een Booleaanse voor waarde.</span><span class="sxs-lookup"><span data-stu-id="95fc5-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="95fc5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="95fc5-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="95fc5-107">voor waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="95fc5-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="95fc5-108">Een voor waarde die wordt gebruikt om te bepalen welke invoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="95fc5-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="95fc5-109">ifTrue: 'T</span><span class="sxs-lookup"><span data-stu-id="95fc5-109">ifTrue : 'T</span></span>

<span data-ttu-id="95fc5-110">De waarde die moet worden geretourneerd `condition` Wanneer `true` .</span><span class="sxs-lookup"><span data-stu-id="95fc5-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="95fc5-111">ifFalse: 'T</span><span class="sxs-lookup"><span data-stu-id="95fc5-111">ifFalse : 'T</span></span>

<span data-ttu-id="95fc5-112">De waarde die moet worden geretourneerd `condition` Wanneer `false` .</span><span class="sxs-lookup"><span data-stu-id="95fc5-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="95fc5-113">Uitvoer: 'T</span><span class="sxs-lookup"><span data-stu-id="95fc5-113">Output : 'T</span></span>

<span data-ttu-id="95fc5-114">`ifTrue` Als dat zo `condition` is `true` , en `ifFalse` anders.</span><span class="sxs-lookup"><span data-stu-id="95fc5-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="95fc5-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="95fc5-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="95fc5-116">T</span><span class="sxs-lookup"><span data-stu-id="95fc5-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="95fc5-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="95fc5-117">Remarks</span></span>

<span data-ttu-id="95fc5-118">In tegens telling tot de `?|` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="95fc5-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="95fc5-119">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="95fc5-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```