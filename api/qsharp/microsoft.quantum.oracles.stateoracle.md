---
uid: Microsoft.Quantum.Oracles.StateOracle
title: Door de gebruiker gedefinieerd StateOracle-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: StateOracle
qsharp.summary: >-
  Represents an oracle for state preparation.

  The inputs to the oracle $O$ are:

  - An integer indexing the flag qubit $f$. - The system register $s$ that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 65f4edcf2101190da0c6d00eb4dd21881143ceb0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708748"
---
# <a name="stateoracle-user-defined-type"></a>Door de gebruiker gedefinieerd StateOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een Oracle voor status voorbereiding.

De invoer voor de Oracle-$O $ zijn:

- Een geheel getal dat de vlag Qubit $f $ indexeert.
- De systeem register $s $ waarin de gewenste Quantum status $ \ket{\psi} \_ s $ wordt opgeslagen.

```qsharp

newtype StateOracle = (((Int, Qubit[]) => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Opmerkingen

Deze Oracle die is gedefinieerd door $ $ O\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, $ $ treedt op bij berekening van de status $ \ket {0} \_ {f} \ket {0} \_ s $ om de doel status $ \ket{\psi} \_ s $ met amplitude $ \lambda $ te maken in de basis van $ \ket {1} \_ f $.
De eerste para meter is een index van het Qubit-REGI ster van $ \ket {0} \_ f $. De tweede para meter omvat beide registers.