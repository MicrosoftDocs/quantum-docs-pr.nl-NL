---
uid: Microsoft.Quantum.Arrays.LookupFunction
title: De functie LookupFunction
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: LookupFunction
qsharp.summary: Given an array, returns a function which returns elements of that array.
ms.openlocfilehash: 22b56bb7e9f03ebc5b2225efb2e6450d56022664
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845705"
---
# <a name="lookupfunction-function"></a>De functie LookupFunction

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een functie die elementen van die matrix retourneert, uitgedrukt in een matrix.

```qsharp
function LookupFunction<'T> (array : 'T[]) : (Int -> 'T)
```


## <a name="input"></a>Invoer

### <a name="array--t"></a>matrix: 'T []

De matrix die moet worden weer gegeven als een opzoek functie.



## <a name="output--int---t"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int) -> niet

Een functie `f` `f(idx) == f[idx]` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de elementen van de matrix die wordt weer gegeven als een opzoek functie.

## <a name="remarks"></a>Opmerkingen

Deze functie is vooral nuttig voor het samen werken met functies en bewerkingen die `Int -> 'T` functies als argumenten hebben. Dit is bijvoorbeeld gebruikelijk in de representatieve generator, waarbij functies worden gebruikt om te voor komen dat een volledige matrix in het geheugen hoeft te worden geregistreerd.