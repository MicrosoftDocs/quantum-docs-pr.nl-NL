---
uid: Microsoft.Quantum.Canon.ApplyToPartitionC
title: Bewerking ApplyToPartitionC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToPartitionC
qsharp.summary: Applies a pair of operations to a given partition of a register into two parts. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: 43cf43fa2bf9c00a4096b39555b8f6080dd506d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850531"
---
# <a name="applytopartitionc-operation"></a>Bewerking ApplyToPartitionC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een paar bewerkingen toegepast op een bepaalde partitie van een REGI ster in twee delen.
De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.

```qsharp
operation ApplyToPartitionC (op : ((Qubit[], Qubit[]) => Unit is Ctl), numberOfQubitsToFirstArgument : Int, target : Qubit[]) : Unit is Ctl
```


## <a name="input"></a>Invoer

### <a name="op--qubitqubit--unit--is-ctl"></a>op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Het paar bewerkingen dat moet worden toegepast op de opgegeven partitie.


### <a name="numberofqubitstofirstargument--int"></a>numberOfQubitsToFirstArgument: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits van het doel dat in het eerste deel van de partitie moet worden geplaatst.
De resterende qubits vormt het tweede deel van de partitie.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een REGI ster van qubits die worden gepartitioneerd en worden uitgevoerd door de opgegeven twee bewerkingen.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyToPartition](xref:Microsoft.Quantum.Canon.ApplyToPartition)