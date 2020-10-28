---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareSparseMultiConfigurationalState
title: Bewerking PrepareSparseMultiConfigurationalState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareSparseMultiConfigurationalState
qsharp.summary: Sparse multi-configurational state preparation of trial state by adding excitations to initial trial state.
ms.openlocfilehash: 1182f79a33784cdb49cb13db5cc97a0a45e59f9f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703130"
---
# <a name="preparesparsemulticonfigurationalstate-operation"></a>Bewerking PrepareSparseMultiConfigurationalState

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Sparse status van de proef versie van de evaluatie periode voor meerdere configuraties door aanstellingen toe te voegen aan de status van de eerste proef versie.

```qsharp
operation PrepareSparseMultiConfigurationalState (initialStatePreparation : (Qubit[] => Unit), excitations : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="initialstatepreparation--qubit--unit"></a>initialStatePreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Unitary om de status van de eerste proef versie voor te bereiden.


### <a name="excitations--jordanwignerinputstate"></a>bekrachtigingen: [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]

Door de amplitude van de aandrijf acties gestarte statussen van de eerste proef versie en Qubit indices worden uitgevoerd.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits van Hamiltonian.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

