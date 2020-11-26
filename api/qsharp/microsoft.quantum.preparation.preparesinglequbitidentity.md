---
uid: Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity
title: Bewerking PrepareSingleQubitIdentity
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareSingleQubitIdentity
qsharp.summary: >-
  Prepares a qubit in the maximally mixed state.

  It prepares the given qubit in the $\boldone / 2$ state by applying the depolarizing channel $$ \begin{align} \Omega(\rho) \mathrel{:=} \frac{1}{4} \sum_{\mu \in \{0, 1, 2, 3\}} \sigma\_{\mu} \rho \sigma\_{\mu}^{\dagger}, \end{align} $$ where $\sigma\_i$ is the $i$th Pauli operator, and where $\rho$ is a density operator representing a mixed state.
ms.openlocfilehash: 1c8c161ec2eae73a81c46e7941af49145cde0493
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193621"
---
# <a name="preparesinglequbitidentity-operation"></a>Bewerking PrepareSingleQubitIdentity

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bereidt een Qubit voor in de gemengde status maximally.

De opgegeven Qubit wordt voor bereid in de status $ \boldone/$2 door het depolarizing-kanaal $ $ \begin{align} \Omega (\rho) \mathrel{toe te passen: =} \frac {1} {4} \ sum_ {\mu \in \{ 0, 1, 2, 3 \} } \sigma \_ {\mu} \rho \sigma \_ {\mu} ^ {\dagger}, \end{align} $ $ waarbij $ \sigma \_ i $ de $i $ de Pauli-operator is en waarbij $ \rho $ een dichtheids operator is die een gemengde staat vertegenwoordigt.

```qsharp
operation PrepareSingleQubitIdentity (qubit : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een Qubit waarvan de status moet worden ontpolair op de manier die hierboven wordt beschreven.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De gemengde status $ \boldone/$2, waarmee het resultaat van het Toep assen van deze bewerking wordt impliciet beschreven in een status, beschrijft een verwachte waarde voor wille keurige keuzes die zijn gemaakt in deze bewerking.
Voor elke afzonderlijke toepassing wordt met deze bewerking echter zuivere statussen aan zuivere staten toegewezen, maar dit gebeurt zoals beschreven in verwachting.
Met name deze bewerking kan worden gebruikt in process tomography om de *niet-eenheids* onderdelen van een kanaal te meten.