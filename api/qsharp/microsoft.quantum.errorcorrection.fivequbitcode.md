---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCode
title: De functie FiveQubitCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCode
qsharp.summary: Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.
ms.openlocfilehash: 540dcf1eafa7449f386676a9a3c9562a4d4bf29c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853144"
---
# <a name="fivequbitcode-function"></a><span data-ttu-id="9b4a9-102">De functie FiveQubitCode</span><span class="sxs-lookup"><span data-stu-id="9b4a9-102">FiveQubitCode function</span></span>

<span data-ttu-id="9b4a9-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="9b4a9-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="9b4a9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9b4a9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9b4a9-105">Retourneert een QECC-waarde die de ⟦ 5, 1, 3 ⟧ code encoder en de decoder met in-place Syndrome meting.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-105">Returns a QECC value representing the ⟦5, 1, 3⟧ code encoder and decoder with in-place syndrome measurement.</span></span>

```qsharp
function FiveQubitCode () : Microsoft.Quantum.ErrorCorrection.QECC
```


## <a name="output--qecc"></a><span data-ttu-id="9b4a9-106">Uitvoer: [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span><span class="sxs-lookup"><span data-stu-id="9b4a9-106">Output : [QECC](xref:Microsoft.Quantum.ErrorCorrection.QECC)</span></span>

<span data-ttu-id="9b4a9-107">Retourneert een implementatie van een Quantum fout correctie code door een type op te geven `QECC` .</span><span class="sxs-lookup"><span data-stu-id="9b4a9-107">Returns an implementation of a quantum error correction code by specifying a `QECC` type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b4a9-108">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9b4a9-108">Remarks</span></span>

<span data-ttu-id="9b4a9-109">Deze code is onafhankelijk van de volgende twee documenten gevonden:</span><span class="sxs-lookup"><span data-stu-id="9b4a9-109">This code was found independently in the following two papers:</span></span>

- <span data-ttu-id="9b4a9-110">C.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-110">C.</span></span> <span data-ttu-id="9b4a9-111">HxBxD.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-111">H.</span></span> <span data-ttu-id="9b4a9-112">Bennett,, D. DiVincenzo, J. A.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-112">Bennett, D. DiVincenzo, J. A.</span></span> <span data-ttu-id="9b4a9-113">Smolin en W. K.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-113">Smolin and W. K.</span></span> <span data-ttu-id="9b4a9-114">Wootters, "gemengde status entanglement en Quantum fout correctie," fysiek. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 en</span><span class="sxs-lookup"><span data-stu-id="9b4a9-114">Wootters, "Mixed state entanglement and quantum error correction," Phys. Rev. A, 54 (1996) pp. 3824-3851; https://arxiv.org/abs/quant-ph/9604024 and</span></span>
- <span data-ttu-id="9b4a9-115">N.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-115">R.</span></span> <span data-ttu-id="9b4a9-116">LaFlamme, C. Miquel, J. P.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-116">Laflamme, C. Miquel, J. P.</span></span> <span data-ttu-id="9b4a9-117">Paz en W. H.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-117">Paz and W. H.</span></span> <span data-ttu-id="9b4a9-118">Zurek, "perfecte Quantum fout correctie code," fysiek. Rev. lett.</span><span class="sxs-lookup"><span data-stu-id="9b4a9-118">Zurek, "Perfect quantum error correction code," Phys. Rev. Lett.</span></span> <span data-ttu-id="9b4a9-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span><span class="sxs-lookup"><span data-stu-id="9b4a9-119">77 (1996) pp. 198-201; https://arxiv.org/abs/quant-ph/9602019</span></span>