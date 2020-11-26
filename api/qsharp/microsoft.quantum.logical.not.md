---
uid: Microsoft.Quantum.Logical.Not
title: Niet-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: f2db43f4a2ce83d8cad1d60aa8c481a33b0c7d44
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197446"
---
# <a name="not-function"></a>Niet-functie

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de Boole-ontkenning van een waarde.

```qsharp
function Not (value : Bool) : Bool
```


## <a name="input"></a>Invoer

### <a name="value--bool"></a>waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De waarde die moet worden genegeerd.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` alleen als dat zo `value` is `false` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let x = not value;
let x = Not(value);
```