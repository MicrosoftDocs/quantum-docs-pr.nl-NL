---
title: Quantum Toffoli Simulator-Quantum Development Kit
description: Meer informatie over de micro soft QDK Toffoli Simulator, een speciale Quantum Simulator die kan worden gebruikt met miljoenen qubits.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 6/25/2020
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8a981645703423856e667be7c3dccf5270a5885f
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868097"
---
# <a name="quantum-development-kit-qdk-toffoli-simulator"></a><span data-ttu-id="e459b-103">Quantum Development Kit (QDK) Toffoli Simulator</span><span class="sxs-lookup"><span data-stu-id="e459b-103">Quantum Development Kit (QDK) Toffoli simulator</span></span>

<span data-ttu-id="e459b-104">De QDK Toffoli Simulator is een speciale Simulator met een beperkt bereik en ondersteunt alleen, en biedt ondersteuning voor `X` `CNOT` meerdere beheerde `X` Quantum bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="e459b-104">The QDK Toffoli simulator is a special-purpose simulator with a limited scope and only supports `X`, `CNOT`, and multi-controlled `X` quantum operations.</span></span> <span data-ttu-id="e459b-105">Alle klassieke logica en berekeningen zijn beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="e459b-105">All classical logic and computations are available.</span></span>

<span data-ttu-id="e459b-106">Hoewel de Toffoli-Simulator meer functionaliteit heeft dan de [volledige status Simulator](xref:microsoft.quantum.machines.full-state-simulator), heeft het voor deel dat u veel meer qubits kunt simuleren.</span><span class="sxs-lookup"><span data-stu-id="e459b-106">While the Toffoli simulator is more restricted in functionality than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it has the advantage of being able to simulate far more qubits.</span></span> <span data-ttu-id="e459b-107">De Toffoli Simulator kan worden gebruikt met miljoenen qubits, terwijl de volledige status Simulator is beperkt tot ongeveer 30 qubits.</span><span class="sxs-lookup"><span data-stu-id="e459b-107">The Toffoli simulator can be used with millions of qubits, while the full state simulator is limited to about 30 qubits.</span></span> <span data-ttu-id="e459b-108">Dit is bijvoorbeeld handig voor Oracle die Booleaanse functies evalueren: ze kunnen worden geïmplementeerd met behulp van de beperkte set ondersteunde algoritmen en worden getest op een groot aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="e459b-108">This is useful, for example, with oracles that evaluate Boolean functions - they can be implemented using the limited set of supported algorithms and tested on a large number of qubits.</span></span>

## <a name="invoking-the-toffoli-simulator"></a><span data-ttu-id="e459b-109">De Toffoli Simulator aanroepen</span><span class="sxs-lookup"><span data-stu-id="e459b-109">Invoking the Toffoli simulator</span></span>

