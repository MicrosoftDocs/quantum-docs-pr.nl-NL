---
uid: Microsoft.Quantum.Canon.ApplyLowDepthAnd
title: Bewerking ApplyLowDepthAnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyLowDepthAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.
ms.openlocfilehash: 092a350e42d8d90942de13530fefd761b5187e1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705205"
---
# <a name="applylowdepthand-operation"></a><span data-ttu-id="7142a-102">Bewerking ApplyLowDepthAnd</span><span class="sxs-lookup"><span data-stu-id="7142a-102">ApplyLowDepthAnd operation</span></span>

<span data-ttu-id="7142a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="7142a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="7142a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7142a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7142a-105">Hiermee wordt een bepaalde doel-Qubit als en alleen als beide Control qubits zich in de status 1 bevinden, met T-diepte 1, met behulp van meting om de adjoint-bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="7142a-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, with T-depth 1, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyLowDepthAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="7142a-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7142a-106">Description</span></span>

<span data-ttu-id="7142a-107">Keert `target` alleen als beide besturings elementen 1 zijn, maar er wordt van uitgegaan dat de `target` status 0 is.</span><span class="sxs-lookup"><span data-stu-id="7142a-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="7142a-108">De bewerking heeft T-Count 4, T-diepte 1 en vereist een helper-Qubit en kan daarom de voor keur geven aan een CCNOT-bewerking, als `target` bekend is dat deze 0 is.</span><span class="sxs-lookup"><span data-stu-id="7142a-108">The operation has T-count 4, T-depth 1 and requires one helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="7142a-109">De adjoint van deze bewerking wordt gemeten op basis van de meting en vereist geen T-poorten en geen helper-Qubit.</span><span class="sxs-lookup"><span data-stu-id="7142a-109">The adjoint of this operation is measurement based and requires no T gates, and no helper qubit.</span></span>

## <a name="input"></a><span data-ttu-id="7142a-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="7142a-110">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="7142a-111">control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7142a-111">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7142a-112">Eerste besturings element Qubit</span><span class="sxs-lookup"><span data-stu-id="7142a-112">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="7142a-113">control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7142a-113">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7142a-114">Qubit voor het tweede besturings element</span><span class="sxs-lookup"><span data-stu-id="7142a-114">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="7142a-115">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="7142a-115">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="7142a-116">Doel hulp Qubit; moet de status 0 hebben</span><span class="sxs-lookup"><span data-stu-id="7142a-116">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="7142a-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="7142a-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="7142a-118">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="7142a-118">References</span></span>

- <span data-ttu-id="7142a-119">Cody Jones: ' nieuwe constructies voor de fout tolerante Toffoli-Gate ', fysiek. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) DOI: 10.1103/PhysRevA. 87.022328</span><span class="sxs-lookup"><span data-stu-id="7142a-119">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="7142a-120">Peter Selinger: ' Quantum circuits One ', fysiek. Rev. A 87, 042302, 2013 [arXiv: 1210.0974](https://arxiv.org/abs/1210.0974) DOI: 10.1103/PhysRevA. 87.042302</span><span class="sxs-lookup"><span data-stu-id="7142a-120">Peter Selinger: "Quantum circuits of T-depth one", Phys. Rev. A 87, 042302, 2013 [arXiv:1210.0974](https://arxiv.org/abs/1210.0974) doi:10.1103/PhysRevA.87.042302</span></span>