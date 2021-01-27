---
uid: Microsoft.Quantum.Oracles.ContinuousOracle
title: Door de gebruiker gedefinieerd ContinuousOracle-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ContinuousOracle
qsharp.summary: >-
  Represents a continuous-time oracle.

  This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.
ms.openlocfilehash: ac254b7556878550216d5c0c9222620fdc5c5702
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855936"
---
# <a name="continuousoracle-user-defined-type"></a><span data-ttu-id="95256-102">Door de gebruiker gedefinieerd ContinuousOracle-type</span><span class="sxs-lookup"><span data-stu-id="95256-102">ContinuousOracle user defined type</span></span>

<span data-ttu-id="95256-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="95256-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="95256-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="95256-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="95256-105">Hiermee wordt een doorlopende Oracle-fase aangeduid.</span><span class="sxs-lookup"><span data-stu-id="95256-105">Represents a continuous-time oracle.</span></span>

<span data-ttu-id="95256-106">Dit is een Oracle die $U (\delta t) implementeert: \ket{\psi (t)} \mapsto \ket{\psi (t + \delta t)} $ voor alle tijden $t $, waarbij $U $ een vaste bewerking is, waarbij $ \delta t $ een niet-negatief reëel getal is.</span><span class="sxs-lookup"><span data-stu-id="95256-106">This is an oracle that implements $U(\delta t) : \ket{\psi(t)} \mapsto \ket{\psi(t + \delta t)}$ for all times $t$, where $U$ is a fixed operation, and where $\delta t$ is a non-negative real number.</span></span>

```qsharp

newtype ContinuousOracle = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

