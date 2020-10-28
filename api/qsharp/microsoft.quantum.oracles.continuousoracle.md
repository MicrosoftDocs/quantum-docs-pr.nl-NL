---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Door de gebruiker gedefinieerd ContinuousOracle-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: 9bc9b4bbdab6905a6a79893b1d559425ac679400
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708785"
---
# <a name="continuousoracle-user-defined-type"></a>Door de gebruiker gedefinieerd ContinuousOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een doorlopende Oracle-fase aangeduid.

Dit is een Oracle die $U (\delta t) implementeert: \ket{\psi (t)} \mapsto \ket{\psi (t + \delta t)} $ voor alle tijden $t $, waarbij $U $ een vaste bewerking is, waarbij $ \delta t $ een niet-negatief reëel getal is.

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

