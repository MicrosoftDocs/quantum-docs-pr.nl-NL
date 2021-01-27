---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBE
title: De functie ReversedOpBE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBE
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 878b0fae8a803b3136d1537309c945c052e1052c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846487"
---
# <a name="reversedopbe-function"></a>De functie ReversedOpBE

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er een bewerking wordt uitgevoerd waarbij een big endian-invoer wordt gebruikt, wordt er een nieuwe bewerking met een invoer van Little Endian geretourneerd.

```qsharp
function ReversedOpBE (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)
```


## <a name="input"></a>Invoer

### <a name="op--bigendian--unit"></a>op: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

De bewerking waarvan de invoer moet worden omgekeerd.



## <a name="output--littleendian--unit"></a>Uitvoer: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een nieuwe bewerking die de invoer accepteert als een little endian-registratie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. ApplyReversedOpBE](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBE)
- [Micro soft. Quantum. aritmetische. ReversedOpBEA](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [Micro soft. Quantum. aritmetische. ReversedOpBEC](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEC)
- [Micro soft. Quantum. aritmetische. ReversedOpBECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)