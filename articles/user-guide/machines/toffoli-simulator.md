---
title: Quantum Toffoli Simulator-Quantum Development Kit
description: Meer informatie over de micro soft QDK Toffoli Simulator, een speciale Quantum Simulator die kan worden gebruikt met miljoenen qubits.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6a0885035c12a99ae43533f04cdc95c5c529380a
ms.sourcegitcommit: 11bd357baeb6ab53a402882979e75964d0869b57
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/27/2020
ms.locfileid: "88992205"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a>Quantum Development Kit (QDK) Toffoli Simulator

De QDK Toffoli Simulator is een speciale Simulator met een beperkt bereik en ondersteunt alleen, en biedt ondersteuning voor `X` `CNOT` meerdere beheerde `X` Quantum bewerkingen. Alle klassieke logica en berekeningen zijn beschikbaar.

Hoewel de Toffoli-Simulator meer functionaliteit heeft dan de [volledige status Simulator](xref:microsoft.quantum.machines.full-state-simulator), heeft het voor deel dat u veel meer qubits kunt simuleren. De Toffoli Simulator kan worden gebruikt met miljoenen qubits, terwijl de volledige status Simulator is beperkt tot ongeveer 30 qubits. Dit is bijvoorbeeld handig voor Oracle die Booleaanse functies evalueren: ze kunnen worden geïmplementeerd met behulp van de beperkte set ondersteunde algoritmen en worden getest op een groot aantal qubits.

## <a name="invoking-the-toffoli-simulator"></a>De Toffoli Simulator aanroepen

U maakt de Toffoli Simulator via de- `ToffoliSimulator` klasse beschikbaar. Zie [manieren om een Q# programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.

### <a name="invoking-the-toffoli-simulator-from-c"></a>Het aanroepen van Toffoli Simulator vanaf C #

Net als bij andere doelmachines maakt u eerst een exemplaar van de klasse `ToffoliSimulator` en geeft u deze vervolgens door als de eerste parameter van de methode `Run` van een bewerking.

Houd er rekening mee dat, in tegenstelling tot de klasse `QuantumSimulator`, de klasse `ToffoliSimulator` de interface <xref:System.IDisposable> niet implementeert, zodat u deze niet hoeft in te sluiten in een instructie `using`.

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a>De Toffoli Simulator vanuit python aanroepen

Gebruik de methode [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) vanuit de python-bibliotheek met de geïmporteerde Q# bewerking:

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a>Het aanroepen van Toffoli Simulator vanaf de opdracht regel

Wanneer u een Q# programma uitvoert vanaf de opdracht regel, gebruikt u de para meter **--Simulator** (of **-s** ) om de doel computer van de Toffoli Simulator op te geven. Met de volgende opdracht voert u een programma uit met behulp van de resources Estimator: 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a>De Toffoli Simulator van Juptyer-notebooks aanroepen

Gebruik de Q# opdracht I Magic [% Toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) om de bewerking uit te voeren Q# .

```
%toffoli myOperation
```

## <a name="supported-operations"></a>Ondersteunde bewerkingen

De Toffoli Simulator ondersteunt:

* Rotaties en exponentiated Paulis, zoals `R` en `Exp` , wanneer de resulterende bewerking gelijk is aan `X` of de identiteits matrix.
* Metings-en [bevestigings](xref:microsoft.quantum.diagnostics.assertmeasurement) bewerkingen, maar alleen op basis van de Pauli `Z` . Houd er rekening mee dat de kans op een meting bewerking altijd **0** of **1**is; Er is geen wille keurige Toffoli Simulator.
* `DumpMachine` en- `DumpRegister` functies.
Beide functies voeren de huidige `Z` status van elke qubit, één Qubit per regel.

## <a name="specifying-the-number-of-qubits"></a>Het aantal qubits opgeven

Een `ToffoliSimulator` instantie wijst standaard ruimte toe voor 65.536 qubits.
Als voor uw algoritme meer qubits vereist zijn, kunt u het aantal Qubit opgeven door een waarde voor de `qubitCount` para meter op te geven voor de constructor.
Voor elke extra Qubit is slechts één byte geheugen vereist, dus er zijn geen aanzienlijke kosten voor het overberekenen van het aantal qubits dat u nodig hebt.

Bijvoorbeeld:

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a>Zie ook

- [Quantum bronnen estimator](xref:microsoft.quantum.machines.resources-estimator)
- [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Quantum Full State Simulator](xref:microsoft.quantum.machines.full-state-simulator) 