---
uid: Microsoft.Quantum.Chemistry.IsNotZero
title: De functie IsNotZero
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry
qsharp.name: IsNotZero
qsharp.summary: Checks whether a `Double` number is not approximately zero.
ms.openlocfilehash: 3c0f9c6695e8c9ec4a0953d5217c28c512ac7de1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703550"
---
# <a name="isnotzero-function"></a>De functie IsNotZero

Naam ruimte: [micro soft. Quantum. chemie](xref:Microsoft.Quantum.Chemistry)

Pakket [](https://nuget.org/packages/)


Hiermee wordt gecontroleerd of een `Double` getal niet ongeveer nul is.

```qsharp
function IsNotZero (number : Double) : Bool
```


## <a name="input"></a>Invoer

### <a name="number--double"></a>nummer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Nummer dat moet worden gecontroleerd



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

Retourneert waar als `number` een absolute waarde groter is dan `1e-15` .