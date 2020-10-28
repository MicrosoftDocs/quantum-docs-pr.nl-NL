---
uid: Microsoft.Quantum.Environment.GetQubitsAvailableToBorrow
title: Bewerking GetQubitsAvailableToBorrow
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Environment
qsharp.name: GetQubitsAvailableToBorrow
qsharp.summary: Returns the number of qubits currently available to borrow. This includes unused qubits; that is, this includes the qubits returned by `GetQubitsAvailableToUse`.
ms.openlocfilehash: cb56ce4aefd7a03c0f0827b8d34688ef17988f56
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702590"
---
# <a name="getqubitsavailabletoborrow-operation"></a>Bewerking GetQubitsAvailableToBorrow

Naam ruimte: [micro soft. Quantum. Environment](xref:Microsoft.Quantum.Environment)

Pakket [](https://nuget.org/packages/)


Retourneert het aantal qubits dat momenteel beschikbaar is om te lenen.
Dit omvat niet-gebruikte qubits; dat wil zeggen dat de qubits die wordt geretourneerd door `GetQubitsAvailableToUse` .

```qsharp
operation GetQubitsAvailableToBorrow () : Int
```


## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits dat in een instructie kan worden toegewezen `borrowing` .
Als de gebruikte doel computer deze informatie niet verstrekt, `-1` wordt deze geretourneerd.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Environment. GetQubitsAvailableToUse](xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse)