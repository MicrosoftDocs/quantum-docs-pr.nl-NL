---
uid: Microsoft.Quantum.Convert.BoolArrayAsPauli
title: De functie BoolArrayAsPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: BoolArrayAsPauli
qsharp.summary: Given a bit string, returns a multi-qubit Pauli operator represented as an array of single-qubit Pauli operators.
ms.openlocfilehash: c11ca05ad8a939d704547c65a8e8a6537d0df4b7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98834236"
---
# <a name="boolarrayaspauli-function"></a>De functie BoolArrayAsPauli

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een bit string retourneert een multi-Qubit Pauli-operator die wordt weer gegeven als een matrix van Pauli-Opera tors met één Qubit.

```qsharp
function BoolArrayAsPauli (pauli : Pauli, bitApply : Bool, bits : Bool[]) : Pauli[]
```


## <a name="input"></a>Invoer

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

De operator Pauli die moet worden toegepast op qubits WHERE `bitsApply == bits[idx]` .


### <a name="bitapply--bool"></a>bitApply: [BOOL](xref:microsoft.quantum.lang-ref.bool)

pas Pauli toe als bit deze waarde is.


### <a name="bits--bool"></a>bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Boole-matrix.



## <a name="output--pauli"></a>Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]



## <a name="remarks"></a>Opmerkingen

De Boole-matrix en het Quantum register moeten even lang zijn.