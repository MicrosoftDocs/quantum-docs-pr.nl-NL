---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Door de gebruiker gedefinieerd StateOracle-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 6b2cf09c23942a586414daccb99cbb27b5026b9d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226601"
---
# <a name="stateoracle-user-defined-type"></a><span data-ttu-id="aad04-102">Door de gebruiker gedefinieerd StateOracle-type</span><span class="sxs-lookup"><span data-stu-id="aad04-102">StateOracle user defined type</span></span>

<span data-ttu-id="aad04-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="aad04-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="aad04-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aad04-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aad04-105">Vertegenwoordigt een Oracle voor status voorbereiding.</span><span class="sxs-lookup"><span data-stu-id="aad04-105">Represents an oracle for state preparation.</span></span>

<span data-ttu-id="aad04-106">De invoer voor de Oracle-$O $ zijn:</span><span class="sxs-lookup"><span data-stu-id="aad04-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="aad04-107">Een geheel getal dat de vlag Qubit $f $ indexeert.</span><span class="sxs-lookup"><span data-stu-id="aad04-107">An integer indexing the flag qubit $f$.</span></span>
- <span data-ttu-id="aad04-108">De systeem register $s $ waarin de gewenste Quantum status $ \ket{\psi} \_ s $ wordt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="aad04-108">The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.</span></span>

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="aad04-109">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="aad04-109">Remarks</span></span>

<span data-ttu-id="aad04-110">Deze Oracle die is gedefinieerd door $ $ O\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, $ $ treedt op bij berekening van de status $ \ket {0} \_ {f} \ket {0} \_ s $ om de doel status $ \ket{\psi} \_ s $ met amplitude $ \lambda $ te maken in de basis van $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="aad04-110">This oracle defined by $$ O\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, $$ acts on the on computational basis state $\ket{0}\_{f}\ket{0}\_s$ to create the target state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{1}\_f$.</span></span>
<span data-ttu-id="aad04-111">De eerste para meter is een index van het Qubit-REGI ster van $ \ket {0} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="aad04-111">The first parameter is an index to the qubit register of $\ket{0}\_f$.</span></span> <span data-ttu-id="aad04-112">De tweede para meter omvat beide registers.</span><span class="sxs-lookup"><span data-stu-id="aad04-112">The second parameter encompassed both registers.</span></span>