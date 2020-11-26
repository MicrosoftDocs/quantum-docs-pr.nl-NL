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
# <a name="obliviousoracle-user-defined-type"></a>Door de gebruiker gedefinieerd ObliviousOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een Oracle voor Oblivious-amplitude versterking.

De invoer voor de Oracle-$O $ zijn:

- Het ancilla-REGI ster $a $ waarvoor $ wordt $O.
- Het systeem register $s $ waarop de gewenste unitary $U $ wordt toegepast, post-selected on REGI ster $a $ met de status $ \ket{t} \_ a $.

```qsharp

newtype ObliviousOracle = (((Qubit[], Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Opmerkingen

Deze Oracle gedefinieerd door $ $ O\ket {s} \_ a\ket {\ psi} \_ s = \Lambda\ket{t} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{t ^ \perp} \_ a\cdots $ $ handelt op de ancilla-status $ \ket{s} \_ a $ om de unitary $U $ te implementeren op een systeem status $ \ket{\psi} \_ s $ met amplitude $ \lambda $ in de basis die is gemarkeerd met $ \ket{t} \_ a $.
De eerste para meter is het Qubit-REGI ster van $ \ket{s} \_ a $. De tweede para meter is het Qubit-REGI ster van $ \ket{\psi} \_ s $.