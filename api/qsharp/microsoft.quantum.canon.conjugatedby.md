---
uid: Microsoft.Quantum.Canon.ConjugatedBy
title: De functie ConjugatedBy
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ConjugatedBy
qsharp.summary: Given outer and inner operations, returns a new operation that conjugates the inner operation by the outer operation.
ms.openlocfilehash: c11e6b2cc97e682bf4fe266997f60ce69e87ba96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840878"
---
# <a name="conjugatedby-function"></a>De functie ConjugatedBy

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er buiten-en binnenste bewerkingen worden uitgevoerd, retourneert een nieuwe bewerking die de binnenste bewerking aan de buitenste bewerking heeft toegezien.

```qsharp
function ConjugatedBy<'T> (outerOperation : ('T => Unit is Adj), innerOperation : ('T => Unit)) : ('T => Unit)
```


## <a name="input"></a>Invoer

### <a name="outeroperation--t--unit--is-adj"></a>outerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

De bewerking $U $ die moet worden gebruikt voor geconjugeerde $V $. Houd er rekening mee dat de buitenste bewerking $U $ moet worden adjointable, maar niet hoeft te worden bestuurd.


### <a name="inneroperation--t--unit"></a>innerOperation: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

De bewerking $V $ wordt geconjugeerd.



## <a name="output--t--unit"></a>Uitvoer: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een nieuwe bewerking waarvan de actie wordt vertegenwoordigd door de unitary $U ^ {\dagger} V U $.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type doel waarop de interne en externe bewerkingen handelen.

## <a name="remarks"></a>Opmerkingen

Er wordt altijd aangenomen dat de buitenste bewerking adjointable is, maar deze hoeft niet te worden bestuurd om de gecombineerde bewerking te kunnen bewerkbaar te maken.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ConjugatedByA](xref:Microsoft.Quantum.Canon.ConjugatedByA)
- [Micro soft. Quantum. Canon. ConjugatedByC](xref:Microsoft.Quantum.Canon.ConjugatedByC)
- [Micro soft. Quantum. Canon. ConjugatedByCA](xref:Microsoft.Quantum.Canon.ConjugatedByCA)
- [Micro soft. Quantum. Canon. ApplyWith](xref:Microsoft.Quantum.Canon.ApplyWith)