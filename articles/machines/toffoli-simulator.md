---
title: Quantum Development Kit Toffoli Simulator | Microsoft Docs
description: Overzicht van de micro soft Quantum Development Kit Toffoli Simulator
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 26940d1a8fe31f1035e2d23a68940cd999517c6b
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442348"
---
# <a name="quantum-development-kit-toffoli-simulator"></a>Quantum Development Kit Toffoli Simulator

De Quantum Development Kit biedt een Toffoli Simulator, een speciale Simulator waarmee Quantum algoritmen kunnen worden gesimuleerd die beperkt zijn tot X-, CNOT-en multi-Controlled X Quantum-bewerkingen (alle klassieke logica en berekeningen zijn beschikbaar).

Hoewel de Toffoli-Simulator veel meer beperkt is in de bewerking dan de [volledige status Simulator](xref:microsoft.quantum.machines.full-state-simulator), kan deze nog veel meer qubits simuleren.
De Toffoli Simulator kan worden gebruikt met miljoenen qubits, terwijl de volledige status Simulator doorgaans beperkt is tot ongeveer 30.
Het kan een beperkt aantal Quantum algoritmen die zijn geschreven in Q # op uw computer uitvoeren en fouten opsporen. Zo kunnen Oracle die Booleaanse functies evalueren, worden geïmplementeerd met behulp van deze Gates en dus worden getest op het variëren van grote aantallen qubits met behulp van deze simulator.

Deze Quantum Simulator wordt weer gegeven via de `ToffoliSimulator` klasse.
Als u de Simulator wilt gebruiken, maakt u gewoon een exemplaar van deze klasse en geeft u het door aan de `Run` methode van de Quantum bewerking die u wilt uitvoeren, samen met de rest van de para meters:

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a>Andere bewerkingen

Het `ToffoliSimulator` ondersteunt rotaties en exponentiated Paulis, zoals `R` en `Exp`, wanneer de resulterende bewerking gelijk is aan `X` of aan de identiteit.

Meting en bevestiging worden alleen ondersteund in de Pauli `Z` basis.
Houd er rekening mee dat de kans op een bepaalde meting altijd 0 of 1 is. Er is geen wille keurige Toffoli Simulator.

`DumpMachine` en `DumpRegister` worden ondersteund.
Ze voeren beide de huidige `Z`-basis status van elke qubit uit, één Qubit per regel.

## <a name="qubitcount"></a>QubitCount

De `ToffoliSimulator` wijst standaard ruimte toe voor 65.536 qubits.
Als er meer dan dit algoritme vereist is, kunt u het aantal Qubit wijzigen door een waarde voor de para meter `qubitCount` op te geven voor de constructor.
Elke extra Qubit vereist een extra byte geheugen, zodat er geen aanzienlijke kosten in rekening worden geschat voor het aantal qubits dat u nodig hebt.

Bijvoorbeeld:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```