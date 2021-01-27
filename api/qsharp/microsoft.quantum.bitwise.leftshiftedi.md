---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: De functie LeftShiftedI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3f551bdba5c8e2a1456838769e4cee0660d0f969
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845310"
---
# <a name="leftshiftedi-function"></a><span data-ttu-id="d3e70-102">De functie LeftShiftedI</span><span class="sxs-lookup"><span data-stu-id="d3e70-102">LeftShiftedI function</span></span>

<span data-ttu-id="d3e70-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="d3e70-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="d3e70-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d3e70-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d3e70-105">Hiermee wordt de bitsgewijze weer gave van een getal overgelaten door een bepaald aantal bits.</span><span class="sxs-lookup"><span data-stu-id="d3e70-105">Shifts the bitwise representation of a number left by a given number of bits.</span></span>

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="d3e70-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d3e70-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="d3e70-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d3e70-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d3e70-108">Het getal waarvan de bitsgewijze weer gave naar links moet worden verplaatst (significanter).</span><span class="sxs-lookup"><span data-stu-id="d3e70-108">The number whose bitwise representation is to be shifted to the left (more significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="d3e70-109">bedrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d3e70-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d3e70-110">Het aantal bits dat `value` naar links moet worden verplaatst.</span><span class="sxs-lookup"><span data-stu-id="d3e70-110">The number of bits by which `value` is to be shifted to the left.</span></span>



## <a name="output--int"></a><span data-ttu-id="d3e70-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d3e70-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d3e70-112">De waarde van `value` , naar links geschoven op `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="d3e70-112">The value of `value`, shifted left by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3e70-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d3e70-113">Remarks</span></span>

<span data-ttu-id="d3e70-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="d3e70-114">The following are equivalent:</span></span>

```qsharp
let c = a <<< b;
let c = LeftShiftedI(a, b);
```