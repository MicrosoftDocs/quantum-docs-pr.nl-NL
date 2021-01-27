---
uid: Microsoft.Quantum.Canon.OperationPow
title: De functie OperationPow
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: OperationPow
qsharp.summary: >-
  Raises an operation to a power.

  That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.
ms.openlocfilehash: 9ed0d32c084f183527cac0586ad699417f51df29
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852385"
---
# <a name="operationpow-function"></a><span data-ttu-id="ddb75-102">De functie OperationPow</span><span class="sxs-lookup"><span data-stu-id="ddb75-102">OperationPow function</span></span>

<span data-ttu-id="ddb75-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ddb75-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ddb75-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ddb75-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ddb75-105">Hiermee wordt een bewerking naar een stroom gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ddb75-105">Raises an operation to a power.</span></span>

<span data-ttu-id="ddb75-106">Op basis van een bewerking die een Gate $U $ vertegenwoordigt, retourneert een nieuwe bewerking $U ^ m $ voor een Power $m $.</span><span class="sxs-lookup"><span data-stu-id="ddb75-106">That is, given an operation representing a gate $U$, returns a new operation $U^m$ for a power $m$.</span></span>

```qsharp
function OperationPow<'T> (op : ('T => Unit), power : Int) : ('T => Unit)
```


## <a name="input"></a><span data-ttu-id="ddb75-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="ddb75-107">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="ddb75-108">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ddb75-108">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ddb75-109">Een bewerking $U $ die aangeeft dat de poort moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="ddb75-109">An operation $U$ representing the gate to be repeated.</span></span>


### <a name="power--int"></a><span data-ttu-id="ddb75-110">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ddb75-110">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ddb75-111">Het aantal keren dat $U $ moet worden herhaald.</span><span class="sxs-lookup"><span data-stu-id="ddb75-111">The number of times that $U$ is to be repeated.</span></span>



## <a name="output--t--unit"></a><span data-ttu-id="ddb75-112">Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ddb75-112">Output : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ddb75-113">Een nieuwe bewerking die $U ^ m $ vertegenwoordigt, waarbij $m = \texttt{Power} $.</span><span class="sxs-lookup"><span data-stu-id="ddb75-113">A new operation representing $U^m$, where $m = \texttt{power}$.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="ddb75-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ddb75-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ddb75-115">T</span><span class="sxs-lookup"><span data-stu-id="ddb75-115">'T</span></span>

<span data-ttu-id="ddb75-116">Het type van de bewerking die moet worden ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ddb75-116">The type of the operation to be powered.</span></span>

## <a name="see-also"></a><span data-ttu-id="ddb75-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ddb75-117">See Also</span></span>

- [<span data-ttu-id="ddb75-118">Micro soft. Quantum. Canon. OperationPowC</span><span class="sxs-lookup"><span data-stu-id="ddb75-118">Microsoft.Quantum.Canon.OperationPowC</span></span>](xref:Microsoft.Quantum.Canon.OperationPowC)
- [<span data-ttu-id="ddb75-119">Micro soft. Quantum. Canon. OperationPowA</span><span class="sxs-lookup"><span data-stu-id="ddb75-119">Microsoft.Quantum.Canon.OperationPowA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowA)
- [<span data-ttu-id="ddb75-120">Micro soft. Quantum. Canon. OperationPowCA</span><span class="sxs-lookup"><span data-stu-id="ddb75-120">Microsoft.Quantum.Canon.OperationPowCA</span></span>](xref:Microsoft.Quantum.Canon.OperationPowCA)