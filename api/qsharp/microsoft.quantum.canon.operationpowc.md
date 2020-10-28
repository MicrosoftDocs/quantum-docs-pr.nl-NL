---
uid: Microsoft.Quantum.Canon.OperationPowC
title: De functie OperationPowC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowC
qsharp.summary: >-
  Raises an operation to a power. The modifier `C` indicates that the operation is controllable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: f3c51410fb7c091385b64a1c4c99b3972d5055b1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703917"
---
# <a name="operationpowc-function"></a><span data-ttu-id="45f00-102">De functie OperationPowC</span><span class="sxs-lookup"><span data-stu-id="45f00-102">OperationPowC function</span></span>

<span data-ttu-id="45f00-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="45f00-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="45f00-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="45f00-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="45f00-105">Hiermee wordt een bewerking naar een stroom gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="45f00-105">Raises an operation to a power.</span></span>
<span data-ttu-id="45f00-106">De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="45f00-106">The modifier `C` indicates that the operation is controllable.</span></span>

<span data-ttu-id="45f00-107">Op basis van een bewerking die een Gate $U $ vertegenwoordigt, retourneert een nieuwe bewerking $U ^ m $ voor een Power $m $.</span><span class="sxs-lookup"><span data-stu-id="45f00-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowC<'T> (op : ('T => Unit is Ctl), power : Int) : ('T => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="45f00-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="45f00-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="45f00-109">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="45f00-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="45f00-110">Een bewerking $U $ die aangeeft dat de poort moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="45f00-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="45f00-111">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="45f00-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="45f00-112">Het aantal keren dat $U $ moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="45f00-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit-ctl"></a><span data-ttu-id="45f00-113">Output: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="45f00-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="45f00-114">Een nieuwe bewerking die $U ^ m $ vertegenwoordigt, waarbij $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="45f00-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="45f00-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="45f00-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="45f00-116">T</span><span class="sxs-lookup"><span data-stu-id="45f00-116">'T</span></span>

<span data-ttu-id="45f00-117">Het type van de bewerking die moet worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="45f00-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="45f00-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="45f00-118">See Also</span></span>

- [<span data-ttu-id="45f00-119">Micro soft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="45f00-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)