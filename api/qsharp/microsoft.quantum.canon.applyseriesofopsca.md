---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Bewerking ApplySeriesOfOpsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 2327a693e528cf46f95eae5ee052e9dd9b6ee187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705005"
---
# <a name="applyseriesofopsca-operation"></a>Bewerking ApplySeriesOfOpsCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix. (Adjoint + beheerd)

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="listofops--t--unit-adj--ctl"></a>listOfOps: 'T [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []

De lijst met bewerkingen, waarbij elke matrix wordt toegepast. Ze worden eerst opeenvolgend en laagste index toegepast.
Elk moet zowel een adjoint als een beheerde functor hebben.


### <a name="targets--int"></a>doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geneste matrices waarin de doelen van de op-op worden beschreven. Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.


### <a name="register--t"></a>registreren: 'T []

Qubit-REGI ster waarop moet worden gehandeld.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)