---
uid: Microsoft.Quantum.Arrays.Count
title: Functie Count
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 48b75cc6d6584f899223a0803f31fd174836f303
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221552"
---
# <a name="count-function"></a>Functie Count

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, retourneert het aantal elementen een matrix die bestaat uit die elementen die voldoen aan het predicaat.

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a>Invoer

### <a name="predicate--t---bool"></a>predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie van `'T` naar een Booleaanse waarde die wordt gebruikt voor het filteren van elementen.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal elementen in `array` dat voldoet aan het predicaat.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.

## <a name="remarks"></a>Opmerkingen

De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een predikaat hebben waarop `'T -> Bool` we elementen kunnen filteren.