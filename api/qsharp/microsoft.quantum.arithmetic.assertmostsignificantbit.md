---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Bewerking AssertMostSignificantBit
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 41381455d1a96970647f887e038f7dff3a4eb204
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223779"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="586ae-102">Bewerking AssertMostSignificantBit</span><span class="sxs-lookup"><span data-stu-id="586ae-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="586ae-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="586ae-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="586ae-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="586ae-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="586ae-105">Beweringen dat de meest significante Qubit van een Qubit-REGI ster die een niet-ondertekend geheel getal vertegenwoordigt, zich in een bepaalde staat bevindt.</span><span class="sxs-lookup"><span data-stu-id="586ae-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="586ae-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="586ae-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="586ae-107">waarde: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="586ae-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="586ae-108">De waarde van de hoogste bit die wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="586ae-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="586ae-109">nummer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="586ae-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="586ae-110">Niet-ondertekende integer waarvan de hoogste bit wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="586ae-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="586ae-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="586ae-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="586ae-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="586ae-112">Remarks</span></span>

<span data-ttu-id="586ae-113">De gecontroleerde versie van deze bewerking negeert besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="586ae-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="586ae-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="586ae-114">See Also</span></span>

- [<span data-ttu-id="586ae-115">Micro soft. Quantum. intrinsiek. assert</span><span class="sxs-lookup"><span data-stu-id="586ae-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)