---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Bewerking ApplyMultiControlledCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 5662efe0dc6f665206b8773596bf885ce631413c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705196"
---
# <a name="applymulticontrolledca-operation"></a><span data-ttu-id="57f72-102">Bewerking ApplyMultiControlledCA</span><span class="sxs-lookup"><span data-stu-id="57f72-102">ApplyMultiControlledCA operation</span></span>

<span data-ttu-id="57f72-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="57f72-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="57f72-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="57f72-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="57f72-105">Past een door vermenigvuldigde versie van een gecontroleerde bewerking toe.</span><span class="sxs-lookup"><span data-stu-id="57f72-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="57f72-106">De aanpassings functie `CA` geeft aan dat de bewerking met één qubit kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="57f72-106">The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="57f72-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="57f72-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit-adj"></a><span data-ttu-id="57f72-108">singlyControlledOp: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="57f72-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="57f72-109">Een bewerking die wordt beheerd op één Qubit.</span><span class="sxs-lookup"><span data-stu-id="57f72-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="57f72-110">Voor de eerste Qubit in het argument van de bewerking wordt aangenomen dat het om een besturings element gaat en wordt aangenomen dat de rest qubits is.</span><span class="sxs-lookup"><span data-stu-id="57f72-110">The first qubit in the argument of the operation assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="57f72-111">`ApplyMultiControlled` roept altijd `singlyControlledOp` een lengte van ten minste 1 aan.</span><span class="sxs-lookup"><span data-stu-id="57f72-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="57f72-112">ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="57f72-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="57f72-113">De Controlled-NOT-Gate die voor de bouw moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="57f72-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="57f72-114">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="57f72-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="57f72-115">De qubits waarop moet `singlyControlledOp` worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="57f72-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="57f72-116">De lengte van `controls` moet mini maal 1 zijn.</span><span class="sxs-lookup"><span data-stu-id="57f72-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="57f72-117">doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="57f72-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="57f72-118">De doel-qubits die op wordt uitgevoerd `singlyControlledOp` .</span><span class="sxs-lookup"><span data-stu-id="57f72-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="57f72-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="57f72-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="57f72-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="57f72-120">Remarks</span></span>

<span data-ttu-id="57f72-121">Deze bewerking maakt alleen gebruik van schone ancilla qubits.</span><span class="sxs-lookup"><span data-stu-id="57f72-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="57f72-122">Zie afbeelding 4,10, sectie 4,3 in Nielsen & Chuang voor uitleg en circuit diagram.</span><span class="sxs-lookup"><span data-stu-id="57f72-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="57f72-123">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="57f72-123">References</span></span>

- [<span data-ttu-id="57f72-124">*Michael A. Nielsen, Isaac L. Chuang* , Quantum Computation en Quantum Information</span><span class="sxs-lookup"><span data-stu-id="57f72-124"> *Michael A. Nielsen , Isaac L. Chuang* , Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="57f72-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="57f72-125">See Also</span></span>

- [<span data-ttu-id="57f72-126">Micro soft. Quantum. Canon. ApplyMultiControlledC</span><span class="sxs-lookup"><span data-stu-id="57f72-126">Microsoft.Quantum.Canon.ApplyMultiControlledC</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)