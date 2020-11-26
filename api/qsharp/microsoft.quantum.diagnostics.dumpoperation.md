---
uid: Microsoft.Quantum.Diagnostics.DumpOperation
title: Bewerking DumpOperation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: DumpOperation
qsharp.summary: Given an operation, displays diagnostics about the operation that are made available by the current execution target.
ms.openlocfilehash: b0e07173ddbeb8a96d4a85928258b6e30deb394d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202053"
---
# <a name="dumpoperation-operation"></a>Bewerking DumpOperation

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een bewerking worden diagnostische gegevens weer gegeven over de bewerking die beschikbaar is gemaakt door het huidige doel van de uitvoering.

```qsharp
operation DumpOperation (nQubits : Int, op : (Qubit[] => Unit is Adj)) : Unit
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits waarop de opgegeven bewerking reageert.


### <a name="op--qubit--unit--is-adj"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

De bewerking die moet worden gecontroleerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Het aanroepen van deze bewerking heeft geen waarneembaar effect van binnen Q #. De exacte diagnostische gegevens die worden weer gegeven, zijn afhankelijk van de huidige uitvoer doel-en-Editor omgeving.
Als er bijvoorbeeld gebruik wordt gemaakt van de volledige Quantum-Simulator, wordt een unitary-matrix weer gegeven die wordt gebruikt om aan te duiden `op` .

Houd er rekening mee dat bij het uitvoeren van simulatoren die een globale fase ambiguïteit veroorzaken (bijvoorbeeld: de Full-State Simulator), geretourneerde representaties kunnen variëren tot een globale fase.

De volg orde van de weer gaven van rijen en kolommen matrix kan ook verschillen met de conventies die worden gebruikt door elke Simulator die deze bewerking ondersteunt.