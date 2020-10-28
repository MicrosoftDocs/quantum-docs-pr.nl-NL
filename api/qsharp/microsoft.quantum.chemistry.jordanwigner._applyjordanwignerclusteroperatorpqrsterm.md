---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerClusterOperatorPQRSTerm
title: _ApplyJordanWignerClusterOperatorPQRSTerm bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerClusterOperatorPQRSTerm
qsharp.summary: Applies time-evolution by a cluster operator PQRS term described by a `GeneratorIndex`.
ms.openlocfilehash: 9f5cd58747b16d3fc755c202fd905394fc221d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703539"
---
# <a name="_applyjordanwignerclusteroperatorpqrsterm-operation"></a><span data-ttu-id="24f34-102">_ApplyJordanWignerClusterOperatorPQRSTerm bewerking</span><span class="sxs-lookup"><span data-stu-id="24f34-102">_ApplyJordanWignerClusterOperatorPQRSTerm operation</span></span>

<span data-ttu-id="24f34-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="24f34-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="24f34-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="24f34-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="24f34-105">Past tijd-evolutie toe door een cluster operator PQRS term die wordt beschreven door een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="24f34-105">Applies time-evolution by a cluster operator PQRS term described by a `GeneratorIndex`.</span></span>

```qsharp
operation _ApplyJordanWignerClusterOperatorPQRSTerm (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="24f34-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="24f34-106">Input</span></span>

### <a name="term--generatorindex"></a><span data-ttu-id="24f34-107">term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="24f34-107">term : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="24f34-108">`GeneratorIndex` een PQRS term van een cluster operator vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="24f34-108">`GeneratorIndex` representing a cluster operator PQRS term.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="24f34-109">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="24f34-109">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="24f34-110">Duur van tijd-ontwikkeling.</span><span class="sxs-lookup"><span data-stu-id="24f34-110">Duration of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="24f34-111">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="24f34-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="24f34-112">Qubits van Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="24f34-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="24f34-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="24f34-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

