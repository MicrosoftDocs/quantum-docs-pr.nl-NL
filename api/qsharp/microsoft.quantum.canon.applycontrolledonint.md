---
uid: Microsoft.Quantum.Canon.ApplyControlledOnInt
title: Bewerking ApplyControlledOnInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnInt
qsharp.summary: Applies a unitary operation on the target register if the control register state corresponds to a specified positive integer.
ms.openlocfilehash: 499a25104742b2d03886065baad4d535ea92e83b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845103"
---
# <a name="applycontrolledonint-operation"></a>Bewerking ApplyControlledOnInt

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een unitary-bewerking op het doel register toe als de register status van het besturings element overeenkomt met een opgegeven positief geheel getal.

```qsharp
operation ApplyControlledOnInt<'T> (numberState : Int, oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="numberstate--int"></a>numberState: [int](xref:microsoft.quantum.lang-ref.int)

Een niet-negatief geheel getal waarop de bewerking `oracle` moet worden beheerd.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een unitary-bewerking die moet worden beheerd.


### <a name="controlregister--qubit"></a>controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Quantum registratie waarmee de toepassing van wordt bepaald `oracle` .


### <a name="targetregister--t"></a>targetRegister: 'T

Een REGI ster waarop moet worden toegepast `oracle` .



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

De waarde van `numberState` wordt geïnterpreteerd met een little-endian-code ring.

`numberState` mag Maxi maal $2 ^ \texttt{Length (controlRegister)}-$1 zijn.
`numberState = 537`Betekent bijvoorbeeld dat `oracle` wordt toegepast als en alleen als `controlRegister` de status $ \ket {537} $.