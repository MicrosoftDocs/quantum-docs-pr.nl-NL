---
uid: Microsoft.Quantum.Math.BitSizeL
title: De functie BitSizeL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeL
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: 8b3d4cceb69619ed32977337fc0fe7401db38cbd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211046"
---
# <a name="bitsizel-function"></a>De functie BitSizeL

Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Voor een niet-negatief geheel getal `a` retourneert het aantal bits dat is vereist om aan te duiden `a` .

Dat wil zeggen, retourneert de kleinste $n $, zodat $a < 2 ^ n $.

```qsharp
function BitSizeL (a : BigInt) : Int
```


## <a name="input"></a>Invoer

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Het gehele getal waarvan de bitlengte moet worden berekend.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De bits-grootte van `a` .