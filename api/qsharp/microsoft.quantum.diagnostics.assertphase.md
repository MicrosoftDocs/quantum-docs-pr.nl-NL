---
uid: Microsoft.Quantum.Diagnostics.AssertPhase
title: Bewerking AssertPhase
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertPhase
qsharp.summary: Asserts that the phase of an equal superposition state has the expected value.
ms.openlocfilehash: 59fa0f2f68b4de271b972aef776ee5097fd5c201
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830085"
---
# <a name="assertphase-operation"></a><span data-ttu-id="0033c-102">Bewerking AssertPhase</span><span class="sxs-lookup"><span data-stu-id="0033c-102">AssertPhase operation</span></span>

<span data-ttu-id="0033c-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="0033c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="0033c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0033c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0033c-105">Er wordt bevestigd dat de fase van een gelijke superpositie status de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="0033c-105">Asserts that the phase of an equal superposition state has the expected value.</span></span>

```qsharp
operation AssertPhase (expected : Double, qubit : Qubit, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="0033c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0033c-106">Description</span></span>

<span data-ttu-id="0033c-107">Met deze bewerking wordt in de fase $ \phi $ van een Quantum status aangegeven dat kan worden uitgedrukt als $ \frac{e ^ {i t}} {\sqrt {2} } (e ^ {i\phi} \ Ket {0} + e ^ {-i\phi} \ Ket {1} ) $ voor een wille keurig Real $t $ de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="0033c-107">This operation asserts that the phase $\phi$ of a quantum state that may be expressed as $\frac{e^{i t}}{\sqrt{2}}(e^{i\phi}\ket{0} + e^{-i\phi}\ket{1})$ for some arbitrary real $t$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="0033c-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="0033c-108">Input</span></span>

### <a name="expected--double"></a><span data-ttu-id="0033c-109">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0033c-109">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0033c-110">De verwachte waarde van $ \phi \in (-\pi, \pi] $.</span><span class="sxs-lookup"><span data-stu-id="0033c-110">The expected value of $\phi \in (-\pi,\pi]$.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="0033c-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0033c-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0033c-112">De Qubit waarin de verwachte status wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="0033c-112">The qubit that stores the expected state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="0033c-113">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="0033c-113">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="0033c-114">Absolute tolerantie voor het verschil tussen werkelijk en verwacht.</span><span class="sxs-lookup"><span data-stu-id="0033c-114">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0033c-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0033c-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="0033c-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="0033c-116">Example</span></span>

<span data-ttu-id="0033c-117">De volgende assert is geslaagd: `qubit` heeft de status $ \ket{\psi} = e ^ {i 0.5} \ SQRT {1/2} \ Ket {0} + e ^ {i 0.5} \ SQRT {1/2} \ Ket {1} $;</span><span class="sxs-lookup"><span data-stu-id="0033c-117">The following assert succeeds: `qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.0,qubit,10e-10);`

<span data-ttu-id="0033c-118">`qubit` heeft de status $ \ket{\psi} = e ^ {i 0.5} \ SQRT {1/2} \ Ket {0} + e ^ {-i 0.5} \ SQRT {1/2} \ Ket {1} $;</span><span class="sxs-lookup"><span data-stu-id="0033c-118">`qubit` is in state $\ket{\psi}=e^{i 0.5}\sqrt{1/2}\ket{0}+e^{-i 0.5}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(0.5,qubit,10e-10);`

<span data-ttu-id="0033c-119">`qubit` heeft de status $ \ket{\psi} = e ^ {-i 2,2} \ SQRT {1/2} \ Ket {0} + e ^ {i 0,2} \ SQRT {1/2} \ Ket {1} $;</span><span class="sxs-lookup"><span data-stu-id="0033c-119">`qubit` is in state $\ket{\psi}=e^{-i 2.2}\sqrt{1/2}\ket{0}+e^{i 0.2}\sqrt{1/2}\ket{1}$;</span></span>

- `AssertPhase(-1.2,qubit,10e-10);`