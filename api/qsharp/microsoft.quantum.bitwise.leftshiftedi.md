---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: De functie LeftShiftedI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: ce68311adf211169c2fb499bb189332370a6d6ac
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705637"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="ca4f7-102">De functie LeftShiftedI</span><span class="sxs-lookup"><span data-stu-id="ca4f7-102">LeftShiftedI function</span></span>

<span data-ttu-id="ca4f7-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="ca4f7-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="ca4f7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ca4f7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ca4f7-105">Hiermee wordt de bitsgewijze weer gave van een getal overgelaten door een bepaald aantal bits.</span><span class="sxs-lookup"><span data-stu-id="ca4f7-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="ca4f7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ca4f7-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="ca4f7-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ca4f7-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ca4f7-108">Het getal waarvan de bitsgewijze weer gave naar links moet worden verplaatst (significanter).</span><span class="sxs-lookup"><span data-stu-id="ca4f7-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="ca4f7-109">bedrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ca4f7-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ca4f7-110">Het aantal bits dat `value` naar links moet worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="ca4f7-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="ca4f7-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ca4f7-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ca4f7-112">De waarde van `value` , naar links geschoven op `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="ca4f7-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca4f7-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ca4f7-113">Remarks</span></span>

<span data-ttu-id="ca4f7-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="ca4f7-114">The following are equivalent:</span></span>

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```