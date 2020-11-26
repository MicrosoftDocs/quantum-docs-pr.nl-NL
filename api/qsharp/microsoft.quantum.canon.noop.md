---
uid: Microsoft.Quantum.Canon.NoOp
title: Bewerking Nooperation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: NoOp
qsharp.summary: Performs the identity operation (no-op) on an argument.
ms.openlocfilehash: 35b6b62cab35f941f04b150dcca763457ddaa084
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205963"
---
# <a name="noop-operation"></a>Bewerking Nooperation

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Hiermee wordt de identiteits bewerking (geen-op) uitgevoerd op een argument.

```qsharp
operation NoOp<'T> (input : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Met deze bewerking wordt een waarde van elk type gebruikt en gebeurt er niets.
Dit kan handig zijn wanneer een invoer van een bewerkings type wordt verwacht, maar er geen actie moet worden ondernomen.
Als bijvoorbeeld een bepaalde fout correctie Syndrome aangeeft dat er geen fout is opgetreden, `NoOp<Qubit[]>` kan de juiste herstel procedure zijn.
Als een bewerking een status voorbereidings procedure als invoer verwacht, `NoOp<Qubit[]>` kan deze ook worden gebruikt om de status te voorbereiden $ \ket{0 \cdots 0} $.

## <a name="input"></a>Invoer

### <a name="input--t"></a>invoer: 'T

Een waarde die moet worden genegeerd.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

In bijna alle gevallen moet de para meter type `NoOp` expliciet worden opgegeven. `NoOp<Qubit>`Is bijvoorbeeld gelijk aan <xref:microsoft.quantum.intrinsic.i> .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. intrinsiek. Ik](xref:Microsoft.Quantum.Intrinsic.I)