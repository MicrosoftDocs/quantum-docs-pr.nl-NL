---
uid: Microsoft.Quantum.Canon.ApplyWithCA
title: Bewerking ApplyWithCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWithCA
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: e86c452e9693c5a4d0d4e5a36471ab46bbf66dfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208139"
---
# <a name="applywithca-operation"></a>Bewerking ApplyWithCA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er twee bewerkingen worden uitgevoerd, geldt er een als conjugaat met de andere.

```qsharp
operation ApplyWithCA<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit is Adj + Ctl), target : 'T) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Als er twee bewerkingen worden uitgevoerd, die respectievelijk worden beschreven door unitary Opera tors $U $ en $V $, worden deze toegepast in de volg orde $U ^ {\dagger} V U $. Dat wil zeggen dat met deze bewerking de unitary-operator wordt geïmplementeerd die is opgegeven door $V $ geconjugeerde met $U $.

## <a name="input"></a>Invoer

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

De bewerking $U $ die moet worden gebruikt voor geconjugeerde $V $. Houd er rekening mee dat de buitenste bewerking $U $ moet worden adjointable, maar niet hoeft te worden bestuurd.


### <a name="inneroperation--t--unit--is-adj--ctl"></a>innerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De bewerking $V $ wordt geconjugeerd.


### <a name="target--t"></a>doel: 'T

De invoer die moet worden opgegeven voor de buiten-en de binnenste bewerkingen.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het doel waarop elk van de interne en externe bewerkingen handelen.

## <a name="remarks"></a>Opmerkingen

Er wordt altijd aangenomen dat de buitenste bewerking adjointable is, maar deze hoeft niet te worden bestuurd om de gecombineerde bewerking te kunnen bewerkbaar te maken.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplyWith](xref:Microsoft.Quantum.Canon.ApplyWith)
- [Micro soft. Quantum. Canon. ApplyWithA](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [Micro soft. Quantum. Canon. ApplyWithC](xref:Microsoft.Quantum.Canon.ApplyWithC)