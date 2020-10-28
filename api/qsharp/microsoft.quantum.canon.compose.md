---
uid: Microsoft.Quantum.Canon.Compose
title: Functie voor opstellen
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Compose
qsharp.summary: Returns the composition of two functions.
ms.openlocfilehash: 02cff7eef4d55d27d5d72e6219a90b7d8f5beb3b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704356"
---
# <a name="compose-function"></a>Functie voor opstellen

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


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