---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: De functie LeftShiftedL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 17e5c845755f74e9703381bc82bfd63be836d038
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705620"
---
# <a name="leftshiftedl-function"></a><span data-ttu-id="90ad1-102">De functie LeftShiftedL</span><span class="sxs-lookup"><span data-stu-id="90ad1-102">LeftShiftedL function</span></span>

<span data-ttu-id="90ad1-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="90ad1-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="90ad1-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="90ad1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="90ad1-105">Hiermee wordt de bitsgewijze weer gave van een getal overgelaten door een bepaald aantal bits.</span><span class="sxs-lookup"><span data-stu-id="90ad1-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="90ad1-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="90ad1-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="90ad1-107">waarde: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="90ad1-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="90ad1-108">Het getal waarvan de bitsgewijze weer gave naar links moet worden verplaatst (significanter).</span><span class="sxs-lookup"><span data-stu-id="90ad1-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="90ad1-109">bedrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="90ad1-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="90ad1-110">Het aantal bits dat `value` naar links moet worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="90ad1-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="90ad1-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="90ad1-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="90ad1-112">De waarde van `value` , naar links geschoven op `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="90ad1-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ad1-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="90ad1-113">Remarks</span></span>

<span data-ttu-id="90ad1-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="90ad1-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedL(a, b);
```