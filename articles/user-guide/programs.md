---
title: 'Q # introdution'
description: "Snel Inleiding tot Quantum Program ma's in Q #"
author: beheim
ms.author: beheim
ms.date: 11/08/2020
ms.topic: article
uid: microsoft.quantum.guide.programs
ms.openlocfilehash: 975bcda5e0042406b465a83f17f1d2d3f5a1ec4f
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96233485"
---
# <a name="q-quantum-programming-language"></a><span data-ttu-id="1c179-103">Q # Quantum-programmeer taal</span><span class="sxs-lookup"><span data-stu-id="1c179-103">Q# Quantum Programming Language</span></span>

<span data-ttu-id="1c179-104">Alles wat u moet weten over de Q # programmeer taal wordt beschreven in de [taal gids q #](xref:microsoft.quantum.qsharp.index).</span><span class="sxs-lookup"><span data-stu-id="1c179-104">Everything you need to know about the Q# programming language is detailed in the [Q# language guide](xref:microsoft.quantum.qsharp.index).</span></span> <span data-ttu-id="1c179-105">Net als bij iets anders is het [ontwerp proces](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) voor de open source en onze bijdragen.</span><span class="sxs-lookup"><span data-stu-id="1c179-105">Like anything else, our [language design process](https://github.com/microsoft/qsharp-language#q-language-and-core-libraries-design) is open source and we welcome contributions.</span></span>
<span data-ttu-id="1c179-106">Zie [Waarom hebben we q # nodig](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/)voor meer achtergrond informatie over de stichtingen en motivaties achter Q #.</span><span class="sxs-lookup"><span data-stu-id="1c179-106">For more background about the foundations and motivation behind Q#, see [Why do we need Q#?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).</span></span>  
<span data-ttu-id="1c179-107">Q # wordt geleverd als onderdeel van de Quantum Development Kit (QDK) voor een kort overzicht, [Wat is de QDK?](xref:microsoft.quantum.overview.q-sharp).</span><span class="sxs-lookup"><span data-stu-id="1c179-107">Q# is shipped as part of the Quantum Development Kit (QDK) For a quick overview, check out [What is the QDK?](xref:microsoft.quantum.overview.q-sharp).</span></span> 

## <a name="what-is-a-quantum-program"></a><span data-ttu-id="1c179-108">Wat is een Quantum programma?</span><span class="sxs-lookup"><span data-stu-id="1c179-108">What is a quantum program?</span></span>

<span data-ttu-id="1c179-109">Een Quantum programma kan worden gezien als een bepaalde set klassieke subroutines die, indien aangeroepen, een berekening uitvoeren door interactie met een Quantum systeem; een programma geschreven in Q # maakt niet rechtstreeks een model van de Quantum status, maar in plaats daarvan wordt beschreven hoe een klassieke controle computer communiceert met qubits.</span><span class="sxs-lookup"><span data-stu-id="1c179-109">A quantum program can be seen as a particular set of classical subroutines which, when called, perform a computation by interacting with a quantum system; a program written in Q# does not directly model the quantum state, but rather describes how a classical control computer interacts with qubits.</span></span>
<span data-ttu-id="1c179-110">Op deze manier kunnen we volledig neutraal over wat een Quantum staat, *zelfs op elke* doel computer, die verschillende interpretaties kan hebben, afhankelijk van de computer.</span><span class="sxs-lookup"><span data-stu-id="1c179-110">This allows us to be entirely agnostic about what a quantum state even *is* on each target machine, which might have different interpretations depending on the machine.</span></span> 

<span data-ttu-id="1c179-111">Een belang rijk gevolg hiervan is dat Q # geen mogelijkheid heeft om rechtstreeks introspect te maken van een Qubit of andere eigenschappen van Quantum monteurs, wat garandeert dat een Q #-programma fysiek kan worden uitgevoerd op een quantum computer.</span><span class="sxs-lookup"><span data-stu-id="1c179-111">An important consequence of that is that Q# has no ability to introspect into the state of a qubit or other properties of quantum mechanics directly, which guarantees that a Q# program can be physically executed on a quantum computer.</span></span>
<span data-ttu-id="1c179-112">Een programma kan in plaats daarvan bewerkingen aanroepen zoals [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) om klassieke informatie uit een Qubit te halen.</span><span class="sxs-lookup"><span data-stu-id="1c179-112">Instead, a program can call operations such as [`Measure`](xref:Microsoft.Quantum.Intrinsic.Measure) to extract classical information from a qubit.</span></span>

<span data-ttu-id="1c179-113">Zodra de toewijzing is toegewezen, kan een Qubit worden door gegeven aan bewerkingen en functies, ook wel *callables* genoemd.</span><span class="sxs-lookup"><span data-stu-id="1c179-113">Once allocated, a qubit can be passed to operations and functions, also referred to as *callables*.</span></span> <span data-ttu-id="1c179-114">In sommige zin is dit alles wat een Q #-programma kan doen met een Qubit. Alle directe acties op de status van een Qubit zijn allemaal gedefinieerd door *intrinsieke* callables, zoals [`X`](xref:Microsoft.Quantum.Intrinsic.X) en [`H`](xref:Microsoft.Quantum.Intrinsic.H) -callables waarvan de implementaties niet zijn gedefinieerd in Q #, maar die in plaats daarvan worden gedefinieerd door de doel computer.</span><span class="sxs-lookup"><span data-stu-id="1c179-114">In some sense, this is all that a Q# program can do with a qubit; Any direct actions on state of a qubit are all defined by *intrinsic* callables such as [`X`](xref:Microsoft.Quantum.Intrinsic.X) and [`H`](xref:Microsoft.Quantum.Intrinsic.H) - i.e. callables whose implementations are not defined within Q# but are instead defined by the target machine.</span></span> <span data-ttu-id="1c179-115">Wat deze bewerkingen eigenlijk *doen* , worden alleen concreet gemaakt door de doel computer die we gebruiken om het specifieke Q #-programma uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="1c179-115">What these operations actually *do* is only made concrete by the target machine we use to run the particular Q# program.</span></span>

<span data-ttu-id="1c179-116">Als bijvoorbeeld het programma wordt uitgevoerd op onze [volle Simulator](xref:microsoft.quantum.machines.full-state-simulator), voert de Simulator de bijbehorende wiskundige bewerkingen uit op het gesimuleerde Quantum systeem.</span><span class="sxs-lookup"><span data-stu-id="1c179-116">For example, if running the program on our [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), the simulator performs the corresponding mathematical operations to the simulated quantum system.</span></span>
<span data-ttu-id="1c179-117">Maar in de toekomst kijken, wanneer de doel computer een echte quantum computer is, leidt het aanroepen van dergelijke bewerkingen in Q # ervoor dat de quantum computer de overeenkomstige *real* -bewerkingen op het *echte* Quantum systeem kan uitvoeren (bijvoorbeeld nauw keurig verlopen Laser pulsen).</span><span class="sxs-lookup"><span data-stu-id="1c179-117">But looking toward the future, when the target machine is a real quantum computer, calling such operations in Q# will direct the quantum computer to perform the corresponding *real* operations on the *real* quantum system (e.g. precisely timed laser pulses).</span></span>

<span data-ttu-id="1c179-118">Een Q #-programma recombineert deze bewerkingen, zoals gedefinieerd door een doel machine, om nieuwe bewerkingen op een hoger niveau te maken voor een snelle Quantum berekening.</span><span class="sxs-lookup"><span data-stu-id="1c179-118">A Q# program recombines these operations as defined by a target machine to create new, higher-level operations to express quantum computation.</span></span>
<span data-ttu-id="1c179-119">Op deze manier maakt Q # het eenvoudig om de logische en hybride Quantum-algoritmen van de logica te expresseren, en is deze ook algemeen wat betreft de structuur van een doel machine of Simulator.</span><span class="sxs-lookup"><span data-stu-id="1c179-119">In this way, Q# makes it easy to express the logic underlying quantum and hybrid quantum–classical algorithms, while also being general with respect to the structure of a target machine or simulator.</span></span>

<span data-ttu-id="1c179-120">Een eenvoudig voor beeld is het volgende programma, dat één Qubit toewijst in de $ \ket {0} $-status, waarna een Hadamard-bewerking wordt toegepast op het `H` bestand en het resultaat op basis hiervan wordt gemeten `PauliZ` .</span><span class="sxs-lookup"><span data-stu-id="1c179-120">A simple example is the following program, which allocates one qubit in the $\ket{0}$ state, then applies a Hadamard operation `H` to it and measures the result in the `PauliZ` basis.</span></span>

```qsharp
@EntryPoint()
operation MeasureOneQubit() : Result {
    // The following using block creates a fresh qubit and initializes it
    // in the |0〉 state.
    using (qubit = Qubit()) {
        // We apply a Hadamard operation H to the state, thereby preparing the
        // state 1 / sqrt(2) (|0〉 + |1〉).
        H(qubit);
        // Now we measure the qubit in Z-basis.
        let result = M(qubit);
        // As the qubit is now in an eigenstate of the measurement operator,
        // we reset the qubit before releasing it.
        if (result == One) { X(qubit); }
        // Finally, we return the result of the measurement.
        return result;
    }
}
```

<span data-ttu-id="1c179-121">Onze [Quantum Katas](https://github.com/microsoft/QuantumKatas#introduction) biedt een goede inleiding in de [quantum computing-concepten](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) , zoals algemene Quantum bewerkingen en het manipuleren van qubits.</span><span class="sxs-lookup"><span data-stu-id="1c179-121">Our [Quantum Katas](https://github.com/microsoft/QuantumKatas#introduction) give a good introduction on [Quantum Computing Concepts](https://github.com/microsoft/QuantumKatas#quantum-computing-concepts-qubits-and-gates) such as common quantum operations and how to manipulate qubits.</span></span> <span data-ttu-id="1c179-122">Meer voor beelden zijn ook te vinden in [intrinsieke bewerkingen en functies](xref:microsoft.quantum.libraries.standard.prelude).</span><span class="sxs-lookup"><span data-stu-id="1c179-122">More examples can also be found in [Intrinsic Operations and Functions](xref:microsoft.quantum.libraries.standard.prelude).</span></span>



