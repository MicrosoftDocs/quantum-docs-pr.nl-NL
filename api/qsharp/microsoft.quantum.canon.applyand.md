---
uid: Microsoft.Quantum.Canon.ApplyAnd
title: Bewerking ApplyAnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyAnd
qsharp.summary: Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.
ms.openlocfilehash: 5a4e18cb0361708e1fc00e8d62c0a6c2415d6bed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705501"
---
# <a name="applyand-operation"></a><span data-ttu-id="d0bb9-102">Bewerking ApplyAnd</span><span class="sxs-lookup"><span data-stu-id="d0bb9-102">ApplyAnd operation</span></span>

<span data-ttu-id="d0bb9-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d0bb9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d0bb9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0bb9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0bb9-105">Hiermee wordt een bepaalde doel-Qubit als en alleen als beide besturings qubits de status 1 hebben, met behulp van meting om de adjoint-bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d0bb9-105">Inverts a given target qubit if and only if both control qubits are in the 1 state, using measurement to perform the adjoint operation.</span></span>

```qsharp
operation ApplyAnd (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="d0bb9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d0bb9-106">Description</span></span>

<span data-ttu-id="d0bb9-107">Keert `target` alleen als beide besturings elementen 1 zijn, maar er wordt van uitgegaan dat de `target` status 0 is.</span><span class="sxs-lookup"><span data-stu-id="d0bb9-107">Inverts `target` if and only if both controls are 1, but assumes that `target` is in state 0.</span></span>  <span data-ttu-id="d0bb9-108">De bewerking heeft T-Count 4, T-diepte 2 en vereist geen helper Qubit. Dit kan daarom de voor keur hebben voor een CCNOT-bewerking, als `target` bekend is dat deze 0 is.</span><span class="sxs-lookup"><span data-stu-id="d0bb9-108">The operation has T-count 4, T-depth 2 and requires no helper qubit, and may therefore be preferable to a CCNOT operation, if `target` is known to be 0.</span></span>  <span data-ttu-id="d0bb9-109">De adjoint van deze bewerking is gebaseerd op metingen en vereist geen T-poorten.</span><span class="sxs-lookup"><span data-stu-id="d0bb9-109">The adjoint of this operation is measurement based and requires no T gates.</span></span>

<span data-ttu-id="d0bb9-110">De beheerde toepassing van deze bewerking vereist geen Qubit, `2^c` `Rz` poorten en is niet geoptimaliseerd voor diepte, waarbij `c` het aantal algemene besturings elementen qubits, met inbegrip van de twee controles van de `ApplyAnd` bewerking.</span><span class="sxs-lookup"><span data-stu-id="d0bb9-110">The controlled application of this operation requires no helper qubit, `2^c` `Rz` gates and is not optimized for depth, where `c` is the number of overall control qubits including the two controls from the `ApplyAnd` operation.</span></span>  <span data-ttu-id="d0bb9-111">De door adjoint beheerde toepassing vereist `2^c - 1` `Rz` poorten (met een hoek van twee keer de grootte van de niet-adjoint bewerking), geen helper-Qubit en is niet geoptimaliseerd voor diepte.</span><span class="sxs-lookup"><span data-stu-id="d0bb9-111">The adjoint controlled application requires `2^c - 1` `Rz` gates (with an angle twice the size of the non-adjoint operation), no helper qubit and is not optimized for depth.</span></span>

## <a name="input"></a><span data-ttu-id="d0bb9-112">Invoer</span><span class="sxs-lookup"><span data-stu-id="d0bb9-112">Input</span></span>

### <a name="control1--qubit"></a><span data-ttu-id="d0bb9-113">control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d0bb9-113">control1 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d0bb9-114">Eerste besturings element Qubit</span><span class="sxs-lookup"><span data-stu-id="d0bb9-114">First control qubit</span></span>


### <a name="control2--qubit"></a><span data-ttu-id="d0bb9-115">control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d0bb9-115">control2 : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d0bb9-116">Qubit voor het tweede besturings element</span><span class="sxs-lookup"><span data-stu-id="d0bb9-116">Second control qubit</span></span>


### <a name="target--qubit"></a><span data-ttu-id="d0bb9-117">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d0bb9-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d0bb9-118">Doel hulp Qubit; moet de status 0 hebben</span><span class="sxs-lookup"><span data-stu-id="d0bb9-118">Target auxiliary qubit; must be in state 0</span></span>



## <a name="output--unit"></a><span data-ttu-id="d0bb9-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0bb9-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="d0bb9-120">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="d0bb9-120">References</span></span>

- <span data-ttu-id="d0bb9-121">Cody Jones: ' nieuwe constructies voor de fout tolerante Toffoli-Gate ', fysiek. Rev. A 87, 022328, 2013 [arXiv: 1212.5069](https://arxiv.org/abs/1212.5069) DOI: 10.1103/PhysRevA. 87.022328</span><span class="sxs-lookup"><span data-stu-id="d0bb9-121">Cody Jones: "Novel constructions for the fault-tolerant Toffoli gate", Phys. Rev. A 87, 022328, 2013 [arXiv:1212.5069](https://arxiv.org/abs/1212.5069) doi:10.1103/PhysRevA.87.022328</span></span>
- <span data-ttu-id="d0bb9-122">Craig Gidney: "de kosten van een Quantum toevoeging", Quantum 2, pagina 74, 2018 [arXiv: 1709.06648](https://arxiv.org/abs/1709.06648) DOI: 10.1103/PhysRevA. 85.044302</span><span class="sxs-lookup"><span data-stu-id="d0bb9-122">Craig Gidney: "Halving the cost of quantum addition", Quantum 2, page 74, 2018 [arXiv:1709.06648](https://arxiv.org/abs/1709.06648) doi:10.1103/PhysRevA.85.044302</span></span>
- <span data-ttu-id="d0bb9-123">Mathias soeken: "Quantum Oracle-circuits en het patroon voor kerst boom", [blog artikel van 19 December 2019](https://msoeken.github.io/blog_qac.html) (Opmerking: uitleg over de meerdere bewaakte constructie)</span><span class="sxs-lookup"><span data-stu-id="d0bb9-123">Mathias Soeken: "Quantum Oracle Circuits and the Christmas Tree Pattern", [Blog article from December 19, 2019](https://msoeken.github.io/blog_qac.html) (note: explains the multiple controlled construction)</span></span>