---
uid: Microsoft.Quantum.Math.ModulusI
title: De functie ModulusI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusI
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 3f698a00b2c8d94b7cb3cca4f1721c659918f4a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708262"
---
# <a name="modulusi-function"></a>De functie ModulusI

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


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

Deze functie werkt anders als de operator `%` zich gedraagt in C# en Q # als in het resultaat altijd een positief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.