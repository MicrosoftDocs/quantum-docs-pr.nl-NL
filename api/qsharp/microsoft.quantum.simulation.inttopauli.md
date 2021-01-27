---
uid: Microsoft.Quantum.Simulation.IntToPauli
title: De functie IntToPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntToPauli
qsharp.summary: Converts a integer to a single-qubit Pauli operator.
ms.openlocfilehash: 76f482b86ff4a27b6e6ce6ae4ec3d59422563f12
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842255"
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