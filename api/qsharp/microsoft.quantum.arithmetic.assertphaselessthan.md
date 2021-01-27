---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Bewerking AssertPhaseLessThan
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: 7b7a4fea8973727da4dcab6f739c6db8da835a2f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843432"
---
# <a name="assertphaselessthan-operation"></a><span data-ttu-id="4a303-102">Bewerking AssertPhaseLessThan</span><span class="sxs-lookup"><span data-stu-id="4a303-102">AssertPhaseLessThan operation</span></span>

<span data-ttu-id="4a303-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="4a303-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="4a303-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4a303-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4a303-105">Beweringen dat de `number` versleutelde in PhaseLittleEndian kleiner is dan `value` .</span><span class="sxs-lookup"><span data-stu-id="4a303-105">Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.</span></span>

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="4a303-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4a303-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="4a303-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4a303-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4a303-108">`number` moet kleiner zijn dan dit.</span><span class="sxs-lookup"><span data-stu-id="4a303-108">`number` must be less than this.</span></span>


### <a name="number--phaselittleendian"></a><span data-ttu-id="4a303-109">nummer: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="4a303-109">number : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="4a303-110">Niet-ondertekend geheel getal dat is vergeleken met `value` .</span><span class="sxs-lookup"><span data-stu-id="4a303-110">Unsigned integer which is compared to `value`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="4a303-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="4a303-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="4a303-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4a303-112">Remarks</span></span>

<span data-ttu-id="4a303-113">De gecontroleerde versie van deze bewerking negeert besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="4a303-113">The controlled version of this operation ignores controls.</span></span>