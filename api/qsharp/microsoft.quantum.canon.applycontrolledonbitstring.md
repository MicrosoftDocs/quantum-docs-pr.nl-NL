---
uid: Microsoft.Quantum.Canon.ApplyControlledOnBitString
title: Bewerking ApplyControlledOnBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyControlledOnBitString
qsharp.summary: Applies a unitary operation on the target register, controlled on a a state specified by a given bit mask.
ms.openlocfilehash: 82adc74e23e1d50cb6436176a973fdd1a0eeb3bd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841949"
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