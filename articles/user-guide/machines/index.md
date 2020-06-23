---
title: Kwantumsimulatoren en hosttoepassingen | Microsoft Docs
description: Hierin wordt beschreven hoe u kwantumsimulatoren kunt aansturen met een klassieke .NET-programmeertaal, zoals C# of Q#.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 14aed75ed0ed192f88699b1c7dbacfae23f74642
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273335"
---
# <a name="quantum-simulators-and-host-applications"></a>Kwantumsimulatoren en hosttoepassingen

## <a name="what-youll-learn"></a>U leert het volgende

> [!div class="checklist"]
> * Hoe kwantumalgoritmen worden uitgevoerd
> * Welke kwantumsimulatoren deze versie bevat
> * Hoe u een C#-stuurprogramma schrijft voor uw kwantumalgoritme

## <a name="the-quantum-development-kit-execution-model"></a>Het uitvoeringsmodel van de Quantum development kit

In [Een kwantumprogramma schrijven](xref:microsoft.quantum.write-program) hebben we ons kwantumalgoritme uitgevoerd door het object `QuantumSimulator` door te geven aan de methode `Run` van de algoritmeklasse.
De klasse `QuantumSimulator` voert het kwantumalgoritme uit door de kwantumtoestandsvector volledig te simuleren, wat perfect is voor het uitvoeren en testen van `Teleport`.
Zie de [handleiding Concepten](xref:microsoft.quantum.concepts.intro) voor meer informatie over kwantumtoestandsvectoren.

Andere doelcomputers kunnen worden gebruikt om een kwantumalgoritme uit te voeren.
De computer is verantwoordelijk voor het leveren van de implementaties van kwantumprimitieven voor het algoritme.
Dit omvat primitieve bewerkingen, zoals H, CNOT en Measure, plus qubitbeheer en -tracering.
Verschillende klassen van kwantumcomputers vertegenwoordigen verschillende uitvoeringsmodellen voor hetzelfde kwantumalgoritme.

Op elk type kwantumcomputer kunnen verschillende implementaties van deze primitieven worden geïnstalleerd.
Met de kwantumcomputer-traceersimulator die deel uitmaakt van de development kit wordt bijvoorbeeld helemaal geen simulatie uitgevoerd.
In plaats daarvan worden het gebruik van gates, qubits en andere resources bijgehouden voor het algoritme.

### <a name="quantum-machines"></a>Kwantumcomputers

In de toekomst zullen we aanvullende kwantumcomputerklassen definiëren om andere typen simulaties en uitvoering op topologische kwantumcomputers te ondersteunen.
Het algoritme kan constant blijven terwijl de onderliggende computerimplementatie wordt gewijzigd. Dit maakt het eenvoudig om een algoritme in simulatie te testen en fouten op te sporen en het vervolgens op echte hardware uit te voeren in de wetenschap dat het algoritme niet is gewijzigd.

### <a name="whats-included-in-this-release"></a>Wat bevat deze versie?

Deze versie van de Quantum Development Kit bevat verschillende kwantumcomputerklassen.
Deze zijn allemaal gedefinieerd in de naamruimte `Microsoft.Quantum.Simulation.Simulators`.

* Een [volledige toestandsvectorsimulator](xref:microsoft.quantum.machines.full-state-simulator), de klasse `QuantumSimulator`.
* Een [eenvoudige resource-estimator](xref:microsoft.quantum.machines.resources-estimator), de klasse `ResourcesEstimator`, waarmee u een algemene schatting kunt maken van de benodigde resources voor het uitvoeren van een kwantumalgoritme.
* Een [op tracering gebaseerde resource-estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), de klasse `QCTraceSimulator`, waarmee u een geavanceerde analyse kunt maken van de verbruikte resources voor de hele call-graph (aanroepgrafiek) van het algoritme.
* Een [Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator), de klasse `ToffoliSimulator`.

## <a name="writing-a-host-application"></a>Een hosttoepassing schrijven

In [Een kwantumprogramma schrijven](xref:microsoft.quantum.write-program) hebben we een eenvoudig C#-stuurprogramma voor ons teleporteeralgoritme geschreven. Een C#-stuurprogramma heeft 4 hoofddoelen:

* De doelcomputer maken
* Eventuele benodigde argumenten voor het kwantumalgoritme berekenen
* Het kwantumalgoritme uitvoeren met behulp van de simulator
* Het resultaat van de bewerking verwerken

Hieronder bespreken we elke stap in meer detail.

### <a name="constructing-the-target-machine"></a>De doelcomputer maken

Kwantumcomputers zijn exemplaren van normale .NET-klassen en worden, net als elke andere .NET-klasse, gemaakt door hun constructor aan te roepen.
Sommige simulatoren, met inbegrip van de `QuantumSimulator`, implementeren de .NET-interface <xref:System.IDisposable?displayProperty=nameWithType> en moeten dus worden verpakt in een C#-instructie met `using`.

### <a name="computing-arguments-for-the-algorithm"></a>Argumenten berekenen voor het algoritme

In het voorbeeld `Teleport` hebben we enkele relatief kunstmatige argumenten berekend om die door te geven aan het kwantumalgoritme.
Doorgaans is er een aanzienlijke hoeveelheid gegevens nodig voor het kwantumalgoritme. Het is het gemakkelijkst om deze op te geven via het klassieke stuurprogramma.

