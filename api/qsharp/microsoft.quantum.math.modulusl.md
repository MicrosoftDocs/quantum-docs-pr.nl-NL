---
uid: Microsoft.Quantum.Math.ModulusL
title: De functie ModulusL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ModulusL
qsharp.summary: Computes the canonical residue of `value` modulo `modulus`.
ms.openlocfilehash: 6be2edb052cf55f8e8465c76b5dcadeb61ff11ea
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842746"
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

Deze functie werkt anders als de operator `%` zich in C# en Q # bevindt, zoals in het resultaat altijd een niet-negatief geheel getal tussen 0 en `modulus - 1` , zelfs als de waarde negatief is.