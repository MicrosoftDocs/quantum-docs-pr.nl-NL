---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterTTKAdder
title: Bewerking ApplyOuterTTKAdder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterTTKAdder
qsharp.summary: Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.
ms.openlocfilehash: 3d6d7c3446075130e5a8ee93abbd27e617d50b3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707572"
---
# <a name="applyouterttkadder-operation"></a><span data-ttu-id="5f3d5-102">Bewerking ApplyOuterTTKAdder</span><span class="sxs-lookup"><span data-stu-id="5f3d5-102">ApplyOuterTTKAdder operation</span></span>

<span data-ttu-id="5f3d5-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="5f3d5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="5f3d5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5f3d5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5f3d5-105">Implementeert de buitenste bewerking voor RippleCarryAdderTTK naar geconjugeerde de binnenste bewerking voor het samen stellen van de volledige Adder.</span><span class="sxs-lookup"><span data-stu-id="5f3d5-105">Implements the outer operation for RippleCarryAdderTTK to conjugate the inner operation to construct the full adder.</span></span>

```qsharp
operation ApplyOuterTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="5f3d5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5f3d5-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="5f3d5-107">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5f3d5-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5f3d5-108">LittleEndian Qubit registreert de eerste integer summand-invoer in RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="5f3d5-108">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="5f3d5-109">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="5f3d5-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="5f3d5-110">LittleEndian Qubit registreert de tweede integer summand-invoer op RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="5f3d5-110">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5f3d5-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5f3d5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="5f3d5-112">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="5f3d5-112">References</span></span>

- <span data-ttu-id="5f3d5-113">Yasuhiro Takahashi, seiichiro Tani, Noboru Kunihiro: "Quantum extra-circuits en niet-gebonden ventilatoren", quantum informatie en berekening, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="5f3d5-113">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530