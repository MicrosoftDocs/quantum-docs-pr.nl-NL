---
uid: Microsoft.Quantum.ErrorCorrection.QECC
title: Door de gebruiker gedefinieerd QECC-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: QECC
qsharp.summary: Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.
ms.openlocfilehash: 4fab7e25f6ccf9f9af2744e0ebe40418d9681309
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853081"
---
# <a name="qecc-user-defined-type"></a><span data-ttu-id="6a5d4-102">Door de gebruiker gedefinieerd QECC-type</span><span class="sxs-lookup"><span data-stu-id="6a5d4-102">QECC user defined type</span></span>

<span data-ttu-id="6a5d4-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="6a5d4-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="6a5d4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a5d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a5d4-105">Hiermee wordt een code voor fout correctie aangeduid, zoals gedefinieerd door de coderings-, decoder-en Syndrome-meet procedure.</span><span class="sxs-lookup"><span data-stu-id="6a5d4-105">Represents an error-correcting code as defined by its encoder, decoder, and syndrome measurement procedure.</span></span>

```qsharp

newtype QECC = (Microsoft.Quantum.ErrorCorrection.EncodeOp, Microsoft.Quantum.ErrorCorrection.DecodeOp, Microsoft.Quantum.ErrorCorrection.SyndromeMeasOp);
```

