---
title: 'Kwantumtraceersimulator: Quantum Development Kit'
description: Meer informatie over hoe u de Microsoft-quantumcomputertracesimulator kunt gebruiken om fouten in klassieke code op te sporen en om resourcevereisten van een Q#-programma in te schatten.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: c01f01973ea08153cbfa35d87a588a4eae46f1b7
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871107"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a>Microsoft Quantum Development Kit (QDK)-kwantumtraceersimulator

De QDK-klasse <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> voert een kwantumprogramma uit zonder de status van een kwantumcomputer werkelijk te simuleren. Daarom kunnen met de kwantumtraceersimulator kwantumprogramma's van duizenden qubits worden uitgevoerd.  De simulator is handig voor twee hoofddoelen: 

* Het opsporen van fouten in klassieke code die deel uitmaakt van een kwantumprogramma. 
* Het schatten van de benodigde resources voor het uitvoeren van een bepaald exemplaar van een kwantumprogramma op een kwantumcomputer. De [Resources-estimator](xref:microsoft.quantum.machines.resources-estimator), waarmee een beperkt aantal metrische gegevens wordt geboden, is gebaseerd op de traceersimulator.

## <a name="invoking-the-quantum-trace-simulator"></a>De kwantumtraceersimulator aanroepen

U kunt de kwantumtraceersimulator gebruiken om een Q#-bewerking uit te voeren.

Net als bij andere doelmachines maakt u eerst een exemplaar van de klasse `QCTraceSimulator` en geeft u deze vervolgens door als de eerste parameter van de methode `Run` van een bewerking.

Houd er rekening mee dat, in tegenstelling tot de klasse `QuantumSimulator`, de klasse `QCTraceSimulator` de interface <xref:System.IDisposable> niet implementeert, zodat u deze niet hoeft in te sluiten in een instructie `using`.

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a>De waarschijnlijkheid van metingsresultaten opgeven

Omdat de kwantumtraceersimulator de werkelijke kwantumstatus niet simuleert, kan de kans op het meten van resultaten binnen een bewerking niet worden berekend. 

Als een bewerking metingen bevat, moet u deze kansen daarom expliciet opgeven met behulp van de bewerking <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> uit de naamruimte <xref:microsoft.quantum.diagnostics>. Het volgende voorbeeld illustreert dit:

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

Wanneer de kwantumtraceersimulator de `AssertMeasurementProbability` tegenkomt, wordt vastgelegd dat aan meting `PauliZ` op `source` en `q` een resultaat van `Zero` met een waarschijnlijkheid van **0,5** moet worden toegekend. Wanneer de bewerking `M` later wordt uitgevoerd, worden de vastgelegde waarden van de resultaatkansen gevonden en retourneert `M` `Zero` of `One`, met een waarschijnlijkheid van **0,5**. Wanneer dezelfde code wordt uitgevoerd in een simulator die de kwantumtoestand bijhoudt, wordt in die simulator gecontroleerd of de in `AssertMeasurementProbability` opgegeven waarschijnlijkheden juist zijn.

Als een of meer meetbewerkingen niet zijn geannoteerd met behulp van `AssertMeasurementProbability`, wordt door de simulator een [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception) geactiveerd.

## <a name="quantum-trace-simulator-tools"></a>Hulpprogramma's voor de kwantumtraceersimulator

De QDK bevat vijf hulpprogramma's die u met de kwantumtraceersimulator kunt gebruiken om fouten in uw programma's op te sporen en de resourceschattingen van het kwantumprogramma uit te voeren: 

|Hulpprogramma | Beschrijving |
|-----| -----|
|[Controle op verschillende invoer](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |Controleert op mogelijke conflicten met gedeelde qubits |
|[Controle op het gebruik van ongeldige qubits](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |Hiermee wordt gecontroleerd of een bewerking wordt toegepast op een qubit die al is vrijgegeven |
|[Teller primitieve bewerkingen](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | Telt het aantal primitieve uitvoeringen dat wordt gebruikt door elke bewerking die wordt aangeroepen in een kwantumprogramma  |
|[Diepteteller](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |Verzamelt aantallen die de ondergrens vertegenwoordigen van elke bewerking die wordt aangeroepen in een kwantumprogramma   |
|[Breedteteller](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |Telt het aantal qubits dat wordt toegewezen en uitgeleend door elke bewerking in een kwantumprogramma |

Elk van deze hulpprogramma's wordt ingeschakeld door de juiste vlaggen in `QCTraceSimulatorConfiguration` in te stellen en de configuratie vervolgens door te geven aan de declaratie `QCTraceSimulator`. Raadpleeg de links in de voorgaande lijst voor meer informatie over het gebruik van deze hulpprogramma's. Raadpleeg [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) voor meer informatie over het configureren van `QCTraceSimulator`.

## <a name="qctracesimulator-methods"></a>QCTraceSimulator-methoden

`QCTraceSimulator` heeft verschillende ingebouwde methoden voor het ophalen van de waarden van de metrische gegevens die tijdens een kwantumbewerking worden bijgehouden. Voorbeelden van de [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) en de methoden [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) zijn te vinden in de artikelen [Teller voor primitieve bewerkingen](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Diepteteller](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) en [Breedteteller](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter). Raadpleeg [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) in de Q# API-verwijzing voor meer informatie over alle beschikbare methoden.  

## <a name="see-also"></a>Zie ook

- [Kwantumresoure-estimator](xref:microsoft.quantum.machines.resources-estimator)
- [Kwantum Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator)
- [Kwantumsimulator voor volledige toestand](xref:microsoft.quantum.machines.full-state-simulator) 