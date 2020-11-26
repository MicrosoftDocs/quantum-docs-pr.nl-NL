---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Bewerking ApplyControlledOnBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 6947d2dbdec4cfbb592143024a7c8ccd53a32029
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219070"
---
# <a name="applycontrolledonbitstring-operation"></a>Bewerking ApplyControlledOnBitString

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een unitary-bewerking op het doel register toegepast, gecontroleerd op een status die is opgegeven door een opgegeven bitmasker.

```qsharp
operation ApplyControlledOnBitString<'T> (bits : Bool[], oracle : ('T => Unit is Adj + Ctl), controlRegister : Qubit[], targetRegister : 'T) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="bits--bool"></a>bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

De bit-teken reeks voor het beheren van de opgegeven unitary-bewerking op.


### <a name="oracle--t--unit--is-adj--ctl"></a>Oracle: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De unitary-bewerking die moet worden toegepast op het doel register.


### <a name="controlregister--qubit"></a>controlRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Quantum registratie waarmee de toepassing van wordt bepaald `oracle` .


### <a name="targetregister--t"></a>targetRegister: 'T

Het doel register dat moet worden door gegeven `oracle` als invoer.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

Het patroon `bits` dat wordt gegeven door, kan korter zijn dan `controlRegister` , in welk geval extra controle qubits worden genegeerd (dat wil zeggen, hetzij niet beheerd op $ \ket {0} $ noch $ \ket {1} $).
Als `bits` de lengte langer is dan `controlRegister` , treedt er een fout op.

`bits = [0,1,0,0,1]`Betekent bijvoorbeeld dat `oracle` wordt toegepast als en alleen als `controlRegister` de status $ \ket {0} \ket {1} \ket {0} \ket {0} \ket {1} $.