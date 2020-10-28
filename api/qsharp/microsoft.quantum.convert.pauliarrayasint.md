---
uid: Microsoft.Quantum.Convert.PauliArrayAsInt
title: De functie PauliArrayAsInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: PauliArrayAsInt
qsharp.summary: Encodes a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators into an integer.
ms.openlocfilehash: f8ec468dd0f0cfd0d868dfc79ff715b3b4fc2f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702926"
---
# <a name="pauliarrayasint-function"></a>De functie PauliArrayAsInt

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket [](https://nuget.org/packages/)


Codeert een multi-Qubit Pauli-operator die wordt weer gegeven als een matrix van Pauli Opera tors met één Qubit in een geheel getal.

```qsharp
function PauliArrayAsInt (paulis : Pauli[]) : Int
```


## <a name="input"></a>Invoer

### <a name="paulis--pauli"></a>PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een matrix van Maxi maal 31 Opera tors met één Qubit Pauli.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Een unieke identificatie van een geheel getal `paulis` , zoals hieronder wordt beschreven.

## <a name="remarks"></a>Opmerkingen

Elke Pauli-operator kan worden versleuteld met twee bits: $ $ \begin{align} \boldone \mapsto 00, \quad X \mapsto 01, \quad Y \mapsto 11, \quad Z \mapsto 10.
\end{align} $ $

Met een matrix van Pauli-Opera tors `[P0, ..., Pn]` retourneert deze functie een geheel getal met een binaire expansie die is gevormd door het samen voegen van de toewijzingen van elke Pauli-operator in een big-endian-volg orde `bits(Pn) ... bits(P0)` .