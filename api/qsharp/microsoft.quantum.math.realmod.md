---
uid: Microsoft.Quantum.Math.RealMod
title: De functie RealMod
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 56da313fabb20655ec358120b8d9b435e4971159
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848348"
---
# <a name="realmod-function"></a>De functie RealMod

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berekent de modulus tussen twee reële getallen.

```qsharp
function RealMod (value : Double, modulo : Double, minValue : Double) : Double
```


## <a name="input"></a>Invoer

### <a name="value--double"></a>waarde: [Double](xref:microsoft.quantum.lang-ref.double)

Een reëel getal $x $ om de modulus van te maken.


### <a name="modulo--double"></a>modulo: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een reëel getal voor het nemen van de modulus van $x $ ten opzichte van.


### <a name="minvalue--double"></a>minValue: [dubbel](xref:microsoft.quantum.lang-ref.double)

De kleinste waarde die door deze functie moet worden geretourneerd.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)



## <a name="example"></a>Voorbeeld

```qsharp
    // Returns 3 π / 2.
    let y = RealMod(5.5 * PI(), 2.0 * PI(), 0.0);
    // Returns -1.2, since +3.6 and -1.2 are 4.8 apart on the real line,
    // which is a multiple of 2.4.
    let z = RealMod(3.6, 2.4, -1.2);
```

## <a name="remarks"></a>Opmerkingen

Deze functie berekent de werkelijke modulus door de werkelijke lijn over de eenheids cirkel te verpakken en vervolgens de hoek op de eenheids cirkel te vinden die overeenkomt met de invoer.
De `minValue` invoer wordt vervolgens effectief opgegeven waar de eenheids cirkel moet worden geknipt.