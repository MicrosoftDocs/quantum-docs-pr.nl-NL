---
uid: Microsoft.Quantum.Canon.ComposedOutput
title: De functie ComposedOutput
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ComposedOutput
qsharp.summary: Returns the output of the composition of `inner` and `outer` for a given input.
ms.openlocfilehash: d39fcd6b2987b3a4f69df13fa83b69a199d6eddb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840894"
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

