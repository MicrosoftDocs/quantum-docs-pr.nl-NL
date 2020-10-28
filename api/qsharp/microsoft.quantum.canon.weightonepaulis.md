---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: De functie WeightOnePaulis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 89802c1bc6f3da8edef27b698eb61098e47dfc85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703707"
---
# <a name="weightonepaulis-function"></a>De functie WeightOnePaulis

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Retourneert een matrix van alle Pauli-Opera tors van het gewicht-1 op een gegeven aantal qubits.

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarop de geretourneerde Pauli-Opera tors zijn gedefinieerd.



## <a name="output--pauli"></a>Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Een matrix met multi-Qubit Pauli-Opera Tors, die allemaal worden weer gegeven als een matrix met een lengte `nQubits` .