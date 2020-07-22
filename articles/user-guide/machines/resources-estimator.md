---
title: Quantum bronnen Estimator-Quantum Development Kit
description: 'Meer informatie over de micro soft QDK resources Estimator, waarmee de resources die vereist zijn voor het uitvoeren van een bepaald exemplaar van een Q #-bewerking op een quantum computer, worden geschat.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 0909a050e89d6295664e54ab63cfda5d407a8f12
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870533"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a>QDK-resources (Quantum Development Kit) estimator

Zoals de naam al aangeeft, `ResourcesEstimator` schat de klasse de resources die vereist zijn om een bepaald exemplaar van een Q #-bewerking uit te voeren op een quantum computer. Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom schatten IT resources voor Q #-bewerkingen die gebruikmaken van duizenden qubits, op voor waarde dat het klassieke deel van de code in een redelijke tijd wordt uitgevoerd.

De Estimator van de resources is gebaseerd op de [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), die een uitgebreidere set metrische gegevens en hulpprogram ma's biedt om fouten in Q #-Program ma's op te sporen.

## <a name="invoking-and-running-the-resources-estimator"></a>De bronnen Estimator aanroepen en uitvoeren

U kunt de Estimator van resources gebruiken om een Q #-bewerking uit te voeren. Zie [manieren om een Q #-programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.

### <a name="invoking-the-resources-estimator-from-c"></a>Aanroepen van de bronnen Estimator van C # 

Net als bij andere doel machines maakt u eerst een instantie van de `ResourceEstimator` klasse en geeft u deze vervolgens door als de eerste para meter van de methode van een bewerking `Run` .

Houd er rekening mee dat, in tegens telling tot de `QuantumSimulator` -klasse, de- `ResourceEstimator` interface niet wordt geïmplementeerd door de klasse <xref:System.IDisposable> en dat u deze niet hoeft op te nemen in een- `using` instructie.

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

Gebruik de methode [estimate_resources ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) vanuit de python-bibliotheek met de geïmporteerde Q #-bewerking:

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a>Aanroepen van de bronnen Estimator vanaf de opdracht regel

Wanneer u een Q #-programma uitvoert vanaf de opdracht regel, gebruikt u de para meter **--Simulator** (of **-s** ) om de doel computer op te geven `ResourcesEstimator` . Met de volgende opdracht voert u een programma uit met behulp van de resources Estimator: 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a>De bronnen Estimator van Juptyer-notebooks aanroepen

Gebruik de opdracht IQ # Magic [% schatting](xref:microsoft.quantum.iqsharp.magic-ref.simulate) om de Q #-bewerking uit te voeren.

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a>De geschatte gegevens programmatisch ophalen

Naast een TSV-tabel kunt u de resources die zijn geschat tijdens de uitvoering programmatisch ophalen via de `Data` eigenschap van de resources Estimator. De `Data` eigenschap levert een `System.DataTable` exemplaar met twee kolommen: `Metric` en `Sum` , geïndexeerd op basis van de namen van de metrische gegevens.

De volgende code laat zien hoe u het totale aantal `QubitClifford` `T` en de `CNOT` bewerkingen die worden gebruikt door een Q #-bewerking kunt ophalen en afdrukken:

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

|Gegevens|Beschrijving|
|----|----|
|__CNOT__    |Het aantal uitgevoerde `CNOT` bewerkingen (ook wel beheerde Pauli X-bewerkingen genoemd).|
|__QubitClifford__ |Het aantal uitvoeringen van een afzonderlijke Qubit-Clifford-en Pauli-bewerking.|
|__Meting__    |Het aantal uitvoeringen van een wille keurige meting.  |
|__R__    |Het aantal uitvoeringen van een Qubit draaiing, met uitzonde ring van `T` Clifford-en Pauli-bewerkingen.  |
|__T__    |Het aantal uitvoeringen van `T` bewerkingen en hun conjugaat, waaronder de `T` bewerkingen, T_x = h. t. h en T_y = hy. t. hy.  |
|__Diepga__|De ondergrens voor de diepte van het Quantum circuit dat wordt uitgevoerd door de Q #-bewerking. Standaard telt alleen Gates over de diepte waarde `T` . Zie [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)voor meer informatie.   |
|__Breedte__    |De ondergrens voor het maximum aantal qubits dat wordt toegewezen tijdens de uitvoering van de Q #-bewerking. Het is misschien niet mogelijk om tegelijkertijd zowel de __diepte__ als de __breedte__ van de ondergrenzen te verminderen.  |
|__BorrowedWidth__    |Het maximum aantal qubits dat is geleend binnen de Q #-bewerking.  |

## <a name="providing-the-probability-of-measurement-outcomes"></a>De waarschijnlijkheid van metings resultaten opgeven

U kunt <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> uit de <xref:microsoft.quantum.diagnostics> naam ruimte gebruiken om informatie te geven over de verwachte waarschijnlijkheid van een meting bewerking. Zie [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.

## <a name="see-also"></a>Zie ook

- [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [Quantum Toffoli Simulator](xref:microsoft.quantum.machines.toffoli-simulator)
- [Quantum Full State Simulator](xref:microsoft.quantum.machines.full-state-simulator) 