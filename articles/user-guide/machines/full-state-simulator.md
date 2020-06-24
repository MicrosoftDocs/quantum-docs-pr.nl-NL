---
title: Volledige status Simulator
description: "Meer informatie over het uitvoeren van uw Q #-Program ma's op de Microsoft Quantum Development Kit Full State Simulator."
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: f73abbc4366b003e4b22366ed83ca9c897737307
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274945"
---
# <a name="quantum-development-kit-full-state-simulator"></a>Volledige status Simulator van Quantum Development Kit

De Quantum Development Kit biedt een volledige status van een Quantum-Simulator, vergelijkbaar met [LIQ $ UI | \rangle $](http://stationq.github.io/Liquid/) van micro soft Research.
Deze simulator kan worden gebruikt om Quantum-algoritmen die zijn geschreven in Q # op uw computer uit te voeren en op te sporen.

Deze Quantum Simulator wordt weer gegeven via de- `QuantumSimulator` klasse. Als u de Simulator wilt gebruiken, maakt u gewoon een exemplaar van deze klasse en geeft u het door aan de `Run` methode van de Quantum bewerking die u wilt uitvoeren, samen met de rest van de para meters:

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a>IDisposable

De `QuantumSimulator` klasse implementeert <xref:System.IDisposable> , dus de `Dispose` methode moet worden aangeroepen wanneer het exemplaar van de Simulator niet meer wordt gebruikt. De beste manier om dit te doen is door de Simulator binnen een instructie te laten teruglopen `using` , zoals in het bovenstaande voor beeld.

## <a name="seed"></a>Meerder

`QuantumSimulator`Hiermee wordt een wille keurige nummer generator gebruikt voor het simuleren van Quantum wille keurigheid. Voor test doeleinden is het soms nuttig om deterministische resultaten te hebben. Dit kan worden bereikt door een Seed te bieden voor de generator van wille keurige getallen in de `QuantumSimulator` constructor, via de `randomNumberGeneratorSeed` para meter:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Lijnen

De `QuantumSimulator` [OpenMP](http://www.openmp.org/) maakt gebruik van de lineaire algebra vereist. OpenMP gebruikt standaard alle beschikbare hardware-threads, wat wil zeggen dat programma's met kleine aantallen qubits vaak langzaam worden uitgevoerd door de coördinatie die nodig is om het werkelijke werk te klein te laten lijken. Dit kan worden opgelost door de omgevings variabele `OMP_NUM_THREADS` in te stellen op een klein getal. Als brede richtlijn is één thread goed voor ongeveer vier qubits en is vervolgens een aanvullende thread per qubit goed, hoewel dit zeer afhankelijk is van uw algoritme.

