---
uid: Microsoft.Quantum.Canon.OperationPowCA
title: De functie OperationPowCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowCA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is controllable and adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 753063452616747309e3e228ce8a702f4378c61f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703911"
---
# <a name="operationpowca-function"></a><span data-ttu-id="d5078-102">De functie OperationPowCA</span><span class="sxs-lookup"><span data-stu-id="d5078-102">OperationPowCA function</span></span>

<span data-ttu-id="d5078-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d5078-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d5078-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d5078-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d5078-105">Hiermee wordt een bewerking naar een stroom gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d5078-105">Raises an operation to a power.</span></span>
<span data-ttu-id="d5078-106">De aanpassings functie `A` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="d5078-106">The modifier `A` indicates that the operation is controllable and adjointable.</span></span>

<span data-ttu-id="d5078-107">Op basis van een bewerking die een Gate $U $ vertegenwoordigt, retourneert een nieuwe bewerking $U ^ m $ voor een Power $m $.</span><span class="sxs-lookup"><span data-stu-id="d5078-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowCA<'T> (op : ('T => Unit is Ctl + Adj), power : Int) : ('T => Unit is Ctl + Adj)
```


## <a name="input"></a><span data-ttu-id="d5078-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d5078-108">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="d5078-109">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) + correctie</span><span class="sxs-lookup"><span data-stu-id="d5078-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="d5078-110">Een bewerking $U $ die aangeeft dat de poort moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="d5078-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="d5078-111">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d5078-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d5078-112">Het aantal keren dat $U $ moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="d5078-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit-ctl--adj"></a><span data-ttu-id="d5078-113">Output: 'T [=> CTL](xref:microsoft.quantum.lang-ref.unit) en correctie</span><span class="sxs-lookup"><span data-stu-id="d5078-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="d5078-114">Een nieuwe bewerking die $U ^ m $ vertegenwoordigt, waarbij $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="d5078-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d5078-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d5078-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d5078-116">T</span><span class="sxs-lookup"><span data-stu-id="d5078-116">'T</span></span>

<span data-ttu-id="d5078-117">Het type van de bewerking die moet worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d5078-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5078-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d5078-118">See Also</span></span>

- [<span data-ttu-id="d5078-119">Micro soft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="d5078-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)