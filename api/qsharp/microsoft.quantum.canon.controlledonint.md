---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: De functie ControlledOnInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 3cc5c00d9c7295106901149e06571ef1963d1323
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207255"
---
# <a name="controlledonint-function"></a>De functie ControlledOnInt

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een unitary-operator die een Oracle toepast op het doel register als de register status van het besturings element overeenkomt met een opgegeven positief geheel getal.

```qsharp
function ControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl)) : ((Qubit[], 'T) => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="numberstate--int"></a>numberState: [int](xref:microsoft.quantum.lang-ref.int)

Positief geheel getal.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Unitary-operator.



## <a name="output--qubitt--unit--is-adj--ctl"></a>Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[], 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL

Een unitary-operator die van toepassing is `oracle` op het doel register als de register status van het besturings element overeenkomt met de nummer status `numberState` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

De waarde van `numberState` wordt geïnterpreteerd met een little-endian-code ring.