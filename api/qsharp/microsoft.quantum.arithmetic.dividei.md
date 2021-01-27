---
uid: Microsoft.Quantum.Arithmetic.DivideI
title: Bewerking DivideI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: DivideI
qsharp.summary: Divides two quantum integers.
ms.openlocfilehash: 73c4e394ca38b8089b2990f8a8b6a3ee50f644d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846689"
---
# <a name="dividei-operation"></a>Bewerking DivideI

Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)

Pakket: [micro soft. Quantum. numerics](https://nuget.org/packages/Microsoft.Quantum.Numerics)


Deelt twee Quantum-gehele getallen.

```qsharp
operation DivideI (xs : Microsoft.Quantum.Arithmetic.LittleEndian, ys : Microsoft.Quantum.Arithmetic.LittleEndian, result : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

`xs` houdt het restant `xs - floor(xs/ys) * ys` en `result` zal in beslaan `floor(xs/ys)` .

## <a name="input"></a>Invoer

### <a name="xs--littleendian"></a>XS: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bits-dividend wordt vervangen door de rest.


### <a name="ys--littleendian"></a>kalenderda: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$-bit-deler $n


### <a name="result--littleendian"></a>resultaat: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)

$n $-bit-resultaat moet de status $ \ket {0} $ in eerste instantie hebben en wordt vervangen door het resultaat van de deling geheel getal.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Maakt gebruik van een standaard aanpak voor Shift en aftrekken om de deling te implementeren.
De gecontroleerde versie is gespecialiseerd, maar er zijn geen extra besturings elementen vereist voor het aftrekken.