Bij het uitvoeren van chemische simulaties is voor het kwantumalgoritme bijvoorbeeld een grote tabel met moleculaire orbitaalinteractie-integralen vereist.
Over het algemeen worden deze gelezen vanuit een bestand dat wordt aangeleverd bij het uitvoeren van het algoritme.
Omdat in Q# geen mechanisme bestaat voor het openen van het bestandssysteem, kunnen dergelijke gegevens het beste worden verzameld via het klassieke stuurprogramma en vervolgens worden doorgegeven aan de methode `Run` van het kwantumalgoritme.

Ook bij variabele methoden speelt het klassieke stuurprogramma een belangrijke rol.
In deze klasse van algoritmen wordt een kwantumtoestand voorbereid op basis van enkele klassieke parameters, en wordt die toestand gebruikt voor het berekenen van een bepaalde waarde.
De parameters worden aangepast op basis van een type Hill Climbing- of machine learning-algoritme en het kwantumalgoritme wordt opnieuw uitgevoerd.
Voor dergelijke algoritmen kan het Hill Climbing-algoritme zelf het beste worden geïmplementeerd als een louter klassieke functie die wordt aangeroepen door het klassieke stuurprogramma; de resultaten van het Hill Climbing-algoritme worden vervolgens doorgegeven aan de volgende uitvoering van het kwantumalgoritme.

### <a name="running-the-quantum-algorithm"></a>Het kwantumalgoritme uitvoeren

Dit deel is over het algemeen zeer eenvoudig.
Elke Q#-bewerking wordt gecompileerd in een klasse die voorziet in een statische `Run`-methode.
De argumenten voor deze methode worden doorgegeven door de tuple van het afgevlakte argument van de bewerking zelf, plus een extra eerste argument voor de simulator waarmee de methode moet worden uitgevoerd. Voor een bewerking waarin de benoemde tuple van het type `(a: String, (b: Double, c: Double))` wordt verwacht, is het afgevlakte equivalent van het type `(String a, Double b, Double c)`.


Er zijn wel enkele subtiliteiten om rekening mee te houden bij het doorgeven van argumenten aan een `Run`-methode:

* Matrices moeten worden verpakt in een `Microsoft.Quantum.Simulation.Core.QArray<T>`-object.
    Een `QArray`-klasse heeft een constructor waarin u een geordende verzameling (`IEnumerable<T>`) van de juiste objecten kunt opgeven.
* De lege tuple, `()` in Q#, wordt opgegeven met `QVoid.Instance` in C#.
* Niet-lege tuples worden opgegeven als .NET `ValueTuple`-exemplaren.
* Door de gebruiker gedefinieerde typen in Q# worden doorgegeven als het bijbehorende basistype.
* Als u een bewerking of functie wilt doorgeven aan een `Run`-methode, moet u een exemplaar van de klasse van de bewerking of functie verkrijgen met behulp van de methode `Get<>` van de simulator.

### <a name="processing-the-results"></a>De resultaten verwerken

De resultaten van het kwantumalgoritme worden geretourneerd met behulp van de methode `Run`.
De methode `Run` wordt asynchroon uitgevoerd zodat er een exemplaar van <xref:System.Threading.Tasks.Task`1> wordt geretourneerd.
Er zijn meerdere manieren om de werkelijke resultaten van de bewerking te verkrijgen. De eenvoudigste manier is met behulp van de eigenschap [`Result` van `Task`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result):

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
maar andere technieken, zoals het gebruik van de methode [`Wait`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) of het C#-sleutelwoord [`await`](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) werken ook.

Net als bij argumenten, worden Q#-tuples weergegeven als exemplaren van `ValueTuple`, en Q#-matrices als exemplaren van `QArray`.
Door de gebruiker gedefinieerde typen worden geretourneerd als de bijbehorende basistypen.
De lege tuple, `()`, wordt geretourneerd als een exemplaar van de klasse `QVoid`.

Voor veel kwantumalgoritmen is een aanzienlijke hoeveelheid naverwerking nodig om nuttige antwoorden te kunnen afleiden.
Het kwantumdeel van het algoritme van Shor is slechts het begin van een berekening waarmee de factoren van een getal worden gevonden.

In de meeste gevallen kan dergelijke naverwerking het snelst en eenvoudigst worden uitgevoerd in het klassieke stuurprogramma.
Alleen met het klassieke stuurprogramma kunnen resultaten worden gerapporteerd aan de gebruiker of naar schijf worden geschreven.
Het klassieke stuurprogramma biedt toegang tot analysebibliotheken en andere wiskundige functies die niet beschikbaar zijn in Q#.


## <a name="failures"></a>Fouten

Wanneer de Q#-instructie `fail` wordt bereikt tijdens het uitvoeren van een bewerking, wordt er een `ExecutionFailException`-uitzondering gegenereerd.

Als gevolg van het gebruik van `System.Task` in de methode `Run`, wordt de uitzondering die is opgetreden als gevolg van een `fail`-instructie verpakt in een `System.AggregateException`.
Als u de werkelijke oorzaak van de fout wilt achterhalen, moet u dit herhalen in de `AggregateException` 
`InnerExceptions`, bijvoorbeeld:

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a>Andere klassieke talen

Hoewel de gegeven voorbeelden zijn geschreven in C#, F# en Python, biedt de Quantum development kit ook ondersteuning voor het schrijven van klassieke hostprogramma's in andere talen.
Als u bijvoorbeeld een hostprogramma wilt schrijven in Visual Basic, [zou het programma gewoon moeten werken](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).
