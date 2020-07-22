---
title: Full State Quantum Simulator-Quantum Development Kit
description: "Meer informatie over het uitvoeren van uw Q #-Program ma's op de Microsoft Quantum Development Kit Full State Simulator."
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.full-state-simulator
ms.openlocfilehash: 563fdbd2a45461d112e4c46651eddd75c6fc3db2
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871175"
---
# <a name="quantum-development-kit-qdk-full-state-simulator"></a><span data-ttu-id="81c2e-103">Quantum Development Kit (QDK) Full State Simulator</span><span class="sxs-lookup"><span data-stu-id="81c2e-103">Quantum Development Kit (QDK) full state simulator</span></span>

<span data-ttu-id="81c2e-104">De QDK biedt een volledige status Simulator die een quantum computer op uw lokale computer simuleert.</span><span class="sxs-lookup"><span data-stu-id="81c2e-104">The QDK provides a full state simulator that simulates a quantum machine on your local computer.</span></span> <span data-ttu-id="81c2e-105">U kunt de volledige status Simulator gebruiken om de Quantum algoritmen uit te voeren en fouten op te sporen in Q #, waarbij Maxi maal 30 qubits wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="81c2e-105">You can use the full state simulator to run and debug quantum algorithms written in Q#, utilizing up to 30 qubits.</span></span> <span data-ttu-id="81c2e-106">De volledige status Simulator is vergelijkbaar met de Quantum Simulator die wordt gebruikt in het [LIQ $ UI | \rangle $](http://stationq.github.io/Liquid/) -platform van micro soft Research.</span><span class="sxs-lookup"><span data-stu-id="81c2e-106">The full state simulator is similar to the quantum simulator used in the  [LIQ$Ui|\rangle$](http://stationq.github.io/Liquid/) platform from Microsoft Research.</span></span>

## <a name="invoking-and-running-the-full-state-simulator"></a><span data-ttu-id="81c2e-107">De volledige status Simulator aanroepen en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="81c2e-107">Invoking and running the full state simulator</span></span>

