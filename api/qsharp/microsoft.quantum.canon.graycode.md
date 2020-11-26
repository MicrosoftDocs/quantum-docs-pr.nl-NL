---
uid: Microsoft.Quantum.Canon.GrayCode
title: De functie GrayCode
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206881"
---
# <a name="graycode-function"></a>De functie GrayCode

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maakt grijze code reeksen

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>Invoer

### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Aantal bits



## <a name="output--intint"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

De matrix van Tuples. De eerste waarde in tuple is een waarde in de tweede waarde van de GrayCode-reeks in tuple is position om de huidige waarde te wijzigen in volgende.