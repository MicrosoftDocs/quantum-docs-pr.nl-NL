---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Bewerking ContinuousPhaseEstimationIteration
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: 925b9040f6d9cda074b18a6f9079ccb653f9fa98
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851895"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="bded0-102">Bewerking ContinuousPhaseEstimationIteration</span><span class="sxs-lookup"><span data-stu-id="bded0-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="bded0-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="bded0-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="bded0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bded0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bded0-105">Voert een enkele herhaling van een iteratieve fase van een herhaald (klassiek) Phase uit met wille keurige echte bevoegdheden van een unitary Oracle.</span><span class="sxs-lookup"><span data-stu-id="bded0-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="bded0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bded0-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="bded0-107">Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="bded0-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="bded0-108">De bewerking wordt uitgevoerd op een dubbel $t $ en een REGI ster, waardoor $U ^ t $ wordt toegepast op het betreffende REGI ster, waarbij $U $ de unitary is waarvan de fase moet worden geschat, waarbij $t $ de gehele kracht is die aan de Oracle is gegeven</span><span class="sxs-lookup"><span data-stu-id="bded0-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="bded0-109">tijd: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bded0-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bded0-110">Aantal keren dat de opgegeven unitary Oracle moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="bded0-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="bded0-111">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="bded0-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="bded0-112">De hoek waarmee de fase van het besturings element Qubit wordt omgekeerd voordat de doel status wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="bded0-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="bded0-113">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bded0-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bded0-114">REGI ster van de door de opgegeven unitary Oracle gehandelde status.</span><span class="sxs-lookup"><span data-stu-id="bded0-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="bded0-115">controlQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bded0-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="bded0-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bded0-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

