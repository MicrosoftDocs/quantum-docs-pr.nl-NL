---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Bewerking MeasureStabilizerGenerators
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: a3f48ff24a39d13a57f7a144e21d4e41bb8a8b49
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702452"
---
# <a name="measurestabilizergenerators-operation"></a><span data-ttu-id="e04a2-102">Bewerking MeasureStabilizerGenerators</span><span class="sxs-lookup"><span data-stu-id="e04a2-102">MeasureStabilizerGenerators operation</span></span>

<span data-ttu-id="e04a2-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="e04a2-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="e04a2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e04a2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e04a2-105">Meet de opgegeven set met Generators van een stabilisatoren groep.</span><span class="sxs-lookup"><span data-stu-id="e04a2-105">Measures the given set of generators of a stabilizer group.</span></span>

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a><span data-ttu-id="e04a2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e04a2-106">Input</span></span>

### <a name="stabilizergroup--pauli"></a><span data-ttu-id="e04a2-107">stabilizerGroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="e04a2-107">stabilizerGroup : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="e04a2-108">Een matrix met multiqubit Pauli-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="e04a2-108">An array of multiqubit Pauli operators.</span></span>
<span data-ttu-id="e04a2-109">Een voor beeld: `stabilizerGroup[0]` een lijst met Qubit Pauli-matrices, het tensor-product van een stabilisatorer-generator.</span><span class="sxs-lookup"><span data-stu-id="e04a2-109">For example, `stabilizerGroup[0]` is a list of single-qubit Pauli matrices, the tensor product of which is a stabilizer generator.</span></span>


### <a name="logicalregister--logicalregister"></a><span data-ttu-id="e04a2-110">logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="e04a2-110">logicalRegister : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="e04a2-111">Een matrix met qubits waarvan de stabilisatorer code is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="e04a2-111">An array of qubits where the stabilizer code is defined.</span></span>


### <a name="gadget--pauliqubit--__invalidresult__"></a><span data-ttu-id="e04a2-112">Gadget: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="e04a2-112">gadget : ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __invalid<Result>__</span></span> 

<span data-ttu-id="e04a2-113">Een bewerking die aangeeft hoe een multiqubit Pauli-operator moet worden gemeten.</span><span class="sxs-lookup"><span data-stu-id="e04a2-113">An operation that specifies how to measure a multiqubit Pauli operator.</span></span>



## <a name="output--syndrome"></a><span data-ttu-id="e04a2-114">Uitvoer: [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span><span class="sxs-lookup"><span data-stu-id="e04a2-114">Output : [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)</span></span>

<span data-ttu-id="e04a2-115">Het resultaat van metingen.</span><span class="sxs-lookup"><span data-stu-id="e04a2-115">The result of measurements.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04a2-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e04a2-116">Remarks</span></span>

<span data-ttu-id="e04a2-117">Hiermee wordt niet gecontroleerd of de opgegeven set generatoren werkt.</span><span class="sxs-lookup"><span data-stu-id="e04a2-117">This does not check if the given set of generators are commuting.</span></span>
<span data-ttu-id="e04a2-118">Als ze niet werken, kan het resultaat van metingen wille keurig zijn.</span><span class="sxs-lookup"><span data-stu-id="e04a2-118">If they are not commuting, the result of measurements may be arbitrary.</span></span>