---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Bewerking ApplyControlledOnInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3dd17e6bc913e84941a6b81f134e60536a4c4122
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219002"
---
# <a name="applycontrolledonint-operation"></a><span data-ttu-id="ff3f5-102">Bewerking ApplyControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="ff3f5-102">ApplyControlledOnInt operation</span></span>

<span data-ttu-id="ff3f5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ff3f5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ff3f5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ff3f5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ff3f5-105">Past een unitary-bewerking op het doel register toe als de register status van het besturings element overeenkomt met een opgegeven positief geheel getal.</span><span class="sxs-lookup"><span data-stu-id="ff3f5-105">Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ff3f5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ff3f5-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="ff3f5-107">numberState: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ff3f5-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ff3f5-108">Een niet-negatief geheel getal waarop de bewerking `oracle` moet worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="ff3f5-108">A nonnegative integer on which the operation `oracle` should be controlled.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="ff3f5-109">Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="ff3f5-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ff3f5-110">Een unitary-bewerking die moet worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="ff3f5-110">A unitary operation to be controlled.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="ff3f5-111">controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ff3f5-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ff3f5-112">Een Quantum registratie waarmee de toepassing van wordt bepaald `oracle` .</span><span class="sxs-lookup"><span data-stu-id="ff3f5-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="ff3f5-113">targetRegister: 'T</span><span class="sxs-lookup"><span data-stu-id="ff3f5-113">targetRegister : 'T</span></span>

<span data-ttu-id="ff3f5-114">Een REGI ster waarop moet worden toegepast `oracle` .</span><span class="sxs-lookup"><span data-stu-id="ff3f5-114">A register on which to apply `oracle`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ff3f5-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ff3f5-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ff3f5-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ff3f5-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ff3f5-117">T</span><span class="sxs-lookup"><span data-stu-id="ff3f5-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="ff3f5-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ff3f5-118">Remarks</span></span>

<span data-ttu-id="ff3f5-119">De waarde van `numberState` wordt geïnterpreteerd met een little-endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="ff3f5-119">The value of `numberState` is interpreted using a little-endian encoding.</span></span>

<span data-ttu-id="ff3f5-120">`numberState` mag Maxi maal $2 ^ \texttt{Length (controlRegister)}-$1 zijn.</span><span class="sxs-lookup"><span data-stu-id="ff3f5-120">`numberState` must be at most $2^\texttt{Length(controlRegister)} - 1$.</span></span>
<span data-ttu-id="ff3f5-121">`numberState = 537`Betekent bijvoorbeeld dat `oracle` wordt toegepast als en alleen als `controlRegister` de status $ \ket {537} $.</span><span class="sxs-lookup"><span data-stu-id="ff3f5-121">For example, `numberState = 537` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{537}$.</span></span>