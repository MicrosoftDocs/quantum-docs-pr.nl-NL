---
uid: Microsoft.Quantum.Canon.Compose
title: Functie voor opstellen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: f8c6ad36220b48be1723c2d91cbf7c0a4947af14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96216758"
---
# <a name="compose-function"></a>Functie voor opstellen

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de samen stelling van twee functies.

```qsharp
function Compose<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U)) : ('T -> 'V)
```


## <a name="description"></a>Beschrijving

Als er twee functies $f $ en $g $ worden opgegeven, wordt een nieuwe functie geretourneerd die $f \circ g $ vertegenwoordigt.

## <a name="input"></a>Invoer

### <a name="outer--u---v"></a>Outer: ' U-> ' V

De tweede functie die moet worden toegepast.


### <a name="inner--t---u"></a>binnenste: 'T-> ' U

De eerste functie die moet worden toegepast.



## <a name="output--t---v"></a>Uitvoer: niet-> ' V

Een nieuwe functie $h $, zoals voor alle invoer waarden $x $, $f (g (x)) = h (x) $.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het invoer type van de eerste functie die moet worden toegepast.
### <a name="u"></a>' U

Het uitvoer type van de eerste functie die moet worden toegepast en het invoer type van de tweede functie die moet worden toegepast.
### <a name="v"></a>' V

Het uitvoer type van de tweede functie die moet worden toegepast.