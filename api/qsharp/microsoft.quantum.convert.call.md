---
uid: Microsoft.Quantum.Convert.Call
title: Aanroep bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 92c159cef878fb587b0ed514fd6660dd19527cab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214208"
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