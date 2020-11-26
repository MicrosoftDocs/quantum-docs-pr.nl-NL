---
uid: Microsoft.Quantum.Logical.LexographicComparison
title: De functie LexographicComparison
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LexographicComparison
qsharp.summary: Given a comparison function, returns a new function that lexographically compares two arrays.
ms.openlocfilehash: 4d8596c52b0fc8082a2b766d95d4052a4964b8b9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197581"
---
# <a name="lexographiccomparison-function"></a>De functie LexographicComparison

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een vergelijkings functie retourneert een nieuwe functie die lexographically twee matrices vergelijkt.

```qsharp
function LexographicComparison<'T> (elementComparison : (('T, 'T) -> Bool)) : (('T[], 'T[]) -> Bool)
```


## <a name="input"></a>Invoer

### <a name="elementcomparison--tt---bool"></a>elementComparison: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie die twee elementen vergelijkt `x` en `y` retourneert als deze `x` kleiner is dan of gelijk is aan `y` .



## <a name="output--tt---bool"></a>Output: ('T [], 'T [])-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie die twee matrices vergelijkt `xs` en `ys` retourneert als deze `xs` voor of gelijk is aan `ys` in lexographical-volg orde.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de elementen van de matrices die worden vergeleken.

## <a name="remarks"></a>Opmerkingen

De lexographic vergelijking tussen twee matrices `xs` en `ys` wordt gedefinieerd door de volgende procedure. We zeggen dat twee elementen `x` en `y` gelijkwaardig zijn als `elementComparison(x, y)` en `elementComparison(y, x)` beide waar zijn.

- Beide matrices worden tot het eerste paar elementen vergeleken die niet gelijk zijn aan het element. De matrix met het element dat als eerste plaatsvindt volgens de naam die `elementComparison` als eerste moet worden uitgevoerd in de lexographical-volg orde.
- Als er geen equivalente elementen worden gevonden en één matrix langer is dan de andere, wordt de kortere matrix als eerste gegenereerd.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. gesorteerd](xref:Microsoft.Quantum.Arrays.Sorted)