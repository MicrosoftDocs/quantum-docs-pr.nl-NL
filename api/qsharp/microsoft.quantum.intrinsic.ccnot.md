---
uid: Microsoft.Quantum.Intrinsic.CCNOT
title: Bewerking CCNOT
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: CCNOT
qsharp.summary: Applies the doubly controlled–NOT (CCNOT) gate to three qubits.
ms.openlocfilehash: bf20ff1e9d25d72e7e8e0207ab947a57dc394cf4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702140"
---
# <a name="ccnot-operation"></a>Bewerking CCNOT

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket [](https://nuget.org/packages/)


Past de CCNOT-poort (dubbele controle – niet) toe op drie qubits.

```qsharp
operation CCNOT (control1 : Qubit, control2 : Qubit, target : Qubit) : Unit
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