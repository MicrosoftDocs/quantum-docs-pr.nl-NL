---
uid: Microsoft.Quantum.Oracles.DiscreteOracle
title: Door de gebruiker gedefinieerd DiscreteOracle-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DiscreteOracle
qsharp.summary: >-
  Represents a discrete-time oracle.

  This is an oracle that implements $U^m$ for a fixed operation $U$ and a non-negative integer $m$.
ms.openlocfilehash: ccbcc92d4b6f1c800b576ad54739d26665e6d6d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709048"
---
# <a name="discreteoracle-user-defined-type"></a>Door de gebruiker gedefinieerd DiscreteOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een eenmalige Oracle.

Dit is een Oracle die $U ^ m $ implementeert voor een vaste bewerking $U $ en een niet-negatief geheel getal $m $.

```qsharp

newtype DiscreteOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```

