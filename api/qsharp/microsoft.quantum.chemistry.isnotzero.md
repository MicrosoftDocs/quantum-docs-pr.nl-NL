---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: De functie IsNotZero
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: f80dbba6a51e62970e87c2782faba558340d2bd8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204059"
---
# <a name="isnotzero-function"></a>De functie IsNotZero

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Hiermee wordt gecontroleerd of een `Double` getal niet ongeveer nul is.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Invoer

### <a name="number--double"></a>nummer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Nummer dat moet worden gecontroleerd



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

Retourneert waar als `number` een absolute waarde groter is dan `1e-15` .