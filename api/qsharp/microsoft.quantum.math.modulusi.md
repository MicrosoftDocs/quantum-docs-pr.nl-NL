---
uid: Microsoft.Quantum.Math.ModulusI
title: De functie ModulusI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6bbb3877b93e1fc6b38f85a716ba617311c7cfba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96227774"
---
# <a name="modulusi-function"></a><span data-ttu-id="2393c-102">De functie ModulusI</span><span class="sxs-lookup"><span data-stu-id="2393c-102">ModulusI function</span></span>

<span data-ttu-id="2393c-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2393c-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2393c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2393c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2393c-105">Berekent het canonieke residu van `value` modulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="2393c-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a><span data-ttu-id="2393c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2393c-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="2393c-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2393c-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2393c-108">De waarde van welk residu wordt berekend</span><span class="sxs-lookup"><span data-stu-id="2393c-108">The value of which residue is computed</span></span>


### <a name="modulus--int"></a><span data-ttu-id="2393c-109">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2393c-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2393c-110">De modulus waarmee residuen worden uitgevoerd, moet positief zijn</span><span class="sxs-lookup"><span data-stu-id="2393c-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--int"></a><span data-ttu-id="2393c-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2393c-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2393c-112">Geheel getal $r $ tussen 0 en `modulus - 1` dat `value - r` deelbaar is door modulus</span><span class="sxs-lookup"><span data-stu-id="2393c-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="2393c-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2393c-113">Remarks</span></span>

<span data-ttu-id="2393c-114">Deze functie werkt anders als de operator `%` zich gedraagt in C# en Q # als in het resultaat altijd een positief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.</span><span class="sxs-lookup"><span data-stu-id="2393c-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>