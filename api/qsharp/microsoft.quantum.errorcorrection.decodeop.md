---
uid: Microsoft.Quantum.ErrorCorrection.DecodeOp
title: Door de gebruiker gedefinieerd DecodeOp-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: DecodeOp
qsharp.summary: >-
  Represents an operation which decodes an encoded register into a physical register and the scratch qubits used to record a syndrome.

  The argument to a DecodeOp is the same as the return from an EncodeOp, and vice versa.
ms.openlocfilehash: f1fc2851b7ed8b12cf8a47fabe794235a3083d31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200999"
---
# <a name="decodeop-user-defined-type"></a>Door de gebruiker gedefinieerd DecodeOp-type

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking aangeduid waarmee een gecodeerd REGI ster wordt gedecodeerd in een fysiek REGI ster en het scratch qubits dat wordt gebruikt om een Syndrome op te nemen.

Het argument voor een DecodeOp is hetzelfde als het resultaat van een EncodeOp, en omgekeerd.

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

