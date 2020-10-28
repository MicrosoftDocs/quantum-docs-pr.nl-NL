---
uid: Microsoft.Quantum.Canon.AndLadder
title: Bewerking AndLadder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 05a0e8110539742501883fea75ac368d9946164d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705517"
---
# <a name="andladder-operation"></a><span data-ttu-id="5fa8d-102">Bewerking AndLadder</span><span class="sxs-lookup"><span data-stu-id="5fa8d-102">AndLadder operation</span></span>

<span data-ttu-id="5fa8d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5fa8d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5fa8d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5fa8d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5fa8d-105">Hiermee wordt een beheerde "en ladder" uitgevoerd op een REGI ster van doel-qubits.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-105">Performs a controlled "AND ladder" on a register of target qubits.</span></span>

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5fa8d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5fa8d-106">Description</span></span>

<span data-ttu-id="5fa8d-107">Met deze bewerking wordt een trans formatie toegepast die wordt beschreven door de volgende toewijzing van de berekening, $ $ \begin{align} \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1, \dots, y \_ {n-1}} \mapsto \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1 \oplus (x \_ 1 \land x \_ 2), \dots, y \_ {n-1} \oplus (x \_ 1 \land x \_ 2 \land \cdots \land x \_ {n-1}}, \end{align} $ $ waarbij $ \ket{x \_ 1, \dots, x \_ n} $ verwijst naar de berekening basis status van `controls` , en waarbij $ \ket{y \_ 1, \dots, y \_ {n-1}} $ verwijst naar de berekening basis statussen van `targets` .</span><span class="sxs-lookup"><span data-stu-id="5fa8d-107">This operation applies a transformation described by the following mapping of the computational basis, $$ \begin{align} \ket{x\_1, \dots, x\_n} \ket{y\_1, \dots, y\_{n - 1}} \mapsto \ket{x\_1, \dots, x\_n} \ket{ y\_1 \oplus (x\_1 \land x\_2), \dots, y\_{n - 1} \oplus (x\_1 \land x\_2 \land \cdots \land x\_{n - 1} }, \end{align} $$ where $\ket{x\_1, \dots, x\_n}$ refers to the computational basis states of `controls`, and where $\ket{y\_1, \dots, y\_{n - 1}}$ refers to the computational basis states of `targets`.</span></span>

## <a name="input"></a><span data-ttu-id="5fa8d-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="5fa8d-108">Input</span></span>

### <a name="ccnot--ccnotop"></a><span data-ttu-id="5fa8d-109">ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span><span class="sxs-lookup"><span data-stu-id="5fa8d-109">ccnot : [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)</span></span>

<span data-ttu-id="5fa8d-110">De CCNOT-poort die moet worden gebruikt voor de constructie.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-110">The CCNOT gate to use for the construction.</span></span>


### <a name="controls--qubit"></a><span data-ttu-id="5fa8d-111">Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5fa8d-111">controls : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5fa8d-112">Een REGI ster van qubits die als besturings elementen voor de en ladder moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-112">A register of qubits to be used as controls for the and ladder.</span></span>
<span data-ttu-id="5fa8d-113">Met deze bewerking worden de reken kundige basis provincies van `controls` invariant gelaten.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-113">This operation leaves computational basis states of `controls` invariant.</span></span>
<span data-ttu-id="5fa8d-114">De lengte van `controls` moet ten minste 2 zijn en moet gelijk zijn aan een plus de lengte van `targets` .</span><span class="sxs-lookup"><span data-stu-id="5fa8d-114">The length of `controls` must be at least 2, and must be equal to one plus the length of `targets`.</span></span>


### <a name="targets--qubit"></a><span data-ttu-id="5fa8d-115">doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5fa8d-115">targets : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5fa8d-116">De lengte `targets` moet mini maal 1 zijn en gelijk zijn aan de lengte van `controls` min één.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-116">The length of `targets` must be at least 1 and equal to the length of `controls` minus one.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5fa8d-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5fa8d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="5fa8d-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5fa8d-118">Remarks</span></span>

- <span data-ttu-id="5fa8d-119">Wordt gebruikt als onderdeel van <xref:microsoft.quantum.canon.applymulticontrolledc> en <xref:microsoft.quantum.canon.applymulticontrolledca> .</span><span class="sxs-lookup"><span data-stu-id="5fa8d-119">Used as a part of <xref:microsoft.quantum.canon.applymulticontrolledc> and <xref:microsoft.quantum.canon.applymulticontrolledca>.</span></span>
- <span data-ttu-id="5fa8d-120">Zie afbeelding 4,10, sectie 4,3 in Nielsen & Chuang voor uitleg en circuit diagram.</span><span class="sxs-lookup"><span data-stu-id="5fa8d-120">For the explanation and circuit diagram see Figure 4.10, Section 4.3 in Nielsen & Chuang.</span></span>

## <a name="references"></a><span data-ttu-id="5fa8d-121">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="5fa8d-121">References</span></span>

- [<span data-ttu-id="5fa8d-122">*Michael A. Nielsen, Isaac L. Chuang* , Quantum Computation en Quantum Information</span><span class="sxs-lookup"><span data-stu-id="5fa8d-122"> *Michael A. Nielsen , Isaac L. Chuang* , Quantum Computation and Quantum Information </span></span>](http://doi.org/10.1017/CBO9780511976667)