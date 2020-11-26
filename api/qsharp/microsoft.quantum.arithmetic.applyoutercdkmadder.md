---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Bewerking ApplyOuterCDKMAdder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: 81311a75beedb62331184faf4e1523f3ccc74f43
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190663"
---
# <a name="applyoutercdkmadder-operation"></a><span data-ttu-id="f38a5-102">Bewerking ApplyOuterCDKMAdder</span><span class="sxs-lookup"><span data-stu-id="f38a5-102">ApplyOuterCDKMAdder operation</span></span>

<span data-ttu-id="f38a5-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f38a5-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f38a5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f38a5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f38a5-105">Omkeerbaar, in-place rimpel bewerking die wordt gebruikt in de RippleCarryAdderCDKM-bewerking voor het tellen van gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="f38a5-105">Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below.</span></span>
<span data-ttu-id="f38a5-106">Als er twee Qubit `xs` -registers en `ys` dezelfde lengte worden gebruikt, past de bewerking een rimpeling toe van CNOT-en CCNOT-poorten met qubits in `xs` en `ys` als de besturings elementen en qubits als `xs` doel.</span><span class="sxs-lookup"><span data-stu-id="f38a5-106">Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.</span></span>

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="f38a5-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="f38a5-107">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="f38a5-108">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f38a5-108">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f38a5-109">Het eerste Qubit-REGI ster met besturings elementen en doelen.</span><span class="sxs-lookup"><span data-stu-id="f38a5-109">First qubit register, containing controls and targets.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="f38a5-110">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f38a5-110">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f38a5-111">Tweede Qubit-REGI ster, bijdragen aan de besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="f38a5-111">Second qubit register, contributing to the controls.</span></span>


### <a name="ancilla--qubit"></a><span data-ttu-id="f38a5-112">ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f38a5-112">ancilla : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f38a5-113">De ancilla-Qubit die wordt gebruikt in RippleCarryAdderCDKM die is door gegeven aan deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="f38a5-113">The ancilla qubit used in RippleCarryAdderCDKM passed to this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f38a5-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f38a5-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="f38a5-115">Referenties</span><span class="sxs-lookup"><span data-stu-id="f38a5-115">References</span></span>

- <span data-ttu-id="f38a5-116">Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="f38a5-116">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1