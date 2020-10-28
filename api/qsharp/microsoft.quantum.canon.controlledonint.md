---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: De functie ControlledOnInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 4c48f3257f91fc50040d02cae7c2f7bdf87ea7c5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704309"
---
# <a name="controlledonint-function"></a><span data-ttu-id="57343-102">De functie ControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="57343-102">ControlledOnInt function</span></span>

<span data-ttu-id="57343-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="57343-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="57343-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="57343-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="57343-105">Retourneert een unitary-operator die een Oracle toepast op het doel register als de register status van het besturings element overeenkomt met een opgegeven positief geheel getal.</span><span class="sxs-lookup"><span data-stu-id="57343-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="57343-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="57343-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="57343-107">numberState: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="57343-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="57343-108">Positief geheel getal.</span><span class="sxs-lookup"><span data-stu-id="57343-108">Positive integer.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="57343-109">Oracle: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="57343-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="57343-110">Unitary-operator.</span><span class="sxs-lookup"><span data-stu-id="57343-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="57343-111">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="57343-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="57343-112">Een unitary-operator die van toepassing is `oracle` op het doel register als de register status van het besturings element overeenkomt met de nummer status `numberState` .</span><span class="sxs-lookup"><span data-stu-id="57343-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="57343-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="57343-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="57343-114">T</span><span class="sxs-lookup"><span data-stu-id="57343-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="57343-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="57343-115">Remarks</span></span>

<span data-ttu-id="57343-116">De waarde van `numberState` wordt geïnterpreteerd met een little-endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="57343-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>