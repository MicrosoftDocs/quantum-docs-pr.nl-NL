---
uid: Microsoft.Quantum.Canon.ApplyToEachCA
title: Bewerking ApplyToEachCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachCA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: c85b33760eba8d10d9650be2f8306e4afdd1f307
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841478"
---
# <a name="applytoeachca-operation"></a>Bewerking ApplyToEachCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.
De aanpassings functie `CA` geeft aan dat de bewerking met één qubit kan worden bestuurd en adjointable.

```qsharp
operation ApplyToEachCA<'T> (singleElementOperation : ('T => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="singleelementoperation--t--unit--is-adj--ctl"></a>singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Bewerking die moet worden toegepast op elke qubit.


### <a name="register--t"></a>registreren: 'T []

Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het doel waarop de bewerking reageert.

## <a name="example"></a>Voorbeeld

Een Qubit $ \ket{+} $-status voorbereiden:

```qsharp
using (register = Qubit[3]) {
    ApplyToEach(H, register);
}
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToEach](xref:Microsoft.Quantum.Canon.ApplyToEach)