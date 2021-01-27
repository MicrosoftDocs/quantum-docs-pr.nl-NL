---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Gepartitioneerde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: 43d99a0e33a813e4af23a3890ace808e91c1049c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845545"
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



## <a name="example"></a>Voorbeeld

```qsharp
// The following returns [[1, 5], [3], [7]];
let split = Partitioned([2,1], [1,5,3,7]);
```