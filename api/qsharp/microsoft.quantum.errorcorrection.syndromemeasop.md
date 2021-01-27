---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Door de gebruiker gedefinieerd SyndromeMeasOp-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 36336f9e47e5f360cf5e19ffb6e15b4af88b2580
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850053"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="a84c0-102">Door de gebruiker gedefinieerd SyndromeMeasOp-type</span><span class="sxs-lookup"><span data-stu-id="a84c0-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="a84c0-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="a84c0-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="a84c0-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a84c0-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a84c0-105">Hiermee wordt een bewerking aangeduid die wordt gebruikt om de Syndrome van een fout-correct code blok te meten.</span><span class="sxs-lookup"><span data-stu-id="a84c0-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="example"></a><span data-ttu-id="a84c0-106">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a84c0-106">Example</span></span>

<span data-ttu-id="a84c0-107">Meet Syndromes voor de bits-Flip code $S = \langle ZZI, IZZ \rangle $ lege qubits op een niet-fout tolerante manier:</span><span class="sxs-lookup"><span data-stu-id="a84c0-107">Measure syndromes for the bit-flip code $S = \langle ZZI, IZZ \rangle$ using scratch qubits in a non–fault tolerant manner:</span></span>

```qsharp
    let syndMeasOp = SyndromeMeasOp(MeasureStabilizerGenerators([
            [PauliZ, PauliZ, PauliI],
            [PauliI, PauliZ, PauliZ]
        ], _, MeasureWithScratch));
```

## <a name="remarks"></a><span data-ttu-id="a84c0-108">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a84c0-108">Remarks</span></span>

<span data-ttu-id="a84c0-109">De hand tekening `(LogicalRegister => Syndrome)` vertegenwoordigt een bewerking die gezamenlijk werkt op de qubits in `LogicalRegister` en een aantal hulp qubits, gevolgd door een meting van de hulp qubits om een waarde op te halen `Syndrome` die `Result[]` van deze metingen is.</span><span class="sxs-lookup"><span data-stu-id="a84c0-109">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="a84c0-110">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a84c0-110">See Also</span></span>

- [<span data-ttu-id="a84c0-111">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="a84c0-111">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="a84c0-112">Micro soft. Quantum. ErrorCorrection. Syndrome</span><span class="sxs-lookup"><span data-stu-id="a84c0-112">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)