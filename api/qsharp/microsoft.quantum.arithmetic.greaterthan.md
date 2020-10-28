---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: Bewerking GreaterThan
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: b7214b43dacd07b4750be4b681f30937185ac953
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707285"
---
# <a name="greaterthan-operation"></a><span data-ttu-id="664a9-102">Bewerking GreaterThan</span><span class="sxs-lookup"><span data-stu-id="664a9-102">GreaterThan operation</span></span>

<span data-ttu-id="664a9-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="664a9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="664a9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="664a9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="664a9-105">Past een groter-dan-vergelijking toe tussen twee gehele getallen die zijn gecodeerd in Qubit-journalen, waarbij een doel-Qubit wordt gespiegeld op basis van het resultaat van de vergelijking.</span><span class="sxs-lookup"><span data-stu-id="664a9-105">Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.</span></span>

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="664a9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="664a9-106">Description</span></span>

<span data-ttu-id="664a9-107">Voert een strikt groter dan vergelijking van twee gehele getallen uit $x $ en $y $, gecodeerd in Qubit registreert XS en kalenderda.</span><span class="sxs-lookup"><span data-stu-id="664a9-107">Carries out a strictly greater than comparison of two integers $x$ and $y$, encoded in qubit registers xs and ys.</span></span> <span data-ttu-id="664a9-108">Als $x > y $, wordt het resultaat Qubit gespiegeld, anders behoudt het resultaat Qubit de status.</span><span class="sxs-lookup"><span data-stu-id="664a9-108">If $x > y$, then the result qubit will be flipped, otherwise the result qubit will retain its state.</span></span>

## <a name="input"></a><span data-ttu-id="664a9-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="664a9-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="664a9-110">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="664a9-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="664a9-111">LittleEndian Qubit Registreer Codeer de eerste integer $x $.</span><span class="sxs-lookup"><span data-stu-id="664a9-111">LittleEndian qubit register encoding the first integer $x$.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="664a9-112">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="664a9-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="664a9-113">LittleEndian Qubit Registreer code ring de tweede integer $y $.</span><span class="sxs-lookup"><span data-stu-id="664a9-113">LittleEndian qubit register encoding the second integer $y$.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="664a9-114">resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="664a9-114">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="664a9-115">Eén Qubit die wordt gespiegeld als $x > y $.</span><span class="sxs-lookup"><span data-stu-id="664a9-115">Single qubit that will be flipped if $x > y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="664a9-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="664a9-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="664a9-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="664a9-117">Remarks</span></span>

<span data-ttu-id="664a9-118">Maakt gebruik van de slag die $x-y = (x ' + y) ' $, waarbij ' de complement vormt.</span><span class="sxs-lookup"><span data-stu-id="664a9-118">Uses the trick that $x - y = (x'+y)'$, where ' denotes the one's complement.</span></span>

## <a name="references"></a><span data-ttu-id="664a9-119">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="664a9-119">References</span></span>

- <span data-ttu-id="664a9-120">Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="664a9-120">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1

- <span data-ttu-id="664a9-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "factoring met behulp van 2n + 2 qubits met op Toffoli gebaseerde modulaire vermenigvuldiging", 2016 https://arxiv.org/abs/1611.07995</span><span class="sxs-lookup"><span data-stu-id="664a9-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "Factoring using 2n+2 qubits with Toffoli based modular multiplication", 2016 https://arxiv.org/abs/1611.07995</span></span>