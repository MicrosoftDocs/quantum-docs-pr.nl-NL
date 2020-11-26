---
uid: Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp
title: Door de gebruiker gedefinieerd SyndromeMeasOp-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SyndromeMeasOp
qsharp.summary: Represents an operation that is used to measure the syndrome of an error-correcting code block.
ms.openlocfilehash: 65e47d82546b1df0beec2c00f435d3e7a28e6ae6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200251"
---
# <a name="syndromemeasop-user-defined-type"></a><span data-ttu-id="8d775-102">Door de gebruiker gedefinieerd SyndromeMeasOp-type</span><span class="sxs-lookup"><span data-stu-id="8d775-102">SyndromeMeasOp user defined type</span></span>

<span data-ttu-id="8d775-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="8d775-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="8d775-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8d775-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8d775-105">Hiermee wordt een bewerking aangeduid die wordt gebruikt om de Syndrome van een fout-correct code blok te meten.</span><span class="sxs-lookup"><span data-stu-id="8d775-105">Represents an operation that is used to measure the syndrome of an error-correcting code block.</span></span>

```qsharp

newtype SyndromeMeasOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => Microsoft.Quantum.ErrorCorrection.Syndrome));
```



## <a name="remarks"></a><span data-ttu-id="8d775-106">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8d775-106">Remarks</span></span>

<span data-ttu-id="8d775-107">De hand tekening `(LogicalRegister => Syndrome)` vertegenwoordigt een bewerking die gezamenlijk werkt op de qubits in `LogicalRegister` en een aantal hulp qubits, gevolgd door een meting van de hulp qubits om een waarde op te halen `Syndrome` die `Result[]` van deze metingen is.</span><span class="sxs-lookup"><span data-stu-id="8d775-107">The signature `(LogicalRegister => Syndrome)` represents an operation that acts jointly on the qubits in `LogicalRegister` and some auxiliary qubits followed by a measurements of the auxiliary qubits to extract a `Syndrome` value representing the `Result[]` of these measurements.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d775-108">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8d775-108">See Also</span></span>

- [<span data-ttu-id="8d775-109">Micro soft. Quantum. ErrorCorrection. LogicalRegister</span><span class="sxs-lookup"><span data-stu-id="8d775-109">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="8d775-110">Micro soft. Quantum. ErrorCorrection. Syndrome</span><span class="sxs-lookup"><span data-stu-id="8d775-110">Microsoft.Quantum.ErrorCorrection.Syndrome</span></span>](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)