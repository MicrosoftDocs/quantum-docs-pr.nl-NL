---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: De functie FiveQubitCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 3b45af29897735905f7fe52340e2a8e425bd8cbe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200880"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="fc42b-102">De functie FiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="fc42b-102">FiveQubitCode function</span></span>

<span data-ttu-id="fc42b-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="fc42b-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="fc42b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fc42b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fc42b-105">Retourneert een QECC-waarde die de ⟦ 5, 1, 3 ⟧ code encoder en de decoder met in-place Syndrome meting.</span><span class="sxs-lookup"><span data-stu-id="fc42b-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="fc42b-106">Uitvoer: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="fc42b-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="fc42b-107">Retourneert een implementatie van een Quantum fout correctie code door een type op te geven `QECC` .</span><span class="sxs-lookup"><span data-stu-id="fc42b-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc42b-108">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fc42b-108">Remarks</span></span>

<span data-ttu-id="fc42b-109">Deze code is onafhankelijk van de volgende twee documenten gevonden:</span><span class="sxs-lookup"><span data-stu-id="fc42b-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="fc42b-110">C.</span><span class="sxs-lookup"><span data-stu-id="fc42b-110">C.</span></span> <span data-ttu-id="fc42b-111">HxBxD.</span><span class="sxs-lookup"><span data-stu-id="fc42b-111">H.</span></span> <span data-ttu-id="fc42b-112">Bennett,, D. DiVincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="fc42b-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="fc42b-113">Smolin en W. K.</span><span class="sxs-lookup"><span data-stu-id="fc42b-113">Smolin and W. K.</span></span> <span data-ttu-id="fc42b-114">Wootters, "gemengde status entanglement en Quantum fout correctie," fysiek. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 en</span><span class="sxs-lookup"><span data-stu-id="fc42b-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="fc42b-115">N.</span><span class="sxs-lookup"><span data-stu-id="fc42b-115">R.</span></span> <span data-ttu-id="fc42b-116">LaFlamme, C. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="fc42b-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="fc42b-117">Paz en W. H.</span><span class="sxs-lookup"><span data-stu-id="fc42b-117">Paz and W. H.</span></span> <span data-ttu-id="fc42b-118">Zurek, "perfecte Quantum fout correctie code," fysiek. Rev. lett.</span><span class="sxs-lookup"><span data-stu-id="fc42b-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="fc42b-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="fc42b-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>