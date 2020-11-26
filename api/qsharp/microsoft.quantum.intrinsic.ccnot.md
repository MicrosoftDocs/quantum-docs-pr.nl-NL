---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Bewerking CCNOT
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: 715796ddd915d80036933e3f1ceefa97aa62cecf
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212474"
---
# <a name="ccnot-operation"></a>Bewerking CCNOT

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Past de CCNOT-poort (dubbele controle – niet) toe op drie qubits.

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="control1--qubit"></a>control1: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

First Control Qubit voor de CCNOT-Gate.


### <a name="control2--qubit"></a>control2: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Tweede besturings element Qubit voor de CCNOT-Gate.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Doel-Qubit voor de CCNOT-Gate.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Gelijk aan:

```qsharp
Controlled X([control1, control2], target);
```