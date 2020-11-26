---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Bewerking GetQubitsAvailableToUse
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: ce461b03a08b4c83b9de142c957ce5c590fe9659
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201407"
---
# <a name="getqubitsavailabletouse-operation"></a>Bewerking GetQubitsAvailableToUse

Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert het aantal qubits dat momenteel beschikbaar is voor gebruik.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits dat in een instructie kan worden toegewezen `using` .
Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Environment. GetQubitsAvailableToBorrow](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)