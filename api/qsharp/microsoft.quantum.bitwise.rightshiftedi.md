---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: De functie RightShiftedI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b0ca7d3cb84c58429e9b3a29893a6140a717006b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705581"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="d72da-102">De functie RightShiftedI</span><span class="sxs-lookup"><span data-stu-id="d72da-102">RightShiftedI function</span></span>

<span data-ttu-id="d72da-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="d72da-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="d72da-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d72da-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d72da-105">Hiermee wordt de bitsgewijze weer gave van een getal naar rechts verplaatst met een opgegeven aantal bits.</span><span class="sxs-lookup"><span data-stu-id="d72da-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="d72da-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d72da-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="d72da-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d72da-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d72da-108">Het getal waarvan de bitsgewijze weer gave naar rechts wordt geschoven (minder significant).</span><span class="sxs-lookup"><span data-stu-id="d72da-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="d72da-109">bedrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d72da-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d72da-110">Het aantal bits dat `value` naar rechts wordt geschoven.</span><span class="sxs-lookup"><span data-stu-id="d72da-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="d72da-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d72da-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d72da-112">De waarde van `value` , naar geschoven op `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="d72da-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="d72da-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d72da-113">Remarks</span></span>

<span data-ttu-id="d72da-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="d72da-114">The following are equivalent:</span></span>

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```