---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: De functie RightShiftedI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 5c3106eb73178554184cbfb37333c027805c69f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845261"
---
# <a name="rightshiftedi-function"></a><span data-ttu-id="f4720-102">De functie RightShiftedI</span><span class="sxs-lookup"><span data-stu-id="f4720-102">RightShiftedI function</span></span>

<span data-ttu-id="f4720-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="f4720-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="f4720-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f4720-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f4720-105">Hiermee wordt de bitsgewijze weer gave van een getal naar rechts verplaatst met een opgegeven aantal bits.</span><span class="sxs-lookup"><span data-stu-id="f4720-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a><span data-ttu-id="f4720-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f4720-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="f4720-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4720-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4720-108">Het getal waarvan de bitsgewijze weer gave naar rechts wordt geschoven (minder significant).</span><span class="sxs-lookup"><span data-stu-id="f4720-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="f4720-109">bedrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4720-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4720-110">Het aantal bits dat `value` naar rechts wordt geschoven.</span><span class="sxs-lookup"><span data-stu-id="f4720-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--int"></a><span data-ttu-id="f4720-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f4720-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f4720-112">De waarde van `value` , naar geschoven op `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="f4720-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4720-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f4720-113">Remarks</span></span>

<span data-ttu-id="f4720-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="f4720-114">The following are equivalent:</span></span>

```qsharp
let c = a >>> b;
let c = RightShiftedI(a, b);
```