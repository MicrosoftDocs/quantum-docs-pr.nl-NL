---
uid: Microsoft.Quantum.ErrorCorrection.MeasureStabilizerGenerators
title: Bewerking MeasureStabilizerGenerators
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: MeasureStabilizerGenerators
qsharp.summary: Measures the given set of generators of a stabilizer group.
ms.openlocfilehash: a3f48ff24a39d13a57f7a144e21d4e41bb8a8b49
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702452"
---
# <a name="measurestabilizergenerators-operation"></a>Bewerking MeasureStabilizerGenerators

Naam ruimte: [micro soft. Quantum. ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)

Pakket [](https://nuget.org/packages/)


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


### <a name="gadget--pauliqubit--__invalidresult__"></a>Gadget: ( [Pauli](xref:microsoft.quantum.lang-ref.pauli)[], [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => __ongeldig <Result>__ 

Een bewerking die aangeeft hoe een multiqubit Pauli-operator moet worden gemeten.



## <a name="output--syndrome"></a>Uitvoer: [Syndrome](xref:Microsoft.Quantum.ErrorCorrection.Syndrome)

Het resultaat van metingen.

## <a name="remarks"></a>Opmerkingen

Hiermee wordt niet gecontroleerd of de opgegeven set generatoren werkt.
Als ze niet werken, kan het resultaat van metingen wille keurig zijn.