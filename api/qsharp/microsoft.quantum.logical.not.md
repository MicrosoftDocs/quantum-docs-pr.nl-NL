---
uid: Microsoft.Quantum.Logical.Not
title: Niet-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: 3a688aac0178a2f4127496c1009fe7d5ee7ae198
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701421"
---
# <a name="not-function"></a>Niet-functie

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


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