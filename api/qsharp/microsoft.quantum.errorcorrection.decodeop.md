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
# <a name="decodeop-user-defined-type"></a>Door de gebruiker gedefinieerd DecodeOp-type

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een bewerking aangeduid waarmee een gecodeerd REGI ster wordt gedecodeerd in een fysiek REGI ster en het scratch qubits dat wordt gebruikt om een Syndrome op te nemen.

Het argument voor een DecodeOp is hetzelfde als het resultaat van een EncodeOp, en omgekeerd.

```qsharp

newtype DecodeOp = ((Microsoft.Quantum.ErrorCorrection.LogicalRegister => (Qubit[], Qubit[])));
```

