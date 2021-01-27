---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: De functie ControlledOnBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: 176170cc972ca67b812b84f79cf97ba5418be9b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840808"
---
# <a name="controlledonbitstring-function"></a><span data-ttu-id="d31ed-102">De functie ControlledOnBitString</span><span class="sxs-lookup"><span data-stu-id="d31ed-102">ControlledOnBitString function</span></span>

<span data-ttu-id="d31ed-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d31ed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d31ed-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d31ed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d31ed-105">Retourneert een unitary-bewerking die een Oracle toepast op het doel register als de register status van het besturings element overeenkomt met een opgegeven bitmasker.</span><span class="sxs-lookup"><span data-stu-id="d31ed-105">Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.</span></span>

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="d31ed-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d31ed-106">Description</span></span>

<span data-ttu-id="d31ed-107">De uitvoer van deze functie is een bewerking die kan worden weer gegeven met een unitary-trans formatie $U $, waarmee \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} waarbij $V $ een unitary-trans formatie is die de actie van de `oracle` bewerking vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="d31ed-107">The output of this function is an operation that can be represented by a unitary transformation $U$ such that \begin{align} U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V$ is a unitary transformation that represents the action of the `oracle` operation.</span></span>

## <a name="input"></a><span data-ttu-id="d31ed-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d31ed-108">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="d31ed-109">bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="d31ed-109">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="d31ed-110">De bit-teken reeks voor het beheren van de opgegeven unitary-bewerking op.</span><span class="sxs-lookup"><span data-stu-id="d31ed-110">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit--is-adj--ctl"></a><span data-ttu-id="d31ed-111">Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="d31ed-111">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d31ed-112">De unitary-bewerking die moet worden toegepast op het doel register.</span><span class="sxs-lookup"><span data-stu-id="d31ed-112">The unitary operation to be applied on the target register.</span></span>



## <a name="output--qubitt--unit--is-adj--ctl"></a><span data-ttu-id="d31ed-113">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="d31ed-113">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d31ed-114">Een unitary-bewerking die van toepassing is `oracle` op het doel register als de register status van het besturings element overeenkomt met het bitmasker `bits` .</span><span class="sxs-lookup"><span data-stu-id="d31ed-114">A unitary operation that applies `oracle` on the target register if the control register state corresponds to the bit mask `bits`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d31ed-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d31ed-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d31ed-116">T</span><span class="sxs-lookup"><span data-stu-id="d31ed-116">'T</span></span>



## <a name="example"></a><span data-ttu-id="d31ed-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d31ed-117">Example</span></span>

<span data-ttu-id="d31ed-118">De volgende code fragmenten zijn gelijk:</span><span class="sxs-lookup"><span data-stu-id="d31ed-118">The following code snippets are equivalent:</span></span>

```qsharp
(ControlledOnBitString(bits, oracle))(controlRegister, targetRegister);
```

<span data-ttu-id="d31ed-119">en</span><span class="sxs-lookup"><span data-stu-id="d31ed-119">and</span></span>

```qsharp
within {
    ApplyPauliFromBitString(PauliX, false, bits, controlRegister);
} apply {
    Controlled oracle(controlRegister, targetRegister);
}
```

<span data-ttu-id="d31ed-120">Met de volgende code wordt een status $ \frac {1} {2} (\ket {00} -\ket {01} + \ket {10} + \ket {11} ) voor bereid.</span><span class="sxs-lookup"><span data-stu-id="d31ed-120">The following code prepares a state $\frac{1}{2}(\ket{00} - \ket{01} + \ket{10} + \ket{11})$:</span></span>

```qsharp
using (register = Qubit[2]) {
    ApplyToEach(H, register);
    (ControlledOnBitString([false], Z))(register[0..0], register[1]);
}
```

## <a name="remarks"></a><span data-ttu-id="d31ed-121">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d31ed-121">Remarks</span></span>

<span data-ttu-id="d31ed-122">Het patroon `bits` dat wordt gegeven door, kan korter zijn dan `controlRegister` , in welk geval extra controle qubits worden genegeerd (dat wil zeggen, hetzij niet beheerd op $ \ket {0} $ noch $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="d31ed-122">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="d31ed-123">Als `bits` de lengte langer is dan `controlRegister` , treedt er een fout op.</span><span class="sxs-lookup"><span data-stu-id="d31ed-123">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="d31ed-124">Op basis van een Boole `bits` -matrix en een unitary `oracle` -bewerking is de uitvoer van deze functie een bewerking die de volgende stappen uitvoert:</span><span class="sxs-lookup"><span data-stu-id="d31ed-124">Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function is an operation that performs the following steps:</span></span>

* <span data-ttu-id="d31ed-125">een bewerking Toep assen `X` op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` ;</span><span class="sxs-lookup"><span data-stu-id="d31ed-125">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits`;</span></span>
* <span data-ttu-id="d31ed-126">Toep assen `Controlled oracle` op het besturings element en de doel registers;</span><span class="sxs-lookup"><span data-stu-id="d31ed-126">apply `Controlled oracle` to the control and target registers;</span></span>
* <span data-ttu-id="d31ed-127">pas een `X` bewerking toe op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` opnieuw om het controle register te retour neren naar de oorspronkelijke staat.</span><span class="sxs-lookup"><span data-stu-id="d31ed-127">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits` again to return the control register to the original state.</span></span>

<span data-ttu-id="d31ed-128">De uitvoer van de `Controlled` functor is een speciaal geval `ControlledOnBitString` waar `bits` is gelijk aan `[true, ..., true]` .</span><span class="sxs-lookup"><span data-stu-id="d31ed-128">The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.</span></span>