---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBECA
title: De functie ReversedOpBECA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBECA
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 09bb99645d5946af0e0c654500165077691f8da3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846416"
---
# <a name="reversedopbeca-function"></a>De functie ReversedOpBECA

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.

```qsharp
function ReversedOpBECA (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Adj + Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="op--bigendian--unit--is-adj--ctl"></a>op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

De bewerking waarvan de invoer moet worden omgekeerd.



## <a name="output--littleendian--unit--is-adj--ctl"></a>Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL

Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. ApplyReversedOpBECA](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBECA)
- [Micro soft. Quantum. aritmetische. ReversedOpBE](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [Micro soft. Quantum. aritmetische. ReversedOpBEA](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [Micro soft. Quantum. aritmetische. ReversedOpBEC](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)