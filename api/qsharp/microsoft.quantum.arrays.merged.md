---
uid: Microsoft.Quantum.Arrays.Merged
title: Samengevoegde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: da15a36f8f057cdc15062c96070ec21becc4794a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705869"
---
# <a name="merged-function"></a>Samengevoegde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Als er twee gesorteerde matrices worden opgegeven, wordt er één matrix met de elementen van beide in gesorteerde volg orde geretourneerd. Intern gebruikt door samen voegen sorteren.

```qsharp
function Merged<'T> (comparison : (('T, 'T) -> Bool), left : 'T[], right : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="comparison--tt---bool"></a>vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)




### <a name="left--t"></a>links: ' []




### <a name="right--t"></a>rechts: ' []





## <a name="output--t"></a>Uitvoer: ' []



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

