---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLEC
title: De functie ReversedOpLEC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLEC
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: 2dc6a596970f909af9c329dbe7002c165854cfec
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846382"
---
# <a name="reversedoplec-function"></a>De functie ReversedOpLEC

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er een bewerking wordt uitgevoerd die de invoer van Little Endian accepteert, wordt een nieuwe bewerking met een invoer van big endian geretourneerd.

```qsharp
function ReversedOpLEC (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)
```


## <a name="input"></a>Invoer

### <a name="op--littleendian--unit--is-ctl"></a>op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is CTL

De bewerking waarvan de invoer moet worden omgekeerd.



## <a name="output--bigendian--unit--is-ctl"></a>Output: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL

Een nieuwe bewerking die de invoer accepteert als een big endian-REGI ster.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. ApplyReversedOpLEC](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLEC)
- [Micro soft. Quantum. aritmetische. ReversedOpLE](xref:Microsoft.Quantum.Arithmetic.ReversedOpLE)
- [Micro soft. Quantum. aritmetische. ReversedOpLEA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Micro soft. Quantum. aritmetische. ReversedOpLECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)