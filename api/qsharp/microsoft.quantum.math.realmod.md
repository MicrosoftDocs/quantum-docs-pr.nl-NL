---
uid: Microsoft.Quantum.Math.RealMod
title: De functie RealMod
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: RealMod
qsharp.summary: Computes the modulus between two real numbers.
ms.openlocfilehash: 6ec799885bd2f0d35314ed727356499efbe9fcf8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706797"
---
# <a name="realmod-function"></a>De functie RealMod

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket [](https://nuget.org/packages/)


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



## <a name="remarks"></a>Opmerkingen

Deze functie berekent de werkelijke modulus door de werkelijke lijn over de eenheids cirkel te verpakken en vervolgens de hoek op de eenheids cirkel te vinden die overeenkomt met de invoer.
De `minValue` invoer wordt vervolgens effectief opgegeven waar de eenheids cirkel moet worden geknipt.