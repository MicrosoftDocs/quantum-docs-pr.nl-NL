---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyFixedPointAmplification
title: Bewerking ApplyFixedPointAmplification
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyFixedPointAmplification
qsharp.summary: Fixed-Point Amplitude Amplification algorithm
ms.openlocfilehash: f506be7b2e3f65cf89694e30d79c04ec30d25035
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707753"
---
# <a name="applyfixedpointamplification-operation"></a><span data-ttu-id="6526c-102">Bewerking ApplyFixedPointAmplification</span><span class="sxs-lookup"><span data-stu-id="6526c-102">ApplyFixedPointAmplification operation</span></span>

<span data-ttu-id="6526c-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="6526c-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="6526c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6526c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6526c-105">Fixed-Point amplitude-versterkings algoritme</span><span class="sxs-lookup"><span data-stu-id="6526c-105">Fixed-Point Amplitude Amplification algorithm</span></span>

```qsharp
operation ApplyFixedPointAmplification (statePrepOracle : Microsoft.Quantum.Oracles.StateOracle, startQubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="6526c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6526c-106">Input</span></span>

### <a name="statepreporacle--stateoracle"></a><span data-ttu-id="6526c-107">statePrepOracle: [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="6526c-107">statePrepOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="6526c-108">Unitary Oracle waarmee de start status wordt voor bereid.</span><span class="sxs-lookup"><span data-stu-id="6526c-108">Unitary oracle that prepares the start state.</span></span>


### <a name="startqubits--qubit"></a><span data-ttu-id="6526c-109">startQubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="6526c-109">startQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="6526c-110">Qubit registreren</span><span class="sxs-lookup"><span data-stu-id="6526c-110">Qubit register</span></span>



## <a name="output--unit"></a><span data-ttu-id="6526c-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6526c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6526c-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6526c-112">Remarks</span></span>

<span data-ttu-id="6526c-113">De startQubits moet de status $ \ket{0 \cdots 0} $ hebben.</span><span class="sxs-lookup"><span data-stu-id="6526c-113">The startQubits must be in the $\ket{0 \cdots 0}$ state.</span></span> <span data-ttu-id="6526c-114">Met deze bewerking wordt een aantal query's herhaald in bevoegdheden van $2 $ totdat een maximum aantal query's is bereikt of de doel status is gevonden.</span><span class="sxs-lookup"><span data-stu-id="6526c-114">This operation iterates over a number of queries in powers of $2$ until either a maximal number of queries is reached, or the target state is found.</span></span>