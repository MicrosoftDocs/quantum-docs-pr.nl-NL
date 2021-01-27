---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedHpqTerm
title: _JWOptimizedHpqTerm bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedHpqTerm
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: b008315ded7cabc085e6d5da8f646e92914bf743
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854816"
---
# <a name="_jwoptimizedhpqterm-operation"></a><span data-ttu-id="e99ff-102">_JWOptimizedHpqTerm bewerking</span><span class="sxs-lookup"><span data-stu-id="e99ff-102">_JWOptimizedHpqTerm operation</span></span>

<span data-ttu-id="e99ff-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e99ff-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="e99ff-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e99ff-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="e99ff-105">Past tijd-evolutie toe met een PQ-term die wordt beschreven door een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="e99ff-105">Applies time-evolution by a PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _JWOptimizedHpqTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="e99ff-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e99ff-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="e99ff-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e99ff-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e99ff-108">`GeneratorIndex` een PQ-term vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="e99ff-108">`GeneratorIndex` representing a PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="e99ff-109">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e99ff-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e99ff-110">Duur van tijd-ontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="e99ff-110">Duration of time-evolution.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="e99ff-111">parityQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e99ff-111">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e99ff-112">Qubit die het teken van de tijd ontwikkeling bepaalt.</span><span class="sxs-lookup"><span data-stu-id="e99ff-112">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="e99ff-113">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="e99ff-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="e99ff-114">Qubits van Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="e99ff-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e99ff-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e99ff-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

