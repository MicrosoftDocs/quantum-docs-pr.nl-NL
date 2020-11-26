---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: De functie ComposedOutput
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: 7e361a62679ab93e9a0ebc04fa52be193805c78d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207459"
---
# <a name="composedoutput-function"></a>De functie ComposedOutput

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

