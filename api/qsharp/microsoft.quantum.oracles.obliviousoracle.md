---
uid: Microsoft.Quantum.Oracles.ObliviousOracle
title: Door de gebruiker gedefinieerd ObliviousOracle-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: ObliviousOracle
qsharp.summary: >-
  Represents an oracle for oblivious amplitude amplification.

  The inputs to the oracle $O$ are:

  - The ancilla register $a$ that $O$ acts on. - The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.
ms.openlocfilehash: 2f92dcb28ec669229dfaf9bcb23eef9234552b8a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193876"
---
# <a name="obliviousoracle-user-defined-type"></a><span data-ttu-id="c9159-102">Door de gebruiker gedefinieerd ObliviousOracle-type</span><span class="sxs-lookup"><span data-stu-id="c9159-102">ObliviousOracle user defined type</span></span>

<span data-ttu-id="c9159-103">Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)</span><span class="sxs-lookup"><span data-stu-id="c9159-103">Namespace: [Microsoft.Quantum.Oracles](xref:Microsoft.Quantum.Oracles)</span></span>

<span data-ttu-id="c9159-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c9159-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c9159-105">Vertegenwoordigt een Oracle voor Oblivious-amplitude versterking.</span><span class="sxs-lookup"><span data-stu-id="c9159-105">Represents an oracle for oblivious amplitude amplification.</span></span>

<span data-ttu-id="c9159-106">De invoer voor de Oracle-$O $ zijn:</span><span class="sxs-lookup"><span data-stu-id="c9159-106">The inputs to the oracle $O$ are:</span></span>

- <span data-ttu-id="c9159-107">Het ancilla-REGI ster $a $ waarvoor $ wordt $O.</span><span class="sxs-lookup"><span data-stu-id="c9159-107">The ancilla register $a$ that $O$ acts on.</span></span>
- <span data-ttu-id="c9159-108">Het systeem register $s $ waarop de gewenste unitary $U $ wordt toegepast, post-selected on REGI ster $a $ met de status $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="c9159-108">The system register $s$ on which the desired unitary $U$ is applied, post-selected on register $a$ being in state $\ket{t}\_a$.</span></span>

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a><span data-ttu-id="c9159-109">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c9159-109">Remarks</span></span>

<span data-ttu-id="c9159-110">Deze Oracle gedefinieerd door $ $ O\ket {s} \_ a\ket {\ psi} \_ s = \Lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} \_ a\cdots $ $ handelt op de ancilla-status $ \ket{s} \_ a $ om de unitary $U $ te implementeren op een systeem status $ \ket{\psi} \_ s $ met amplitude $ \lambda $ in de basis die is gemarkeerd met $ \ket{t} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="c9159-110">This oracle defined by $$ O\ket{s}\_a\ket{\psi}\_s= \lambda\ket{t}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{t^\perp}\_a\cdots $$ acts on the ancilla state $\ket{s}\_a$ to implement the unitary $U$ on any system state $\ket{\psi}\_s$ with amplitude $\lambda$ in the basis flagged by $\ket{t}\_a$.</span></span>
<span data-ttu-id="c9159-111">De eerste para meter is het Qubit-REGI ster van $ \ket{s} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="c9159-111">The first parameter is the qubit register of $\ket{s}\_a$.</span></span> <span data-ttu-id="c9159-112">De tweede para meter is het Qubit-REGI ster van $ \ket{\psi} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="c9159-112">The second parameter is the qubit register of $\ket{\psi}\_s$.</span></span>