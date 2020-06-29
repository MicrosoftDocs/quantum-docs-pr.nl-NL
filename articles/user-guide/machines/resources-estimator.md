---
title: Bronnen Estimator van de Quantum Development Kit
description: 'Meer informatie over de bronnen Estimator, die de resources schat die nodig zijn om een bepaald exemplaar van een Q #-bewerking uit te voeren op een quantum computer.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: cbb1c274b64738cc4b47869563d7d02eb717afbc
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415251"
---
# <a name="the-resources-estimator-target-machine"></a>De doel machine van de resources-estimator

Zoals de naam al aangeeft, worden de `ResourcesEstimator` resources die nodig zijn om een bepaald exemplaar van een Q #-bewerking uit te voeren op een quantum computer, geschat.
Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom kunnen er resources worden geschat voor Q #-bewerkingen die gebruikmaken van duizenden qubits als het klassieke deel van de code in een redelijke tijd kan worden uitgevoerd.

## <a name="usage"></a>Gebruik

Het `ResourcesEstimator` is slechts een ander type doel computer, zodat het kan worden gebruikt om elke Q #-bewerking uit te voeren. 

Als andere doel machines kunt u deze gebruiken voor een C#-hostprogramma een exemplaar maken en dit door geven als de eerste para meter van de methode van de bewerking `Run` :

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

Zoals het voor beeld laat zien, `ResourcesEstimator` biedt het een `ToTSV()` methode om een tabel met door tabs gescheiden waarden (TSV) te genereren die in een bestand kunnen worden opgeslagen of naar de console worden geschreven voor analyse. De uitvoer van het bovenstaande programma moet er ongeveer als volgt uitzien:

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
> De `ResourcesEstimator` berekeningen worden bij elke uitvoering niet opnieuw ingesteld, als hetzelfde exemplaar wordt gebruikt om een andere bewerking uit te voeren, wordt het samen voegen van het totaal op bestaande resultaten bewaard.
> Als u berekeningen tussen uitvoeringen wilt resetten, maakt u voor elke uitvoering een nieuw exemplaar.


## <a name="programmatically-retrieving-the-estimated-data"></a>De geschatte gegevens programmatisch ophalen

Naast een TSV-tabel kunnen de geschatte bronnen via een programma worden opgehaald via de `ResourcesEstimator` `Data` eigenschap. `Data`levert een `System.DataTable` exemplaar met twee kolommen: `Metric` en `Sum` , geïndexeerd door de namen van metrische gegevens.

De volgende code laat zien hoe u het totale aantal `QubitClifford` `T` en de `CNOT` poorten die worden gebruikt door een Q #-bewerking kunt ophalen en afdrukken:

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

Hier volgt een lijst met metrische gegevens die worden geschat door `ResourcesEstimator` :

* __CNOT__: het aantal CNOT (ook wel de bewaakte Pauli X Gate)-poorten worden uitgevoerd.
* __QubitClifford__: het aantal uitgevoerde Qubit-Clifford en Pauli-poorten.
* __Meting__: het aantal uitgevoerde metingen.
* __R__: het aantal Qubit draaiingen dat wordt uitgevoerd, met uitzonde ring van T, Clifford en Pauli-poorten.
* __T__: het aantal t-poorten en hun bijbehorende conjugaat, inclusief de t-poort, T_x = H. t. H en T_y = hy. t. hy, uitgevoerd.
* __Diepte__: de ondergrens voor de diepte van het Quantum circuit dat wordt uitgevoerd door de Q #-bewerking. Standaard worden alleen T-poorten in de diepte geteld. Zie de [diepte teller](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) voor meer informatie.
* __Width__: de ondergrens voor het maximum aantal qubits dat wordt toegewezen tijdens de uitvoering van de Q #-bewerking. Het is misschien niet mogelijk om tegelijkertijd zowel de __diepte__ als de __breedte__ van de ondergrenzen te verminderen.
* __BorrowedWidth__: het maximum aantal qubits dat is geleend binnen de Q #-bewerking.


## <a name="providing-the-probability-of-measurement-outcomes"></a>De waarschijnlijkheid van metingsresultaten opgeven

<xref:microsoft.quantum.intrinsic.assertprob>vanuit de <xref:microsoft.quantum.intrinsic> naam ruimte kan worden gebruikt om informatie over de verwachte waarschijnlijkheid van een meting te bieden om de uitvoering van het Q #-programma te verhelpen. Het volgende voorbeeld illustreert dit:

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

Als er `ResourcesEstimator` wordt gestuit `AssertProb` , wordt dat meet tijdstip vastgelegd `PauliZ` `source` en `q` moet er een resultaat worden gegeven van de `Zero` kans 0,5. Wanneer het later wordt uitgevoerd `M` , worden de vastgelegde waarden van de resultaten kansen gevonden en `M` geretourneerd, `Zero` of `One` met kans van 0,5.


## <a name="see-also"></a>Zie ook

De `ResourcesEstimator` is gebouwd op basis van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), met een uitgebreidere set metrische gegevens, de mogelijkheid om metrische gegevens te rapporteren over de volledige aanroep-Graph en functies als [afzonderlijke invoer controle](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) om te helpen bij het vinden van fouten in Q #-Program ma's. Raadpleeg de documentatie over de [traceer Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.

