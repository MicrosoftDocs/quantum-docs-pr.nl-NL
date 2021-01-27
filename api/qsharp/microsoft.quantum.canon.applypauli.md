---
uid: Microsoft.Quantum.Canon.ApplyPauli
title: Bewerking ApplyPauli
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauli
qsharp.summary: Given a multi-qubit Pauli operator, applies the corresponding operation to a register.
ms.openlocfilehash: b3557c6d8b5a90019f6d4cfa7b405475a3ab39fb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844738"
---
# <a name="applypauli-operation"></a>Bewerking ApplyPauli

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een multi-Qubit Pauli-operator, wordt de bijbehorende bewerking toegepast op een registratie.

```qsharp
operation ApplyPauli (pauli : Pauli[], target : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Een multi-Qubit Pauli-operator wordt weer gegeven als een matrix van Pauli Opera tors met één Qubit.


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registreer om de opgegeven Pauli-bewerking op toe te passen.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

De volgende zijn gelijkwaardig:

```qsharp
ApplyPauli([PauliY, PauliZ, PauliX], target);
```

en

```qsharp
Y(target[0]);
Z(target[1]);
X(target[2]);
```