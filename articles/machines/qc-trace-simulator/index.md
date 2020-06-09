---
title: Trajectsimulator kwantumcomputer
description: Meer informatie over hoe u de Microsoft Quantum-computertracesimulator kunt gebruiken om fouten in klassieke code op te sporen en om resourcevereisten van een kwantumprogramma in te schatten.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 4cec688da35951271d87396d9b6a8fed744defc6
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84577662"
---
# <a name="quantum-trace-simulator"></a>Kwantumtraceersimulator

De kwantumcomputer-traceersimulator voert een kwantumprogramma uit zonder de toestand van een kwantumcomputer daadwerkelijk te simuleren.  Daarom kunnen met de traceersimulator kwantumprogramma's van duizenden qubits worden uitgevoerd.  De simulator is handig voor twee hoofddoelen: 

* Het opsporen van fouten in klassieke code die deel uitmaakt van een kwantumprogramma. 
* Het schatten van de benodigde resources voor het uitvoeren van een bepaald exemplaar van een kwantumprogramma op een kwantumcomputer.

De traceersimulator is afhankelijk van aanvullende gegevens die door de gebruiker worden verstrekt wanneer er metingen moeten worden uitgevoerd. Zie de sectie [De waarschijnlijkheid van metingsresultaten opgeven](#providing-the-probability-of-measurement-outcomes) voor meer informatie hierover. 

## <a name="providing-the-probability-of-measurement-outcomes"></a>De waarschijnlijkheid van metingsresultaten opgeven

Er zijn twee soorten metingen die voorkomen in kwantumalgoritmen. De eerste soort speelt een ondersteunende rol waarbij de gebruiker de waarschijnlijkheid van de resultaten doorgaans kent. In dit geval kan de gebruiker <xref:microsoft.quantum.intrinsic.assertprob> schrijven vanuit de naamruimte <xref:microsoft.quantum.intrinsic> om deze kennis uit te drukken. Het volgende voorbeeld illustreert dit:

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

Wanneer `AssertProb` wordt uitgevoerd met de traceersimulator, wordt vastgelegd dat aan meting `PauliZ` op `source` en `q` een resultaat van `Zero` met een waarschijnlijkheid van 0,5 moet worden toegekend. Wanneer later `M` wordt uitgevoerd, worden de vastgelegde waarden van de waarschijnlijkheid van de resultaten gevonden en wordt voor `M` een resultaat van `Zero` of `One` geretourneerd met een waarschijnlijkheid van 0,5. Wanneer dezelfde code wordt uitgevoerd in een simulator die de kwantumtoestand bijhoudt, wordt in die simulator gecontroleerd of de in `AssertProb` opgegeven waarschijnlijkheden juist zijn.

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a>Uw programma uitvoeren met de kwantumcomputertraceersimulator 

De kwantumcomputertraceersimulator kan in feite gewoon worden gezien als een andere doelcomputer. Het C#-stuurprogramma voor het gebruik ervan lijkt veel op dat van elke willekeurige andere kwantumsimulator: 

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

Als een of meer metingen niet zijn geannoteerd met behulp van `AssertProb`, wordt door de simulator een `UnconstrainedMeasurementException`-uitzondering van de naamruimte `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` geactiveerd. Zie de API-documentatie over [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) voor meer informatie.

Naast het onderdeel voor het uitvoeren van kwantumprogramma's bevat de traceersimulator vijf onderdelen voor het opsporen van fouten in programma's en het schatten van de benodigde resources voor kwantumprogramma's: 

* [Controle op verschillende input](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [Controle op gebruik van ongeldige qubits](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [Teller primitieve bewerkingen](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [Teller circuitdiepte](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [Teller circuitbreedte](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

Elk van deze onderdelen kan worden ingeschakeld door de juiste vlaggen in te stellen in `QCTraceSimulatorConfiguration`. Meer informatie over het gebruik van elk van deze onderdelen vindt u in de bijbehorende referentiebestanden. Zie de API-documentatie over [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) voor specifieke informatie.

## <a name="see-also"></a>Zie ook
Naslaginformatie over de kwantumcomputer-[traceersimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) voor C# 

