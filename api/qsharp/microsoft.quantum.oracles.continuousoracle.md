---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Door de gebruiker gedefinieerd ContinuousOracle-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: fb05e97c635ba75fc2d85dc2a7cea27f3a3af63f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226788"
---
# <a name="continuousoracle-user-defined-type"></a><span data-ttu-id="8cdca-102">Door de gebruiker gedefinieerd ContinuousOracle-type</span><span class="sxs-lookup"><span data-stu-id="8cdca-102">ContinuousOracle user defined type</span></span>

<span data-ttu-id="8cdca-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="8cdca-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="8cdca-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8cdca-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8cdca-105">Hiermee wordt een doorlopende Oracle-fase aangeduid.</span><span class="sxs-lookup"><span data-stu-id="8cdca-105">Represents a continuous-time oracle.</span></span>

<span data-ttu-id="8cdca-106">Dit is een Oracle die $U (\delta t) implementeert: \ket{\psi (t)} \mapsto \ket{\psi (t + \delta t)} $ voor alle tijden $t $, waarbij $U $ een vaste bewerking is, waarbij $ \delta t $ een niet-negatief reëel getal is.</span><span class="sxs-lookup"><span data-stu-id="8cdca-106">This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.</span></span>

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

