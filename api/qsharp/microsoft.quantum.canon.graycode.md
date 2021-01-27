---
uid: Microsoft.Quantum.Canon.GrayCode
title: De functie GrayCode
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: 0a9a19685f0511c44942df7d0bc8d257ad6b18c6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840502"
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

## <a name="example"></a>Voorbeeld

```qsharp
GrayCode(2); // [(0, 0),(1, 1),(3, 0),(2, 1)]
```