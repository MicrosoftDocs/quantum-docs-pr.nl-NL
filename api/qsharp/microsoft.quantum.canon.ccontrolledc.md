---
uid: Microsoft.Quantum.Canon.CControlledC
title: De functie CControlledC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: CControlledC
qsharp.summary: Given an operation op, returns a new operation which applies the op if a classical control bit is true. If `false`, nothing happens. The modifier `C` indicates that the operation is controllable.
ms.openlocfilehash: e5975455385e182236d7e2864e26ca00795a40c6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704404"
---
# <a name="ccontrolledc-function"></a>De functie CControlledC

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Als er een bewerking op wordt uitgevoerd, wordt er een nieuwe bewerking geretourneerd waarmee de op voor waarde voor klassieke besturings element wordt toegepast. Als `false` , gebeurt er niets.
De aanpassings functie `C` geeft aan dat de bewerking kan worden bestuurd.

```qsharp
function CControlledC<'T> (op : ('T => Unit is Ctl)) : ((Bool, 'T) => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="op--t--unit-ctl"></a>op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)

Een bewerking die voorwaardelijk moet worden toegepast.



## <a name="output--boolt--unit-ctl"></a>Output: ([BOOL](xref:microsoft.quantum.lang-ref.bool), 't) =>-CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)

Een nieuwe bewerking die zich op bevindt als de klassieke Control-bit True is.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. CControlled](xref:Microsoft.Quantum.Canon.CControlled)