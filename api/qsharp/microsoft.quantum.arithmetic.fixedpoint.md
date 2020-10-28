---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Door de gebruiker gedefinieerd FixedPoint-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: f1370cd2f8a7d6488ae0f6be841abd95e61f038e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707293"
---
# <a name="fixedpoint-user-defined-type"></a><span data-ttu-id="e97ca-102">Door de gebruiker gedefinieerd FixedPoint-type</span><span class="sxs-lookup"><span data-stu-id="e97ca-102">FixedPoint user defined type</span></span>

<span data-ttu-id="e97ca-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e97ca-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e97ca-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e97ca-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e97ca-105">Hiermee wordt een REGI ster van qubits-code ring voor een getal met vaste komma aangeduid.</span><span class="sxs-lookup"><span data-stu-id="e97ca-105">Represents a register of qubits encoding a fixed-point number.</span></span> <span data-ttu-id="e97ca-106">Bestaat uit een geheel getal dat gelijk is aan het aantal qubits links van het binaire punt, d.w.z. qubits van gewicht groter dan of gelijk aan 1, en een Quantum register.</span><span class="sxs-lookup"><span data-stu-id="e97ca-106">Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.</span></span>

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

