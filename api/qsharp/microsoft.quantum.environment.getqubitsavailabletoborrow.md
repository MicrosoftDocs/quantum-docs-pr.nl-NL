---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Bewerking GetQubitsAvailableToBorrow
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow.
ms.openlocfilehash: 30b97c2b6e1353f008d085c3bae6160763557c67
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201458"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Bewerking GetQubitsAvailableToBorrow

Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert het aantal qubits dat momenteel beschikbaar is om te lenen.

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits dat kan worden uitgeleend en niet als onderdeel van een instructie wordt toegewezen `borrowing` .
Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Environment. GetQubitsAvailableToUse](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)