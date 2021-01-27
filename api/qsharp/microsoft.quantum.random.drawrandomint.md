---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Bewerking DrawRandomInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851143"
---
# <a name="drawrandomint-operation"></a>Bewerking DrawRandomInt

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Hiermee wordt een wille keurig geheel getal in een opgegeven, inclusief bereik getekend.

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a>Invoer

### <a name="min--int"></a>min: [int](xref:microsoft.quantum.lang-ref.int)

Het kleinste gehele getal dat moet worden getekend.


### <a name="max--int"></a>Max.: [int](xref:microsoft.quantum.lang-ref.int)

Het grootste gehele getal dat moet worden getekend.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Een geheel getal in het inclusieve bereik van `min` tot `max` en met een uniforme kans.

## <a name="example"></a>Voorbeeld

Het volgende Q #-fragment rolt een wille keurige dobbel steen op met zes zijden:

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a>Opmerkingen

Mislukt als `max <= min` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. DiscreteUniformDistribution](xref:Microsoft.Quantum.DiscreteUniformDistribution)