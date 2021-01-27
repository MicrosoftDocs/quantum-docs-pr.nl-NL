---
uid: Microsoft.Quantum.Canon.ControlledOnInt
title: De functie ControlledOnInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ControlledOnInt
qsharp.summary: Returns a unitary operator that applies an oracle on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 6c7f46c44f2a2427f702e463195f26660cb4fca1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840791"
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