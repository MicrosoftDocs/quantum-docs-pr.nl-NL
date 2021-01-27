---
uid: Microsoft.Quantum.Math.ModulusI
title: De functie ModulusI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 7bad044db9e2229c85cb3909dc4802bceaee6382
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847294"
---
# <a name="modulusi-function"></a>De functie ModulusI

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berekent het canonieke residu van `value` modulo `modulus` .

```qsharp
function ModulusI (value : Int, modulus : Int) : Int
```


## <a name="input"></a>Invoer

### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)

De waarde van welk residu wordt berekend


### <a name="modulus--int"></a>modulus: [int](xref:microsoft.quantum.lang-ref.int)

De modulus waarmee residuen worden uitgevoerd, moet positief zijn



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Geheel getal $r $ tussen 0 en `modulus - 1` dat `value - r` deelbaar is door modulus

## <a name="remarks"></a>Opmerkingen

Deze functie werkt anders als de operator `%` zich in C# en Q # bevindt, zoals in het resultaat altijd een niet-negatief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.