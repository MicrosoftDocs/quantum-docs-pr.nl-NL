---
uid: Microsoft.Quantum.Canon.ControlledOnBitString
title: De functie ControlledOnBitString
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnBitString
qsharp.summary: Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.
ms.openlocfilehash: ca5a6e116eff187060f7a160e42836b170f0362d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704325"
---
# <a name="controlledonbitstring-function"></a><span data-ttu-id="cef4f-102">De functie ControlledOnBitString</span><span class="sxs-lookup"><span data-stu-id="cef4f-102">ControlledOnBitString function</span></span>

<span data-ttu-id="cef4f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cef4f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cef4f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cef4f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cef4f-105">Retourneert een unitary-bewerking die een Oracle toepast op het doel register als de register status van het besturings element overeenkomt met een opgegeven bitmasker.</span><span class="sxs-lookup"><span data-stu-id="cef4f-105">Returns a unitary operation that applies an oracle on the target register if the control register state corresponds to a specified bit mask.</span></span>

```qsharp
function ControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="cef4f-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="cef4f-106">Description</span></span>

<span data-ttu-id="cef4f-107">De uitvoer van deze functie is een bewerking die kan worden weer gegeven met een unitary-trans formatie $U $, waarmee \begin{align} U \ket{b_0 b_1 \cdots b_ {n-1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_ {n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_ {n-1}) = \texttt{bits} \\ \\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} waarbij $V $ een unitary-trans formatie is die de actie van de `oracle` bewerking vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="cef4f-107">The output of this function is an operation that can be represented by a unitary transformation $U$ such that \begin{align} U \ket{b_0 b_1 \cdots b_{n - 1}} \ket{\psi} = \ket{b_0 b_1 \cdots b_{n-1}} \otimes \begin{cases} V \ket{\psi} & \textrm{if} (b_0 b_1 \cdots b_{n - 1}) = \texttt{bits} \\\\ \ket{\psi} & \textrm{otherwise} \end{cases}, \end{align} where $V$ is a unitary transformation that represents the action of the `oracle` operation.</span></span>

## <a name="input"></a><span data-ttu-id="cef4f-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="cef4f-108">Input</span></span>

### <a name="bits--bool"></a><span data-ttu-id="cef4f-109">bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]</span><span class="sxs-lookup"><span data-stu-id="cef4f-109">bits : [Bool](xref:microsoft.quantum.lang-ref.bool)[]</span></span>

<span data-ttu-id="cef4f-110">De bit-teken reeks voor het beheren van de opgegeven unitary-bewerking op.</span><span class="sxs-lookup"><span data-stu-id="cef4f-110">The bit string to control the given unitary operation on.</span></span>


### <a name="oracle--t--unit-adj--ctl"></a><span data-ttu-id="cef4f-111">Oracle: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="cef4f-111">oracle : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="cef4f-112">De unitary-bewerking die moet worden toegepast op het doel register.</span><span class="sxs-lookup"><span data-stu-id="cef4f-112">The unitary operation to be applied on the target register.</span></span>



## <a name="output--qubitt--unit-adj--ctl"></a><span data-ttu-id="cef4f-113">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="cef4f-113">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],'T) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="cef4f-114">Een unitary-bewerking die van toepassing is `oracle` op het doel register als de register status van het besturings element overeenkomt met het bitmasker `bits` .</span><span class="sxs-lookup"><span data-stu-id="cef4f-114">A unitary operation that applies `oracle` on the target register if the control register state corresponds to the bit mask `bits`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cef4f-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="cef4f-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cef4f-116">T</span><span class="sxs-lookup"><span data-stu-id="cef4f-116">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="cef4f-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cef4f-117">Remarks</span></span>

<span data-ttu-id="cef4f-118">Het patroon `bits` dat wordt gegeven door, kan korter zijn dan `controlRegister` , in welk geval extra controle qubits worden genegeerd (dat wil zeggen, hetzij niet beheerd op $ \ket {0} $ noch $ \ket {1} $).</span><span class="sxs-lookup"><span data-stu-id="cef4f-118">The pattern given by `bits` may be shorter than `controlRegister`, in which case additional control qubits are ignored (that is, neither controlled on $\ket{0}$ nor $\ket{1}$).</span></span>
<span data-ttu-id="cef4f-119">Als `bits` de lengte langer is dan `controlRegister` , treedt er een fout op.</span><span class="sxs-lookup"><span data-stu-id="cef4f-119">If `bits` is longer than `controlRegister`, an error is raised.</span></span>

<span data-ttu-id="cef4f-120">Op basis van een Boole `bits` -matrix en een unitary `oracle` -bewerking is de uitvoer van deze functie een bewerking die de volgende stappen uitvoert:</span><span class="sxs-lookup"><span data-stu-id="cef4f-120">Given a Boolean array `bits` and a unitary operation `oracle`, the output of this function is an operation that performs the following steps:</span></span>

* <span data-ttu-id="cef4f-121">een bewerking Toep assen `X` op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` ;</span><span class="sxs-lookup"><span data-stu-id="cef4f-121">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits`;</span></span>
* <span data-ttu-id="cef4f-122">Toep assen `Controlled oracle` op het besturings element en de doel registers;</span><span class="sxs-lookup"><span data-stu-id="cef4f-122">apply `Controlled oracle` to the control and target registers;</span></span>
* <span data-ttu-id="cef4f-123">pas een `X` bewerking toe op elke qubit van het controle register dat overeenkomt met `false` het element van de `bits` opnieuw om het controle register te retour neren naar de oorspronkelijke staat.</span><span class="sxs-lookup"><span data-stu-id="cef4f-123">apply an `X` operation to each qubit of the control register that corresponds to `false` element of the `bits` again to return the control register to the original state.</span></span>

<span data-ttu-id="cef4f-124">De uitvoer van de `Controlled` functor is een speciaal geval `ControlledOnBitString` waar `bits` is gelijk aan `[true, ..., true]` .</span><span class="sxs-lookup"><span data-stu-id="cef4f-124">The output of the `Controlled` functor is a special case of `ControlledOnBitString` where `bits` is equal to `[true, ..., true]`.</span></span>