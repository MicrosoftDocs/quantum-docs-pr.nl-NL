---
uid: Microsoft.Quantum.ErrorCorrection.EncodeOp
title: Door de gebruiker gedefinieerd EncodeOp-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeOp
qsharp.summary: >-
  Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.

  The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.
ms.openlocfilehash: 18d6df6037b1fe66a171acea1936fcb9ba1b27e5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200897"
---
# <a name="encodeop-user-defined-type"></a><span data-ttu-id="77d88-102">Door de gebruiker gedefinieerd EncodeOp-type</span><span class="sxs-lookup"><span data-stu-id="77d88-102">EncodeOp user defined type</span></span>

<span data-ttu-id="77d88-103">Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="77d88-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="77d88-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77d88-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77d88-105">Hiermee wordt een bewerking aangeduid waarmee een fysiek REGI ster wordt gecodeerd in een logisch REGI ster, met behulp van de meegeleverde Scratch qubits.</span><span class="sxs-lookup"><span data-stu-id="77d88-105">Represents an operation which encodes a physical register into a logical register, using the provided scratch qubits.</span></span>

<span data-ttu-id="77d88-106">Het eerste argument wordt opgehaald als het fysieke REGI ster dat wordt gecodeerd, terwijl het tweede argument wordt gebruikt om de Scratch-register te zijn die wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="77d88-106">The first argument is taken to be the physical register that will be encoded, while the second argument is taken to be the scratch register that will be used.</span></span>

```qsharp

newtype EncodeOp = (((Qubit[], Qubit[]) => Microsoft.Quantum.ErrorCorrection.LogicalRegister));
```

