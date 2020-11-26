---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Functie _DeltaParityCNOTbitstring
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 0c0da60e3c389f8208f9f7d5c84a09893f3c1bda
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226074"
---
# <a name="_deltaparitycnotbitstring-function"></a>Functie _DeltaParityCNOTbitstring

Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)

Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Klassieke verwerkings stap van `ApplyDeltaParity` .
Hiermee wordt een lijst met besturings element qubits voor het evalueren van het pariteits verschil tussen twee PQRS... voor waarden van even lengte.

```qsharp
function _DeltaParityCNOTbitstring (prevFermionicTerm : Int[], nextFermionicTerm : Int[]) : (Int, Bool[])
```


## <a name="input"></a>Invoer

### <a name="prevfermionicterm--int"></a>prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="nextfermionicterm--int"></a>nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]





## <a name="output--intbool"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[BOOL](xref:microsoft.quantum.lang-ref.bool)[])



## <a name="remarks"></a>Opmerkingen

Hierbij wordt ervan uitgegaan dat de lengte van de voor waarden even is.
Reken lijst met besturings elementen voor het pariteits verschil tussen twee termen.
Hierbij wordt ervan uitgegaan dat de invoer lijsten in oplopende volg orde zijn gesorteerd.