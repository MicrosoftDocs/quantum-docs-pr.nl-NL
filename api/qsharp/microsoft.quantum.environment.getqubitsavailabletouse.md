---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToUse
title: Bewerking GetQubitsAvailableToUse
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToUse
qsharp.summary: Returns the number of qubits currently available to use.
ms.openlocfilehash: 2ed8c3789331a15b351769be960d06f6364d8047
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98827806"
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