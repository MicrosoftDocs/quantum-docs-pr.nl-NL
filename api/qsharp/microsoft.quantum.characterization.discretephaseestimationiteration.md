---
uid: Microsoft.Quantum.Characterization.DiscretePhaseEstimationIteration
title: Bewerking DiscretePhaseEstimationIteration
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: DiscretePhaseEstimationIteration
qsharp.summary: Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.
ms.openlocfilehash: 167b53d7108c64d11a4f258d17e90ba78d7dd8d8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703653"
---
# <a name="discretephaseestimationiteration-operation"></a><span data-ttu-id="5b1f6-102">Bewerking DiscretePhaseEstimationIteration</span><span class="sxs-lookup"><span data-stu-id="5b1f6-102">DiscretePhaseEstimationIteration operation</span></span>

<span data-ttu-id="5b1f6-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="5b1f6-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="5b1f6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5b1f6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5b1f6-105">Voert een enkele herhaling van een iteratieve fase van een herhaald (klassiek) Phase uit met een geheel getal van een unitary Oracle.</span><span class="sxs-lookup"><span data-stu-id="5b1f6-105">Performs a single iteration of an iterative (classically-controlled) phase estimation algorithm using integer powers of a unitary oracle.</span></span>

```qsharp
operation DiscretePhaseEstimationIteration (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, power : Int, theta : Double, targetState : Qubit[], controlQubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="5b1f6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5b1f6-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="5b1f6-107">Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="5b1f6-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="5b1f6-108">De bewerking wordt uitgevoerd op een geheel getal en een REGI ster, waardoor de $U ^ m $ wordt toegepast op het opgegeven REGI ster, waarbij $U $ de unitary is waarvan de fase wordt geschat en waarbij $m $ de gehele voeding is die aan de Oracle is gegeven</span><span class="sxs-lookup"><span data-stu-id="5b1f6-108">Operation acting on an integer and a register, such that $U^m$ is applied to the given register, where $U$ is the unitary whose phase is to be estimated, and where $m$ is the integer power given to the oracle</span></span>


### <a name="power--int"></a><span data-ttu-id="5b1f6-109">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5b1f6-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5b1f6-110">Aantal keren dat de opgegeven unitary Oracle moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="5b1f6-110">Number of times to apply the given unitary oracle.</span></span>


### <a name="theta--double"></a><span data-ttu-id="5b1f6-111">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5b1f6-111">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5b1f6-112">De hoek waarmee de fase van het besturings element Qubit wordt omgekeerd voordat de doel status wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="5b1f6-112">Angle by which to invert the phase on the control qubit before acting on the target state.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="5b1f6-113">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="5b1f6-113">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="5b1f6-114">REGI ster van de door de opgegeven unitary Oracle gehandelde status.</span><span class="sxs-lookup"><span data-stu-id="5b1f6-114">Register of state acted upon by the given unitary oracle.</span></span>


### <a name="controlqubit--qubit"></a><span data-ttu-id="5b1f6-115">controlQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="5b1f6-115">controlQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="5b1f6-116">Een hulp Qubit gebruikt om de toepassing van de opgegeven Oracle te beheren.</span><span class="sxs-lookup"><span data-stu-id="5b1f6-116">An auxiliary qubit used to control the application of the given oracle.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5b1f6-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5b1f6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

