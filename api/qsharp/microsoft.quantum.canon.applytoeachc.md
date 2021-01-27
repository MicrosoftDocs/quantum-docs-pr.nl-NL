---
uid: Microsoft.Quantum.Canon.ApplyToEachC
title: Bewerking ApplyToEachC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachC
qsharp.summary: Applies a single-qubit operation to each element in a register. The modifier `C` indicates that the single-qubit operation is controllable.
ms.openlocfilehash: b8b51e1c8d52c140c3ca1e5a54d0bd4cf4873046
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850843"
---
# <a name="applytoeachc-operation"></a>Bewerking ApplyToEachC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking met één Qubit toegepast op elk element in een REGI ster.
De aanpassings functie `C` geeft aan dat de bewerking met één qubit kan worden bestuurd.

```qsharp
operation ApplyToEachC<'T> (singleElementOperation : ('T => Unit is Ctl), register : 'T[]) : Unit is Ctl
```


## <a name="input"></a>Invoer

### <a name="singleelementoperation--t--unit--is-ctl"></a>singleElementOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

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