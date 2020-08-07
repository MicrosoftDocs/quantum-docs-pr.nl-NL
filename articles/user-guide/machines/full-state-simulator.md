---
title: Full State Quantum Simulator-Quantum Development Kit
description: Meer informatie over het uitvoeren Q# van uw Program ma's op de Microsoft Quantum Development Kit Full State Simulator.
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: b15af66123dadae09815cde1966c69b3ce2e9e64
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868335"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a>Quantum Development Kit (QDK) Full State Simulator

De QDK biedt een volledige status Simulator die een quantum computer op uw lokale computer simuleert. U kunt de volledige status Simulator gebruiken voor het uitvoeren van en het opsporen van fouten in de Quantum-algoritmen die zijn geschreven in Q# , waarbij Maxi maal 30 qubits wordt gebruikt. De volledige status Simulator is vergelijkbaar met de Quantum Simulator die wordt gebruikt in het [LIQ $ UI | \rangle $](http://stationq.github.io/Liquid/) -platform van micro soft Research.

## <a name="invoking-and-running-the-full-state-simulator"></a>De volledige status Simulator aanroepen en uitvoeren

U hebt de volledige status Simulator beschikbaar via de- `QuantumSimulator` klasse. Zie [manieren om een Q# programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.

### <a name="invoking-the-simulator-from-c"></a>Het aanroepen van de Simulator vanaf C #

Maak een instantie van de `QuantumSimulator` klasse en geef deze vervolgens door aan de `Run` methode van een Quantum bewerking, samen met eventuele aanvullende para meters.
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

Omdat de `QuantumSimulator` klasse de interface implementeert <xref:System.IDisposable> , moet u de methode aanroepen `Dispose` Wanneer u het exemplaar van de Simulator niet meer nodig hebt. De beste manier om dit te doen, is het verpakken van de Simulator-declaratie en-bewerkingen binnen een [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) -instructie, die automatisch de-methode aanroept `Dispose` .

### <a name="invoking-the-simulator-from-python"></a>De Simulator vanuit python aanroepen

Gebruik de methode [simuleren ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) vanuit de Q# python-bibliotheek met de geïmporteerde Q# bewerking:

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a>Het aanroepen van de Simulator vanaf de opdracht regel

Wanneer een programma wordt uitgevoerd Q# vanaf de opdracht regel, is de volledige status Simulator de standaard doel computer. U kunt desgewenst de para meter **--Simulator** (of **-s** ) gebruiken om de gewenste doel computer op te geven. De volgende opdrachten voeren een programma uit met behulp van de volledige status Simulator. 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a>Het aanroepen van de Simulator vanuit Juptyer-notebooks

Gebruik de I Q# Magic-opdracht [% simuleren](xref:microsoft.quantum.iqsharp.magic-ref.simulate) om de bewerking uit te voeren Q# .

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a>De Simulator seeden

De volledige status Simulator maakt standaard gebruik van een wille keurige nummer generator om de wille keurige Quantum te simuleren. Voor test doeleinden is het soms nuttig om deterministische resultaten te hebben. In een C#-programma kunt u dit doen door een Seed te bieden voor de generator van wille keurige getallen in de `QuantumSimulator` constructor via de `randomNumberGeneratorSeed` para meter.

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a>Threads configureren

De volledige status Simulator maakt gebruik van [OpenMP](http://www.openmp.org/) om de vereiste lineaire algebra te parallelliseren. OpenMP maakt standaard gebruik van alle beschik bare hardware-threads, wat betekent dat Program ma's met een klein aantal qubits vaak langzaam worden uitgevoerd omdat de coördinatie die is vereist Dwarfs de werkelijke hoeveelheid werk. U kunt dit probleem oplossen door de omgevings variabele `OMP_NUM_THREADS` in te stellen op een klein getal. Als vuist regel configureert u één thread voor Maxi maal vier qubits en vervolgens één extra thread per Qubit. Mogelijk moet u de variabele aanpassen afhankelijk van uw algoritme.

## <a name="see-also"></a>Zie ook

- [Kwantumresoure-estimator](xref:microsoft.quantum.machines.resources-estimator)
- [Kwantum Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator)
- [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)