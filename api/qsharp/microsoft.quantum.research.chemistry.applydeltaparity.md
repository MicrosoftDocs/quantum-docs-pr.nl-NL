---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Bewerking ApplyDeltaParity
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: bb01eb684ff1820be08a573c0ca6cfc12efeb889
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708641"
---
# <a name="applydeltaparity-operation"></a>Bewerking ApplyDeltaParity

Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)

Pakket [](https://nuget.org/packages/)


Berekent het verschil in pariteit tussen een vorige PQRS... voor waarden en de volgende PQRS... mandaat. Dit verschil wordt berekend op een hulp Qubit.

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="prevfermionicterm--int"></a>prevFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]

Lijst met indexen voor vorige PQRS... inzake.


### <a name="nextfermionicterm--int"></a>nextFermionicTerm: [int](xref:microsoft.quantum.lang-ref.int)[]

Lijst met indexen voor de volgende PQRS... inzake.


### <a name="aux--qubit"></a>AUX: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Hulp Qubit waarop de resultaten van de pariteits berekening worden opgeslagen.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit verwerkt door alle PQRS... inzake.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Hierbij wordt ervan uitgegaan dat de indices P < Q < R < S <... voor zowel prevPQ als nextPQ.