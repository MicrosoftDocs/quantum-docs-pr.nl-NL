---
title: Volledige status Simulator van Quantum Development Kit | Microsoft Docs
description: Overzicht van de volledige status Simulator van de Quantum Development Kit van micro soft
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 12/7/2017
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: ab0e65765d27e301a59948d7c02105a523022e68
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184675"
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

## <a name="seed"></a>Meerder

De `QuantumSimulator` gebruikt een generator voor wille keurige getallen om de wille keurige Quantum te simuleren. Voor test doeleinden is het soms nuttig om deterministische resultaten te hebben. Dit kan worden bereikt door een Seed te geven voor de generator voor wille keurige getallen in de constructor van de `QuantumSimulator`via de para meter `randomNumberGeneratorSeed`:

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a>Lijnen

De `QuantumSimulator` maakt gebruik van [OpenMP](http://www.openmp.org/) om de vereiste lineaire algebra te parallelliseren. Standaard gebruikt OpenMP alle beschik bare hardware-threads, wat betekent dat Program ma's met een klein aantal qubits vaak langzaam worden uitgevoerd omdat de coördinatie vereist dat de werkelijke hoeveelheid werk wordt Dwarf. Dit kan worden opgelost door de omgevings variabele `OMP_NUM_THREADS` in te stellen op een klein getal. Als vuist regel is één thread geschikt voor Maxi maal 4 qubits, en dan is een extra thread per Qubit goed, hoewel dit zeer afhankelijk is van uw algoritme.

