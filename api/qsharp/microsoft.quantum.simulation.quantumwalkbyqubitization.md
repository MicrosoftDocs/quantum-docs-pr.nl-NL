---
uid: Microsoft.Quantum.Simulation.QuantumWalkByQubitization
title: De functie QuantumWalkByQubitization
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: QuantumWalkByQubitization
qsharp.summary: Converts a block-encoding reflection into a quantum walk.
ms.openlocfilehash: ef9740f1867cee3c79a7ec0bf90f2c2f4b39ad28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709325"
---
# <a name="quantumwalkbyqubitization-function"></a><span data-ttu-id="7fb66-102">De functie QuantumWalkByQubitization</span><span class="sxs-lookup"><span data-stu-id="7fb66-102">QuantumWalkByQubitization function</span></span>

<span data-ttu-id="7fb66-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="7fb66-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="7fb66-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7fb66-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7fb66-105">Hiermee wordt een weer spiegeling van blok-encoding omgezet in een Quantum Walk.</span><span class="sxs-lookup"><span data-stu-id="7fb66-105">Converts a block-encoding reflection into a quantum walk.</span></span>

```qsharp
function QuantumWalkByQubitization (blockEncoding : Microsoft.Quantum.Simulation.BlockEncodingReflection) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="description"></a><span data-ttu-id="7fb66-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="7fb66-106">Description</span></span>

<span data-ttu-id="7fb66-107">Gezien een `BlockEncodingReflection` vertegenwoordigd door een unitary $U $ waarmee een bepaalde operator $H $ of interest wordt gecodeerd, wordt deze omgezet in een Quantum walk $W $ met het spectrum $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.</span><span class="sxs-lookup"><span data-stu-id="7fb66-107">Given a `BlockEncodingReflection` represented by a unitary $U$ that encodes some operator $H$ of interest, converts it into a quantum walk $W$ containing the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="input"></a><span data-ttu-id="7fb66-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="7fb66-108">Input</span></span>

### <a name="blockencoding--blockencodingreflection"></a><span data-ttu-id="7fb66-109">blockEncoding: [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span><span class="sxs-lookup"><span data-stu-id="7fb66-109">blockEncoding : [BlockEncodingReflection](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)</span></span>

<span data-ttu-id="7fb66-110">Een `BlockEncodingReflection` unitary $U $ worden geconverteerd naar een Quantum Walk.</span><span class="sxs-lookup"><span data-stu-id="7fb66-110">A `BlockEncodingReflection` unitary $U$ to be converted into a Quantum walk.</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="7fb66-111">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="7fb66-111">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="7fb66-112">Een Quantum Walk $W $ communiceert samen met `a` de registers en `s` de blok code ring $H $, en bevat het spectrum $ \pm e ^ {\pm i\sin ^ {-1} (H)} $.</span><span class="sxs-lookup"><span data-stu-id="7fb66-112">A quantum walk $W$ acting jointly on registers `a` and `s` that block- encodes $H$, and contains the spectrum of $\pm e^{\pm i\sin^{-1}(H)}$.</span></span>

## <a name="references"></a><span data-ttu-id="7fb66-113">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="7fb66-113">References</span></span>

- <span data-ttu-id="7fb66-114">Hamiltonian simulatie door Qubitization Guang Hao laag, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span><span class="sxs-lookup"><span data-stu-id="7fb66-114">Hamiltonian Simulation by Qubitization Guang Hao Low, Isaac L. Chuang https://arxiv.org/abs/1610.06546</span></span>

## <a name="see-also"></a><span data-ttu-id="7fb66-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7fb66-115">See Also</span></span>

- [<span data-ttu-id="7fb66-116">Micro soft. Quantum. simulatie. BlockEncoding</span><span class="sxs-lookup"><span data-stu-id="7fb66-116">Microsoft.Quantum.Simulation.BlockEncoding</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncoding)
- [<span data-ttu-id="7fb66-117">Micro soft. Quantum. simulatie. BlockEncodingReflection</span><span class="sxs-lookup"><span data-stu-id="7fb66-117">Microsoft.Quantum.Simulation.BlockEncodingReflection</span></span>](xref:Microsoft.Quantum.Simulation.BlockEncodingReflection)