---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Bewerking GetQubitsAvailableToUse
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 25d43d369193fc7453fd5ce9c50769c438a69afb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702585"
---
# <a name="getqubitsavailabletouse-operation"></a>Bewerking GetQubitsAvailableToUse

Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Pakket [](https://nuget.org/packages/)


Retourneert het aantal qubits dat momenteel beschikbaar is voor gebruik.

```qsharp
operation GetQubitsAvailableToUse () : Int
```


## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits dat in een instructie kan worden toegewezen `using` .
Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Environment. GetQubitsAvailableToBorrow](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow)