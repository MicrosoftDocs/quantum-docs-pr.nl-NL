---
uid: Microsoft.Quantum.Canon.ApplyWith
title: Bewerking ApplyWith
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyWith
qsharp.summary: Given two operations, applies one as conjugated with the other.
ms.openlocfilehash: 7127df047a260b18d75efb092e8e090e2d0b207a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850413"
---
# <a name="applywith-operation"></a>Bewerking ApplyWith

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er twee bewerkingen worden uitgevoerd, geldt er een als conjugaat met de andere.

```qsharp
operation ApplyWith<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit), target : 'T) : Unit
```


## <a name="description"></a>Beschrijving

Als er twee bewerkingen worden uitgevoerd, die respectievelijk worden beschreven door unitary Opera tors $U $ en $V $, worden deze toegepast in de volg orde $U ^ {\dagger} V U $. Dat wil zeggen dat met deze bewerking de unitary-operator wordt geïmplementeerd die is opgegeven door $V $ geconjugeerde met $U $.

## <a name="input"></a>Invoer

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

De bewerking $U $ die moet worden gebruikt voor geconjugeerde $V $. Houd er rekening mee dat de buitenste bewerking $U $ moet worden adjointable, maar niet hoeft te worden bestuurd.


### <a name="inneroperation--t--unit"></a>innerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

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

- [Micro soft. Quantum. Canon. ApplyWithA](xref:Microsoft.Quantum.Canon.ApplyWithA)
- [Micro soft. Quantum. Canon. ApplyWithC](xref:Microsoft.Quantum.Canon.ApplyWithC)
- [Micro soft. Quantum. Canon. ApplyWithCA](xref:Microsoft.Quantum.Canon.ApplyWithCA)