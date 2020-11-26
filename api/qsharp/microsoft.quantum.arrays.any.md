---
uid: Microsoft.Quantum.Arrays.Any
title: Een functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: 717ab9ebcbb864a6faf1c14cd36125e589849f2e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221654"
---
# <a name="any-function"></a>Een functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, wordt gecontroleerd of ten minste één element van de matrix voldoet aan het predicaat.

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Invoer

### <a name="predicate--t---bool"></a>predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie van `'T` naar `Bool` die wordt gebruikt om elementen te controleren.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een `Bool` waarde van de functie or van het predikaat dat is toegepast op alle elementen.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.

## <a name="remarks"></a>Opmerkingen

De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een functie hebben `predicate: 'T -> Bool` die we een `Bool` waarde kunnen produceren die aangeeft of een bepaald element voldoet aan het resultaat `predicate` .