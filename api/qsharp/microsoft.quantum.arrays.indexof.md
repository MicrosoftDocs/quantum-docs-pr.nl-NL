---
uid: Microsoft.Quantum.Arrays.IndexOf
title: De functie IndexOf
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexOf
qsharp.summary: Returns the first index of the first element in an array that satisfies a given predicate. If no such element exists, returns -1.
ms.openlocfilehash: 7ff80f13f432a18f216b2dee4bd65b1e82034fa5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705980"
---
# <a name="indexof-function"></a>De functie IndexOf

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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