<span data-ttu-id="e459b-110">U maakt de Toffoli Simulator via de- `ToffoliSimulator` klasse beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="e459b-110">You expose the Toffoli simulator via the `ToffoliSimulator` class.</span></span> <span data-ttu-id="e459b-111">Zie [manieren om een Q# programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e459b-111">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-toffoli-simulator-from-c"></a><span data-ttu-id="e459b-112">Het aanroepen van Toffoli Simulator vanaf C #</span><span class="sxs-lookup"><span data-stu-id="e459b-112">Invoking the Toffoli simulator from C#</span></span>

<span data-ttu-id="e459b-113">Net als bij andere doelmachines maakt u eerst een exemplaar van de klasse `ToffoliSimulator` en geeft u deze vervolgens door als de eerste parameter van de methode `Run` van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="e459b-113">As with other target machines, you first create an instance of the `ToffoliSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="e459b-114">Houd er rekening mee dat, in tegenstelling tot de klasse `QuantumSimulator`, de klasse `ToffoliSimulator` de interface <xref:System.IDisposable> niet implementeert, zodat u deze niet hoeft in te sluiten in een instructie `using`.</span><span class="sxs-lookup"><span data-stu-id="e459b-114">Note that, unlike the `QuantumSimulator` class, the `ToffoliSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

### <a name="invoking-the-toffoli-simulator-from-python"></a><span data-ttu-id="e459b-115">De Toffoli Simulator vanuit python aanroepen</span><span class="sxs-lookup"><span data-stu-id="e459b-115">Invoking the Toffoli simulator from Python</span></span>

<span data-ttu-id="e459b-116">Gebruik de methode [toffoli_simulate ()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) vanuit de python-bibliotheek met de geïmporteerde Q# bewerking:</span><span class="sxs-lookup"><span data-stu-id="e459b-116">Use the [toffoli_simulate()](https://docs.microsoft.com/python/qsharp/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.toffoli_simulate()
```

### <a name="invoking-the-toffoli-simulator-from-the-command-line"></a><span data-ttu-id="e459b-117">Het aanroepen van Toffoli Simulator vanaf de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="e459b-117">Invoking the Toffoli simulator from the command line</span></span>

<span data-ttu-id="e459b-118">Wanneer u een Q# programma uitvoert vanaf de opdracht regel, gebruikt u de para meter **--Simulator** (of **-s** ) om de doel computer van de Toffoli Simulator op te geven.</span><span class="sxs-lookup"><span data-stu-id="e459b-118">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the Toffoli simulator target machine.</span></span> <span data-ttu-id="e459b-119">Met de volgende opdracht voert u een programma uit met behulp van de resources Estimator:</span><span class="sxs-lookup"><span data-stu-id="e459b-119">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ToffoliSimulator
```

### <a name="invoking-the-toffoli-simulator-from-juptyer-notebooks"></a><span data-ttu-id="e459b-120">De Toffoli Simulator van Juptyer-notebooks aanroepen</span><span class="sxs-lookup"><span data-stu-id="e459b-120">Invoking the Toffoli simulator from Juptyer Notebooks</span></span>

<span data-ttu-id="e459b-121">Gebruik de Q# opdracht I Magic [% Toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) om de bewerking uit te voeren Q# .</span><span class="sxs-lookup"><span data-stu-id="e459b-121">Use the IQ# magic command [%toffoli](xref:microsoft.quantum.iqsharp.magic-ref.toffoli) to run the Q# operation.</span></span>

```
%toffoli myOperation
```

## <a name="supported-operations"></a><span data-ttu-id="e459b-122">Ondersteunde bewerkingen</span><span class="sxs-lookup"><span data-stu-id="e459b-122">Supported operations</span></span>

<span data-ttu-id="e459b-123">De Toffoli Simulator ondersteunt:</span><span class="sxs-lookup"><span data-stu-id="e459b-123">The Toffoli simulator supports:</span></span>

* <span data-ttu-id="e459b-124">Rotaties en exponentiated Paulis, zoals `R` en `Exp` , wanneer de resulterende bewerking gelijk is aan `X` of de identiteits matrix.</span><span class="sxs-lookup"><span data-stu-id="e459b-124">Rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation equals `X` or the identity matrix.</span></span>
* <span data-ttu-id="e459b-125">Metings-en [bevestigings](xref:microsoft.quantum.diagnostics.assertmeasurement) bewerkingen, maar alleen op basis van de Pauli `Z` .</span><span class="sxs-lookup"><span data-stu-id="e459b-125">Measurement and [assert](xref:microsoft.quantum.diagnostics.assertmeasurement) operations, but only in the Pauli `Z` basis.</span></span> <span data-ttu-id="e459b-126">Houd er rekening mee dat de kans op een meting bewerking altijd **0** of **1**is; Er is geen wille keurige Toffoli Simulator.</span><span class="sxs-lookup"><span data-stu-id="e459b-126">Note that a measurement operation's probability is always either **0** or **1**; there is no randomness in the Toffoli simulator.</span></span>
* <span data-ttu-id="e459b-127">`DumpMachine`en- `DumpRegister` functies.</span><span class="sxs-lookup"><span data-stu-id="e459b-127">`DumpMachine` and `DumpRegister` functions.</span></span>
<span data-ttu-id="e459b-128">Beide functies voeren de huidige `Z` status van elke qubit, één Qubit per regel.</span><span class="sxs-lookup"><span data-stu-id="e459b-128">Both functions output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="specifying-the-number-of-qubits"></a><span data-ttu-id="e459b-129">Het aantal qubits opgeven</span><span class="sxs-lookup"><span data-stu-id="e459b-129">Specifying the number of qubits</span></span>

<span data-ttu-id="e459b-130">Een `ToffoliSimulator` instantie wijst standaard ruimte toe voor 65.536 qubits.</span><span class="sxs-lookup"><span data-stu-id="e459b-130">By default, a `ToffoliSimulator` instance allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="e459b-131">Als voor uw algoritme meer qubits vereist zijn, kunt u het aantal Qubit opgeven door een waarde voor de `qubitCount` para meter op te geven voor de constructor.</span><span class="sxs-lookup"><span data-stu-id="e459b-131">If your algorithm requires more qubits than this, you can specify the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="e459b-132">Voor elke extra Qubit is slechts één byte geheugen vereist, dus er zijn geen aanzienlijke kosten voor het overberekenen van het aantal qubits dat u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="e459b-132">Each additional qubit requires only one byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="e459b-133">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="e459b-133">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```

## <a name="see-also"></a><span data-ttu-id="e459b-134">Zie tevens</span><span class="sxs-lookup"><span data-stu-id="e459b-134">See also</span></span>

- [<span data-ttu-id="e459b-135">Quantum bronnen estimator</span><span class="sxs-lookup"><span data-stu-id="e459b-135">Quantum Resources Estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="e459b-136">Quantum Trace Simulator</span><span class="sxs-lookup"><span data-stu-id="e459b-136">Quantum Trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="e459b-137">Quantum Full State Simulator</span><span class="sxs-lookup"><span data-stu-id="e459b-137">Quantum Full State simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 