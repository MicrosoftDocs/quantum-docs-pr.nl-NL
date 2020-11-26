---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Bewerking MeasureInteger
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: e3ff06e5cbb2ef8a63e4ad12308b382347c90fc3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222640"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="6eb14-102">Bewerking MeasureInteger</span><span class="sxs-lookup"><span data-stu-id="6eb14-102">MeasureInteger operation</span></span>

<span data-ttu-id="6eb14-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="6eb14-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="6eb14-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6eb14-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6eb14-105">Hiermee wordt de inhoud van een Quantum register gemeten en omgezet in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="6eb14-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="6eb14-106">De meting wordt uitgevoerd met betrekking tot de standaard berekening, d.w.z. de eigenbasis van `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="6eb14-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="6eb14-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="6eb14-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="6eb14-108">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="6eb14-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="6eb14-109">Een Quantum register in de code ring met little endian.</span><span class="sxs-lookup"><span data-stu-id="6eb14-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="6eb14-110">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6eb14-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="6eb14-111">Een niet-ondertekend geheel getal dat de gemeten waarde van bevat `target` .</span><span class="sxs-lookup"><span data-stu-id="6eb14-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eb14-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6eb14-112">Remarks</span></span>

<span data-ttu-id="6eb14-113">Met deze bewerking wordt de invoer register opnieuw ingesteld op de status $ \ket{00\cdots 0} $, die geschikt is om terug te gaan naar een doel machine.</span><span class="sxs-lookup"><span data-stu-id="6eb14-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="6eb14-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6eb14-114">See Also</span></span>

- [<span data-ttu-id="6eb14-115">Micro soft. Quantum. Canon. MeasureIntegerBE</span><span class="sxs-lookup"><span data-stu-id="6eb14-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)