---
uid: Microsoft.Quantum.Math.ModulusL
title: De functie ModulusL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: e7e692059051fde295634c37892ec54e2cf1b095
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709121"
---
# <a name="modulusl-function"></a>De functie ModulusL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


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