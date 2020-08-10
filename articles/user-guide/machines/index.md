---
title: Kwantumsimulators en Q#-programma's
description: Beschrijft de kwantumsimulators die beschikbaar zijn als doelmachines voor Q#-programma's.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 6/17/2020
ms.topic: article
uid: microsoft.quantum.machines
no-loc:
- Q#
- $$v
ms.openlocfilehash: 77401ca3642b89d708f338f852dc60bf7346b87b
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868301"
---
# <a name="quantum-simulators"></a>Kwantumsimulators

Kwantumsimulators zijn softwareprogramma's die worden uitgevoerd op klassieke computers en fungeren als *doelmachine* voor een Q#-programma. Dit maakt het mogelijk om kwantumprogramma's uit te voeren en te testen in een omgeving die voorspelt hoe qubits op verschillende bewerkingen reageren. In dit artikel wordt beschreven welke kwantumsimulators zijn opgenomen in de Quantum Development Kit (QDK), evenals de verschillende manieren waarop u een Q#-programma kunt doorgeven aan de kwantumsimulators, bijvoorbeeld via de opdrachtregel of met behulp van stuurprogrammacodes die in een klassieke taal zijn geschreven.  



## <a name="the-quantum-development-kit-qdk-quantum-simulators"></a>De Quantum Development Kit (QDK)-kwantumsimulators

De kwantumsimulator is verantwoordelijk voor het leveren van de implementaties van kwantumprimitieven voor een algoritme. Dit omvat primitieve bewerkingen, zoals `H`, `CNOT` en `Measure`, plus qubitbeheer en -tracering. De QDK bevat verschillende klassen van kwantumsimulators die verschillende uitvoeringsmodellen voor hetzelfde kwantumalgoritme vertegenwoordigen. 


Op elk type kwantumsimulator kunnen verschillende implementaties van deze primitieven worden geïnstalleerd. Bijvoorbeeld: de [simulator voor volledige toestand](xref:microsoft.quantum.machines.full-state-simulator) voert het kwantumalgoritme uit door de [kwantumstatusvector](xref:microsoft.quantum.glossary#quantum-state) volledig te simuleren, terwijl de [trajectsimulator kwantumcomputer](xref:microsoft.quantum.machines.qc-trace-simulator.intro) geen rekening houdt met de daadwerkelijke kwantumstatus. In plaats daarvan worden het gebruik van gates, qubits en andere resources bijgehouden voor het algoritme.

### <a name="quantum-machine-classes"></a>Klassen van kwantumcomputers

In de toekomst zal de QDK aanvullende kwantumcomputerklassen definiëren om andere typen simulaties en uitvoering op topologische kwantumhardware te ondersteunen. Het algoritme kan constant blijven terwijl de onderliggende computerimplementatie wordt gewijzigd. Dit maakt het eenvoudig om een algoritme in simulatie te testen en fouten op te sporen en het vervolgens op echte hardware uit te voeren in de wetenschap dat het algoritme niet is gewijzigd.

De QDK bevat verschillende klassen kwantumcomputers, die allemaal zijn gedefinieerd in de naamruimte `Microsoft.Quantum.Simulation.Simulators`.

|Simulator |Klasse|Beschrijving|
|-----|------|---|
|[Simulator voor volledige toestand](xref:microsoft.quantum.machines.full-state-simulator)| `QuantumSimulator` | Hiermee worden kwantumalgoritmen uitgevoerd en fouten opgespoord. Deze simulator is beperkt tot 30 qubits. |
|[Eenvoudige resource-estimator](xref:microsoft.quantum.machines.resources-estimator)| `ResourcesEstimator` | Hiermee kunt u een algemene schatting maken van de benodigde resources voor het uitvoeren van een kwantumalgoritme. Deze simulator ondersteunt duizenden qubits.|
|[Op tracering gebaseerde resource-estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)|  `QCTraceSimulator` |Hiermee kunt u een geavanceerde analyse uitvoeren van de verbruikte resources voor de hele call-graph (aanroepgrafiek) van het algoritme. Deze simulator ondersteunt duizenden qubits.|
|[Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator)| `ToffoliSimulator` |Hiermee simuleert u kwantumalgoritmen die beperkt zijn tot `X`, `CNOT` en meerdere beheerde `X` kwantumbewerkingen. Deze simulator ondersteunt miljoenen qubits. |

## <a name="invoking-the-quantum-simulator"></a>De kwantumsimulator aanroepen

In [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs) worden drie manieren beschreven waarop de Q#-code wordt doorgegeven aan de kwantumsimulator: 

* De opdrachtregel gebruiken
* Een Python-hostprogramma gebruiken
* Een C#-hostprogramma gebruiken

Kwantumcomputers zijn exemplaren van normale .NET-klassen en worden, net als elke andere .NET-klasse, gemaakt door hun constructor aan te roepen. Hoe u dit doet, is afhankelijk van hoe u het Q#-programma uitvoert.

## <a name="next-steps"></a>Volgende stappen

* Raadpleeg [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs) voor meer informatie over het aanroepen van doelcomputers voor Q#-programma's in verschillende omgevingen.
