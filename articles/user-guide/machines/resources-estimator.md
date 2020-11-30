---
title: Quantum bronnen Estimator-Quantum Development Kit
description: Meer informatie over de micro soft QDK resources Estimator, waarmee de resources die nodig zijn voor het uitvoeren van een bepaald exemplaar van een Q# bewerking op een quantum computer, worden geschat.
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 57f6602effd25fff353a8fee7f27acc529ce82af
ms.sourcegitcommit: c3c892ef35eae6926d0c4339d9d26bfd8be77e9a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/30/2020
ms.locfileid: "96318487"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>QDK-resources (Quantum Development Kit) estimator

Zoals de naam al aangeeft, `ResourcesEstimator` schat de klasse de resources die vereist zijn om een bepaald exemplaar van een Q# bewerking op een quantum computer uit te voeren. Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom schatten IT resources voor Q# bewerkingen die gebruikmaken van duizenden qubits, op voor waarde dat het klassieke deel van de code in een redelijke tijd wordt uitgevoerd.

De bronnen Estimator is gebaseerd op de [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), die een uitgebreidere verzameling metrische gegevens en hulpprogram ma's biedt om fouten in Program ma's op te sporen Q# .

## <a name="invoking-and-running-the-resources-estimator"></a>De bronnen Estimator aanroepen en uitvoeren

U kunt de resources Estimator gebruiken om een wille keurige bewerking uit te voeren Q# . Zie [manieren om een Q# programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.

### <a name="invoking-the-resources-estimator-from-c"></a>Aanroepen van de bronnen Estimator van C # 

Net als bij andere doelmachines maakt u eerst een exemplaar van de klasse `ResourceEstimator` en geeft u deze vervolgens door als de eerste parameter van de methode `Run` van een bewerking.

Houd er rekening mee dat, in tegenstelling tot de klasse `QuantumSimulator`, de klasse `ResourceEstimator` de interface <xref:System.IDisposable> niet implementeert, zodat u deze niet hoeft in te sluiten in een instructie `using`.

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

Zoals in het voor beeld wordt weer gegeven, `ResourcesEstimator` biedt de `ToTSV()` methode, waarmee een tabel wordt gegenereerd met door tabs gescheiden waarden (TSV). U kunt de tabel opslaan in een bestand of weer geven in de-console voor analyse. Hier volgt een voor beeld van de uitvoer van het voor gaande programma:

```output
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
> `ResourcesEstimator`Bij elke uitvoering worden de berekeningen niet opnieuw door een exemplaar opnieuw ingesteld. Als u hetzelfde exemplaar gebruikt om een andere bewerking uit te voeren, worden de nieuwe resultaten geaggregeerd met de bestaande resultaten. Als u berekeningen tussen uitvoeringen wilt resetten, maakt u voor elke uitvoering een nieuw exemplaar.

### <a name="invoking-the-resources-estimator-from-python"></a>De bronnen Estimator van python worden aangeroepen

Gebruik de methode [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) vanuit de python-bibliotheek met de geïmporteerde Q# bewerking:

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a>Aanroepen van de bronnen Estimator vanaf de opdracht regel

Wanneer u een Q# programma uitvoert vanaf de opdracht regel, gebruikt u de para meter **--Simulator** (of **-s** ) om de doel computer op te geven `ResourcesEstimator` . Met de volgende opdracht voert u een programma uit met behulp van de resources Estimator: 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a>De bronnen Estimator van Juptyer-notebooks aanroepen

Gebruik de I Q# Magic-opdracht [% schatting](xref:microsoft.quantum.iqsharp.magic-ref.simulate) om de bewerking uit te voeren Q# .

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a>De geschatte gegevens programmatisch ophalen

Naast een TSV-tabel kunt u de resources die zijn geschat tijdens de uitvoering programmatisch ophalen via de `Data` eigenschap van de resources Estimator. De `Data` eigenschap levert een `System.DataTable` exemplaar met twee kolommen: `Metric` en `Sum` , geïndexeerd op basis van de namen van de metrische gegevens.

De volgende code laat zien hoe u het totale aantal `QubitClifford` `T` en de `CNOT` bewerkingen die worden gebruikt door een bewerking Q# kunt ophalen en afdrukken:

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

De resources Estimator traceert de volgende metrische gegevens:

|Metrisch|Beschrijving|
|----|----|
|__CNOT__    |Het aantal uitgevoerde `CNOT` bewerkingen (ook wel beheerde Pauli X-bewerkingen genoemd).|
|__QubitClifford__ |Het aantal uitvoeringen van een afzonderlijke Qubit-Clifford-en Pauli-bewerking.|
|__Measure__    |Het aantal uitvoeringen van een wille keurige meting.  |
|__R__    |Het aantal uitvoeringen van een Qubit draaiing, met uitzonde ring van `T` Clifford-en Pauli-bewerkingen.  |
|__T__    |Het aantal uitvoeringen van `T` bewerkingen en hun conjugaat, waaronder de `T` bewerkingen, T_x = h. t. h en T_y = hy. t. hy.  |
|__Diepga__|Diepte van het Quantum circuit dat door de Q# bewerking wordt uitgevoerd (Zie [hieronder](#depth-width-and-qubitcount)). Standaard telt alleen Gates over de diepte waarde `T` . Zie [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)voor meer informatie.   |
|__Breedte__|De breedte van het Quantum circuit dat door de bewerking wordt uitgevoerd Q# (Zie [hieronder](#depth-width-and-qubitcount)). Standaard telt alleen Gates over de diepte waarde `T` . Zie [width Counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)(Engelstalig) voor meer informatie.   |
|__QubitCount__    |De ondergrens voor het maximum aantal toegewezen qubits tijdens het uitvoeren van de Q# bewerking. Deze metrische gegevens zijn mogelijk niet compatibel met de __diepte__ (zie hieronder).  |
|__BorrowedWidth__    |Het maximale aantal qubits dat in de bewerking is geleend Q# .  |


## <a name="depth-width-and-qubitcount"></a>Diepte, breedte en QubitCount

De gerapporteerde diepte-en breedte schattingen zijn compatibel met elkaar.
(Voorheen zijn beide nummers haalbaar, maar er zijn verschillende circuits vereist voor diepte en breedte.) Momenteel kunnen beide metrische gegevens in dit paar tegelijk worden bereikt door hetzelfde circuit.

De volgende metrische gegevens worden gerapporteerd:

__Diepte:__ Voor het uitvoeren van de bewerking-tijd die nodig is om het uit te voeren, wordt uitgegaan van specifieke Gate-tijden.
Voor bewerkingen die worden aangeroepen of een volgend verwerkings tijd verschil tussen de meest recente Qubit-beschikbaarheids tijd aan het begin en het einde van de bewerking.

__Breedte:__ Voor het hoofd bewerking-aantal qubits dat daad werkelijk wordt gebruikt om het uit te voeren (en de bewerking te starten).
Voor bewerkingen die of volgende bewerkingen worden uitgevoerd, is het aantal meer qubits gebruikt naast de qubits die al aan het begin van de bewerking worden gebruikt.

Houd er rekening mee dat de hergebruikte qubits geen bijdrage levert aan dit aantal.
Dat wil zeggen dat een aantal qubits is vrijgegeven voordat een start werd uitgevoerd en dat alle Qubit die door deze bewerking zijn gevraagd A (en de bewerkingen van A) zijn voldaan door eerdere release-qubits opnieuw te gebruiken, de breedte van bewerking A wordt gerapporteerd als 0. Qubits is een bijdrage leveren aan de breedte.

__QubitCount:__ Voor de hoofd bewerking-minimum aantal qubits dat voldoende is om deze bewerking uit te voeren (en de bewerkingen zijn aangeroepen).
Voor bewerkingen met de naam of de volgende bewerkingen-minimum aantal qubits dat voldoende is om deze bewerking afzonderlijk uit te voeren. Dit nummer bevat geen invoer qubits. Dit omvat gelede qubits.

Twee bewerkings modi worden ondersteund. De modus wordt geselecteerd door QCTraceSimulatorConfiguration. OptimizeDepth in te stellen.

__OptimizeDepth = True:__ QubitManager wordt ontmoedigd bij het opnieuw gebruiken van Qubit en wijst nieuwe Qubit toe elke keer dat deze wordt gevraagd voor een Qubit. De __diepte__ van de hoofd bewerking wordt de minimale diepte (ondergrens). Er wordt voor deze diepte een compatibele __breedte__ gerapporteerd (beide kunnen tegelijkertijd worden bereikt). Houd er rekening mee dat deze breedte waarschijnlijk niet optimaal is op basis van deze diepte. __QubitCount__ kan kleiner zijn dan de breedte voor de hoofd bewerking, omdat het opnieuw wordt aangenomen.

__OptimizeDepth = False:__ QubitManager wordt aangemoedigd om qubits opnieuw te gebruiken en om vrijgegeven qubits te hergebruiken voordat nieuwe objecten worden toegewezen. De __breedte__ van de hoofd bewerking wordt de minimale breedte (ondergrens). Er wordt een compatibele __diepte__ gerapporteerd waarop het kan worden bereikt. __QubitCount__ is hetzelfde als de __breedte__ voor de hoofd bewerking, uitgaande van geen leningen.

## <a name="providing-the-probability-of-measurement-outcomes"></a>De waarschijnlijkheid van metingsresultaten opgeven

U kunt <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> uit de <xref:Microsoft.Quantum.Diagnostics> naam ruimte gebruiken om informatie te geven over de verwachte waarschijnlijkheid van een meting bewerking. Zie [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.

## <a name="see-also"></a>Zie ook

- [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Kwantum Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator)
- [Kwantumsimulator voor volledige toestand](xref:microsoft.quantum.machines.full-state-simulator) 
