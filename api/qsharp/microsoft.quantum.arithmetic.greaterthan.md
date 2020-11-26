---
uid: Microsoft.Quantum.Arithmetic.GreaterThan
title: Bewerking GreaterThan
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: GreaterThan
qsharp.summary: Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.
ms.openlocfilehash: 644d68affbdb508938f76de5025a1a463e7284e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223082"
---
# <a name="greaterthan-operation"></a><span data-ttu-id="79efa-102">Bewerking GreaterThan</span><span class="sxs-lookup"><span data-stu-id="79efa-102">GreaterThan operation</span></span>

<span data-ttu-id="79efa-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="79efa-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="79efa-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="79efa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="79efa-105">Past een groter-dan-vergelijking toe tussen twee gehele getallen die zijn gecodeerd in Qubit-journalen, waarbij een doel-Qubit wordt gespiegeld op basis van het resultaat van de vergelijking.</span><span class="sxs-lookup"><span data-stu-id="79efa-105">Applies a greater-than comparison between two integers encoded into qubit registers, flipping a target qubit based on the result of the comparison.</span></span>

```qsharp
operation GreaterThan (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="79efa-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="79efa-106">Description</span></span>

<span data-ttu-id="79efa-107">Voert een strikt groter dan vergelijking van twee gehele getallen uit $x $ en $y $, gecodeerd in Qubit registreert XS en kalenderda.</span><span class="sxs-lookup"><span data-stu-id="79efa-107">Carries out a strictly greater than comparison of two integers $x$ and $y$, encoded in qubit registers xs and ys.</span></span> <span data-ttu-id="79efa-108">Als $x > y $, wordt het resultaat Qubit gespiegeld, anders behoudt het resultaat Qubit de status.</span><span class="sxs-lookup"><span data-stu-id="79efa-108">If $x > y$, then the result qubit will be flipped, otherwise the result qubit will retain its state.</span></span>

## <a name="input"></a><span data-ttu-id="79efa-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="79efa-109">Input</span></span>

### <a name="xs--littleendian"></a><span data-ttu-id="79efa-110">XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="79efa-110">xs : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="79efa-111">LittleEndian Qubit Registreer Codeer de eerste integer $x $.</span><span class="sxs-lookup"><span data-stu-id="79efa-111">LittleEndian qubit register encoding the first integer $x$.</span></span>


### <a name="ys--littleendian"></a><span data-ttu-id="79efa-112">kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="79efa-112">ys : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="79efa-113">LittleEndian Qubit Registreer code ring de tweede integer $y $.</span><span class="sxs-lookup"><span data-stu-id="79efa-113">LittleEndian qubit register encoding the second integer $y$.</span></span>


### <a name="result--qubit"></a><span data-ttu-id="79efa-114">resultaat: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="79efa-114">result : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="79efa-115">Eén Qubit die wordt gespiegeld als $x > y $.</span><span class="sxs-lookup"><span data-stu-id="79efa-115">Single qubit that will be flipped if $x > y$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="79efa-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="79efa-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="79efa-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="79efa-117">Remarks</span></span>

<span data-ttu-id="79efa-118">Maakt gebruik van de slag die $x-y = (x ' + y) ' $, waarbij ' de complement vormt.</span><span class="sxs-lookup"><span data-stu-id="79efa-118">Uses the trick that $x - y = (x'+y)'$, where ' denotes the one's complement.</span></span>

## <a name="references"></a><span data-ttu-id="79efa-119">Referenties</span><span class="sxs-lookup"><span data-stu-id="79efa-119">References</span></span>

- <span data-ttu-id="79efa-120">Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.</span><span class="sxs-lookup"><span data-stu-id="79efa-120">Steven A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "A new quantum ripple-carry addition circuit", 2004.</span></span>
  https://arxiv.org/abs/quant-ph/0410184v1

- <span data-ttu-id="79efa-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "factoring met behulp van 2n + 2 qubits met op Toffoli gebaseerde modulaire vermenigvuldiging", 2016 https://arxiv.org/abs/1611.07995</span><span class="sxs-lookup"><span data-stu-id="79efa-121">Thomas Haener, Martin Roetteler, Krysta M. Svore: "Factoring using 2n+2 qubits with Toffoli based modular multiplication", 2016 https://arxiv.org/abs/1611.07995</span></span>