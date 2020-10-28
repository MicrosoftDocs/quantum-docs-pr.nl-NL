---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Bewerking AssertPhase
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: e042c03d2a72d9ce4816a8cdb56603e175b22807
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702746"
---
# <a name="assertphase-operation"></a><span data-ttu-id="d3ddf-102">Bewerking AssertPhase</span><span class="sxs-lookup"><span data-stu-id="d3ddf-102">AssertPhase operation</span></span>

<span data-ttu-id="d3ddf-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d3ddf-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d3ddf-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d3ddf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d3ddf-105">Er wordt bevestigd dat de fase van een gelijke superpositie status de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="d3ddf-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d3ddf-106">Description</span></span>

<span data-ttu-id="d3ddf-107">Met deze bewerking wordt in de fase $ \phi $ van een Quantum status aangegeven dat kan worden uitgedrukt als $ \frac{e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ Ket {0} + e ^ {-i\phi} \ Ket {1} ) $ voor een wille keurig Real $t $ de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="d3ddf-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d3ddf-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="d3ddf-109">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d3ddf-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d3ddf-110">De verwachte waarde van $ \phi \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="d3ddf-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="d3ddf-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="d3ddf-112">De Qubit waarin de verwachte status wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="d3ddf-113">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d3ddf-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d3ddf-114">Absolute tolerantie voor het verschil tussen werkelijk en verwacht.</span><span class="sxs-lookup"><span data-stu-id="d3ddf-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3ddf-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3ddf-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

