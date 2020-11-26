---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Bewerking MeasureStabilizerGenerators
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: 6c048c17df21d1026dc671f30d72a13ed8d8b7f5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200625"
---
# <a name="measurestabilizergenerators-operation"></a>Bewerking MeasureStabilizerGenerators

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Meet de opgegeven set met Generators van een stabilisatoren groep.

```qsharp
operation MeasureStabilizerGenerators (stabilizerGroup : Pauli[][], logicalRegister : Microsoft.Quantum.ErrorCorrection.LogicalRegister, gadget : ((Pauli[], Qubit[]) => Result)) : Microsoft.Quantum.ErrorCorrection.Syndrome
```


## <a name="input"></a>Invoer

### <a name="stabilizergroup--pauli"></a>stabilizerGroup: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []

Een matrix met multiqubit Pauli-Opera tors.
Een voor beeld: `stabilizerGroup[0]` een lijst met Qubit Pauli-matrices, het tensor-product van een stabilisatorer-generator.


### <a name="logicalregister--logicalregister"></a>logicalRegister: [logicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)

Een matrix met qubits waarvan de stabilisatorer code is gedefinieerd.


### <a name="gadget--pauliqubit--__invalidresult__"></a>Gadget: ([Pauli](xref:microsoft.quantum.lang-ref.pauli)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ongeldig <Result>__ 

Een bewerking die aangeeft hoe een multiqubit Pauli-operator moet worden gemeten.



## <a name="output--syndrome"></a>Uitvoer: [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Het resultaat van metingen.

## <a name="remarks"></a>Opmerkingen

Hiermee wordt niet gecontroleerd of de opgegeven set generatoren werkt.
Als ze niet werken, kan het resultaat van metingen wille keurig zijn.