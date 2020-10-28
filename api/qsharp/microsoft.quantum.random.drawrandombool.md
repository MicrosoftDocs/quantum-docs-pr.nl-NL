---
uid: Microsoft.Quantum.Random.DrawRandomBool
title: Bewerking DrawRandomBool
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomBool
qsharp.summary: Given a success probability, returns a single Bernoulli trial that is true with the given probability.
ms.openlocfilehash: 05cf8ad939691aac90625c5d056ea79aa062f553
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706716"
---
# <a name="drawrandombool-operation"></a>Bewerking DrawRandomBool

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket [](https://nuget.org/packages/)


Als gevolg van een kans op succes, retourneert een enkele Bernoulli-proef versie die waar is met de opgegeven kans.

```qsharp
operation DrawRandomBool (successProbability : Double) : Bool
```


## <a name="input"></a>Invoer

### <a name="successprobability--double"></a>successProbability: [dubbel](xref:microsoft.quantum.lang-ref.double)

De kans dat `true` moet worden geretourneerd.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` met waarschijnlijkheid `successProbability` en `false` met waarschijnlijkheid `1.0 - successProbability` .