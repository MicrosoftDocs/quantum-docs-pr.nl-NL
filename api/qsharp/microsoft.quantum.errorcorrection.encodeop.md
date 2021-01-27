---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: Door de gebruiker gedefinieerd EncodeOp-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: c9959f1afbd44df974c06b79f73eccd090b17985
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98826179"
---
# <a name="encodeop-user-defined-type"></a>Door de gebruiker gedefinieerd EncodeOp-type

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking aangeduid waarmee een fysiek REGI ster wordt gecodeerd in een logisch REGI ster, met behulp van de meegeleverde Scratch qubits.

Het eerste argument wordt opgehaald als het fysieke REGI ster dat wordt gecodeerd, terwijl het tweede argument wordt gebruikt om de Scratch-register te zijn die wordt toegepast.

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```

