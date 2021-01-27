---
uid: Microsoft.Quantum.Arrays.Prefixes
title: De functie voor voegsels
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Prefixes
qsharp.summary: Given an array, returns all its prefixes.
ms.openlocfilehash: a2e1721f8f59bf9aa425f04710637023d482a2ca
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845517"
---
# <a name="prefixes-function"></a>De functie voor voegsels

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix, worden alle bijbehorende voor voegsels geretourneerd.

```qsharp
function Prefixes<'T> (array : 'T[]) : 'T[][]
```


## <a name="description"></a>Beschrijving

Retourneert een matrix van alle voor voegsels, beginnend met een matrix die alleen het eerste element tot de volledige matrix heeft.

## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: 'T []

Een matrix met elementen.



## <a name="output--t"></a>Uitvoer: ' [] []



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.

## <a name="example"></a>Voorbeeld

```qsharp
let prefixes = Prefixes([23, 42, 144]);
// prefixes = [[23], [23, 42], [23, 42, 144]]
```