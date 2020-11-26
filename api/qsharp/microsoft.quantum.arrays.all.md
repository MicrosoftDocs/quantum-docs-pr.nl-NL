---
uid: Microsoft.Quantum.Arrays.All
title: Functie all
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: a7c83e38c3c101b712215eb664486fe29863a52b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221688"
---
# <a name="all-function"></a>Functie all

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gegeven een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix en controleert of alle elementen van de matrix voldoen aan het predicaat.

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Invoer

### <a name="predicate--t---bool"></a>predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie van `'T` naar `Bool` die wordt gebruikt om elementen te controleren.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een `Bool` waarde van de functie en van het predikaat dat is toegepast op alle elementen.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.

## <a name="remarks"></a>Opmerkingen

De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een functie hebben `predicate: 'T -> Bool` die we een `Bool` waarde kunnen produceren die aangeeft of alle elementen voldoen `predicate` .