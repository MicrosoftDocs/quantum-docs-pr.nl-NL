---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: De functie ComposedOutput
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 4da66616692055a7d60abbf1fac6e6799806675d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704349"
---
# <a name="composedoutput-function"></a>De functie ComposedOutput

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Retourneert de uitvoer van de samen stelling van `inner` en `outer` voor een gegeven invoer.

```qsharp
function ComposedOutput<'T, 'U, 'V> (outer : ('U -> 'V), inner : ('T -> 'U), target : 'T) : 'V
```


## <a name="input"></a>Invoer

### <a name="outer--u---v"></a>Outer: ' U-> ' V




### <a name="inner--t---u"></a>binnenste: 'T-> ' U




### <a name="target--t"></a>doel: 'T





## <a name="output--v"></a>Uitvoer: ' V



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T


### <a name="u"></a>' U


### <a name="v"></a>' V

