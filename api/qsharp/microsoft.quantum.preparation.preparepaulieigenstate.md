---
uid: Microsoft.Quantum.Preparation.PreparePauliEigenstate
title: Bewerking PreparePauliEigenstate
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PreparePauliEigenstate
qsharp.summary: Prepares a qubit in the positive eigenstate of a given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.
ms.openlocfilehash: b24852bb3a455a9fe04b3535156d0c3dfb1a7d12
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193689"
---
# <a name="preparepaulieigenstate-operation"></a>Bewerking PreparePauliEigenstate

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Bereidt een Qubit voor in de positieve eigenstate van een bepaalde Pauli-operator.
Als de identiteits operator wordt opgegeven, wordt de Qubit voor bereid in de gemengde status maximally.

```qsharp
operation PreparePauliEigenstate (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="description"></a>Beschrijving

Als de Qubit in eerste instantie de $ \ket {0} $-status had, bereidt deze bewerking de Qubit voor in de $ + $1-eigenstate van een bepaalde Pauli-operator of, `PauliI` in plaats daarvan, in de gemengde status maximally (Zie <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).

Als de Qubit een andere status heeft dan $ \ket {0} $, geldt deze bewerking voor de volgende poorten: $H $ voor `PauliX` , $HS $ voor `PauliY` , $I $ voor `PauliZ` en <xref:microsoft.quantum.preparation.preparesinglequbitidentity> voor `PauliI` .

## <a name="input"></a>Invoer

### <a name="basis--pauli"></a>basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Een Pauli-operator $P $.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een Qubit die moet worden voor bereid.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

