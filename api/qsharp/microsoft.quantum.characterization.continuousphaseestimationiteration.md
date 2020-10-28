---
uid: Microsoft.Quantum.Characterization.ContinuousPhaseEstimationIteration
title: Bewerking ContinuousPhaseEstimationIteration
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: ContinuousPhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.
ms.openlocfilehash: a3914a4b19e3b898b6de8808699da09d386f487a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703658"
---
# <a name="continuousphaseestimationiteration-operation"></a><span data-ttu-id="699bb-102">Bewerking ContinuousPhaseEstimationIteration</span><span class="sxs-lookup"><span data-stu-id="699bb-102">ContinuousPhaseEstimationIteration operation</span></span>

<span data-ttu-id="699bb-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="699bb-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="699bb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="699bb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="699bb-105">Voert een enkele herhaling van een iteratieve fase van een herhaald (klassiek) Phase uit met wille keurige echte bevoegdheden van een unitary Oracle.</span><span class="sxs-lookup"><span data-stu-id="699bb-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using arbitrary real powers of a unitary oracle.</span></span>

```qsharp
operation ContinuousPhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.ContinuousOracle, time : Double, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="699bb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="699bb-106">Input</span></span>

### <a name="oracle--continuousoracle"></a><span data-ttu-id="699bb-107">Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="699bb-107">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="699bb-108">De bewerking wordt uitgevoerd op een dubbel $t $ en een REGI ster, waardoor $U ^ t $ wordt toegepast op het betreffende REGI ster, waarbij $U $ de unitary is waarvan de fase moet worden geschat, waarbij $t $ de gehele kracht is die aan de Oracle is gegeven</span><span class="sxs-lookup"><span data-stu-id="699bb-108">Operation acting on a double $t$ and a register, such that $U^t$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $t$ is the integer power given to the oracle</span></span>


### <a name="time--double"></a><span data-ttu-id="699bb-109">tijd: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="699bb-109">time : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="699bb-110">Aantal keren dat de opgegeven unitary Oracle moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="699bb-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="699bb-111">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="699bb-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="699bb-112">De hoek waarmee de fase van het besturings element Qubit wordt omgekeerd voordat de doel status wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="699bb-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="699bb-113">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="699bb-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="699bb-114">REGI ster van de door de opgegeven unitary Oracle gehandelde status.</span><span class="sxs-lookup"><span data-stu-id="699bb-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="699bb-115">controlQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="699bb-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="699bb-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="699bb-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

