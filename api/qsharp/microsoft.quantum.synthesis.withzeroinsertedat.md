---
uid: Microsoft.Quantum.Synthesis.WithZeroInsertedAt
title: De functie WithZeroInsertedAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: WithZeroInsertedAt
qsharp.summary: Insert a 0-bit into an integer
ms.openlocfilehash: 7d5f8838b6ae555524fb0e82e14f93e6c77e43d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855201"
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