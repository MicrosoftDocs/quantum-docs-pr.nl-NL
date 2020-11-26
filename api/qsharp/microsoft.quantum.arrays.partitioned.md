---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Gepartitioneerde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220498"
---
# <a name="partitioned-function"></a>Gepartitioneerde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee splitst u een matrix in meerdere delen.

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a>Invoer

### <a name="nelements--int"></a>nElements: [int](xref:microsoft.quantum.lang-ref.int)[]

Aantal elementen in elk deel van de matrix


### <a name="arr--t"></a>ARR: 'T []

De invoer matrix die moet worden gesplitst.



## <a name="output--t"></a>Uitvoer: ' [] []

Meerdere matrices waarbij de eerste matrix het eerste is `nElements[0]` `arr` en de tweede matrix, `nElements[1]` `arr` enzovoort. De laatste matrix bevat alle resterende elementen.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

