---
uid: Microsoft.Quantum.Math.ExpModL
title: De functie ExpModL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 127f2e51e19c76f4f7973bf1ac2217d4fffd72f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848360"
---
# <a name="expmodl-function"></a>De functie ExpModL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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