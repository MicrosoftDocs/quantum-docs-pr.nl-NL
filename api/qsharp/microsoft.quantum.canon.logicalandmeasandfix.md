---
uid: Microsoft.Quantum.Canon.LogicalANDMeasAndFix
title: Bewerking LogicalANDMeasAndFix
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: LogicalANDMeasAndFix
qsharp.summary: Computes the logical AND of multiple qubits.
ms.openlocfilehash: 86e4b9a8c6ed5f4f56db0ceefc8051d34e911c4c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704029"
---
# <a name="logicalandmeasandfix-operation"></a><span data-ttu-id="bf29b-102">Bewerking LogicalANDMeasAndFix</span><span class="sxs-lookup"><span data-stu-id="bf29b-102">LogicalANDMeasAndFix operation</span></span>

<span data-ttu-id="bf29b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bf29b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bf29b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bf29b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bf29b-105">Hiermee worden de logische en van meerdere qubits berekend.</span><span class="sxs-lookup"><span data-stu-id="bf29b-105">Computes the logical AND of multiple qubits.</span></span>

```qsharp
operation LogicalANDMeasAndFix (ctrlRegister : Qubit[], target : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="bf29b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bf29b-106">Input</span></span>

### <a name="ctrlregister--qubit"></a><span data-ttu-id="bf29b-107">ctrlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bf29b-107">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bf29b-108">Qubits invoer naar de meervoudige invoer en poort.</span><span class="sxs-lookup"><span data-stu-id="bf29b-108">Qubits input to the multiple-input AND gate.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="bf29b-109">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bf29b-109">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bf29b-110">Qubit waarop de uitvoer van en wordt geschreven.</span><span class="sxs-lookup"><span data-stu-id="bf29b-110">Qubit on which output of AND is written to.</span></span> <span data-ttu-id="bf29b-111">Hierbij wordt ervan uitgegaan dat deze altijd begint in de $ \ket {0} $-status.</span><span class="sxs-lookup"><span data-stu-id="bf29b-111">This is assumed to always start in the $\ket{0}$ state.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bf29b-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bf29b-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bf29b-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="bf29b-113">Remarks</span></span>

<span data-ttu-id="bf29b-114">Wanneer `ctrlRegister` heeft precies $2 $ qubits, is dit gelijk aan de `CCNOT` bewerking, maar met een fase $e ^ {i \ pi/2} $ op $ \ket {001} $ en $-e ^ {i \ pi/2} $ op $ \ket {101} $ en $ \ket {011} $.</span><span class="sxs-lookup"><span data-stu-id="bf29b-114">When `ctrlRegister` has exactly $2$ qubits, this is equivalent to the `CCNOT` operation but phase with a phase $e^{i\Pi/2}$ on $\ket{001}$ and $-e^{i\Pi/2}$ on $\ket{101}$ and $\ket{011}$.</span></span>
<span data-ttu-id="bf29b-115">De adjoint is ook een aanpak-en reparatie methode die de inverse van de oorspronkelijke bewerking alleen in speciale gevallen (zie verwijzingen) is, maar die minder T-poorten gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bf29b-115">The Adjoint is also measure-and-fixup approach that is the inverse of the original operation only in special cases (see references), but uses fewer T-gates.</span></span>

## <a name="references"></a><span data-ttu-id="bf29b-116">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="bf29b-116">References</span></span>

- [<span data-ttu-id="bf29b-117">*Craig Gidney* , 1709,06648</span><span class="sxs-lookup"><span data-stu-id="bf29b-117"> *Craig Gidney* , 1709.06648</span></span>](https://arxiv.org/abs/1709.06648)