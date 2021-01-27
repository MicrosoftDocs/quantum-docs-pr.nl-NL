---
uid: Microsoft.Quantum.Research.Chemistry._DeltaParityCNOTbitstring
title: Functie _DeltaParityCNOTbitstring
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _DeltaParityCNOTbitstring
qsharp.summary: Classical processing step of `ApplyDeltaParity`. This computes a list of control qubits for evaluating parity difference between any two PQRS... terms of even length.
ms.openlocfilehash: 3dd2d299a094577d377780d731e76287815e8d03
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847606"
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