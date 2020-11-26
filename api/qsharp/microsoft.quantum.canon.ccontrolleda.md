---
uid: Microsoft.Quantum.Canon.CControlledA
title: De functie CControlledA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledA
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: cb72ca5b3dab99b9ee8a994ba9fde46e0eae5594
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207510"
---
# <a name="ccontrolleda-function"></a>De functie CControlledA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast. Als `false` , gebeurt er niets.
De aanpassings functie `A` geeft aan dat de bewerking is adjointable.

```qsharp
function CControlledA<'T> (op : ('T => Unit is Adj)) : ((Bool, 'T) => Unit is Adj)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit--is-adj"></a>op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie

Een bewerking die voorwaardelijk moet worden toegepast.



## <a name="output--boolt--unit--is-adj"></a>Output: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. CControlled](xref:Microsoft.Quantum.Canon.CControlled)