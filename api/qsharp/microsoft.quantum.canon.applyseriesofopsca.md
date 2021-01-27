---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Bewerking ApplySeriesOfOpsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9a1f6189428b086c38b1d0f289afb18c2cf1be40
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850873"
---
# <a name="applyseriesofopsca-operation"></a>Bewerking ApplySeriesOfOpsCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix. (Adjoint + beheerd)

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="listofops--t--unit--is-adj--ctl"></a>listOfOps: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL []

De lijst met bewerkingen, waarbij elke matrix wordt toegepast. Ze worden eerst opeenvolgend en laagste index toegepast.
Elk moet zowel een adjoint als een beheerde functor hebben.


### <a name="targets--int"></a>doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geneste matrices waarin de doelen van de op-op worden beschreven. Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.


### <a name="register--t"></a>registreren: 'T []

Qubit-REGI ster waarop moet worden gehandeld.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="example"></a>Voorbeeld

Het volgende is van toepassing exp ([PauliX, PauliY], 0,5) op qubits 0, 1//X tot Qubit 2 toestaan OPS = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubitCA (X, _)]; indices = [[0, 1], [2]]; ApplySeriesOfOpsCA (OPS, indices, qubitArray);

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)