---
uid: Microsoft.Quantum.Math.ModulusL
title: De functie ModulusL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: e7e692059051fde295634c37892ec54e2cf1b095
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709121"
---
# <a name="modulusl-function"></a><span data-ttu-id="9e6b4-102">De functie ModulusL</span><span class="sxs-lookup"><span data-stu-id="9e6b4-102">ModulusL function</span></span>

<span data-ttu-id="9e6b4-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="9e6b4-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="9e6b4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9e6b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9e6b4-105">Berekent het canonieke residu van `value` modulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="9e6b4-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="9e6b4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9e6b4-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="9e6b4-107">waarde: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9e6b4-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9e6b4-108">De waarde van welk residu wordt berekend</span><span class="sxs-lookup"><span data-stu-id="9e6b4-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="9e6b4-109">modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9e6b4-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9e6b4-110">De modulus waarmee residuen worden uitgevoerd, moet positief zijn</span><span class="sxs-lookup"><span data-stu-id="9e6b4-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="9e6b4-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9e6b4-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9e6b4-112">Geheel getal $r $ tussen 0 en `modulus - 1` dat `value - r` deelbaar is door modulus</span><span class="sxs-lookup"><span data-stu-id="9e6b4-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6b4-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9e6b4-113">Remarks</span></span>

<span data-ttu-id="9e6b4-114">Deze functie werkt anders als de operator `%` zich gedraagt in C# en Q # als in het resultaat altijd een positief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.</span><span class="sxs-lookup"><span data-stu-id="9e6b4-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a positive integer between 0 and `modulus - 1`, even if value is negative.</span></span>