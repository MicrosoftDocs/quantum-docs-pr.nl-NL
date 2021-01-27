---
uid: Microsoft.Quantum.Arithmetic.MeasureInteger
title: Bewerking MeasureInteger
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: MeasureInteger
qsharp.summary: Measures the content of a quantum register and converts it to an integer. The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.
ms.openlocfilehash: 288aee24e0ae6425db35312b560630a6bb9bfc80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843108"
---
# <a name="measureinteger-operation"></a><span data-ttu-id="2588e-102">Bewerking MeasureInteger</span><span class="sxs-lookup"><span data-stu-id="2588e-102">MeasureInteger operation</span></span>

<span data-ttu-id="2588e-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="2588e-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="2588e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2588e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2588e-105">Hiermee wordt de inhoud van een Quantum register gemeten en omgezet in een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="2588e-105">Measures the content of a quantum register and converts it to an integer.</span></span> <span data-ttu-id="2588e-106">De meting wordt uitgevoerd met betrekking tot de standaard berekening, d.w.z. de eigenbasis van `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="2588e-106">The measurement is performed with respect to the standard computational basis, i.e., the eigenbasis of `PauliZ`.</span></span>

```qsharp
operation MeasureInteger (target : Microsoft.Quantum.Arithmetic.LittleEndian) : Int
```


## <a name="input"></a><span data-ttu-id="2588e-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="2588e-107">Input</span></span>

### <a name="target--littleendian"></a><span data-ttu-id="2588e-108">doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="2588e-108">target : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="2588e-109">Een Quantum register in de code ring met little endian.</span><span class="sxs-lookup"><span data-stu-id="2588e-109">A quantum register in the little-endian encoding.</span></span>



## <a name="output--int"></a><span data-ttu-id="2588e-110">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2588e-110">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2588e-111">Een niet-ondertekend geheel getal dat de gemeten waarde van bevat `target` .</span><span class="sxs-lookup"><span data-stu-id="2588e-111">An unsigned integer that contains the measured value of `target`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2588e-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2588e-112">Remarks</span></span>

<span data-ttu-id="2588e-113">Met deze bewerking wordt de invoer register opnieuw ingesteld op de status $ \ket{00\cdots 0} $, die geschikt is om terug te gaan naar een doel machine.</span><span class="sxs-lookup"><span data-stu-id="2588e-113">This operation resets its input register to the $\ket{00\cdots 0}$ state, suitable for releasing back to a target machine.</span></span>

## <a name="see-also"></a><span data-ttu-id="2588e-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2588e-114">See Also</span></span>

- [<span data-ttu-id="2588e-115">Micro soft. Quantum. Canon. MeasureIntegerBE</span><span class="sxs-lookup"><span data-stu-id="2588e-115">Microsoft.Quantum.Canon.MeasureIntegerBE</span></span>](xref:Microsoft.Quantum.Canon.MeasureIntegerBE)