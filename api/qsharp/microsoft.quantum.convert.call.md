---
uid: Microsoft.Quantum.Convert.Call
title: Aanroep bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: Call
qsharp.summary: Calls a function with a given input.
ms.openlocfilehash: 8630f846b4b9823ce1c1dfd61dc8ca81e468517d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702993"
---
# <a name="call-operation"></a>Aanroep bewerking

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket [](https://nuget.org/packages/)


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