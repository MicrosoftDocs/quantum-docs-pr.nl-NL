---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 3605c0d0bc43cdb1097d025861c3ec2424763c86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848120"
---
# <a name="interleaved-function"></a>Interleaved functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Interleaving heeft twee matrices van (bijna) dezelfde grootte.

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a>Beschrijving

Deze functie retourneert de interleaving van twee matrices, te beginnen met het eerste element van de eerste matrix, vervolgens het eerste element van de tweede matrix, enzovoort.

De eerste matrix moet even lang zijn als de tweede, of kan een groter element hebben.

## <a name="input"></a>Invoer

### <a name="first--t"></a>First: ' []

De eerste matrix die u wilt laten Interleaved.


### <a name="second--t"></a>seconde: ' []

De tweede matrix die u wilt laten Interleaved.



## <a name="output--t"></a>Uitvoer: ' []

Interleaved matrix

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `first` en `second` .

## <a name="example"></a>Voorbeeld

```qsharp
// same as int1 = [1, -1, 2, -2, 3, -3]
let int1 = Interleaved([1, 2, 3], [-1, -2, -3])

// same as int2 = [false, true, false, true, false]
let int2 = Interleaved(ConstantArray(3, false), ConstantArray(2, true));
```