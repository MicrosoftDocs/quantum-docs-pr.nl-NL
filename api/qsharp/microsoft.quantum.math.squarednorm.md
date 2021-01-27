---
uid: Microsoft.Quantum.Math.SquaredNorm
title: De functie SquaredNorm
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: SquaredNorm
qsharp.summary: Returns the squared 2-norm of a vector.
ms.openlocfilehash: 72ae8266492bef64eaec34cd70c5fe725ee1e8c9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848221"
---
# <a name="squarednorm-function"></a>De functie SquaredNorm

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de vier Kante 2-norm van een vector.

```qsharp
function SquaredNorm (array : Double[]) : Double
```


## <a name="description"></a>Beschrijving

Retourneert de vier Kante 2-norm van een vector; op basis van de invoer $ \vec{x} $ retourneert $ \ sum_i x_i ^ 2 $.

## <a name="input"></a>Invoer

### <a name="array--double"></a>matrix: [dubbel](xref:microsoft.quantum.lang-ref.double)[]

De vector waarvan het kwadraat 2-norm moet worden geretourneerd.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

De vier Kante 2-norm van `array` .