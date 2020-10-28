---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705957"
---
# <a name="interleaved-function"></a>Interleaved functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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