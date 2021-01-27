---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: De functie RightShiftedL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 03ed69c7151e62b91c4a036e301f99b45ce5ab62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842101"
---
# <a name="rightshiftedl-function"></a><span data-ttu-id="0fc94-102">De functie RightShiftedL</span><span class="sxs-lookup"><span data-stu-id="0fc94-102">RightShiftedL function</span></span>

<span data-ttu-id="0fc94-103">Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)</span><span class="sxs-lookup"><span data-stu-id="0fc94-103">Namespace: [Microsoft.Quantum.Bitwise](xref:Microsoft.Quantum.Bitwise)</span></span>

<span data-ttu-id="0fc94-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0fc94-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0fc94-105">Hiermee wordt de bitsgewijze weer gave van een getal naar rechts verplaatst met een opgegeven aantal bits.</span><span class="sxs-lookup"><span data-stu-id="0fc94-105">Shifts the bitwise representation of a number right by a given number of bits.</span></span>

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a><span data-ttu-id="0fc94-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0fc94-106">Input</span></span>

### <a name="value--bigint"></a><span data-ttu-id="0fc94-107">waarde: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0fc94-107">value : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0fc94-108">Het getal waarvan de bitsgewijze weer gave naar rechts wordt geschoven (minder significant).</span><span class="sxs-lookup"><span data-stu-id="0fc94-108">The number whose bitwise representation is to be shifted to the right (less significant).</span></span>


### <a name="amount--int"></a><span data-ttu-id="0fc94-109">bedrag: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0fc94-109">amount : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0fc94-110">Het aantal bits dat `value` naar rechts wordt geschoven.</span><span class="sxs-lookup"><span data-stu-id="0fc94-110">The number of bits by which `value` is to be shifted to the right.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="0fc94-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="0fc94-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="0fc94-112">De waarde van `value` , naar geschoven op `amount` bits.</span><span class="sxs-lookup"><span data-stu-id="0fc94-112">The value of `value`, shifted right by `amount` bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fc94-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0fc94-113">Remarks</span></span>

<span data-ttu-id="0fc94-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="0fc94-114">The following are equivalent:</span></span>

```qsharp
let c = a >>> b;
let c = RightShiftedL(a, b);
```