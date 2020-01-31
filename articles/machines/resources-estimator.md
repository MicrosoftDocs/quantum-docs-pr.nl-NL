---
title: Bronnen over de Quantum Development Kit estimator | Microsoft Docs
description: Overzicht van de resources van de Quantum Development Kit van micro soft estimator
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 960fda3dade7648f9cd24496c3a49fd11d6f807a
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820858"
---
# <a name="the-resourcesestimator-target-machine"></a>De doel computer van de ResourcesEstimator

Zoals de naam al aangeeft, schat het `ResourcesEstimator` de resources die nodig zijn om een bepaald exemplaar van een Q #-bewerking uit te voeren op een quantum computer.
Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom kunnen er resources worden geschat voor Q #-bewerkingen die gebruikmaken van duizenden qubits.

## <a name="usage"></a>Gebruik

De `ResourcesEstimator` is maar een ander type doel computer, zodat deze kan worden gebruikt om elke Q #-bewerking uit te voeren. 

Als andere doel machines kunt u deze gebruiken voor een C# hostprogramma een exemplaar maken en dit door geven als de eerste para meter van de `Run` methode van de bewerking:

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

Zoals in het voor beeld wordt weer gegeven, biedt de `ResourcesEstimator` een `ToTSV()` methode voor het genereren van een tabel met tab-gescheiden waarden (TSV) die in een bestand kunnen worden opgeslagen of naar de console worden geschreven voor analyse. De uitvoer van het bovenstaande programma moet er ongeveer als volgt uitzien:

```Output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> Met de `ResourcesEstimator` worden de berekeningen bij elke uitvoering niet opnieuw ingesteld, als hetzelfde exemplaar wordt gebruikt om een andere bewerking uit te voeren, wordt het samen voegen van het aantal bestaande resultaten bewaard.
> Als u berekeningen tussen uitvoeringen wilt resetten, maakt u voor elke uitvoering een nieuw exemplaar.


## <a name="programmatically-retrieving-the-estimated-data"></a>De geschatte gegevens programmatisch ophalen

Naast een TSV-tabel kunnen de geschatte resources via een programma worden opgehaald via de eigenschap `Data` van de `ResourcesEstimator`. `Data` levert een `System.DataTable`-exemplaar met twee kolommen: `Metric` en `Sum`, geïndexeerd op basis van de namen van metrische gegevens.

De volgende code laat zien hoe u het totale aantal `QubitClifford`, `T` en `CNOT` poorten die worden gebruikt door een Q #-bewerking kunt ophalen en afdrukken:

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a>Gemelde metrische gegevens

Hier volgt een lijst met metrische gegevens die worden geschat door de `ResourcesEstimator`:

* __CNOT__: het aantal CNOT (ook wel de bewaakte Pauli X Gate)-poorten worden uitgevoerd.
* __QubitClifford__: het aantal uitgevoerde Qubit-Clifford en Pauli-poorten.
* __Meting__: het aantal uitgevoerde metingen.
* __R__: het aantal Qubit draaiingen dat wordt uitgevoerd, met uitzonde ring van T, Clifford en Pauli-poorten.
* __T__: het aantal t-poorten en hun bijbehorende conjugaat, inclusief de t-poort, T_x = H. t. H en T_y = hy. t. hy, uitgevoerd.
* __Diepte__: de diepte van het Quantum circuit dat wordt uitgevoerd door de Q #-bewerking. Standaard worden alleen T-poorten in de diepte geteld. Zie de [diepte teller](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) voor meer informatie.
* __Breedte__: het maximum aantal toegewezen qubits tijdens de uitvoering van de Q #-bewerking.
* __BorrowedWidth__: het maximum aantal qubits dat is geleend binnen de Q #-bewerking.


## <a name="providing-the-probability-of-measurement-outcomes"></a>De waarschijnlijkheid van metingsresultaten opgeven

<xref:microsoft.quantum.intrinsic.assertprob> van de <xref:microsoft.quantum.intrinsic> naam ruimte kan worden gebruikt om informatie over de verwachte waarschijnlijkheid van een meting te bieden om de uitvoering van het Q #-programma te verhelpen. Het volgende voorbeeld illustreert dit:

```qsharp
operation Teleport(source : Qubit, target : Qubit) : Unit {

    using (qubit = Qubit()) {

        H(q);
        CNOT(qubit, target);

        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [qubit], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(qubit) == One) { X(target); X(qubit); }
    }
}
```

Wanneer de `ResourcesEstimator` zich voordoet `AssertProb` wordt de meting `PauliZ` op `source` vastgelegd en moet `q` een resultaat van `Zero` met de kans 0,5 worden gegeven. Wanneer het `M` later wordt uitgevoerd, worden de vastgelegde waarden van de waarschijnlijkheid van de uitkomst gevonden en `M` wordt `Zero` of `One` geretourneerd met kans 0,5.


## <a name="see-also"></a>Zie ook

De `ResourcesEstimator` is gebouwd op basis van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Dit biedt een uitgebreidere set metrische gegevens, de mogelijkheid om metrische gegevens te rapporteren over de volledige aanroep-Graph en functies als [afzonderlijke invoer controle](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) om te helpen bij het vinden van fouten in Q #-Program ma's. Raadpleeg de documentatie over de [traceer Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.

