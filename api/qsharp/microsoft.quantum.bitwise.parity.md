---
uid: Microsoft.Quantum.Bitwise.Parity
title: De functie parity
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: Parity
qsharp.summary: Returns the bitwise PARITY of an integer (1 if its binary representation contains odd number of ones and 0 otherwise).
ms.openlocfilehash: b34ef36b0336ec1dea7fdbd878c6d695b38d623e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842128"
---
# <a name="parity-function"></a>De functie parity

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert de bitsgewijze PARITEIT van een geheel getal (1 als de binaire representatie een oneven aantal records bevat en 0 anders).

```qsharp
function Parity (a : Int) : Int
```


## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)



## <a name="example"></a>Voorbeeld

```qsharp
let a = 248;
let x = Parity(a); // x : Int = 1.
```