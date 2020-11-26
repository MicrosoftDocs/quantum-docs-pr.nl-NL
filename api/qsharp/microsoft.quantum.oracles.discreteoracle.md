---
uid: Microsoft.Quantum.Oracles.DiscreteOracle
title: Door de gebruiker gedefinieerd DiscreteOracle-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DiscreteOracle
qsharp.summary: >-
  Represents a discrete-time oracle.

  This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.
ms.openlocfilehash: accbd7b88cc2f6522da20ec1959492310ff0e743
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193893"
---
# <a name="discreteoracle-user-defined-type"></a>Door de gebruiker gedefinieerd DiscreteOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een eenmalige Oracle.

Dit is een Oracle die $U ^ m $ implementeert voor een vaste bewerking $U $ en een niet-negatief geheel getal $m $.

```qsharp

newtype DiscreteOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```

