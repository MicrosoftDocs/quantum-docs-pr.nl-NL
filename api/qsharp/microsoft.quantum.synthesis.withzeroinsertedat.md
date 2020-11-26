---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: De functie WithZeroInsertedAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 414b703151b9152aa69709d9c28e68e5ae63506f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228862"
---
# <a name="withzeroinsertedat-function"></a>De functie WithZeroInsertedAt

Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een 0-bit invoegen in een geheel getal

```qsharp
function WithZeroInsertedAt (position : Int, value : Int) : Int
```


## <a name="description"></a>Beschrijving

Voor deze bewerking wordt een geheel getal gebruikt, wordt een 0-bit ingevoegd `position` en wordt de bijgewerkte waarde als een geheel getal geretourneerd.  Als u bijvoorbeeld een 0 op positie 2 in het getal 10 invoegt ($ 10 _ {10} = 1010_ {2} $), wordt het getal 18 als resultaat gegeven ($18 _ {10} = 10010_ {2} $).

## <a name="input"></a>Invoer

### <a name="position--int"></a>positie: [int](xref:microsoft.quantum.lang-ref.int)

De positie waarop 0 is ingevoegd


### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)

De waarde die is gewijzigd



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Gewijzigde waarde