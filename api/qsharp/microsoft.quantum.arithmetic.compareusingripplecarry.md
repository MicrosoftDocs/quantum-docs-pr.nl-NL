---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Bewerking CompareUsingRippleCarry
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: e2d6e5a663f8c4e101c7e2ab1346d10cade3f4e0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223456"
---
# <a name="compareusingripplecarry-operation"></a><span data-ttu-id="e90e8-102">Bewerking CompareUsingRippleCarry</span><span class="sxs-lookup"><span data-stu-id="e90e8-102">CompareUsingRippleCarry operation</span></span>

<span data-ttu-id="e90e8-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e90e8-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e90e8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e90e8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e90e8-105">Met deze bewerking wordt getest of een geheel getal dat wordt vertegenwoordigd door een REGI ster van qubits groter is dan een ander geheel getal, waarbij een XOR van het resultaat wordt toegepast op een uitvoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="e90e8-105">This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.</span></span>

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e90e8-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e90e8-106">Description</span></span>

<span data-ttu-id="e90e8-107">Als er twee gehele getallen zijn opgegeven `x` en `y` zijn opgeslagen in Qubit-registers met een gelijke grootte, controleert deze bewerking of ze voldoen `x > y` .</span><span class="sxs-lookup"><span data-stu-id="e90e8-107">Given two integers `x` and `y` stored in equal-size qubit registers, this operation checks if they satisfy `x > y`.</span></span> <span data-ttu-id="e90e8-108">Als deze waarde True is, wordt 1 XORed in een uitvoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="e90e8-108">If true, 1 is XORed into an output qubit.</span></span> <span data-ttu-id="e90e8-109">Anders wordt 0 XORed in een uitvoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="e90e8-109">Otherwise, 0 is XORed into an output qubit.</span></span>
<span data-ttu-id="e90e8-110">Met andere woorden, deze bewerking kan worden weer gegeven door de unitary $ $ \begin{align} U\ket {x} \ Ket {y} \ Ket {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span><span class="sxs-lookup"><span data-stu-id="e90e8-110">In other words, this operation can be represented by the unitary $$ \begin{align} U\ket{x}\ket{y}\ket{z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span></span>
<span data-ttu-id="e90e8-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="e90e8-111">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="e90e8-112">Invoer</span><span class="sxs-lookup"><span data-stu-id="e90e8-112">Input</span></span>

### <a name="x--littleendian"></a><span data-ttu-id="e90e8-113">x: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e90e8-113">x : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e90e8-114">Het eerste getal dat moet worden vergeleken, wordt opgeslagen in `LittleEndian` de indeling in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="e90e8-114">First number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="y--littleendian"></a><span data-ttu-id="e90e8-115">y: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e90e8-115">y : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e90e8-116">Het tweede getal dat moet worden vergeleken, wordt opgeslagen in `LittleEndian` de indeling in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="e90e8-116">Second number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="output--qubit"></a><span data-ttu-id="e90e8-117">uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="e90e8-117">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="e90e8-118">Qubit waarin het resultaat van de vergelijking wordt opgeslagen $x>y $.</span><span class="sxs-lookup"><span data-stu-id="e90e8-118">Qubit that stores the result of the comparison $x>y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e90e8-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e90e8-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="e90e8-120">Referenties</span><span class="sxs-lookup"><span data-stu-id="e90e8-120">References</span></span>

- <span data-ttu-id="e90e8-121">Een nieuwe Quantum rimpel: Voeg circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span><span class="sxs-lookup"><span data-stu-id="e90e8-121">A new quantum ripple-carry addition circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span></span>