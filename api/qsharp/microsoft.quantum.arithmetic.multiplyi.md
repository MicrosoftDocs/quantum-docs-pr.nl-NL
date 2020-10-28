---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Bewerking MultiplyI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 7b44f64fdddfd95f51683c2c3b2f4d37d0cf6841
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706372"
---
# <a name="multiplyi-operation"></a><span data-ttu-id="101c1-102">Bewerking MultiplyI</span><span class="sxs-lookup"><span data-stu-id="101c1-102">MultiplyI operation</span></span>

<span data-ttu-id="101c1-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="101c1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="101c1-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="101c1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="101c1-105">Vermenigvuldig het geheel getal `xs` met een geheel getal `ys` en sla het resultaat op in `result` . dit moet aanvankelijk nul zijn.</span><span class="sxs-lookup"><span data-stu-id="101c1-105">Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="101c1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="101c1-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="101c1-107">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="101c1-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="101c1-108">$n $-bits multiplicand (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="101c1-108">$n$-bit multiplicand (LittleEndian)</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="101c1-109">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="101c1-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="101c1-110">$n $-bits vermenigvuldiger (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="101c1-110">$n$-bit multiplier (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="101c1-111">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="101c1-111">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="101c1-112">$2n $-bit result (LittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="101c1-112">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="101c1-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="101c1-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="101c1-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="101c1-114">Remarks</span></span>

<span data-ttu-id="101c1-115">Maakt gebruik van een standaard methode voor Shift en toevoegen om de vermenigvuldiging te implementeren.</span><span class="sxs-lookup"><span data-stu-id="101c1-115">Uses a standard shift-and-add approach to implement the multiplication.</span></span>
<span data-ttu-id="101c1-116">De gecontroleerde versie is verbeterd door $x _i $ te kopiëren naar een ancilla Qubit die is voor bereid op het besturings element qubits en vervolgens de toevoeging van de ancilla Qubit te beheren.</span><span class="sxs-lookup"><span data-stu-id="101c1-116">The controlled version was improved by copying out $x_i$ to an ancilla qubit conditioned on the control qubits, and then controlling the addition on the ancilla qubit.</span></span>