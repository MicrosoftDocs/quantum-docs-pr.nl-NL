---
title: Volledige status Simulator
description: "Meer informatie over het uitvoeren van uw Q #-Program ma's op de Microsoft Quantum Development Kit Full State Simulator."
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: f73abbc4366b003e4b22366ed83ca9c897737307
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906114"
---
# <a name="quantum-development-kit-full-state-simulator"></a>Volledige status Simulator van Quantum Development Kit

De Quantum Development Kit biedt een volledige status van een Quantum-Simulator, vergelijkbaar met [LIQ $ UI | \rangle $](http://stationq.github.io/Liquid/) van micro soft Research.
Deze simulator kan worden gebruikt om Quantum-algoritmen die zijn geschreven in Q # op uw computer uit te voeren en op te sporen.

Deze Quantum Simulator wordt weer gegeven via de `QuantumSimulator` klasse. Als u de Simulator wilt gebruiken, maakt u gewoon een exemplaar van deze klasse en geeft u het door aan de `Run` methode van de Quantum bewerking die u wilt uitvoeren, samen met de rest van de para meters:

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a>IDisposable

De klasse `QuantumSimulator` implementeert <xref:System.IDisposable>, dus de methode `Dispose` moet worden aangeroepen wanneer het exemplaar van de Simulator niet meer wordt gebruikt. De beste manier om dit te doen is om de Simulator binnen een `using`-instructie te laten teruglopen, zoals in het bovenstaande voor beeld.

## <a name="seed"></a>meerder

De `QuantumSimulator` gebruikt een generator voor wille keurige getallen om de wille keurige Quantum te simuleren. Voor test doeleinden is het soms nuttig om deterministische resultaten te hebben. Dit kan worden bereikt door een Seed te geven voor de generator voor wille keurige getallen in de constructor van de `QuantumSimulator`via de para meter `randomNumberGeneratorSeed`:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Lijnen

De `QuantumSimulator` maakt gebruik van [OpenMP](http://www.openmp.org/) om de vereiste lineaire algebra te parallelliseren. OpenMP gebruikt standaard alle beschikbare hardware-threads, wat wil zeggen dat programma's met kleine aantallen qubits vaak langzaam worden uitgevoerd door de coördinatie die nodig is om het werkelijke werk te klein te laten lijken. Dit kan worden opgelost door de omgevings variabele `OMP_NUM_THREADS` in te stellen op een klein getal. Als brede richtlijn is één thread goed voor ongeveer vier qubits en is vervolgens een aanvullende thread per qubit goed, hoewel dit zeer afhankelijk is van uw algoritme.

