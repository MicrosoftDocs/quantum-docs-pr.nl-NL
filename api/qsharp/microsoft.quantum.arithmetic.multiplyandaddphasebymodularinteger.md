---
uid: Microsoft.Quantum.Arithmetic.MultiplyAndAddPhaseByModularInteger
title: Bewerking MultiplyAndAddPhaseByModularInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MultiplyAndAddPhaseByModularInteger
qsharp.summary: The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.
ms.openlocfilehash: 1ca20b525d2a76e554d5a2e8d4f40060b5ef51cf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223864"
---
# <a name="multiplyandaddphasebymodularinteger-operation"></a><span data-ttu-id="3ec0f-102">Bewerking MultiplyAndAddPhaseByModularInteger</span><span class="sxs-lookup"><span data-stu-id="3ec0f-102">MultiplyAndAddPhaseByModularInteger operation</span></span>

<span data-ttu-id="3ec0f-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="3ec0f-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="3ec0f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3ec0f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3ec0f-105">Hetzelfde als MultiplyAndAddByModularInteger, maar er wordt van uitgegaan dat de summand integers codeert in QFT.</span><span class="sxs-lookup"><span data-stu-id="3ec0f-105">The same as MultiplyAndAddByModularInteger, but assumes that the summand encodes integers in QFT basis.</span></span>

```qsharp
operation MultiplyAndAddPhaseByModularInteger (constMultiplier : Int, modulus : Int, multiplier : Microsoft.Quantum.Arithmetic.LittleEndian, phaseSummand : Microsoft.Quantum.Arithmetic.PhaseLittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3ec0f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3ec0f-106">Input</span></span>

### <a name="constmultiplier--int"></a><span data-ttu-id="3ec0f-107">constMultiplier: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ec0f-107">constMultiplier : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ec0f-108">Een geheel getal $a $ dat moet worden toegevoegd aan elk basis status label.</span><span class="sxs-lookup"><span data-stu-id="3ec0f-108">An integer $a$ to be added to each basis state label.</span></span>


### <a name="modulus--int"></a><span data-ttu-id="3ec0f-109">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ec0f-109">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ec0f-110">De modulus $N $ die optellen en vermenigvuldigen met betrekking tot.</span><span class="sxs-lookup"><span data-stu-id="3ec0f-110">The modulus $N$ which addition and multiplication is taken with respect to.</span></span>


### <a name="multiplier--littleendian"></a><span data-ttu-id="3ec0f-111">vermenigvuldiger: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3ec0f-111">multiplier : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="3ec0f-112">Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt waarvan de waarde moet worden toegevoegd aan elk basis status label van `summand` .</span><span class="sxs-lookup"><span data-stu-id="3ec0f-112">A quantum register representing an unsigned integer whose value is to be added to each basis state label of `summand`.</span></span>


### <a name="phasesummand--phaselittleendian"></a><span data-ttu-id="3ec0f-113">phaseSummand: [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span><span class="sxs-lookup"><span data-stu-id="3ec0f-113">phaseSummand : [PhaseLittleEndian](xref:Microsoft.Quantum.Arithmetic.PhaseLittleEndian)</span></span>

<span data-ttu-id="3ec0f-114">Een Quantum register dat een niet-ondertekend geheel getal vertegenwoordigt dat moet worden gebruikt als doel voor deze bewerking.</span><span class="sxs-lookup"><span data-stu-id="3ec0f-114">A quantum register representing an unsigned integer to use as the target for this operation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3ec0f-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3ec0f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="3ec0f-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3ec0f-116">Remarks</span></span>

<span data-ttu-id="3ec0f-117">Er wordt van uitgegaan dat `phaseSummand` de hoogste bit is ingesteld op 0.</span><span class="sxs-lookup"><span data-stu-id="3ec0f-117">Assumes that `phaseSummand` has the highest bit set to 0.</span></span>
<span data-ttu-id="3ec0f-118">Er wordt ook van uitgegaan dat de waarde van `phaseSummand` kleiner is dan $N $.</span><span class="sxs-lookup"><span data-stu-id="3ec0f-118">Also assumes that the value of `phaseSummand` is less than $N$.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ec0f-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3ec0f-119">See Also</span></span>

- [<span data-ttu-id="3ec0f-120">Micro soft. Quantum. aritmetische. MultiplyAndAddByModularInteger</span><span class="sxs-lookup"><span data-stu-id="3ec0f-120">Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger</span></span>](xref:Microsoft.Quantum.Arithmetic.MultiplyAndAddByModularInteger)