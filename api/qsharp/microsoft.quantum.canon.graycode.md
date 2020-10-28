---
uid: Microsoft.Quantum.Canon.GrayCode
title: De functie GrayCode
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704165"
---
# <a name="graycode-function"></a>De functie GrayCode

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Maakt grijze code reeksen

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>Invoer

### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Aantal bits



## <a name="output--intint"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

De matrix van Tuples. De eerste waarde in tuple is een waarde in de tweede waarde van de GrayCode-reeks in tuple is position om de huidige waarde te wijzigen in volgende.