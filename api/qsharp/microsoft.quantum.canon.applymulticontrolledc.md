---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledC
title: Bewerking ApplyMultiControlledC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledC
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: bf6b78cd18a827a9a4fd9d61dfd4d240de3503e9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844870"
---
# <a name="applymulticontrolledc-operation"></a><span data-ttu-id="42d50-102">Bewerking ApplyMultiControlledC</span><span class="sxs-lookup"><span data-stu-id="42d50-102">ApplyMultiControlledC operation</span></span>

<span data-ttu-id="42d50-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="42d50-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="42d50-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42d50-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42d50-105">Past een door vermenigvuldigde versie van een gecontroleerde bewerking toe.</span><span class="sxs-lookup"><span data-stu-id="42d50-105">Applies a multiply controlled version of a singly controlled operation.</span></span>
<span data-ttu-id="42d50-106">De aanpassings functie `C` geeft aan dat de bewerking met één qubit kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="42d50-106">The modifier `C` indicates that the single-qubit operation is controllable.</span></span>

```qsharp
operation ApplyMultiControlledC (singlyControlledOp : (Qubit[] => Unit), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="42d50-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="42d50-107">Input</span></span>

### <a name="singlycontrolledop--qubit--unit"></a><span data-ttu-id="42d50-108">singlyControlledOp: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42d50-108">singlyControlledOp : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="42d50-109">Een bewerking die wordt beheerd op één Qubit.</span><span class="sxs-lookup"><span data-stu-id="42d50-109">An operation controlled on a single qubit.</span></span>
<span data-ttu-id="42d50-110">Voor de eerste Qubit in het argument van de bewerking wordt aangenomen dat het een besturings element is en wordt aangenomen dat de rest qubits is.</span><span class="sxs-lookup"><span data-stu-id="42d50-110">The first qubit in the argument of the operation is assumed to be a control and the rest are assumed to be target qubits.</span></span>
<span data-ttu-id="42d50-111">`ApplyMultiControlled` roept altijd `singlyControlledOp` een lengte van ten minste 1 aan.</span><span class="sxs-lookup"><span data-stu-id="42d50-111">`ApplyMultiControlled` always calls `singlyControlledOp` with an argument of length at least 1.</span></span>


### <a name="ccnot--ccnotop"></a><span data-ttu-id="42d50-112">ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="42d50-112">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="42d50-113">De Controlled-NOT-Gate die voor de bouw moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="42d50-113">The controlled-controlled-NOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="42d50-114">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="42d50-114">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="42d50-115">De qubits waarop moet `singlyControlledOp` worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="42d50-115">The qubits that `singlyControlledOp` is to be controlled on.</span></span>
<span data-ttu-id="42d50-116">De lengte van `controls` moet mini maal 1 zijn.</span><span class="sxs-lookup"><span data-stu-id="42d50-116">The length of `controls` must be at least 1.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="42d50-117">doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="42d50-117">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="42d50-118">De doel-qubits die op wordt uitgevoerd `singlyControlledOp` .</span><span class="sxs-lookup"><span data-stu-id="42d50-118">The target qubits that `singlyControlledOp` acts upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="42d50-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42d50-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="42d50-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="42d50-120">Remarks</span></span>

<span data-ttu-id="42d50-121">Deze bewerking maakt alleen gebruik van schone ancilla qubits.</span><span class="sxs-lookup"><span data-stu-id="42d50-121">This operation uses only clean ancilla qubits.</span></span>

<span data-ttu-id="42d50-122">Zie afbeelding 4,10, sectie 4,3 in Nielsen & Chuang voor uitleg en circuit diagram.</span><span class="sxs-lookup"><span data-stu-id="42d50-122">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang</span></span>

## <a name="references"></a><span data-ttu-id="42d50-123">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="42d50-123">References</span></span>

- [<span data-ttu-id="42d50-124">*Michael A. Nielsen, Isaac L. Chuang*, Quantum Computation en Quantum Information</span><span class="sxs-lookup"><span data-stu-id="42d50-124"> *Michael A. Nielsen , Isaac L. Chuang*, Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a><span data-ttu-id="42d50-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="42d50-125">See Also</span></span>

- [<span data-ttu-id="42d50-126">Micro soft. Quantum. Canon. ApplyMultiControlledCA</span><span class="sxs-lookup"><span data-stu-id="42d50-126">Microsoft.Quantum.Canon.ApplyMultiControlledCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyMultiControlledCA)