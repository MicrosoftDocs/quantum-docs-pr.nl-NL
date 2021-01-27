---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: De functie IsNotZero
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 9384e5dafd4b5b7d44cb348c9537ebc2c621466d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839604"
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