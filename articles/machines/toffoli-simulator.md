---
title: Quantum Development Kit Toffoli Simulator
description: Meer informatie over de micro soft QDK Toffoli Simulator, een speciale Quantum Simulator die kan worden gebruikt met miljoenen qubits.
author: alan-geller
ms.author: ageller@microsoft.com
ms.date: 01/16/2019
ms.topic: article
uid: microsoft.quantum.machines.toffoli-simulator
ms.openlocfilehash: 8a29caaa0fa058600a74e7d130e644374cbfa19c
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907015"
---
# <a name="quantum-development-kit-toffoli-simulator"></a><span data-ttu-id="77f67-103">Quantum Development Kit Toffoli Simulator</span><span class="sxs-lookup"><span data-stu-id="77f67-103">Quantum Development Kit Toffoli Simulator</span></span>

<span data-ttu-id="77f67-104">De Quantum Development Kit biedt een Toffoli Simulator, een speciale Simulator waarmee Quantum algoritmen kunnen worden gesimuleerd die beperkt zijn tot X-, CNOT-en multi-Controlled X Quantum-bewerkingen (alle klassieke logica en berekeningen zijn beschikbaar).</span><span class="sxs-lookup"><span data-stu-id="77f67-104">The Quantum Development Kit provides a Toffoli simulator, which is a special-purpose simulator that can simulate quantum algorithms that are limited to X, CNOT, and multi-controlled X quantum operations (all classical logic and computations are available).</span></span>

<span data-ttu-id="77f67-105">Hoewel de Toffoli-Simulator veel meer beperkt is in de bewerking dan de [volledige status Simulator](xref:microsoft.quantum.machines.full-state-simulator), kan deze nog veel meer qubits simuleren.</span><span class="sxs-lookup"><span data-stu-id="77f67-105">While the Toffoli simulator is much more restricted in operation than the [full state simulator](xref:microsoft.quantum.machines.full-state-simulator), it can simulate far more qubits.</span></span>
<span data-ttu-id="77f67-106">De Toffoli Simulator kan worden gebruikt met miljoenen qubits, terwijl de volledige status Simulator doorgaans beperkt is tot ongeveer 30.</span><span class="sxs-lookup"><span data-stu-id="77f67-106">The Toffoli simulator can be used with millions of qubits, while the full state simulator is generally limited to about 30.</span></span>
<span data-ttu-id="77f67-107">Het kan een beperkt aantal Quantum algoritmen die zijn geschreven in Q # op uw computer uitvoeren en fouten opsporen. Zo kunnen Oracle die Booleaanse functies evalueren, worden geïmplementeerd met behulp van deze Gates en dus worden getest op het variëren van grote aantallen qubits met behulp van deze simulator.</span><span class="sxs-lookup"><span data-stu-id="77f67-107">It can execute and debug a limited set of quantum algorithms written in Q# on your computer; for instance, oracles that evaluate Boolean functions can be implemented using these gates and so tested on vary large numbers of qubits using this simulator.</span></span>

<span data-ttu-id="77f67-108">Deze Quantum Simulator wordt weer gegeven via de `ToffoliSimulator` klasse.</span><span class="sxs-lookup"><span data-stu-id="77f67-108">This quantum simulator is exposed via the `ToffoliSimulator` class.</span></span>
<span data-ttu-id="77f67-109">Als u de Simulator wilt gebruiken, maakt u gewoon een exemplaar van deze klasse en geeft u het door aan de `Run` methode van de Quantum bewerking die u wilt uitvoeren, samen met de rest van de para meters:</span><span class="sxs-lookup"><span data-stu-id="77f67-109">To use the simulator, simply create an instance of this class and pass it to the `Run` method of the quantum operation you want to execute along with the rest of the parameters:</span></span>

```csharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    ///...
```

## <a name="other-operations"></a><span data-ttu-id="77f67-110">Andere bewerkingen</span><span class="sxs-lookup"><span data-stu-id="77f67-110">Other Operations</span></span>

<span data-ttu-id="77f67-111">Het `ToffoliSimulator` ondersteunt rotaties en exponentiated Paulis, zoals `R` en `Exp`, wanneer de resulterende bewerking gelijk is aan `X` of aan de identiteit.</span><span class="sxs-lookup"><span data-stu-id="77f67-111">The `ToffoliSimulator` supports rotations and exponentiated Paulis, such as `R` and `Exp`, when the resulting operation is equal to `X` or to the identity.</span></span>

<span data-ttu-id="77f67-112">Meting en bevestiging worden alleen ondersteund in de Pauli `Z` basis.</span><span class="sxs-lookup"><span data-stu-id="77f67-112">Measurement and assert are supported, but only in the Pauli `Z` basis.</span></span>
<span data-ttu-id="77f67-113">Houd er rekening mee dat de kans op een bepaalde meting altijd 0 of 1 is. Er is geen wille keurige Toffoli Simulator.</span><span class="sxs-lookup"><span data-stu-id="77f67-113">Note that the probability of some measurement is always either 0 or 1; there is no randomness in the Toffoli simulator.</span></span>

<span data-ttu-id="77f67-114">`DumpMachine` en `DumpRegister` worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="77f67-114">`DumpMachine` and `DumpRegister` are supported.</span></span>
<span data-ttu-id="77f67-115">Ze voeren beide de huidige `Z`-basis status van elke qubit uit, één Qubit per regel.</span><span class="sxs-lookup"><span data-stu-id="77f67-115">They both output the current `Z`-basis state of each qubit, one qubit per line.</span></span>

## <a name="qubitcount"></a><span data-ttu-id="77f67-116">QubitCount</span><span class="sxs-lookup"><span data-stu-id="77f67-116">QubitCount</span></span>

<span data-ttu-id="77f67-117">De `ToffoliSimulator` wijst standaard ruimte toe voor 65.536 qubits.</span><span class="sxs-lookup"><span data-stu-id="77f67-117">By default, the `ToffoliSimulator` allocates space for 65,536 qubits.</span></span>
<span data-ttu-id="77f67-118">Als er meer dan dit algoritme vereist is, kunt u het aantal Qubit wijzigen door een waarde voor de para meter `qubitCount` op te geven voor de constructor.</span><span class="sxs-lookup"><span data-stu-id="77f67-118">If your algorithm requires more than this, you can change the qubit count by providing a value for the `qubitCount` parameter to the constructor.</span></span>
<span data-ttu-id="77f67-119">Elke extra Qubit vereist een extra byte geheugen, zodat er geen aanzienlijke kosten in rekening worden geschat voor het aantal qubits dat u nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="77f67-119">Each additional qubit requires an additional byte of memory, so there is no significant cost to overestimating the number of qubits you'll need.</span></span>

<span data-ttu-id="77f67-120">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="77f67-120">For example:</span></span>

```csharp
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```
