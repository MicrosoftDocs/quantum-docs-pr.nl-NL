---
uid: Microsoft.Quantum.Arithmetic.AssertPhaseLessThan
title: Bewerking AssertPhaseLessThan
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertPhaseLessThan
qsharp.summary: Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.
ms.openlocfilehash: d003d83a84356ce52c5601135000813c7f119e4d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707445"
---
# <a name="assertphaselessthan-operation"></a><span data-ttu-id="3b7b9-102">Bewerking AssertPhaseLessThan</span><span class="sxs-lookup"><span data-stu-id="3b7b9-102">AssertPhaseLessThan operation</span></span>

<span data-ttu-id="3b7b9-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3b7b9-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3b7b9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3b7b9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3b7b9-105">Beweringen dat de `number` versleutelde in PhaseLittleEndian kleiner is dan `value` .</span><span class="sxs-lookup"><span data-stu-id="3b7b9-105">Asserts that the `number` encoded in PhaseLittleEndian is less than `value`.</span></span>

```qsharp
operation AssertPhaseLessThan (value : Int, number : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="3b7b9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3b7b9-106">Input</span></span>

### <a name="value--int"></a><span data-ttu-id="3b7b9-107">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3b7b9-107">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3b7b9-108">`number` moet kleiner zijn dan dit.</span><span class="sxs-lookup"><span data-stu-id="3b7b9-108">`number` must be less than this.</span></span>


### <a name="number--phaselittleendian"></a><span data-ttu-id="3b7b9-109">nummer: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3b7b9-109">number : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="3b7b9-110">Niet-ondertekend geheel getal dat is vergeleken met `value` .</span><span class="sxs-lookup"><span data-stu-id="3b7b9-110">Unsigned integer which is compared to `value`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3b7b9-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3b7b9-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3b7b9-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3b7b9-112">Remarks</span></span>

<span data-ttu-id="3b7b9-113">De gecontroleerde versie van deze bewerking negeert besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="3b7b9-113">The controlled version of this operation ignores controls.</span></span>