---
uid: Microsoft.Quantum.Oracles.DeterministicStateOracle
title: Door de gebruiker gedefinieerd DeterministicStateOracle-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Oracles
qsharp.name: DeterministicStateOracle
qsharp.summary: >-
  Represents an oracle for deterministic state preparation.

  The input to the oracle $O$ is:

  - The register that will store the desired quantum state $\ket{\psi}\_s$.
ms.openlocfilehash: 6f8f80aacd3386ba61675101acb87e09fff5afff
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193927"
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