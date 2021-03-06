---
uid: Microsoft.Quantum.Arithmetic.ApplyOuterCDKMAdder
title: Bewerking ApplyOuterCDKMAdder
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ApplyOuterCDKMAdder
qsharp.summary: Reversible, in-place ripple-carry operation that is used in the integer addition operation RippleCarryAdderCDKM below. Given two qubit registers `xs` and `ys` of the same length, the operation applies a ripple carry sequence of CNOT and CCNOT gates with qubits in `xs` and `ys` as the controls and qubits in `xs` as the targets.
ms.openlocfilehash: acaa563245bb7c701316d2dfd35b5be03d8e024d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843713"
---
# <a name="applyoutercdkmadder-operation"></a>Bewerking ApplyOuterCDKMAdder

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Omkeerbaar, in-place rimpel bewerking die wordt gebruikt in de RippleCarryAdderCDKM-bewerking voor het tellen van gehele getallen.
Als er twee Qubit `xs` -registers en `ys` dezelfde lengte worden gebruikt, past de bewerking een rimpeling toe van CNOT-en CCNOT-poorten met qubits in `xs` en `ys` als de besturings elementen en qubits als `xs` doel.

```qsharp
operation ApplyOuterCDKMAdder (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, ancilla : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Het eerste Qubit-REGI ster met besturings elementen en doelen.


### <a name="ys--littleendian"></a>kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Tweede Qubit-REGI ster, bijdragen aan de besturings elementen.


### <a name="ancilla--qubit"></a>ancilla: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

De ancilla-Qubit die wordt gebruikt in RippleCarryAdderCDKM die is door gegeven aan deze bewerking.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="references"></a>Verwijzingen

- Chris A. Cuccaro, Thomas G. Draper, Samuel A. Kutin, David Petrie Moulton: "een nieuwe Quantum rimpel-transport circuit", 2004.
  https://arxiv.org/abs/quant-ph/0410184v1