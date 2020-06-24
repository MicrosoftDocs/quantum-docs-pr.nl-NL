---
title: Quantum Development Kit Toffoli Simulator
description: Meer informatie over de micro soft QDK Toffoli Simulator, een speciale Quantum Simulator die kan worden gebruikt met miljoenen qubits.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 8a29caaa0fa058600a74e7d130e644374cbfa19c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275146"
---
# <a name="quantum-development-kit-toffoli-simulator"></a>Quantum Development Kit Toffoli Simulator

De Quantum Development Kit biedt een Toffoli Simulator, een speciale Simulator waarmee Quantum algoritmen kunnen worden gesimuleerd die beperkt zijn tot X-, CNOT-en multi-Controlled X Quantum-bewerkingen (alle klassieke logica en berekeningen zijn beschikbaar).

Hoewel de Toffoli-Simulator veel meer beperkt is in de bewerking dan de [volledige status Simulator](xref:microsoft.quantum.machines.full-state-simulator), kan deze nog veel meer qubits simuleren.
De Toffoli Simulator kan worden gebruikt met miljoenen qubits, terwijl de volledige status Simulator doorgaans beperkt is tot ongeveer 30.
Het kan een beperkt aantal Quantum algoritmen die zijn geschreven in Q # op uw computer uitvoeren en fouten opsporen. Zo kunnen Oracle die Booleaanse functies evalueren, worden geïmplementeerd met behulp van deze Gates en dus worden getest op het variëren van grote aantallen qubits met behulp van deze simulator.

Deze Quantum Simulator wordt weer gegeven via de- `ToffoliSimulator` klasse.
Als u de Simulator wilt gebruiken, maakt u gewoon een exemplaar van deze klasse en geeft u het door aan de `Run` methode van de Quantum bewerking die u wilt uitvoeren, samen met de rest van de para meters:

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a>Andere bewerkingen

De `ToffoliSimulator` ondersteunt rotaties en Exponentiated Paulis, zoals `R` en `Exp` , wanneer de resulterende bewerking gelijk is aan `X` of aan de identiteit.

Meting en bevestiging worden alleen in de Pauli-basis ondersteund `Z` .
Houd er rekening mee dat de kans op een bepaalde meting altijd 0 of 1 is. Er is geen wille keurige Toffoli Simulator.

`DumpMachine`en `DumpRegister` worden ondersteund.
Ze hebben zowel de huidige `Z` basis status van elke qubit als één Qubit per regel.

## <a name="qubitcount"></a>QubitCount

Standaard wordt met de `ToffoliSimulator` ruimte toegewezen aan 65.536 qubits.
Als er meer dan dit algoritme vereist is, kunt u het aantal Qubit wijzigen door een waarde voor de `qubitCount` para meter op te geven voor de constructor.
Elke extra Qubit vereist een extra byte geheugen, zodat er geen aanzienlijke kosten in rekening worden geschat voor het aantal qubits dat u nodig hebt.

Bijvoorbeeld:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
