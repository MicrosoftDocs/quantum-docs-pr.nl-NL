---
uid: Microsoft.Quantum.Logical.Conditioned
title: Voorwaarde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707053"
---
# <a name="conditioned-function"></a><span data-ttu-id="4dd1d-102">Voorwaarde functie</span><span class="sxs-lookup"><span data-stu-id="4dd1d-102">Conditioned function</span></span>

<span data-ttu-id="4dd1d-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="4dd1d-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="4dd1d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4dd1d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4dd1d-105">Retourneert een van twee waarden, afhankelijk van de waarde van een Booleaanse voor waarde.</span><span class="sxs-lookup"><span data-stu-id="4dd1d-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="4dd1d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4dd1d-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="4dd1d-107">voor waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4dd1d-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4dd1d-108">Een voor waarde die wordt gebruikt om te bepalen welke invoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="4dd1d-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="4dd1d-109">ifTrue: 'T</span><span class="sxs-lookup"><span data-stu-id="4dd1d-109">ifTrue : 'T</span></span>

<span data-ttu-id="4dd1d-110">De waarde die moet worden geretourneerd `condition` Wanneer `true` .</span><span class="sxs-lookup"><span data-stu-id="4dd1d-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="4dd1d-111">ifFalse: 'T</span><span class="sxs-lookup"><span data-stu-id="4dd1d-111">ifFalse : 'T</span></span>

<span data-ttu-id="4dd1d-112">De waarde die moet worden geretourneerd `condition` Wanneer `false` .</span><span class="sxs-lookup"><span data-stu-id="4dd1d-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="4dd1d-113">Uitvoer: 'T</span><span class="sxs-lookup"><span data-stu-id="4dd1d-113">Output : 'T</span></span>

<span data-ttu-id="4dd1d-114">`ifTrue` Als dat zo `condition` is `true` , en `ifFalse` anders.</span><span class="sxs-lookup"><span data-stu-id="4dd1d-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4dd1d-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="4dd1d-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4dd1d-116">T</span><span class="sxs-lookup"><span data-stu-id="4dd1d-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="4dd1d-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4dd1d-117">Remarks</span></span>

<span data-ttu-id="4dd1d-118">In tegens telling tot de `?|` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="4dd1d-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="4dd1d-119">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="4dd1d-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```