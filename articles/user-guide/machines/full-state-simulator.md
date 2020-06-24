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
# <a name="quantum-development-kit-full-state-simulator"></a><span data-ttu-id="f6eee-103">Volledige status Simulator van Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="f6eee-103">Quantum Development Kit Full State Simulator</span></span>

<span data-ttu-id="f6eee-104">De Quantum Development Kit biedt een volledige status van een Quantum-Simulator, vergelijkbaar met [LIQ $ UI | \rangle $](http://stationq.github.io/Liquid/) van micro soft Research.</span><span class="sxs-lookup"><span data-stu-id="f6eee-104">The Quantum Development Kit provides a full state quantum simulator similar to [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) from Microsoft Research.</span></span>
<span data-ttu-id="f6eee-105">Deze simulator kan worden gebruikt om Quantum-algoritmen die zijn geschreven in Q # op uw computer uit te voeren en op te sporen.</span><span class="sxs-lookup"><span data-stu-id="f6eee-105">This simulator can be used to execute and debug quantum algorithms written in Q# on your computer.</span></span>

<span data-ttu-id="f6eee-106">Deze Quantum Simulator wordt weer gegeven via de- `QuantumSimulator` klasse.</span><span class="sxs-lookup"><span data-stu-id="f6eee-106">This quantum simulator is exposed via the `QuantumSimulator` class.</span></span> <span data-ttu-id="f6eee-107">Als u de Simulator wilt gebruiken, maakt u gewoon een exemplaar van deze klasse en geeft u het door aan de `Run` methode van de Quantum bewerking die u wilt uitvoeren, samen met de rest van de para meters:</span><span class="sxs-lookup"><span data-stu-id="f6eee-107">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

## <a name="idisposable"></a><span data-ttu-id="f6eee-108">IDisposable</span><span class="sxs-lookup"><span data-stu-id="f6eee-108">IDisposable</span></span>

<span data-ttu-id="f6eee-109">De `QuantumSimulator` klasse implementeert <xref:System.IDisposable> , dus de `Dispose` methode moet worden aangeroepen wanneer het exemplaar van de Simulator niet meer wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f6eee-109">The `QuantumSimulator` class implements <xref:System.IDisposable>, thus the `Dispose` method should be called once the instance of the simulator is not used anymore.</span></span> <span data-ttu-id="f6eee-110">De beste manier om dit te doen is door de Simulator binnen een instructie te laten teruglopen `using` , zoals in het bovenstaande voor beeld.</span><span class="sxs-lookup"><span data-stu-id="f6eee-110">The best way to do this is to wrap the simulator within a `using` statement, as in the example above.</span></span>

## <a name="seed"></a><span data-ttu-id="f6eee-111">Meerder</span><span class="sxs-lookup"><span data-stu-id="f6eee-111">Seed</span></span>

<span data-ttu-id="f6eee-112">`QuantumSimulator`Hiermee wordt een wille keurige nummer generator gebruikt voor het simuleren van Quantum wille keurigheid.</span><span class="sxs-lookup"><span data-stu-id="f6eee-112">The `QuantumSimulator` uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="f6eee-113">Voor test doeleinden is het soms nuttig om deterministische resultaten te hebben.</span><span class="sxs-lookup"><span data-stu-id="f6eee-113">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="f6eee-114">Dit kan worden bereikt door een Seed te bieden voor de generator van wille keurige getallen in de `QuantumSimulator` constructor, via de `randomNumberGeneratorSeed` para meter:</span><span class="sxs-lookup"><span data-stu-id="f6eee-114">This can be accomplished by providing a seed for the random number generator in the `QuantumSimulator`'s constructor via the `randomNumberGeneratorSeed` parameter:</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="threads"></a><span data-ttu-id="f6eee-115">Lijnen</span><span class="sxs-lookup"><span data-stu-id="f6eee-115">Threads</span></span>

<span data-ttu-id="f6eee-116">De `QuantumSimulator` [OpenMP](http://www.openmp.org/) maakt gebruik van de lineaire algebra vereist.</span><span class="sxs-lookup"><span data-stu-id="f6eee-116">The `QuantumSimulator` uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="f6eee-117">OpenMP gebruikt standaard alle beschikbare hardware-threads, wat wil zeggen dat programma's met kleine aantallen qubits vaak langzaam worden uitgevoerd door de coördinatie die nodig is om het werkelijke werk te klein te laten lijken.</span><span class="sxs-lookup"><span data-stu-id="f6eee-117">By default OpenMP uses all available hardware threads, which means that programs with small numbers of qubits will often run slowly because the coordination required will dwarf the actual work.</span></span> <span data-ttu-id="f6eee-118">Dit kan worden opgelost door de omgevings variabele `OMP_NUM_THREADS` in te stellen op een klein getal.</span><span class="sxs-lookup"><span data-stu-id="f6eee-118">This can be fixed by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="f6eee-119">Als brede richtlijn is één thread goed voor ongeveer vier qubits en is vervolgens een aanvullende thread per qubit goed, hoewel dit zeer afhankelijk is van uw algoritme.</span><span class="sxs-lookup"><span data-stu-id="f6eee-119">As a very rough rule of thumb, 1 thread is good for up to about 4 qubits, and then an additional thread per qubit is good, although this is highly dependent on your algorithm.</span></span>

