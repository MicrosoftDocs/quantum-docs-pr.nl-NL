---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: Bewerking QuantumPhaseEstimation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 14ba3e012f6561e7089f9fe59b2a13516b211d51
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204212"
---
# <a name="quantumphaseestimation-operation"></a><span data-ttu-id="c14b7-102">Bewerking QuantumPhaseEstimation</span><span class="sxs-lookup"><span data-stu-id="c14b7-102">QuantumPhaseEstimation operation</span></span>

<span data-ttu-id="c14b7-103">Naam ruimte: [micro soft. Quantum. karakte Rise](xref:Microsoft.Quantum.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="c14b7-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="c14b7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c14b7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c14b7-105">Voert het geraamde algoritme van de Quantum fase uit voor een bepaalde Oracle `U` en `targetState` Lees de fase in een Quantum registratie big endian.</span><span class="sxs-lookup"><span data-stu-id="c14b7-105">Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.</span></span>

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c14b7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c14b7-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="c14b7-107">Oracle: [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="c14b7-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="c14b7-108">Een bewerking die $U ^ m $ implementeert voor het opgegeven geheeltallige maatschap m.</span><span class="sxs-lookup"><span data-stu-id="c14b7-108">An operation implementing $U^m$ for given integer powers m.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="c14b7-109">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c14b7-109">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c14b7-110">Een Quantum register dat de status $ \ket{\phi} $ aanduidt op basis van $U $.</span><span class="sxs-lookup"><span data-stu-id="c14b7-110">A quantum register representing the state $\ket{\phi}$ acted on by $U$.</span></span> <span data-ttu-id="c14b7-111">Als $ \ket{\phi} $ een eigenstate is van $U $, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ voor $ \phi \in [0, 2 \ PI) $ een onbekende fase.</span><span class="sxs-lookup"><span data-stu-id="c14b7-111">If $\ket{\phi}$ is an eigenstate of $U$, $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi \in [0, 2\pi)$ an unknown phase.</span></span>


### <a name="controlregister--bigendian"></a><span data-ttu-id="c14b7-112">controlRegister: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="c14b7-112">controlRegister : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="c14b7-113">Een big endian-geheel getal dat kan worden gebruikt voor het beheren van de beschik bare Oracle, en bevat een representatie van $ \phi $ na de toepassing van deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="c14b7-113">A big-endian representation integer register that can be used to control the provided oracle, and that will contain the a representation of $\phi$ following the application of this operation.</span></span> <span data-ttu-id="c14b7-114">Er wordt van uitgegaan dat controlRegister wordt gestart in de oorspronkelijke status $ \ket{00\cdots 0} $, waarbij de lengte van het REGI ster de gewenste precisie aangeeft.</span><span class="sxs-lookup"><span data-stu-id="c14b7-114">The controlRegister is assumed to start in the initial state $\ket{00\cdots 0}$, where the length of the register indicates the desired precision.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c14b7-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c14b7-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

