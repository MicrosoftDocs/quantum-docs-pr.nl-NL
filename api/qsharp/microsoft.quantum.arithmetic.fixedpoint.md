---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Door de gebruiker gedefinieerd FixedPoint-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: 0fea6e4ee1b8c5391e815217f1ddf9e511d46463
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96223099"
---
# <a name="fixedpoint-user-defined-type"></a>Door de gebruiker gedefinieerd FixedPoint-type

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Hiermee wordt een REGI ster van qubits-code ring voor een getal met vaste komma aangeduid. Bestaat uit een geheel getal dat gelijk is aan het aantal qubits links van het binaire punt, d.w.z. qubits van gewicht groter dan of gelijk aan 1, en een Quantum register.

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

