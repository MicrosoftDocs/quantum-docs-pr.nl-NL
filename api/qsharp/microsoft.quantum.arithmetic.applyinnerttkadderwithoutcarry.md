---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdderWithoutCarry
title: Bewerking ApplyInnerTTKAdderWithoutCarry
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdderWithoutCarry
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 3335c63b8509090deed1172419158da0d5e80409
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707628"
---
# <a name="applyinnerttkadderwithoutcarry-operation"></a><span data-ttu-id="a7628-102">Bewerking ApplyInnerTTKAdderWithoutCarry</span><span class="sxs-lookup"><span data-stu-id="a7628-102">ApplyInnerTTKAdderWithoutCarry operation</span></span>

<span data-ttu-id="a7628-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="a7628-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="a7628-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a7628-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a7628-105">Implementeert de functie inner join voor de bewerking RippleCarryAdderNoCarryTTK.</span><span class="sxs-lookup"><span data-stu-id="a7628-105">Implements the inner addition function for the operation RippleCarryAdderNoCarryTTK.</span></span> <span data-ttu-id="a7628-106">Dit is de binnenste bewerking die is gekoppeld aan de buitenste bewerking om de volledige adder te maken.</span><span class="sxs-lookup"><span data-stu-id="a7628-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdderWithoutCarry (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="a7628-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="a7628-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="a7628-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a7628-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a7628-109">LittleEndian Qubit registreert de eerste integer summand-invoer in RippleCarryAdderNoCarryTTK.</span><span class="sxs-lookup"><span data-stu-id="a7628-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderNoCarryTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="a7628-110">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="a7628-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="a7628-111">LittleEndian Qubit registreert de tweede integer summand-invoer op RippleCarryAdderNoCarryTTK.</span><span class="sxs-lookup"><span data-stu-id="a7628-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderNoCarryTTK.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7628-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7628-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a7628-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a7628-113">Remarks</span></span>

<span data-ttu-id="a7628-114">De opgegeven bewaakte bewerking maakt gebruik van symmetrie en wederzijdse annulering van bewerkingen voor het verbeteren van de standaard implementatie waarmee een besturings element wordt toegevoegd aan elke bewerking.</span><span class="sxs-lookup"><span data-stu-id="a7628-114">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="a7628-115">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="a7628-115">References</span></span>

- <span data-ttu-id="a7628-116">Yasuhiro Takahashi, seiichiro Tani, Noboru Kunihiro: "Quantum extra-circuits en niet-gebonden ventilatoren", quantum informatie en berekening, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="a7628-116">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530