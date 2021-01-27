---
uid: Microsoft.Quantum.Logical.Conditioned
title: Voorwaarde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: ea3b8eba960acceb6540978c6fccd9f796b0f67d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817290"
---
# <a name="conditioned-function"></a><span data-ttu-id="cf73f-102">Voorwaarde functie</span><span class="sxs-lookup"><span data-stu-id="cf73f-102">Conditioned function</span></span>

<span data-ttu-id="cf73f-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="cf73f-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="cf73f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cf73f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cf73f-105">Retourneert een van twee waarden, afhankelijk van de waarde van een Booleaanse voor waarde.</span><span class="sxs-lookup"><span data-stu-id="cf73f-105">Returns one of two values, depending on the value of a Boolean condition.</span></span>

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a><span data-ttu-id="cf73f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cf73f-106">Input</span></span>

### <a name="condition--bool"></a><span data-ttu-id="cf73f-107">voor waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cf73f-107">condition : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cf73f-108">Een voor waarde die wordt gebruikt om te bepalen welke invoer wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="cf73f-108">A condition used to control which input is returned.</span></span>


### <a name="iftrue--t"></a><span data-ttu-id="cf73f-109">ifTrue: 'T</span><span class="sxs-lookup"><span data-stu-id="cf73f-109">ifTrue : 'T</span></span>

<span data-ttu-id="cf73f-110">De waarde die moet worden geretourneerd `condition` Wanneer `true` .</span><span class="sxs-lookup"><span data-stu-id="cf73f-110">The value to be returned when `condition` is `true`.</span></span>


### <a name="iffalse--t"></a><span data-ttu-id="cf73f-111">ifFalse: 'T</span><span class="sxs-lookup"><span data-stu-id="cf73f-111">ifFalse : 'T</span></span>

<span data-ttu-id="cf73f-112">De waarde die moet worden geretourneerd `condition` Wanneer `false` .</span><span class="sxs-lookup"><span data-stu-id="cf73f-112">The value to be returned when `condition` is `false`.</span></span>



## <a name="output--t"></a><span data-ttu-id="cf73f-113">Uitvoer: 'T</span><span class="sxs-lookup"><span data-stu-id="cf73f-113">Output : 'T</span></span>

<span data-ttu-id="cf73f-114">`ifTrue` Als dat zo `condition` is `true` , en `ifFalse` anders.</span><span class="sxs-lookup"><span data-stu-id="cf73f-114">`ifTrue` if `condition` is `true`, and `ifFalse` otherwise.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cf73f-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="cf73f-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cf73f-116">T</span><span class="sxs-lookup"><span data-stu-id="cf73f-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="cf73f-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cf73f-117">Remarks</span></span>

<span data-ttu-id="cf73f-118">In tegens telling tot de `?|` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.</span><span class="sxs-lookup"><span data-stu-id="cf73f-118">Unlike the `?|` operator, this function does not short-circuit, such that both inputs are fully evaluated.</span></span>

<span data-ttu-id="cf73f-119">Tot het korte circuit, zijn de volgende equivalenten:</span><span class="sxs-lookup"><span data-stu-id="cf73f-119">Up to short-circuiting behavior, the following are equivalent:</span></span>

```qsharp
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```