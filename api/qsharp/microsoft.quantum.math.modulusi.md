---
uid: Microsoft.Quantum.Math.ModulusI
title: De functie ModulusI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 3f698a00b2c8d94b7cb3cca4f1721c659918f4a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708262"
---
# <a name="modulusi-function"></a><span data-ttu-id="dd363-102">De functie ModulusI</span><span class="sxs-lookup"><span data-stu-id="dd363-102">ModulusI function</span></span>

<span data-ttu-id="dd363-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="dd363-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="dd363-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dd363-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dd363-105">Berekent het canonieke residu van `value` modulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="dd363-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="dd363-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="dd363-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="dd363-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dd363-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dd363-108">De waarde van welk residu wordt berekend</span><span class="sxs-lookup"><span data-stu-id="dd363-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="dd363-109">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dd363-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dd363-110">De modulus waarmee residuen worden uitgevoerd, moet positief zijn</span><span class="sxs-lookup"><span data-stu-id="dd363-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="dd363-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dd363-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dd363-112">Geheel getal $r $ tussen 0 en `modulus - 1` dat `value - r` deelbaar is door modulus</span><span class="sxs-lookup"><span data-stu-id="dd363-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="dd363-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dd363-113">Remarks</span></span>

<span data-ttu-id="dd363-114">Deze functie werkt anders als de operator `%` zich gedraagt in C# en Q # als in het resultaat altijd een positief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.</span><span class="sxs-lookup"><span data-stu-id="dd363-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>