---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Door de gebruiker gedefinieerd DeterministicStateOracle-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 10ae9e52f298cdfb92dd6a9e5cf85960bece6800
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842595"
---
# <a name="deterministicstateoracle-user-defined-type"></a>Door de gebruiker gedefinieerd DeterministicStateOracle-type

Naam ruimte: [micro soft. Quantum. Oracle](xref:Microsoft.Quantum.Oracles)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een Oracle voor deterministische status voorbereiding.

De invoer voor de Oracle-$O $ is:

- Het REGI ster waarin de gewenste Quantum status $ \ket{\psi} \_ s $ wordt opgeslagen.

```qsharp

newtype DeterministicStateOracle = ((Qubit[] => Unit is Adj + Ctl));
```



## <a name="remarks"></a>Opmerkingen

Deze Oracle die is gedefinieerd door $O \ket {0} = \ket{\psi} $, treedt op in de status op basis van de berekening $ \ket {0} $ om de status $ \ket{\psi} $ te maken.
De eerste para meter is het Qubit-REGI ster van $ \ket{\psi} $.