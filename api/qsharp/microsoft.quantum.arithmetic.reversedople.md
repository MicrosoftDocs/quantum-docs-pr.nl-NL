---
uid: Microsoft.Quantum.Arithmetic.ReversedOpLE
title: De functie ReversedOpLE
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpLE
qsharp.summary: Given an operation that takes a little-endian input, returns a new operation that takes a big-endian input.
ms.openlocfilehash: d02817e5372b841f3ab633cafa22af603c5310c2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846394"
---
# <a name="reversedople-function"></a>De functie ReversedOpLE

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er een bewerking wordt uitgevoerd die de invoer van Little Endian accepteert, wordt een nieuwe bewerking met een invoer van big endian geretourneerd.

```qsharp
function ReversedOpLE (op : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit)) : (Microsoft.Quantum.Arithmetic.BigEndian => Unit)
```


## <a name="input"></a>Invoer

### <a name="op--littleendian--unit"></a>op: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

De bewerking waarvan de invoer moet worden omgekeerd.



## <a name="output--bigendian--unit"></a>Uitvoer: [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) - => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een nieuwe bewerking die de invoer accepteert als een big endian-REGI ster.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. aritmetische. ApplyReversedOpLE](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpLE)
- [Micro soft. Quantum. aritmetische. ReversedOpLEA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEA)
- [Micro soft. Quantum. aritmetische. ReversedOpLEC](xref:Microsoft.Quantum.Arithmetic.ReversedOpLEC)
- [Micro soft. Quantum. aritmetische. ReversedOpLECA](xref:Microsoft.Quantum.Arithmetic.ReversedOpLECA)