<span data-ttu-id="81c2e-108">U hebt de volledige status Simulator beschikbaar via de- `QuantumSimulator` klasse.</span><span class="sxs-lookup"><span data-stu-id="81c2e-108">You expose the full state simulator via the `QuantumSimulator` class.</span></span> <span data-ttu-id="81c2e-109">Zie [manieren om een Q #-programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="81c2e-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-simulator-from-c"></a><span data-ttu-id="81c2e-110">Het aanroepen van de Simulator vanaf C #</span><span class="sxs-lookup"><span data-stu-id="81c2e-110">Invoking the simulator from C#</span></span>

<span data-ttu-id="81c2e-111">Maak een instantie van de `QuantumSimulator` klasse en geef deze vervolgens door aan de `Run` methode van een Quantum bewerking, samen met eventuele aanvullende para meters.</span><span class="sxs-lookup"><span data-stu-id="81c2e-111">Create an instance of the `QuantumSimulator` class and then pass it to the `Run` method of a quantum operation, along with any additional parameters.</span></span>
```csharp
    using (var sim = new QuantumSimulator())
    {
        var res = myOperation.Run(sim).Result;
        ///...
    }
```

<span data-ttu-id="81c2e-112">Omdat de `QuantumSimulator` klasse de interface implementeert <xref:System.IDisposable> , moet u de methode aanroepen `Dispose` Wanneer u het exemplaar van de Simulator niet meer nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="81c2e-112">Because the `QuantumSimulator` class implements the <xref:System.IDisposable> interface, you must call the `Dispose` method once you do not need the instance of the simulator anymore.</span></span> <span data-ttu-id="81c2e-113">De beste manier om dit te doen, is het verpakken van de Simulator-declaratie en-bewerkingen binnen een [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) -instructie, die automatisch de-methode aanroept `Dispose` .</span><span class="sxs-lookup"><span data-stu-id="81c2e-113">The best way to do this is to wrap the simulator declaration and operations within a [using](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/using-statement) statement, which automatically calls the `Dispose` method.</span></span>

### <a name="invoking-the-simulator-from-python"></a><span data-ttu-id="81c2e-114">De Simulator vanuit python aanroepen</span><span class="sxs-lookup"><span data-stu-id="81c2e-114">Invoking the simulator from Python</span></span>

<span data-ttu-id="81c2e-115">Gebruik de methode [simuleren ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) vanuit de Q # python-bibliotheek met de geïmporteerde Q #-bewerking:</span><span class="sxs-lookup"><span data-stu-id="81c2e-115">Use the [simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Q# Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.simulate()
```

### <a name="invoking-the-simulator-from-the-command-line"></a><span data-ttu-id="81c2e-116">Het aanroepen van de Simulator vanaf de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="81c2e-116">Invoking the simulator from the command line</span></span>

<span data-ttu-id="81c2e-117">Wanneer u een Q #-programma uitvoert vanaf de opdracht regel, is de volledige status Simulator de standaard doel computer.</span><span class="sxs-lookup"><span data-stu-id="81c2e-117">When running a Q# program from the command line, the full state simulator is the default target machine.</span></span> <span data-ttu-id="81c2e-118">U kunt desgewenst de para meter **--Simulator** (of **-s** ) gebruiken om de gewenste doel computer op te geven.</span><span class="sxs-lookup"><span data-stu-id="81c2e-118">Optionally, you can use the **--simulator** (or **-s** shortcut) parameter to specify the desired target machine.</span></span> <span data-ttu-id="81c2e-119">De volgende opdrachten voeren een programma uit met behulp van de volledige status Simulator.</span><span class="sxs-lookup"><span data-stu-id="81c2e-119">Both of the following commands run a program using the full state simulator.</span></span> 

```dotnetcli
dotnet run
dotnet run -s QuantumSimulator
```

### <a name="invoking-the-simulator-from-juptyer-notebooks"></a><span data-ttu-id="81c2e-120">Het aanroepen van de Simulator vanuit Juptyer-notebooks</span><span class="sxs-lookup"><span data-stu-id="81c2e-120">Invoking the simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="81c2e-121">Gebruik de IQ # Magic opdracht [% simuleren](xref:microsoft.quantum.iqsharp.magic-ref.simulate) om de Q #-bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="81c2e-121">Use the IQ# magic command [%simulate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%simulate myOperation
```
## <a name="seeding-the-simulator"></a><span data-ttu-id="81c2e-122">De Simulator seeden</span><span class="sxs-lookup"><span data-stu-id="81c2e-122">Seeding the simulator</span></span>

<span data-ttu-id="81c2e-123">De volledige status Simulator maakt standaard gebruik van een wille keurige nummer generator om de wille keurige Quantum te simuleren.</span><span class="sxs-lookup"><span data-stu-id="81c2e-123">By default, the full state simulator uses a random number generator to simulate quantum randomness.</span></span> <span data-ttu-id="81c2e-124">Voor test doeleinden is het soms nuttig om deterministische resultaten te hebben.</span><span class="sxs-lookup"><span data-stu-id="81c2e-124">For testing purposes, it is sometimes useful to have deterministic results.</span></span> <span data-ttu-id="81c2e-125">In een C#-programma kunt u dit doen door een Seed te bieden voor de generator van wille keurige getallen in de `QuantumSimulator` constructor via de `randomNumberGeneratorSeed` para meter.</span><span class="sxs-lookup"><span data-stu-id="81c2e-125">In a C# program, you can accomplish this by providing a seed for the random number generator in the `QuantumSimulator` constructor via the `randomNumberGeneratorSeed` parameter.</span></span>

```csharp
    using (var sim = new QuantumSimulator(randomNumberGeneratorSeed: 42))
    {
        var res = myOperationTest.Run(sim).Result;
        ///...
    }
```

## <a name="configuring-threads"></a><span data-ttu-id="81c2e-126">Threads configureren</span><span class="sxs-lookup"><span data-stu-id="81c2e-126">Configuring threads</span></span>

<span data-ttu-id="81c2e-127">De volledige status Simulator maakt gebruik van [OpenMP](http://www.openmp.org/) om de vereiste lineaire algebra te parallelliseren.</span><span class="sxs-lookup"><span data-stu-id="81c2e-127">The full state simulator uses [OpenMP](http://www.openmp.org/) to parallelize the linear algebra required.</span></span> <span data-ttu-id="81c2e-128">OpenMP maakt standaard gebruik van alle beschik bare hardware-threads, wat betekent dat Program ma's met een klein aantal qubits vaak langzaam worden uitgevoerd omdat de coördinatie die is vereist Dwarfs de werkelijke hoeveelheid werk.</span><span class="sxs-lookup"><span data-stu-id="81c2e-128">By default, OpenMP uses all available hardware threads, which means that programs with small numbers of qubits often runs slowly because the coordination that is required dwarfs the actual work.</span></span> <span data-ttu-id="81c2e-129">U kunt dit probleem oplossen door de omgevings variabele `OMP_NUM_THREADS` in te stellen op een klein getal.</span><span class="sxs-lookup"><span data-stu-id="81c2e-129">You can fix this by setting the environment variable `OMP_NUM_THREADS` to a small number.</span></span> <span data-ttu-id="81c2e-130">Als vuist regel configureert u één thread voor Maxi maal vier qubits en vervolgens één extra thread per Qubit.</span><span class="sxs-lookup"><span data-stu-id="81c2e-130">As a rule of thumb, configure one thread for up to four qubits, and then one additional thread per qubit.</span></span> <span data-ttu-id="81c2e-131">Mogelijk moet u de variabele aanpassen afhankelijk van uw algoritme.</span><span class="sxs-lookup"><span data-stu-id="81c2e-131">You might need to adjust the variable depending on your algorithm.</span></span>

## <a name="see-also"></a><span data-ttu-id="81c2e-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="81c2e-132">See also</span></span>

- [<span data-ttu-id="81c2e-133">Quantum bronnen estimator</span><span class="sxs-lookup"><span data-stu-id="81c2e-133">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="81c2e-134">Quantum Toffoli Simulator</span><span class="sxs-lookup"><span data-stu-id="81c2e-134">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="81c2e-135">Quantum Trace Simulator</span><span class="sxs-lookup"><span data-stu-id="81c2e-135">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)