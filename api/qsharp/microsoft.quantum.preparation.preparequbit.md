---
uid: Microsoft.Quantum.Preparation.PrepareQubit
title: Bewerking PrepareQubit
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareQubit
qsharp.summary: >-
  Prepares a qubit in the +1 (`Zero`) eigenstate of the given Pauli operator. If the identity operator is given, then the qubit is prepared in the maximally mixed state.

  If the qubit was initially in the $\ket{0}$ state, this operation prepares the qubit in the $+1$ eigenstate of a given Pauli operator, or, for `PauliI`, in the maximally mixed state instead (see <xref:microsoft.quantum.preparation.preparesinglequbitidentity>).

  If the qubit was in a state other than $\ket{0}$, this operation applies the following gates: $H$ for `PauliX`, $HS$ for `PauliY`, $I$ for `PauliZ` and <xref:microsoft.quantum.preparation.preparesinglequbitidentity> for `PauliI`.
ms.openlocfilehash: 5f42bf26a8f9638ea88c035a18846050c3776b45
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708226"
---
# <a name="preparequbit-operation"></a>Bewerking PrepareQubit

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket [](https://nuget.org/packages/)


Bereidt een Qubit voor in de + 1 ( `Zero` ) eigenstate van de gegeven Pauli-operator.
Als de identiteits operator wordt opgegeven, wordt de Qubit voor bereid in de gemengde status maximally.

Als de Qubit in eerste instantie de $ \ket {0} $-status had, bereidt deze bewerking de Qubit voor in de $ + $1-eigenstate van een bepaalde Pauli-operator of, `PauliI` in plaats daarvan, in de gemengde status maximally (Zie <xref:microsoft.quantum.preparation.preparesinglequbitidentity> ).

Als de Qubit een andere status heeft dan $ \ket {0} $, geldt deze bewerking voor de volgende poorten: $H $ voor `PauliX` , $HS $ voor `PauliY` , $I $ voor `PauliZ` en <xref:microsoft.quantum.preparation.preparesinglequbitidentity> voor `PauliI` .

```qsharp
operation PrepareQubit (basis : Pauli, qubit : Qubit) : Unit
```


## <a name="input"></a>Invoer

### <a name="basis--pauli"></a>basis: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Een Pauli-operator $P $.


### <a name="qubit--qubit"></a>Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Een Qubit die moet worden voor bereid.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

