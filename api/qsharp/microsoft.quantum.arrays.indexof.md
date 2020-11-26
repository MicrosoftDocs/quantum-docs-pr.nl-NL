---
uid: Microsoft.Quantum.Arrays.IndexOf
title: De functie IndexOf
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: d63b204334611f8f2c3860f9ee1d756f637780e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221008"
---
# <a name="indexof-function"></a>De functie IndexOf

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de eerste index van het eerste element in een matrix die voldoet aan een bepaald predicaat. Als dit element niet bestaat, retourneert-1.

```qsharp
function IndexOf<'T> (predicate : ('T -> Bool), arr : 'T[]) : Int
```


## <a name="input"></a>Invoer

### <a name="predicate--t---bool"></a>predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een predikaatshape die wordt gebruikt voor elementen van de matrix.


### <a name="arr--t"></a>ARR: 'T []

Een matrix die moet worden doorzocht met behulp van het opgegeven predicaat.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De kleinste index `idx` `predicate(arr[idx])` , bijvoorbeeld waar, of-1 als er geen dergelijk element bestaat.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

