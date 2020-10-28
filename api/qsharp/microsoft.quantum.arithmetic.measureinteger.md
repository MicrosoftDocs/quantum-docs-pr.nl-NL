---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Bewerking MeasureInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 7cd2d93332eb168c7c2be92a3b910033ca8c10ae
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707173"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="6fbfe-102">Bewerking MeasureInteger</span><span class="sxs-lookup"><span data-stu-id="6fbfe-102">MeasureInteger operation</span></span>

<span data-ttu-id="6fbfe-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6fbfe-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6fbfe-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6fbfe-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6fbfe-105">Hiermee wordt de inhoud van een Quantum register gemeten en omgezet in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="6fbfe-106">De meting wordt uitgevoerd met betrekking tot de standaard berekening, d.w.z. de eigenbasis van `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="6fbfe-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="6fbfe-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="6fbfe-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="6fbfe-108">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6fbfe-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6fbfe-109">Een Quantum register in de code ring met little endian.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="6fbfe-110">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6fbfe-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6fbfe-111">Een niet-ondertekend geheel getal dat de gemeten waarde van bevat `target` .</span><span class="sxs-lookup"><span data-stu-id="6fbfe-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fbfe-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6fbfe-112">Remarks</span></span>

<span data-ttu-id="6fbfe-113">Met deze bewerking wordt de invoer register opnieuw ingesteld op de status $ \ket{00\cdots 0} $, die geschikt is om terug te gaan naar een doel machine.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="6fbfe-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6fbfe-114">See Also</span></span>

- [<span data-ttu-id="6fbfe-115">Micro soft. Quantum. Canon. MeasureIntegerBE</span><span class="sxs-lookup"><span data-stu-id="6fbfe-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)