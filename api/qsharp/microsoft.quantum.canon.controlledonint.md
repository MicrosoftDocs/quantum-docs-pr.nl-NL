---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: De functie ControlledOnInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 6c7f46c44f2a2427f702e463195f26660cb4fca1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840791"
---
# <a name="controlledonint-function"></a><span data-ttu-id="8d7b8-102">De functie ControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="8d7b8-102">ControlledOnInt function</span></span>

<span data-ttu-id="8d7b8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8d7b8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8d7b8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d7b8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d7b8-105">Retourneert een unitary-operator die een Oracle toepast op het doel register als de register status van het besturings element overeenkomt met een opgegeven positief geheel getal.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-105">Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="8d7b8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8d7b8-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="8d7b8-107">numberState: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8d7b8-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8d7b8-108">Positief geheel getal.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-108">Positive integer.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="8d7b8-109">Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="8d7b8-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8d7b8-110">Unitary-operator.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-110">Unitary operator.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="8d7b8-111">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8d7b8-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8d7b8-112">Een unitary-operator die van toepassing is `oracle` op het doel register als de register status van het besturings element overeenkomt met de nummer status `numberState` .</span><span class="sxs-lookup"><span data-stu-id="8d7b8-112">A unitary operator that applies `oracle` on the target register if the control register state corresponds to the number state `numberState`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8d7b8-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8d7b8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8d7b8-114">T</span><span class="sxs-lookup"><span data-stu-id="8d7b8-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="8d7b8-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8d7b8-115">Remarks</span></span>

<span data-ttu-id="8d7b8-116">De waarde van `numberState` wordt geïnterpreteerd met een little-endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-116">The value of `numberState` is interpreted using a little-endian encoding.</span></span>