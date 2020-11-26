---
uid: Microsoft.Quantum.Canon.ApplyToEachIndexCA
title: Bewerking ApplyToEachIndexCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToEachIndexCA
qsharp.summary: Applies a single-qubit operation to each indexed element in a register. The modifier `CA` indicates that the single-qubit operation is adjointable and controllable.
ms.openlocfilehash: abb616498a8ff9c3348df81cf0ca1a1669561eec
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208938"
---
# <a name="applytoeachindexca-operation"></a>Bewerking ApplyToEachIndexCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een bewerking met één Qubit toegepast op elk geïndexeerd element in een REGI ster.
De aanpassings functie `CA` geeft aan dat de bewerking met één Qubit adjointable en kan worden bestuurd.

```qsharp
operation ApplyToEachIndexCA<'T> (singleElementOperation : ((Int, 'T) => Unit is Adj + Ctl), register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="singleelementoperation--intt--unit--is-adj--ctl"></a>singleElementOperation: ([int](xref:microsoft.quantum.lang-ref.int), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Bewerking die moet worden toegepast op elke qubit.


### <a name="register--t"></a>registreren: 'T []

Matrix van qubits waarop de opgegeven bewerking moet worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het doel waarop elk van de bewerkingen optreedt.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToEachIndex](xref:Microsoft.Quantum.Canon.ApplyToEachIndex)