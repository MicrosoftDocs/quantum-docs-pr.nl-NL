---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: Door de gebruiker gedefinieerd EncodeOp-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: da947cdc25cb0edd3a4144022bbfc6ecb84c647f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702488"
---
# <a name="encodeop-user-defined-type"></a>Door de gebruiker gedefinieerd EncodeOp-type

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een bewerking aangeduid waarmee een fysiek REGI ster wordt gecodeerd in een logisch REGI ster, met behulp van de meegeleverde Scratch qubits.

Het eerste argument wordt opgehaald als het fysieke REGI ster dat wordt gecodeerd, terwijl het tweede argument wordt gebruikt om de Scratch-register te zijn die wordt toegepast.

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```

