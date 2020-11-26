---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Bewerking ContinuousPhaseEstimationIteration
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 3c0f6cf084311598346b25dd7028e290946cd87f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216282"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="f19c5-102">Bewerking ContinuousPhaseEstimationIteration</span><span class="sxs-lookup"><span data-stu-id="f19c5-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="f19c5-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="f19c5-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="f19c5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f19c5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f19c5-105">Voert een enkele herhaling van een iteratieve fase van een herhaald (klassiek) Phase uit met wille keurige echte bevoegdheden van een unitary Oracle.</span><span class="sxs-lookup"><span data-stu-id="f19c5-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f19c5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f19c5-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="f19c5-107">Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="f19c5-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="f19c5-108">De bewerking wordt uitgevoerd op een dubbel $t $ en een REGI ster, waardoor $U ^ t $ wordt toegepast op het betreffende REGI ster, waarbij $U $ de unitary is waarvan de fase moet worden geschat, waarbij $t $ de gehele kracht is die aan de Oracle is gegeven</span><span class="sxs-lookup"><span data-stu-id="f19c5-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="f19c5-109">tijd: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f19c5-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f19c5-110">Aantal keren dat de opgegeven unitary Oracle moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f19c5-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="f19c5-111">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f19c5-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f19c5-112">De hoek waarmee de fase van het besturings element Qubit wordt omgekeerd voordat de doel status wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="f19c5-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="f19c5-113">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f19c5-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f19c5-114">REGI ster van de door de opgegeven unitary Oracle gehandelde status.</span><span class="sxs-lookup"><span data-stu-id="f19c5-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="f19c5-115">controlQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f19c5-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="f19c5-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f19c5-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

