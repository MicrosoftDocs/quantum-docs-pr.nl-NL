---
uid: Microsoft.Quantum.Arithmetic.ApplyInnerTTKAdder
title: Bewerking ApplyInnerTTKAdder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyInnerTTKAdder
qsharp.summary: Implements the inner addition function for the operation RippleCarryAdderTTK. This is the inner operation that is conjugated with the outer operation to construct the full adder.
ms.openlocfilehash: 23c1f6dcdf3894cf1b416efd922c9eed01ac8f85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707636"
---
# <a name="applyinnerttkadder-operation"></a><span data-ttu-id="f238f-102">Bewerking ApplyInnerTTKAdder</span><span class="sxs-lookup"><span data-stu-id="f238f-102">ApplyInnerTTKAdder operation</span></span>

<span data-ttu-id="f238f-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f238f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f238f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f238f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f238f-105">Implementeert de functie inner join voor de bewerking RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="f238f-105">Implements the inner addition function for the operation RippleCarryAdderTTK.</span></span> <span data-ttu-id="f238f-106">Dit is de binnenste bewerking die is gekoppeld aan de buitenste bewerking om de volledige adder te maken.</span><span class="sxs-lookup"><span data-stu-id="f238f-106">This is the inner operation that is conjugated with the outer operation to construct the full adder.</span></span>

```qsharp
operation ApplyInnerTTKAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, carry : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f238f-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f238f-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="f238f-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f238f-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f238f-109">LittleEndian Qubit registreert de eerste integer summand-invoer in RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="f238f-109">LittleEndian qubit register encoding the first integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="f238f-110">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f238f-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f238f-111">LittleEndian Qubit registreert de tweede integer summand-invoer op RippleCarryAdderTTK.</span><span class="sxs-lookup"><span data-stu-id="f238f-111">LittleEndian qubit register encoding the second integer summand input to RippleCarryAdderTTK.</span></span>


### <a name="carry--qubit"></a><span data-ttu-id="f238f-112">overdragen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f238f-112">carry : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f238f-113">Qubit, is xored met de meest significante bit van de som.</span><span class="sxs-lookup"><span data-stu-id="f238f-113">Carry qubit, is xored with the most significant bit of the sum.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f238f-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f238f-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="f238f-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f238f-115">Remarks</span></span>

<span data-ttu-id="f238f-116">De opgegeven bewaakte bewerking maakt gebruik van symmetrie en wederzijdse annulering van bewerkingen voor het verbeteren van de standaard implementatie waarmee een besturings element wordt toegevoegd aan elke bewerking.</span><span class="sxs-lookup"><span data-stu-id="f238f-116">The specified controlled operation makes use of symmetry and mutual cancellation of operations to improve on the default implementation that adds a control to every operation.</span></span>

## <a name="references"></a><span data-ttu-id="f238f-117">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="f238f-117">References</span></span>

- <span data-ttu-id="f238f-118">Yasuhiro Takahashi, seiichiro Tani, Noboru Kunihiro: "Quantum extra-circuits en niet-gebonden ventilatoren", quantum informatie en berekening, vol. 10, 2010.</span><span class="sxs-lookup"><span data-stu-id="f238f-118">Yasuhiro Takahashi, Seiichiro Tani, Noboru Kunihiro: "Quantum Addition Circuits and Unbounded Fan-Out", Quantum Information and Computation, Vol. 10, 2010.</span></span>
  https://arxiv.org/abs/0910.2530