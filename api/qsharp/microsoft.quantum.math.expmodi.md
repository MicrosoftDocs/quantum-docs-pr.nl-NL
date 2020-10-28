---
uid: Microsoft.Quantum.Math.ExpModI
title: De functie ExpModI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708377"
---
# <a name="expmodi-function"></a>De functie ExpModI

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


Retourneert een geheel getal dat tot een bepaalde macht is verheven, ten opzichte van een bepaalde modulus.

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a>Beschrijving

Laat ons expBase van $x $, kracht door $p $ en modulus door $N $.
De functie retourneert $x ^ p \operatorname{mod} N $.

We gaan ervan uit dat $N $, $x $ positief is en de stroom niet negatief is.

## <a name="input"></a>Invoer

### <a name="expbase--int"></a>expBase: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="modulus--int"></a>modulus: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="remarks"></a>Opmerkingen

Neemt de tijd in verhouding tot het aantal bits in `power` , niet de `power` zelf.