---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Bewerking ApplyXControlledOnTruthTableWithCleanTarget
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: 904ff7e2e7e81ee966846af120e9427f4e92301c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203260"
---
# <a name="applyxcontrolledontruthtablewithcleantarget-operation"></a>Bewerking ApplyXControlledOnTruthTableWithCleanTarget

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


De bewerking wordt toegepast @"microsoft.quantum.intrinsic.x" op `target` als de Boole-functie `func` resulteert in waar voor de klassieke toewijzing in `controlRegister` .

```qsharp
operation ApplyXControlledOnTruthTableWithCleanTarget (func : BigInt, controlRegister : Qubit[], target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt een speciaal geval geïmplementeerd @"microsoft.quantum.synthesis.applyxcontrolledontruthtable" , waarbij de doel-Qubit bekend staat als de $ \ket $- {0} status.

De implementatie maakt gebruik van @"microsoft.quantum.intrinsic.cnot" en @"microsoft.quantum.intrinsic.r1" poorten.  De implementatie van de adjoint-bewerking is geoptimaliseerd en maakt gebruik van op metingen gebaseerde onreken bewerkingen.

## <a name="input"></a>Invoer

### <a name="func--bigint"></a>FUNC: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Tabel met Boole-waarheid wordt weer gegeven als Big-geheel getal


### <a name="controlregister--qubit"></a>controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

REGI ster van controle qubits


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Doel-Qubit (moet de status $ \ket {0} $ hebben)



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. synthese. ApplyXControlledOnTruthTable](xref:Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTable)