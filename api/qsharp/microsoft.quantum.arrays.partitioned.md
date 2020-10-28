---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Gepartitioneerde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705845"
---
# <a name="partitioned-function"></a>Gepartitioneerde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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

