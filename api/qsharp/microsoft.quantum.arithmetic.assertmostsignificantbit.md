---
uid: Microsoft.Quantum.Arithmetic.AssertMostSignificantBit
title: Bewerking AssertMostSignificantBit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertMostSignificantBit
qsharp.summary: Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.
ms.openlocfilehash: 408e50ed9f2e6c8ba35db20855608d2bd1f24eea
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707452"
---
# <a name="assertmostsignificantbit-operation"></a><span data-ttu-id="b8d0d-102">Bewerking AssertMostSignificantBit</span><span class="sxs-lookup"><span data-stu-id="b8d0d-102">AssertMostSignificantBit operation</span></span>

<span data-ttu-id="b8d0d-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="b8d0d-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="b8d0d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b8d0d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b8d0d-105">Beweringen dat de meest significante Qubit van een Qubit-REGI ster die een niet-ondertekend geheel getal vertegenwoordigt, zich in een bepaalde staat bevindt.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-105">Asserts that the most significant qubit of a qubit register representing an unsigned integer is in a particular state.</span></span>

```qsharp
operation AssertMostSignificantBit (value : Result, number : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="input"></a><span data-ttu-id="b8d0d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b8d0d-106">Input</span></span>

### <a name="value--__invalidresult__"></a><span data-ttu-id="b8d0d-107">waarde: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="b8d0d-107">value : __invalid<Result>__</span></span>

<span data-ttu-id="b8d0d-108">De waarde van de hoogste bit die wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-108">The value of the highest bit being asserted.</span></span>


### <a name="number--littleendian"></a><span data-ttu-id="b8d0d-109">nummer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="b8d0d-109">number : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="b8d0d-110">Niet-ondertekende integer waarvan de hoogste bit wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-110">Unsigned integer of which the highest bit is checked.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b8d0d-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b8d0d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b8d0d-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b8d0d-112">Remarks</span></span>

<span data-ttu-id="b8d0d-113">De gecontroleerde versie van deze bewerking negeert besturings elementen.</span><span class="sxs-lookup"><span data-stu-id="b8d0d-113">The controlled version of this operation ignores controls.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8d0d-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b8d0d-114">See Also</span></span>

- [<span data-ttu-id="b8d0d-115">Micro soft. Quantum. intrinsiek. assert</span><span class="sxs-lookup"><span data-stu-id="b8d0d-115">Microsoft.Quantum.Intrinsic.Assert</span></span>](xref:Microsoft.Quantum.Intrinsic.Assert)