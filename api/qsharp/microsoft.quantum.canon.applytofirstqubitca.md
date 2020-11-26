---
uid: Microsoft.Quantum.Canon.ApplyToFirstQubitCA
title: Bewerking ApplyToFirstQubitCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstQubitCA
qsharp.summary: Applies operation op to the first qubit in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: bc2b1275b4258b9cc2db45c9e5cfe14f7eee0c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208802"
---
# <a name="applytofirstqubitca-operation"></a>Bewerking ApplyToFirstQubitCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de bewerking toegepast op de eerste Qubit in het REGI ster.
De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.

```qsharp
operation ApplyToFirstQubitCA (op : (Qubit => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="op--qubit--unit--is-adj--ctl"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een bewerking die moet worden toegepast op de eerste Qubit


### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-matrix naar de eerste Qubit waarop de bewerking wordt toegepast



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToFirstQubit](xref:Microsoft.Quantum.Canon.ApplyToFirstQubit)