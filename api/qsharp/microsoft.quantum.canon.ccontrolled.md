---
uid: Microsoft.Quantum.Canon.CControlled
title: De functie CControlled
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlled
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens.
ms.openlocfilehash: f4d91471eae859b7018c9e7ea0c1c853619c484d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841016"
---
# <a name="ccontrolled-function"></a>De functie CControlled

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast. Als `false` , gebeurt er niets.

```qsharp
function CControlled<'T> (op : ('T => Unit)) : ((Bool, 'T) => Unit)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit"></a>op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking die voorwaardelijk moet worden toegepast.



## <a name="output--boolt--unit"></a>Uitvoer: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) =>- [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. CControlledC](xref:Microsoft.Quantum.Canon.CControlledC)
- [Micro soft. Quantum. Canon. CControlledA](xref:Microsoft.Quantum.Canon.CControlledA)
- [Micro soft. Quantum. Canon. CControlledCA](xref:Microsoft.Quantum.Canon.CControlledCA)