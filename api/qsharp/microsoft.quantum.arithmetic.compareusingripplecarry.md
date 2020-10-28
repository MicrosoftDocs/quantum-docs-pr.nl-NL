---
uid: Microsoft.Quantum.Arithmetic.CompareUsingRippleCarry
title: Bewerking CompareUsingRippleCarry
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: CompareUsingRippleCarry
qsharp.summary: This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.
ms.openlocfilehash: 842e7ded1e38f4f6e01e79d2758e30afb85dd349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707380"
---
# <a name="compareusingripplecarry-operation"></a><span data-ttu-id="0a30b-102">Bewerking CompareUsingRippleCarry</span><span class="sxs-lookup"><span data-stu-id="0a30b-102">CompareUsingRippleCarry operation</span></span>

<span data-ttu-id="0a30b-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0a30b-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0a30b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="0a30b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="0a30b-105">Met deze bewerking wordt getest of een geheel getal dat wordt vertegenwoordigd door een REGI ster van qubits groter is dan een ander geheel getal, waarbij een XOR van het resultaat wordt toegepast op een uitvoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="0a30b-105">This operation tests if an integer represented by a register of qubits is greater than another integer, applying an XOR of the result onto an output qubit.</span></span>

```qsharp
operation CompareUsingRippleCarry (x : Microsoft.Quantum.Arithmetic.LittleEndian, y : Microsoft.Quantum.Arithmetic.LittleEndian, output : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="0a30b-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="0a30b-106">Description</span></span>

<span data-ttu-id="0a30b-107">Als er twee gehele getallen zijn opgegeven `x` en `y` zijn opgeslagen in Qubit-registers met een gelijke grootte, controleert deze bewerking of ze voldoen `x > y` .</span><span class="sxs-lookup"><span data-stu-id="0a30b-107">Given two integers `x` and `y` stored in equal-size qubit registers, this operation checks if they satisfy `x > y`.</span></span> <span data-ttu-id="0a30b-108">Als deze waarde True is, wordt 1 XORed in een uitvoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="0a30b-108">If true, 1 is XORed into an output qubit.</span></span> <span data-ttu-id="0a30b-109">Anders wordt 0 XORed in een uitvoer Qubit.</span><span class="sxs-lookup"><span data-stu-id="0a30b-109">Otherwise, 0 is XORed into an output qubit.</span></span>
<span data-ttu-id="0a30b-110">Met andere woorden, deze bewerking kan worden weer gegeven door de unitary $ $ \begin{align} U\ket {x} \ Ket {y} \ Ket {z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span><span class="sxs-lookup"><span data-stu-id="0a30b-110">In other words, this operation can be represented by the unitary $$ \begin{align} U\ket{x}\ket{y}\ket{z} = \ket{x}\ket{y}\ket{z\oplus (x>y)}.</span></span>
<span data-ttu-id="0a30b-111">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="0a30b-111">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="0a30b-112">Invoer</span><span class="sxs-lookup"><span data-stu-id="0a30b-112">Input</span></span>

### <a name="x--littleendian"></a><span data-ttu-id="0a30b-113">x: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0a30b-113">x : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0a30b-114">Het eerste getal dat moet worden vergeleken, wordt opgeslagen in `LittleEndian` de indeling in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="0a30b-114">First number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="y--littleendian"></a><span data-ttu-id="0a30b-115">y: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="0a30b-115">y : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="0a30b-116">Het tweede getal dat moet worden vergeleken, wordt opgeslagen in `LittleEndian` de indeling in een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="0a30b-116">Second number to be compared stored in `LittleEndian` format in a qubit register.</span></span>


### <a name="output--qubit"></a><span data-ttu-id="0a30b-117">uitvoer: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="0a30b-117">output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="0a30b-118">Qubit waarin het resultaat van de vergelijking wordt opgeslagen $x>y $.</span><span class="sxs-lookup"><span data-stu-id="0a30b-118">Qubit that stores the result of the comparison $x>y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0a30b-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0a30b-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="references"></a><span data-ttu-id="0a30b-120">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="0a30b-120">References</span></span>

- <span data-ttu-id="0a30b-121">Een nieuwe Quantum rimpel: Voeg circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span><span class="sxs-lookup"><span data-stu-id="0a30b-121">A new quantum ripple-carry addition circuit Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton https://arxiv.org/abs/quant-ph/0410184</span></span>