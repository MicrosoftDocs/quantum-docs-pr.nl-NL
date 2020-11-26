---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZTerm_
title: Bewerking _ApplyJordanWignerZTerm_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZTerm_
qsharp.summary: Applies time-evolution by a Z term described by a `GeneratorIndex`.
ms.openlocfilehash: ad9245b0fd79b4f383d1ef8531537b03d78ae9b8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203991"
---
# <a name="_applyjordanwignerzterm_-operation"></a><span data-ttu-id="1f5bd-102">Bewerking _ApplyJordanWignerZTerm_</span><span class="sxs-lookup"><span data-stu-id="1f5bd-102">_ApplyJordanWignerZTerm_ operation</span></span>

<span data-ttu-id="1f5bd-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="1f5bd-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="1f5bd-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="1f5bd-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="1f5bd-105">Past tijd-evolutie toe met een Z-term die wordt beschreven door een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="1f5bd-105">Applies time-evolution by a Z term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="1f5bd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1f5bd-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="1f5bd-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="1f5bd-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="1f5bd-108">`GeneratorIndex` vertegenwoordigt een Z-term.</span><span class="sxs-lookup"><span data-stu-id="1f5bd-108">`GeneratorIndex` representing a Z term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="1f5bd-109">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1f5bd-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1f5bd-110">Duur van tijd-ontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="1f5bd-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="1f5bd-111">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="1f5bd-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="1f5bd-112">Qubits van Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="1f5bd-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1f5bd-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1f5bd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

