---
uid: Microsoft.Quantum.Arithmetic.MultiplyI
title: Bewerking MultiplyI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyI
qsharp.summary: Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.
ms.openlocfilehash: 8615d0d5100c26f86264ceaecadb7783563216a6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843033"
---
# <a name="multiplyi-operation"></a><span data-ttu-id="6812a-102">Bewerking MultiplyI</span><span class="sxs-lookup"><span data-stu-id="6812a-102">MultiplyI operation</span></span>

<span data-ttu-id="6812a-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6812a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6812a-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="6812a-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="6812a-105">Vermenigvuldig het geheel getal `xs` met een geheel getal `ys` en sla het resultaat op in `result` . dit moet aanvankelijk nul zijn.</span><span class="sxs-lookup"><span data-stu-id="6812a-105">Multiply integer `xs` by integer `ys` and store the result in `result`, which must be zero initially.</span></span>

```qsharp
operation MultiplyI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="6812a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6812a-106">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="6812a-107">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6812a-107">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6812a-108">$n $-bits multiplicand (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6812a-108">$n$-bit multiplicand (LittleEndian)</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="6812a-109">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6812a-109">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6812a-110">$n $-bits vermenigvuldiger (LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6812a-110">$n$-bit multiplier (LittleEndian)</span></span>


### <a name="result--littleendian"></a><span data-ttu-id="6812a-111">resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6812a-111">result : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6812a-112">$2n $-bit result (LittleEndian), moet de status $ \ket {0} $ in eerste instantie hebben.</span><span class="sxs-lookup"><span data-stu-id="6812a-112">$2n$-bit result (LittleEndian), must be in state $\ket{0}$ initially.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6812a-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6812a-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="6812a-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6812a-114">Remarks</span></span>

<span data-ttu-id="6812a-115">Maakt gebruik van een standaard methode voor Shift en toevoegen om de vermenigvuldiging te implementeren.</span><span class="sxs-lookup"><span data-stu-id="6812a-115">Uses a standard shift-and-add approach to implement the multiplication.</span></span>
<span data-ttu-id="6812a-116">De gecontroleerde versie is verbeterd door $x _i $ te kopiëren naar een ancilla Qubit die is voor bereid op het besturings element qubits en vervolgens de toevoeging van de ancilla Qubit te beheren.</span><span class="sxs-lookup"><span data-stu-id="6812a-116">The controlled version was improved by copying out $x_i$ to an ancilla qubit conditioned on the control qubits, and then controlling the addition on the ancilla qubit.</span></span>