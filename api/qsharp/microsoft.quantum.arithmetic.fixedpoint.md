---
uid: Microsoft.Quantum.Arithmetic.FixedPoint
title: Door de gebruiker gedefinieerd FixedPoint-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: FixedPoint
qsharp.summary: Represents a register of qubits encoding a fixed-point number. Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.
ms.openlocfilehash: 18e85120647c5a1f41ccab5fbfb27ea602a279af
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843209"
---
# <a name="fixedpoint-user-defined-type"></a><span data-ttu-id="0c82a-102">Door de gebruiker gedefinieerd FixedPoint-type</span><span class="sxs-lookup"><span data-stu-id="0c82a-102">FixedPoint user defined type</span></span>

<span data-ttu-id="0c82a-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="0c82a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="0c82a-104">Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span><span class="sxs-lookup"><span data-stu-id="0c82a-104">Package: [Microsoft.Quantum.Numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)</span></span>


<span data-ttu-id="0c82a-105">Hiermee wordt een REGI ster van qubits-code ring voor een getal met vaste komma aangeduid.</span><span class="sxs-lookup"><span data-stu-id="0c82a-105">Represents a register of qubits encoding a fixed-point number.</span></span> <span data-ttu-id="0c82a-106">Bestaat uit een geheel getal dat gelijk is aan het aantal qubits links van het binaire punt, d.w.z. qubits van gewicht groter dan of gelijk aan 1, en een Quantum register.</span><span class="sxs-lookup"><span data-stu-id="0c82a-106">Consists of an integer that is equal to the number of qubits to the left of the binary point, i.e., qubits of weight greater than or equal to 1, and a quantum register.</span></span>

```qsharp

newtype FixedPoint = (Int, Qubit[]);
```

