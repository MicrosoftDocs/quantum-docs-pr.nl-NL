---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: Door de gebruiker gedefinieerd DecodeOp-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: 0733ec016e50a320b162b111c7d87c32140fdacb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702513"
---
# <a name="decodeop-user-defined-type"></a><span data-ttu-id="5d1e2-102">Door de gebruiker gedefinieerd DecodeOp-type</span><span class="sxs-lookup"><span data-stu-id="5d1e2-102">DecodeOp user defined type</span></span>

<span data-ttu-id="5d1e2-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="5d1e2-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="5d1e2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5d1e2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5d1e2-105">Hiermee wordt een bewerking aangeduid waarmee een gecodeerd REGI ster wordt gedecodeerd in een fysiek REGI ster en het scratch qubits dat wordt gebruikt om een Syndrome op te nemen.</span><span class="sxs-lookup"><span data-stu-id="5d1e2-105">Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.</span></span>

<span data-ttu-id="5d1e2-106">Het argument voor een DecodeOp is hetzelfde als het resultaat van een EncodeOp, en omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="5d1e2-106">The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.</span></span>

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```
