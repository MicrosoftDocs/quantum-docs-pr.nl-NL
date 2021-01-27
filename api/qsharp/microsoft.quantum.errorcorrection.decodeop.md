---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: Door de gebruiker gedefinieerd DecodeOp-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: 2b3d4558f6528c2e0f597398d12fc9331ab381b5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827378"
---
# <a name="decodeop-user-defined-type"></a><span data-ttu-id="b4977-102">Door de gebruiker gedefinieerd DecodeOp-type</span><span class="sxs-lookup"><span data-stu-id="b4977-102">DecodeOp user defined type</span></span>

<span data-ttu-id="b4977-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="b4977-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="b4977-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4977-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4977-105">Hiermee wordt een bewerking aangeduid waarmee een gecodeerd REGI ster wordt gedecodeerd in een fysiek REGI ster en het scratch qubits dat wordt gebruikt om een Syndrome op te nemen.</span><span class="sxs-lookup"><span data-stu-id="b4977-105">Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.</span></span>

<span data-ttu-id="b4977-106">Het argument voor een DecodeOp is hetzelfde als het resultaat van een EncodeOp, en omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="b4977-106">The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.</span></span>

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

