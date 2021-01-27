---
uid: Microsoft.Quantum.Synthesis.ApplyXControlledOnTruthTableWithCleanTarget
title: Bewerking ApplyXControlledOnTruthTableWithCleanTarget
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyXControlledOnTruthTableWithCleanTarget
qsharp.summary: Applies the @"microsoft.quantum.intrinsic.x" operation on `target`, if the Boolean function `func` evaluates to true for the classical assignment in `controlRegister`.
ms.openlocfilehash: a54544cd026f26784bb0c41cb12187a8885ed9db
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855537"
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