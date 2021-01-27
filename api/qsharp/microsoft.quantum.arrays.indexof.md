---
uid: Microsoft.Quantum.Arrays.IndexOf
title: De functie IndexOf
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 64db55e831078a7130a3ced6a30bfbd2299c392d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848512"
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



## <a name="example"></a>Voorbeeld

Stel dat dit `IsEven : Int -> Bool` een functie is die als resultaat wordt gegeven `true` als de invoer van een even getal is. Dit kan vervolgens worden gebruikt `IndexOf` om het eerste even element in een matrix te vinden:

```qsharp
let items = [1, 3, 17, 2, 21];
let idx = IndexOf(IsEven, items); // returns 3
```