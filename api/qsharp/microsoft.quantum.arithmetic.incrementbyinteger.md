---
uid: Microsoft.Quantum.Arithmetic.IncrementByInteger
title: Bewerking IncrementByInteger
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: IncrementByInteger
qsharp.summary: Increments an unsigned quantum register by a classical integer, using phase rotations.
ms.openlocfilehash: 363d48d697e3b2dad4d4896e6b1e701864649d9b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707269"
---
# <a name="incrementbyinteger-operation"></a>Bewerking IncrementByInteger

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket [](https://nuget.org/packages/)


Verhoogt een niet-ondertekend Quantum register met een klassiek geheel getal, met behulp van fase rotaties.

```qsharp
operation IncrementByInteger (increment : Int, target : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a>Beschrijving

Stel dat `target` een niet-ondertekend geheel getal $x $ in een code ring van little-endian wordt gecodeerd en `increment` gelijk is aan $a $.
Deze bewerking implementeert vervolgens de unitary $ \ket{x} \mapsto \ket{x + a} $, waarbij de aanvulling wordt uitgevoerd modulo $2 ^ n $, waarbij $n = \texttt{Length (doel!)} $.

## <a name="input"></a>Invoer

### <a name="increment--int"></a>interval: [int](xref:microsoft.quantum.lang-ref.int)

Het gehele getal waarmee de `target` wordt verhoogd.


### <a name="target--littleendian"></a>doel: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

Een Quantum register codeert een niet-ondertekend geheel getal door gebruik te maken van code ring van little-endian.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

