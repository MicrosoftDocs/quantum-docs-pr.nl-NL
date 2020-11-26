---
uid: Microsoft.Quantum.Math.BitSizeI
title: De functie BitSizeI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 561450ef43144aa4d7820e1f15d9300018104acd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195848"
---
# <a name="bitsizei-function"></a>De functie BitSizeI

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voor een niet-negatief geheel getal `a` retourneert het aantal bits dat is vereist om aan te duiden `a` .

Dat wil zeggen, retourneert de kleinste $n $, zodat $a < 2 ^ n $.

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Het gehele getal waarvan de bitlengte moet worden berekend.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De bits-grootte van `a` .