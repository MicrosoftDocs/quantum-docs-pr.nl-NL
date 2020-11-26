---
uid: Microsoft.Quantum.Canon.ApplyMultiControlledCA
title: Bewerking ApplyMultiControlledCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiControlledCA
qsharp.summary: Applies a multiply controlled version of a singly controlled operation. The modifier `CA` indicates that the single-qubit operation is controllable and adjointable.
ms.openlocfilehash: 28797583c23e21eb4bcae996a34c70ee06c6dbe8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209278"
---
# <a name="applymulticontrolledca-operation"></a>Bewerking ApplyMultiControlledCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een door vermenigvuldigde versie van een gecontroleerde bewerking toe.
De aanpassings functie `CA` geeft aan dat de bewerking met één qubit kan worden bestuurd en adjointable.

```qsharp
operation ApplyMultiControlledCA (singlyControlledOp : (Qubit[] => Unit is Adj), ccnot : Microsoft.Quantum.Canon.CCNOTop, controls : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="singlycontrolledop--qubit--unit--is-adj"></a>singlyControlledOp: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

Een bewerking die wordt beheerd op één Qubit.
Voor de eerste Qubit in het argument van de bewerking wordt aangenomen dat het om een besturings element gaat en wordt aangenomen dat de rest qubits is.
`ApplyMultiControlled` roept altijd `singlyControlledOp` een lengte van ten minste 1 aan.


### <a name="ccnot--ccnotop"></a>ccnot: [CCNOTop](xref:Microsoft.Quantum.Canon.CCNOTop)

De Controlled-NOT-Gate die voor de bouw moet worden gebruikt.


### <a name="controls--qubit"></a>Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

De qubits waarop moet `singlyControlledOp` worden gecontroleerd.
De lengte van `controls` moet mini maal 1 zijn.


### <a name="targets--qubit"></a>doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

De doel-qubits die op wordt uitgevoerd `singlyControlledOp` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Deze bewerking maakt alleen gebruik van schone ancilla qubits.

Zie afbeelding 4,10, sectie 4,3 in Nielsen & Chuang voor uitleg en circuit diagram.

## <a name="references"></a>Referenties

- [*Michael A. Nielsen, Isaac L. Chuang*, Quantum Computation en Quantum Information](http://doi.org/10.1017/CBO9780511976667)

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyMultiControlledC](xref:Microsoft.Quantum.Canon.ApplyMultiControlledC)