---
uid: Microsoft.Quantum.Canon.ApplyToEachA
title: Bewerking ApplyToEachA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachA
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `A` indicates that the single-qubit operation is adjointable.
ms.openlocfilehash: da901db2bb3c70186bfe0c8812b5710198d1dff3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844606"
---
# <a name="applytoeacha-operation"></a>Bewerking ApplyToEachA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.
De aanpassings functie `A` geeft aan dat de bewerking met één Qubit adjointable is.

```qsharp
operation ApplyToEachA<'T> (singleElementOperation : ('T => Unit is Adj), register : 'T[]) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="singleelementoperation--t--unit--is-adj"></a>singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

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