---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Bewerking PrepareIdentity
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: 6e0a43e61e3c49edef94db63f07ed29132d84c83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210434"
---
# <a name="prepareidentity-operation"></a>Bewerking PrepareIdentity

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een REGI ster, bereidt dat registratie voor op de gemengde status maximally.

De kassa wordt voor bereid in de status $ \boldone/2 ^ N $ door het volledige depolarizing-kanaal toe te passen op elke qubit, waarbij $N $ de lengte van het REGI ster is.

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster waarvan de status moet worden ontpolair op de manier die hierboven wordt beschreven.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. prepare. PrepareSingleQubitIdentity](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)