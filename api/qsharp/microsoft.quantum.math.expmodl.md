---
uid: Microsoft.Quantum.Math.ExpModL
title: De functie ExpModL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708533"
---
# <a name="expmodl-function"></a>De functie ExpModL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


Retourneert een geheel getal dat tot een bepaalde macht is verheven, ten opzichte van een bepaalde modulus.

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a>Beschrijving

Laat ons expBase van $x $, kracht door $p $ en modulus door $N $.
De functie retourneert $x ^ p \operatorname{mod} N $.

We gaan ervan uit dat $N $, $x $ positief is en de stroom niet negatief is.

## <a name="input"></a>Invoer

### <a name="expbase--bigint"></a>expBase: [BigInt](xref:microsoft.quantum.lang-ref.bigint)




### <a name="power--bigint"></a>macht: [BigInt](xref:microsoft.quantum.lang-ref.bigint)




### <a name="modulus--bigint"></a>modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)





## <a name="output--bigint"></a>Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)



## <a name="remarks"></a>Opmerkingen

Neemt de tijd in verhouding tot het aantal bits in `power` , niet de `power` zelf.