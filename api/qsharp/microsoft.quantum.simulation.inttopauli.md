---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: De functie IntToPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 18edb600f7b5b33c7ad98e78e32903c570082225
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229202"
---
# <a name="inttopauli-function"></a>De functie IntToPauli

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Converteert een geheel getal naar een Pauli-operator met één Qubit.

```qsharp
function IntToPauli (idx : Int) : Pauli
```


## <a name="input"></a>Invoer

### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)

Geheel getal in het bereik `0..3` dat moet worden geconverteerd naar Pauli-Opera tors.



## <a name="output--pauli"></a>Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

Een `Pauli` operator die wordt gegeven door `[PauliI, PauliX, PauliY, PauliZ][idx]` .