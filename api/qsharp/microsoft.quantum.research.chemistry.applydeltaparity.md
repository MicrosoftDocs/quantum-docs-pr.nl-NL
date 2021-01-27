---
uid: Microsoft.Quantum.Research.Chemistry.ApplyDeltaParity
title: Bewerking ApplyDeltaParity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: ApplyDeltaParity
qsharp.summary: Computes difference in parity between a previous PQRS... terms and the next PQRS... term. This difference is computed on a auxiliary qubit.
ms.openlocfilehash: f5f1d74274994f042f1bc3f2e0d5332f504be02c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851098"
---
# <a name="applydeltaparity-operation"></a>Bewerking ApplyDeltaParity

Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)

Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)


Berekent het verschil in pariteit tussen een vorige PQRS... voor waarden en de volgende PQRS... mandaat. Dit verschil wordt berekend op een hulp Qubit.

```qsharp
operation ApplyDeltaParity (prevFermionicTerm : Int[], nextFermionicTerm : Int[], aux : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
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