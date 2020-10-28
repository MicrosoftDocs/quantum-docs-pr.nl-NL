---
uid: Microsoft.Quantum.Arithmetic.ApplyMajorityInPlace
title: Bewerking ApplyMajorityInPlace
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyMajorityInPlace
qsharp.summary: Applies the three-qubit majority operation in-place on a register of qubits.
ms.openlocfilehash: 3664ffe96cd1db8cf5e8898387fe7f2d45b4ea98
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707596"
---
# <a name="applymajorityinplace-operation"></a><span data-ttu-id="607cb-102">Bewerking ApplyMajorityInPlace</span><span class="sxs-lookup"><span data-stu-id="607cb-102">ApplyMajorityInPlace operation</span></span>

<span data-ttu-id="607cb-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="607cb-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="607cb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="607cb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="607cb-105">Hiermee wordt de Qubit-hoofd bewerking in-place toegepast op een REGI ster van qubits.</span><span class="sxs-lookup"><span data-stu-id="607cb-105">Applies the three-qubit majority operation in-place on a register of qubits.</span></span>

```qsharp
operation ApplyMajorityInPlace (output : Qubit, input : Qubit[]) : Unit
```


## <a name="description"></a><span data-ttu-id="607cb-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="607cb-106">Description</span></span>

<span data-ttu-id="607cb-107">Met deze bewerking wordt de functie in de hoofd positie op 3 qubits berekend.</span><span class="sxs-lookup"><span data-stu-id="607cb-107">This operation computes the majority function in-place on 3 qubits.</span></span>

<span data-ttu-id="607cb-108">Als we output Qubit als $z $ en invoer qubits als $x $ en $y $ aanduiden, voert de bewerking de volgende trans formatie uit: $ \ket{XYZ} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)} $.</span><span class="sxs-lookup"><span data-stu-id="607cb-108">If we denote output qubit as $z$ and input qubits as $x$ and $y$, the operation performs the following transformation: $\ket{xyz} \rightarrow \ket{x \oplus z} \ket{y \oplus z} \ket{\operatorname{MAJ} (x, y, z)}$.</span></span>

## <a name="input"></a><span data-ttu-id="607cb-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="607cb-109">Input</span></span>

### <a name="output--qubit"></a><span data-ttu-id="607cb-110">uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="607cb-110">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="607cb-111">Eerste invoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="607cb-111">First input qubit.</span></span> <span data-ttu-id="607cb-112">Houd er rekening mee dat de uitvoer op locatie wordt berekend en opgeslagen in deze Qubit.</span><span class="sxs-lookup"><span data-stu-id="607cb-112">Note that the output is computed in-place and stored in this qubit.</span></span>


### <a name="input--qubit"></a><span data-ttu-id="607cb-113">invoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="607cb-113">input : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="607cb-114">Tweede en derde invoer qubits.</span><span class="sxs-lookup"><span data-stu-id="607cb-114">Second and third input qubits.</span></span>



## <a name="output--unit"></a><span data-ttu-id="607cb-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="607cb-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

