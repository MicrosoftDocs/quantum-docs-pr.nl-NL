---
uid: Microsoft.Quantum.Math.ModulusL
title: De functie ModulusL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 5c9a8ceceac5d2cdac6b82f7f74a85e9443382a2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96194930"
---
# <a name="modulusl-function"></a>De functie ModulusL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berekent het canonieke residu van `value` modulo `modulus` .

```qsharp
function ModulusL (value : BigInt, modulus : BigInt) : BigInt
```


## <a name="input"></a>Invoer

### <a name="value--bigint"></a>waarde: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De waarde van welk residu wordt berekend


### <a name="modulus--bigint"></a>modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De modulus waarmee residuen worden uitgevoerd, moet positief zijn



## <a name="output--bigint"></a>Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Geheel getal $r $ tussen 0 en `modulus - 1` dat `value - r` deelbaar is door modulus

## <a name="remarks"></a>Opmerkingen

Deze functie werkt anders als de operator `%` zich gedraagt in C# en Q # als in het resultaat altijd een positief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.