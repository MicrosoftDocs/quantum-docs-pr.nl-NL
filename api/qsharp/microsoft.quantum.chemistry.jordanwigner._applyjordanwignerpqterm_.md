---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQTerm_
title: Bewerking _ApplyJordanWignerPQTerm_
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQTerm_
qsharp.summary: Applies time-evolution by a PQ term described by a `GeneratorIndex`.
ms.openlocfilehash: 6e7d3e422ea751371eeb3111dce88acc6eaf3b62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851713"
---
# <a name="_applyjordanwignerpqterm_-operation"></a><span data-ttu-id="9fa7c-102">Bewerking _ApplyJordanWignerPQTerm_</span><span class="sxs-lookup"><span data-stu-id="9fa7c-102">_ApplyJordanWignerPQTerm_ operation</span></span>

<span data-ttu-id="9fa7c-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="9fa7c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="9fa7c-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="9fa7c-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="9fa7c-105">Past tijd-evolutie toe met een PQ-term die wordt beschreven door een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="9fa7c-105">Applies time-evolution by a PQ term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerPQTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, extraParityQubits : Qubit[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="9fa7c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9fa7c-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="9fa7c-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="9fa7c-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="9fa7c-108">`GeneratorIndex` een PQ-term vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-108">`GeneratorIndex` representing a PQ term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="9fa7c-109">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9fa7c-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9fa7c-110">Duur van tijd-ontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-110">Duration of time-evolution.</span></span>


### <a name="extraparityqubits--qubit"></a><span data-ttu-id="9fa7c-111">extraParityQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9fa7c-111">extraParityQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9fa7c-112">Optionele pariteits qubits die het teken van de tijd evolutie spie gelen.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-112">Optional parity qubits that flip the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="9fa7c-113">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9fa7c-113">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9fa7c-114">Qubits van Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="9fa7c-114">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9fa7c-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9fa7c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

