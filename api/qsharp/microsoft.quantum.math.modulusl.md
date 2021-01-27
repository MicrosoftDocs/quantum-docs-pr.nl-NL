---
uid: Microsoft.Quantum.Math.ModulusL
title: De functie ModulusL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842746"
---
# <a name="modulusl-function"></a><span data-ttu-id="2e75b-102">De functie ModulusL</span><span class="sxs-lookup"><span data-stu-id="2e75b-102">ModulusL function</span></span>

<span data-ttu-id="2e75b-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2e75b-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2e75b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2e75b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2e75b-105">Berekent het canonieke residu van `value` modulo `modulus` .</span><span class="sxs-lookup"><span data-stu-id="2e75b-105">Computes the canonical residue of `value` modulo `modulus`.</span></span>

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="2e75b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2e75b-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="2e75b-107">waarde: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2e75b-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2e75b-108">De waarde van welk residu wordt berekend</span><span class="sxs-lookup"><span data-stu-id="2e75b-108">The value of which residue is computed</span></span>


### <a name="modulus--bigint"></a><span data-ttu-id="2e75b-109">modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2e75b-109">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2e75b-110">De modulus waarmee residuen worden uitgevoerd, moet positief zijn</span><span class="sxs-lookup"><span data-stu-id="2e75b-110">The modulus by which residues are take, must be positive</span></span>



## <a name="output--bigint"></a><span data-ttu-id="2e75b-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2e75b-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2e75b-112">Geheel getal $r $ tussen 0 en `modulus - 1` dat `value - r` deelbaar is door modulus</span><span class="sxs-lookup"><span data-stu-id="2e75b-112">Integer $r$ between 0 and `modulus - 1` such that `value - r` is divisible by modulus</span></span>

## <a name="remarks"></a><span data-ttu-id="2e75b-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2e75b-113">Remarks</span></span>

<span data-ttu-id="2e75b-114">Deze functie werkt anders als de operator `%` zich in C# en Q # bevindt, zoals in het resultaat altijd een niet-negatief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.</span><span class="sxs-lookup"><span data-stu-id="2e75b-114">This function behaves different to how the operator `%` behaves in C# and Q# as in the result is always a non-negative integer between 0 and `modulus - 1`, even if value is negative.</span></span>