---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220957"
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