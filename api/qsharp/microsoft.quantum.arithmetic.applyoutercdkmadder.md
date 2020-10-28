---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Bewerking ApplyOuterCDKMAdder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: 5ec9d31252254e40efb22e06656294325b4cffcd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707573"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="52b7d-102">Bewerking ApplyOuterCDKMAdder</span><span class="sxs-lookup"><span data-stu-id="52b7d-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="52b7d-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="52b7d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="52b7d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="52b7d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="52b7d-105">Omkeerbaar, in-place rimpel bewerking die wordt gebruikt in de RippleCarryAdderCDKM-bewerking voor het tellen van gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="52b7d-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="52b7d-106">Als er twee Qubit `xs` -registers en `ys` dezelfde lengte worden gebruikt, past de bewerking een rimpeling toe van CNOT-en CCNOT-poorten met qubits in `xs` en `ys` als de besturings elementen en qubits als `xs` doel.</span><span class="sxs-lookup"><span data-stu-id="52b7d-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="52b7d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="52b7d-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="52b7d-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="52b7d-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="52b7d-109">Het eerste Qubit-REGI ster met besturings elementen en doelen.</span><span class="sxs-lookup"><span data-stu-id="52b7d-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="52b7d-110">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="52b7d-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="52b7d-111">Tweede Qubit-REGI ster, bijdragen aan de besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="52b7d-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="52b7d-112">ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="52b7d-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="52b7d-113">De ancilla-Qubit die wordt gebruikt in RippleCarryAdderCDKM die is door gegeven aan deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="52b7d-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="52b7d-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="52b7d-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="52b7d-115">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="52b7d-115">References</span></span>

- <span data-ttu-id="52b7d-116">Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="52b7d-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1