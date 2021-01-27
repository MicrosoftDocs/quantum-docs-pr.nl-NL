---
uid: Microsoft.Quantum.Logical.Not
title: Niet-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Not
qsharp.summary: Returns the Boolean negation of a value.
ms.openlocfilehash: bf09cac8d126371df6218b7e92d68a881b732dc8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849073"
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

```qsharp
let x = not value;
let x = Not(value);
```