---
uid: Microsoft.Quantum.Canon.AndLadder
title: Bewerking AndLadder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: AndLadder
qsharp.summary: Performs a controlled "AND ladder" on a register of target qubits.
ms.openlocfilehash: 2c6114ec8a5caabdeea8ab7e26a4877e1633671c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209720"
---
# <a name="andladder-operation"></a>Bewerking AndLadder

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een beheerde "en ladder" uitgevoerd op een REGI ster van doel-qubits.

```qsharp
operation AndLadder (ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt een trans formatie toegepast die wordt beschreven door de volgende toewijzing van de berekening, $ $ \begin{align} \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1, \dots, y \_ {n-1}} \mapsto \ket{x \_ 1, \dots, x \_ n} \ket{y \_ 1 \oplus (x \_ 1 \land x \_ 2), \dots, y \_ {n-1} \oplus (x \_ 1 \land x \_ 2 \land \cdots \land x \_ {n-1}}, \end{align} $ $ waarbij $ \ket{x \_ 1, \dots, x \_ n} $ verwijst naar de berekening basis status van `controls` , en waarbij $ \ket{y \_ 1, \dots, y \_ {n-1}} $ verwijst naar de berekening basis statussen van `targets` .

## <a name="input"></a>Invoer

### <a name="ccnot--ccnotop"></a>ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)

De CCNOT-poort die moet worden gebruikt voor de constructie.


### <a name="controls--qubit"></a>Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van qubits die als besturings elementen voor de en ladder moet worden gebruikt.
Met deze bewerking worden de reken kundige basis provincies van `controls` invariant gelaten.
De lengte van `controls` moet ten minste 2 zijn en moet gelijk zijn aan een plus de lengte van `targets` .


### <a name="targets--qubit"></a>doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

De lengte `targets` moet mini maal 1 zijn en gelijk zijn aan de lengte van `controls` min één.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

- Wordt gebruikt als onderdeel van <xref:microsoft.quantum.canon.applymulticontrolledc> en <xref:microsoft.quantum.canon.applymulticontrolledca> .
- Zie afbeelding 4,10, sectie 4,3 in Nielsen & Chuang voor uitleg en circuit diagram.

## <a name="references"></a>Referenties

- [*Michael A. Nielsen, Isaac L. Chuang*, Quantum Computation en Quantum Information](http://doi.org/10.1017/CBO9780511976667)