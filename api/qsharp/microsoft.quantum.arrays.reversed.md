---
uid: Microsoft.Quantum.Arrays.Reversed
title: Omgekeerde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Reversed
qsharp.summary: Create an array that contains the same elements as an input array but in Reversed order.
ms.openlocfilehash: 50699465711de45ff994095e6c098550d637d608
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845463"
---
# <a name="reversed-function"></a>Omgekeerde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maak een matrix die dezelfde elementen bevat als een invoer matrix, maar in omgekeerde volg orde.

```qsharp
function Reversed<'T> (array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: 'T []

Een matrix waarvan de elementen in omgekeerde volg orde moeten worden gekopieerd.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix met de elementen `array[Length(array) - 1]` .. `array[0]`.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de matrix elementen.