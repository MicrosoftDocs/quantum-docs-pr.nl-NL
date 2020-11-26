---
uid: Microsoft.Quantum.Arrays.Merged
title: Samengevoegde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Merged
qsharp.summary: Given two sorted arrays, returns a single array containing the elements of both in sorted order. Used internally by merge sort.
ms.openlocfilehash: b3383f8a04e6fa23562aa81e5b911d06752f4fb5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220634"
---
# <a name="merged-function"></a>Samengevoegde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

