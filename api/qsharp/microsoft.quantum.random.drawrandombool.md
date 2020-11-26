---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Bewerking DrawRandomBool
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: dbe0836af5aa19f1bdce3cfe93be6833358c22be
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192958"
---
# <a name="drawrandombool-operation"></a>Bewerking DrawRandomBool

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Als gevolg van een kans op succes, retourneert een enkele Bernoulli-proef versie die waar is met de opgegeven kans.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>Invoer

### <a name="successprobability--double"></a>successProbability: [dubbel](xref:microsoft.quantum.lang-ref.double)

De kans dat `true` moet worden geretourneerd.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` met waarschijnlijkheid `successProbability` en `false` met waarschijnlijkheid `1.0 - successProbability` .