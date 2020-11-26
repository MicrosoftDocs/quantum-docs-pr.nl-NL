---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Bewerking ApplyMajorityInPlace
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: c32d7546fb753f78a72479cec11a6ed09c5e6179
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96190731"
---
# <a name="applymajorityinplace-operation"></a><span data-ttu-id="3a88e-102">Bewerking ApplyMajorityInPlace</span><span class="sxs-lookup"><span data-stu-id="3a88e-102">ApplyMajorityInPlace operation</span></span>

<span data-ttu-id="3a88e-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3a88e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3a88e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a88e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a88e-105">Hiermee wordt de Qubit-hoofd bewerking in-place toegepast op een REGI ster van qubits.</span><span class="sxs-lookup"><span data-stu-id="3a88e-105">Applies the three-qubit majority operation in-place on a register of qubits.</span></span>

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="3a88e-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3a88e-106">Description</span></span>

<span data-ttu-id="3a88e-107">Met deze bewerking wordt de functie in de hoofd positie op 3 qubits berekend.</span><span class="sxs-lookup"><span data-stu-id="3a88e-107">This operation computes the majority function in-place on 3 qubits.</span></span>

<span data-ttu-id="3a88e-108">Als we output Qubit als $z $ en invoer qubits als $x $ en $y $ aanduiden, voert de bewerking de volgende trans formatie uit: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="3a88e-108">If we denote output qubit as $z$ and input qubits as $x$ and $y$, the operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="3a88e-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="3a88e-109">Input</span></span>

### <a name="output--qubit"></a><span data-ttu-id="3a88e-110">uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3a88e-110">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3a88e-111">Eerste invoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="3a88e-111">First input qubit.</span></span> <span data-ttu-id="3a88e-112">Houd er rekening mee dat de uitvoer op locatie wordt berekend en opgeslagen in deze Qubit.</span><span class="sxs-lookup"><span data-stu-id="3a88e-112">Note that the output is computed in-place and stored in this qubit.</span></span>


### <a name="input--qubit"></a><span data-ttu-id="3a88e-113">invoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3a88e-113">input : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3a88e-114">Tweede en derde invoer qubits.</span><span class="sxs-lookup"><span data-stu-id="3a88e-114">Second and third input qubits.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3a88e-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3a88e-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

