---
uid: Microsoft.Quantum.Canon.OperationPowA
title: De functie OperationPowA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPowA
qsharp.summary: >-
  Raises an operation to a power. The modifier `A` indicates that the operation is adjointable.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 66df354c6de7e48624712276882759043b78466c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703929"
---
# <a name="operationpowa-function"></a><span data-ttu-id="5da61-102">De functie OperationPowA</span><span class="sxs-lookup"><span data-stu-id="5da61-102">OperationPowA function</span></span>

<span data-ttu-id="5da61-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5da61-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5da61-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5da61-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5da61-105">Hiermee wordt een bewerking naar een stroom gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="5da61-105">Raises an operation to a power.</span></span>
<span data-ttu-id="5da61-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="5da61-106">The modifier `A` indicates that the operation is adjointable.</span></span>

<span data-ttu-id="5da61-107">Op basis van een bewerking die een Gate $U $ vertegenwoordigt, retourneert een nieuwe bewerking $U ^ m $ voor een Power $m $.</span><span class="sxs-lookup"><span data-stu-id="5da61-107">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPowA<'T> (op : ('T => Unit is Adj), power : Int) : ('T => Unit is Adj)
```


## <a name="input"></a><span data-ttu-id="5da61-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="5da61-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="5da61-109">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="5da61-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5da61-110">Een bewerking $U $ die aangeeft dat de poort moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="5da61-110">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="5da61-111">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5da61-111">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5da61-112">Het aantal keren dat $U $ moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="5da61-112">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit-adj"></a><span data-ttu-id="5da61-113">Output: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="5da61-113">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="5da61-114">Een nieuwe bewerking die $U ^ m $ vertegenwoordigt, waarbij $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="5da61-114">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5da61-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5da61-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5da61-116">T</span><span class="sxs-lookup"><span data-stu-id="5da61-116">'T</span></span>

<span data-ttu-id="5da61-117">Het type van de bewerking die moet worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="5da61-117">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="5da61-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5da61-118">See Also</span></span>

- [<span data-ttu-id="5da61-119">Micro soft. Quantum. Canon. OperationPow</span><span class="sxs-lookup"><span data-stu-id="5da61-119">Microsoft.Quantum.Canon.OperationPow</span></span>](xref:Microsoft.Quantum.Canon.OperationPow)