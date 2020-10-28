---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Bewerking ApplyControlledOnInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: c8ea76946143967de4b6ac65986a1c4407ecb633
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705429"
---
# <a name="applycontrolledonint-operation"></a><span data-ttu-id="a9db4-102">Bewerking ApplyControlledOnInt</span><span class="sxs-lookup"><span data-stu-id="a9db4-102">ApplyControlledOnInt operation</span></span>

<span data-ttu-id="a9db4-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a9db4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a9db4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a9db4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a9db4-105">Past een unitary-bewerking op het doel register toe als de register status van het besturings element overeenkomt met een opgegeven positief geheel getal.</span><span class="sxs-lookup"><span data-stu-id="a9db4-105">Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.</span></span>

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit
```


## <a name="input"></a><span data-ttu-id="a9db4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a9db4-106">Input</span></span>

### <a name="numberstate--int"></a><span data-ttu-id="a9db4-107">numberState: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a9db4-107">numberState : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a9db4-108">Een niet-negatief geheel getal waarop de bewerking `oracle` moet worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="a9db4-108">A nonnegative integer on which the operation `oracle` should be controlled.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="a9db4-109">Oracle: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="a9db4-109">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="a9db4-110">Een unitary-bewerking die moet worden beheerd.</span><span class="sxs-lookup"><span data-stu-id="a9db4-110">A unitary operation to be controlled.</span></span>


### <a name="controlregister--qubit"></a><span data-ttu-id="a9db4-111">controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a9db4-111">controlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a9db4-112">Een Quantum registratie waarmee de toepassing van wordt bepaald `oracle` .</span><span class="sxs-lookup"><span data-stu-id="a9db4-112">A quantum register that controls application of `oracle`.</span></span>


### <a name="targetregister--t"></a><span data-ttu-id="a9db4-113">targetRegister: 'T</span><span class="sxs-lookup"><span data-stu-id="a9db4-113">targetRegister : 'T</span></span>

<span data-ttu-id="a9db4-114">Een REGI ster waarop moet worden toegepast `oracle` .</span><span class="sxs-lookup"><span data-stu-id="a9db4-114">A register on which to apply `oracle`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a9db4-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a9db4-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a9db4-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a9db4-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a9db4-117">T</span><span class="sxs-lookup"><span data-stu-id="a9db4-117">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="a9db4-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a9db4-118">Remarks</span></span>

<span data-ttu-id="a9db4-119">De waarde van `numberState` wordt geïnterpreteerd met een little-endian-code ring.</span><span class="sxs-lookup"><span data-stu-id="a9db4-119">The value of `numberState` is interpreted using a little-endian encoding.</span></span>

<span data-ttu-id="a9db4-120">`numberState` mag Maxi maal $2 ^ \texttt{Length (controlRegister)}-$1 zijn.</span><span class="sxs-lookup"><span data-stu-id="a9db4-120">`numberState` must be at most $2^\texttt{Length(controlRegister)} - 1$.</span></span>
<span data-ttu-id="a9db4-121">`numberState = 537`Betekent bijvoorbeeld dat `oracle` wordt toegepast als en alleen als `controlRegister` de status $ \ket {537} $.</span><span class="sxs-lookup"><span data-stu-id="a9db4-121">For example, `numberState = 537` means that `oracle` is applied if and only if `controlRegister` is in the state $\ket{537}$.</span></span>