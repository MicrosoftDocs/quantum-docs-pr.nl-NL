---
uid: Microsoft.Quantum.Synthesis.ApplyUnitary
title: Bewerking ApplyUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyUnitary
qsharp.summary: >-
  Applies gate defined by 2^n x 2^n unitary matrix.

  Fails if matrix is not unitary, or has wrong size.
ms.openlocfilehash: 58215d3b05b8c6974e979d21a13869f27b436310
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859163"
---
# <a name="applyunitary-operation"></a>Bewerking ApplyUnitary

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past Gate toe die is gedefinieerd door 2 ^ n x 2 ^ n unitary matrix.

Mislukt als de matrix niet unitary of een verkeerde grootte heeft.

```qsharp
operation ApplyUnitary (unitary : Microsoft.Quantum.Math.Complex[][], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="unitary--complex"></a>unitary: [complex](xref:Microsoft.Quantum.Math.Complex)[] []

2 ^ n x 2 ^ n unitary matrix met een beschrijving van de bewerking.
Als de matrix niet unitary of niet een geschikte grootte heeft, genereert een uitzonde ring.


### <a name="qubits--littleendian"></a>qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Qubits waarvoor het bewerkings register van de lengte n moet worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

