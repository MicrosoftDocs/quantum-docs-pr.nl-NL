---
uid: Microsoft.Quantum.Convert.Call
title: Aanroep bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 93458d08aa83ffa8b7b33de8bf51c970af291db9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850199"
---
# <a name="call-operation"></a>Aanroep bewerking

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Roept een functie aan met een opgegeven invoer.

```qsharp
operation Call<'Input, 'Output> (fn : ('Input -> 'Output), input : 'Input) : 'Output
```


## <a name="description"></a>Beschrijving

Op basis van een functie en een invoer voor die functie roept u de functie op en wordt de uitvoer geretourneerd.

## <a name="input"></a>Invoer

### <a name="fn--input---output"></a>FN: de uitvoer van invoer >

Een functie die moet worden aangeroepen.


### <a name="input--input"></a>invoer: ' invoer

De invoer die moet worden door gegeven aan de functie.



## <a name="output--output"></a>Uitvoer: uitvoer

Het resultaat van het aanroepen van `fn` .

## <a name="type-parameters"></a>Type parameters

### <a name="input"></a>' Invoer


### <a name="output"></a>' Uitvoer



## <a name="remarks"></a>Opmerkingen

Deze bewerking is vooral nuttig voor het afdwingen van een functie die wordt aangeroepen op een specifieke locatie binnen een bewerking of voor het aanroepen van een functie waarbij een bewerking wordt verwacht.