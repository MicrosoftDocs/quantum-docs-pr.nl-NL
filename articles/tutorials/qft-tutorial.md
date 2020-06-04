---
title: "Program ma's op Qubit-niveau schrijven en simuleren in Q #"
description: Stapsgewijze zelf studie voor het schrijven en simuleren van een Quantum programma dat op het individuele Qubit niveau werkt
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 10/06/2019
uid: microsoft.quantum.circuit-tutorial
ms.topic: tutorial
ms.openlocfilehash: f0b87936c9baf07555e76f295da58c0a6b9ecd17
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84328592"
---
# <a name="tutorial-write-and-simulate-qubit-level-programs-in-q"></a><span data-ttu-id="feb26-103">Zelf studie: Program ma's op Qubit schrijven en simuleren in Q\#</span><span class="sxs-lookup"><span data-stu-id="feb26-103">Tutorial: Write and simulate qubit-level programs in Q\#</span></span>

<span data-ttu-id="feb26-104">Welkom bij de Quantum Development Kit-zelf studie over het schrijven en simuleren van een eenvoudig Quantum programma dat wordt uitgevoerd op afzonderlijke qubits.</span><span class="sxs-lookup"><span data-stu-id="feb26-104">Welcome to the Quantum Development Kit tutorial on writing and simulating a basic quantum program that operates on individual qubits.</span></span> 

<span data-ttu-id="feb26-105">Hoewel Q # primair is gemaakt als een programmeer taal op hoog niveau voor grootschalige Quantum Program ma's, kan deze net zo eenvoudig worden gebruikt om het lagere niveau van Quantum Program ma's te verkennen: rechtstreeks adresseren specifieke qubits.</span><span class="sxs-lookup"><span data-stu-id="feb26-105">Although Q# was primarily created as a high-level programming language for large-scale quantum programs, it can just as easily be used to explore the lower level of quantum programs: directly addressing specific qubits.</span></span>
<span data-ttu-id="feb26-106">Met de flexibiliteit van Q # kunnen gebruikers een Quantum systeem van een dergelijk abstractie niveau benaderen, en in deze zelf studie gaan we in op de qubits zelf.</span><span class="sxs-lookup"><span data-stu-id="feb26-106">The flexibility of Q# allows users to approach quantum systems from any such level of abstraction, and in this tutorial we dive into the qubits themselves.</span></span>
<span data-ttu-id="feb26-107">In het bijzonder kijken we naar de schermen van de [Quantum-Fourier-trans formatie](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), een subroutine die integraal is aan veel grotere Quantum algoritmen.</span><span class="sxs-lookup"><span data-stu-id="feb26-107">Specifically, we take a look under the hood of the [quantum Fourier transform](https://en.wikipedia.org/wiki/Quantum_Fourier_transform), a subroutine that is integral to many larger quantum algorithms.</span></span>

<span data-ttu-id="feb26-108">Houd er rekening mee dat deze weer gave op laag niveau van Quantum gegevens verwerking vaak wordt beschreven in termen van '[Quantum circuits](xref:microsoft.quantum.concepts.circuits)', die de sequentiële toepassing van poorten voor specifieke qubits van een systeem vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="feb26-108">Note that this low-level view of quantum information processing is often described in terms of "[quantum circuits](xref:microsoft.quantum.concepts.circuits)," which represent the sequential application of gates to specific qubits of a system.</span></span>

<span data-ttu-id="feb26-109">Daarom kunnen de single-en multi-Qubit-bewerkingen die we opeenvolgend Toep assen, gemakkelijk worden weer gegeven in een circuit diagram.</span><span class="sxs-lookup"><span data-stu-id="feb26-109">Thus, the single- and multi-qubit operations we sequentially apply can be readily represented in a "circuit diagram."</span></span>
<span data-ttu-id="feb26-110">In ons geval definieert u een Q #-bewerking voor het uitvoeren van de volledige Qubit Quantum-Fourier-trans formatie, die de volgende representatie als een circuit heeft:</span><span class="sxs-lookup"><span data-stu-id="feb26-110">In our case, we will define a Q# operation to perform the full three-qubit quantum Fourier transform, which has the following representation as a circuit:</span></span>

<br/>
<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

## <a name="prerequisites"></a><span data-ttu-id="feb26-111">Vereisten</span><span class="sxs-lookup"><span data-stu-id="feb26-111">Prerequisites</span></span>

* <span data-ttu-id="feb26-112">[Installeer](xref:microsoft.quantum.install) de Quantum Development Kit met uw voorkeurs taal en-ontwikkelings omgeving.</span><span class="sxs-lookup"><span data-stu-id="feb26-112">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your preferred language and development environment.</span></span>
* <span data-ttu-id="feb26-113">Als u de QDK al hebt geïnstalleerd, controleert u of uw versie is [bijgewerkt](xref:microsoft.quantum.update) naar de nieuwste versie</span><span class="sxs-lookup"><span data-stu-id="feb26-113">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>


## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="feb26-114">In deze zelfstudie leert u het volgende:</span><span class="sxs-lookup"><span data-stu-id="feb26-114">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="feb26-115">Quantum bewerkingen definiëren in Q #</span><span class="sxs-lookup"><span data-stu-id="feb26-115">Define quantum operations in Q#</span></span>
> * <span data-ttu-id="feb26-116">Vraag Q #-bewerkingen rechtstreeks vanaf de opdracht regel of met behulp van een klassiek host-programma</span><span class="sxs-lookup"><span data-stu-id="feb26-116">Call Q# operations directly from the command line or using a classical host program</span></span>
> * <span data-ttu-id="feb26-117">Een Quantum bewerking simuleren vanuit Qubit-toewijzing naar meting uitvoer</span><span class="sxs-lookup"><span data-stu-id="feb26-117">Simulate a quantum operation from qubit allocation to measurement output</span></span>
> * <span data-ttu-id="feb26-118">Bekijk hoe de gesimuleerde Wavefunction van het Quantum systeem tijdens de bewerking wordt ontwikkeld</span><span class="sxs-lookup"><span data-stu-id="feb26-118">Observe how the quantum system's simulated wavefunction evolves throughout the operation</span></span>

<span data-ttu-id="feb26-119">Het uitvoeren van een Quantum programma met de Quantum Development Kit van micro soft bestaat meestal uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="feb26-119">Running a quantum program with Microsoft's Quantum Development Kit typically consists of two parts:</span></span>
1. <span data-ttu-id="feb26-120">Het programma zelf, dat wordt geïmplementeerd met behulp van de ' Q # Quantum-programmeer taal en vervolgens wordt aangeroepen om te worden uitgevoerd op een quantum computer of Quantum Simulator.</span><span class="sxs-lookup"><span data-stu-id="feb26-120">The program itself, which is implemented using the Q# quantum programming language, and then invoked to run on a quantum computer or quantum simulator.</span></span> <span data-ttu-id="feb26-121">Deze bestaan uit</span><span class="sxs-lookup"><span data-stu-id="feb26-121">These consist of</span></span> 
    - <span data-ttu-id="feb26-122">V # bewerkingen: subroutines die op Quantum registers handelen, en</span><span class="sxs-lookup"><span data-stu-id="feb26-122">Q# operations: subroutines acting on quantum registers, and</span></span> 
    - <span data-ttu-id="feb26-123">Q # functions: klassieke subroutines die worden gebruikt binnen het Quantum algoritme.</span><span class="sxs-lookup"><span data-stu-id="feb26-123">Q# functions: classical subroutines used within the quantum algorithm.</span></span>
2. <span data-ttu-id="feb26-124">Het ingangs punt dat wordt gebruikt om het Quantum programma aan te roepen en de doel computer op te geven waarop het moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="feb26-124">The entry point used to call the quantum program and specify the target machine on which it should be run.</span></span>
    <span data-ttu-id="feb26-125">U kunt dit rechtstreeks doen via de opdracht regel of via een hostprogramma dat is geschreven in een klassieke programmeer taal, zoals python of C#.</span><span class="sxs-lookup"><span data-stu-id="feb26-125">This can be done directly from the command line, or through a host program written in a classical programming language like Python or C#.</span></span>
    <span data-ttu-id="feb26-126">Deze zelf studie bevat instructies voor de methode die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="feb26-126">This tutorial includes instructions for whichever method you prefer.</span></span>

## <a name="allocate-qubits-and-define-quantum-operations"></a><span data-ttu-id="feb26-127">Qubits toewijzen en Quantum bewerkingen definiëren</span><span class="sxs-lookup"><span data-stu-id="feb26-127">Allocate qubits and define quantum operations</span></span>

<span data-ttu-id="feb26-128">Het eerste deel van deze zelf studie bestaat uit het definiëren van de Q # `Perform3qubitQFT` -bewerking, waarmee de Quantum Fourier-trans formatie op drie qubits wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="feb26-128">The first part of this tutorial consists of defining the Q# operation `Perform3qubitQFT`, which performs the quantum Fourier transform on three qubits.</span></span> 

<span data-ttu-id="feb26-129">Daarnaast gebruiken we de [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) functie om te zien hoe de gesimuleerde Wavefunction van ons drie Qubit systeem zich in de hele bewerking ontwikkelt.</span><span class="sxs-lookup"><span data-stu-id="feb26-129">In addition, we will use the [`DumpMachine`](xref:microsoft.quantum.diagnostics.dumpmachine) function to observe how the simulated wavefunction of our three qubit system evolves across the operation.</span></span>

<span data-ttu-id="feb26-130">In de eerste stap maakt u uw Q #-project en-bestand.</span><span class="sxs-lookup"><span data-stu-id="feb26-130">The first step is creating your Q# project and file.</span></span>
<span data-ttu-id="feb26-131">De stappen hiervoor zijn afhankelijk van de omgeving die u gebruikt om het programma aan te roepen, en u kunt de details vinden in de respectieve [installatie handleidingen](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="feb26-131">The steps for this depend on the environment you will use to call the program, and you can find the details in the respective [installation guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="feb26-132">De onderdelen van het bestand worden stapsgewijs door lopen, maar de code is ook beschikbaar als een volledige blok kering.</span><span class="sxs-lookup"><span data-stu-id="feb26-132">We will walk you through the components of the file step-by-step, but the code is also available as a full block below.</span></span>

### <a name="namespaces-to-access-other-q-operations"></a><span data-ttu-id="feb26-133">Naam ruimten voor toegang tot andere Q #-bewerkingen</span><span class="sxs-lookup"><span data-stu-id="feb26-133">Namespaces to access other Q# operations</span></span>
<span data-ttu-id="feb26-134">In het bestand definieert u eerst de naam ruimte `NamespaceQFT` die wordt gebruikt door de compiler.</span><span class="sxs-lookup"><span data-stu-id="feb26-134">Inside the file, we first define the namespace `NamespaceQFT` which will be accessed by the compiler.</span></span>
<span data-ttu-id="feb26-135">Voor de bewerking om gebruik te maken van bestaande Q #-bewerkingen, openen we de relevante `Microsoft.Quantum.<>` naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="feb26-135">For our operation to make use of existing Q# operations, we open the relevant `Microsoft.Quantum.<>` namespaces.</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    // operations go here
}
```

### <a name="define-operations-with-arguments-and-returns"></a><span data-ttu-id="feb26-136">Bewerkingen met argumenten definiëren en retour neren</span><span class="sxs-lookup"><span data-stu-id="feb26-136">Define operations with arguments and returns</span></span>
<span data-ttu-id="feb26-137">Vervolgens definieert u de `Perform3qubitQFT` bewerking:</span><span class="sxs-lookup"><span data-stu-id="feb26-137">Next, we define the `Perform3qubitQFT` operation:</span></span>

```qsharp
    operation Perform3qubitQFT() : Unit {
        // do stuff
    }
```

<span data-ttu-id="feb26-138">De bewerking heeft nu geen argumenten en retourneert niets---in dit geval schrijven we dat er een object wordt geretourneerd dat in `Unit` `void` C# of een lege tuple `Tuple[()]` in python is Akin.</span><span class="sxs-lookup"><span data-stu-id="feb26-138">For now, the operation takes no arguments and does not return anything---in this case we write that it returns a `Unit` object, which is akin to `void` in C# or an empty tuple, `Tuple[()]`, in Python.</span></span>
<span data-ttu-id="feb26-139">Later gaan we deze wijzigen om een matrix met meet resultaten te retour neren, waarop het punt `Unit` wordt vervangen door `Result[]` .</span><span class="sxs-lookup"><span data-stu-id="feb26-139">Later, we will modify it to return an array of measurement results, at which point `Unit` will be replaced by `Result[]`.</span></span> 

### <a name="allocate-qubits-with-using"></a><span data-ttu-id="feb26-140">Qubits toewijzen aan`using`</span><span class="sxs-lookup"><span data-stu-id="feb26-140">Allocate qubits with `using`</span></span>
<span data-ttu-id="feb26-141">Binnen onze Q #-bewerking wijzen we eerst een REGI ster van drie qubits toe met de `using` instructie:</span><span class="sxs-lookup"><span data-stu-id="feb26-141">Within our Q# operation, we first allocate a register of three qubits with the `using` statement:</span></span>

```qsharp
        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

        }
```

<span data-ttu-id="feb26-142">Met `using` worden automatisch de qubits toegewezen in de status $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="feb26-142">With `using`, the qubits are automatically allocated in the $\ket{0}$ state.</span></span> <span data-ttu-id="feb26-143">We kunnen dit controleren door te gebruiken [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) en [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) , waarmee een teken reeks en de huidige status van het systeem naar de-console worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="feb26-143">We can verify this by using [`Message(<string>)`](xref:microsoft.quantum.intrinsic.message) and [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine), which print a string and the system's current state to the console.</span></span>

> [!NOTE]
> <span data-ttu-id="feb26-144">De `Message(<string>)` `DumpMachine()` functies en (van [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) en [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics) ) worden beide rechtstreeks naar de console afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="feb26-144">The `Message(<string>)` and `DumpMachine()` functions (from [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) and [`Microsoft.Quantum.Diagnostics`](xref:microsoft.quantum.diagnostics), respectively) both print directly to the console.</span></span> <span data-ttu-id="feb26-145">Net als bij een echte Quantum berekening biedt Q # geen rechtstreekse toegang tot Qubit Staten.</span><span class="sxs-lookup"><span data-stu-id="feb26-145">Just like a real quantum computation, Q# does not allow us to directly access qubit states.</span></span>
> <span data-ttu-id="feb26-146">Als `DumpMachine` de huidige status van de doel computer afdrukt, kan dit echter waardevol inzicht geven in het gebruik van fouten in combi natie met de volledige status Simulator.</span><span class="sxs-lookup"><span data-stu-id="feb26-146">However, as `DumpMachine` prints the target machine's current state, it can provide valuable insight for debugging and learning when used in conjunction with the full state simulator.</span></span>


### <a name="applying-single-qubit-and-controlled-gates"></a><span data-ttu-id="feb26-147">Single-Qubit en beheerde poorten Toep assen</span><span class="sxs-lookup"><span data-stu-id="feb26-147">Applying single-qubit and controlled gates</span></span>

<span data-ttu-id="feb26-148">Daarna passen we de Gates toe die de bewerking zelf vormen.</span><span class="sxs-lookup"><span data-stu-id="feb26-148">Next, we apply the gates which comprise the operation itself.</span></span>
<span data-ttu-id="feb26-149">Q # bevat al veel eenvoudige Quantum poorten als bewerkingen in de [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) naam ruimte, en dit is geen uitzonde ring.</span><span class="sxs-lookup"><span data-stu-id="feb26-149">Q# already contains many basic quantum gates as operations in the [`Microsoft.Quantum.Intrinsic`](xref:microsoft.quantum.intrinsic) namespace, and these are no exception.</span></span> 

<span data-ttu-id="feb26-150">Binnen een Q #-bewerking worden de instructies die callables aanroepen, in sequentiële volg orde uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="feb26-150">Within a Q# operation, the statements invoking callables will of course be executed in sequential order.</span></span>
<span data-ttu-id="feb26-151">Daarom is de eerste poort die moet worden toegepast, de [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) voor de eerste Qubit:</span><span class="sxs-lookup"><span data-stu-id="feb26-151">Hence, the first gate to apply is the [`H`](xref:microsoft.quantum.intrinsic.h) (Hadamard) to the first qubit:</span></span>

<br/>
<img src="./qft_firstH.PNG" alt="Circuit diagram for three qubit QFT through first Hadamard" width="120">

<span data-ttu-id="feb26-152">Als u een bewerking wilt Toep assen op een specifieke Qubit van een REGI ster (dat wil zeggen een enkele `Qubit` van een matrix `Qubit[]` ), gebruiken we standaard index notatie.</span><span class="sxs-lookup"><span data-stu-id="feb26-152">To apply an operation to a specific qubit from a register (i.e. a single `Qubit` from an array `Qubit[]`) we use standard index notation.</span></span>
<span data-ttu-id="feb26-153">Het Toep assen [`H`](xref:microsoft.quantum.intrinsic.h) van de op de eerste Qubit van de kassa `qs` heeft dus de volgende vorm:</span><span class="sxs-lookup"><span data-stu-id="feb26-153">So, applying the [`H`](xref:microsoft.quantum.intrinsic.h) to the first qubit of our register `qs` takes the form:</span></span>

```qsharp
            H(qs[0]);
```

<span data-ttu-id="feb26-154">Naast het Toep assen van de `H` (Hadamard)-poort op afzonderlijke qubits, bestaat het QFT-circuit voornamelijk uit beheerde [`R1`](xref:microsoft.quantum.intrinsic.r1) draaiingen.</span><span class="sxs-lookup"><span data-stu-id="feb26-154">Besides applying the `H` (Hadamard) gate to individual qubits, the QFT circuit consists primarily of controlled [`R1`](xref:microsoft.quantum.intrinsic.r1) rotations.</span></span>
<span data-ttu-id="feb26-155">Een `R1(θ, <qubit>)` bewerking in het algemeen laat het onderdeel $ \ket {0} $ van de Qubit ongewijzigd. tijdens het Toep assen van een rotatie van $e ^ {i\theta} $ naar het onderdeel $ \ket {1} $.</span><span class="sxs-lookup"><span data-stu-id="feb26-155">An `R1(θ, <qubit>)` operation in general leaves the $\ket{0}$ component of the qubit unchanged, while applying a rotation of $e^{i\theta}$ to the $\ket{1}$ component.</span></span>

#### <a name="controlled-operations"></a><span data-ttu-id="feb26-156">Beheerde bewerkingen</span><span class="sxs-lookup"><span data-stu-id="feb26-156">Controlled operations</span></span>

<span data-ttu-id="feb26-157">Q # maakt het zeer eenvoudig om een bewerking uit te voeren op een of meer besturings qubits.</span><span class="sxs-lookup"><span data-stu-id="feb26-157">Q# makes it extremely easy to condition the execution of an operation upon one or multiple control qubits.</span></span>
<span data-ttu-id="feb26-158">Over het algemeen hebben we alleen de oproep met en `Controlled` de bewerkings argumenten gewijzigd als:</span><span class="sxs-lookup"><span data-stu-id="feb26-158">In general, we merely preface the call with `Controlled`, and the operation arguments change as:</span></span>

 <span data-ttu-id="feb26-159">`Op(<normal args>)`$ \to $ `Controlled Op([<control qubits>], (<normal args>))` .</span><span class="sxs-lookup"><span data-stu-id="feb26-159">`Op(<normal args>)` $\to$ `Controlled Op([<control qubits>], (<normal args>))`.</span></span>

<span data-ttu-id="feb26-160">Houd er rekening mee dat het besturings element qubits moet worden ingesteld als een matrix, zelfs als het een enkele Qubit is.</span><span class="sxs-lookup"><span data-stu-id="feb26-160">Note that the control qubits must be provided as an array, even if it is a single qubit.</span></span>

<span data-ttu-id="feb26-161">Na de hebben `H` we zien dat de volgende Gates de `R1` poorten op de eerste Qubit zijn (en beheerd door de tweede/derde):</span><span class="sxs-lookup"><span data-stu-id="feb26-161">After the `H`, we see that the next gates are the `R1` gates acting on the first qubit (and controlled by the second/third):</span></span>

<br/>
<img src="./qft_firstqubit.PNG" alt="Circuit diagram for three qubit QFT through first qubit" width="310">

<span data-ttu-id="feb26-162">We noemen deze met</span><span class="sxs-lookup"><span data-stu-id="feb26-162">We call these with</span></span>

```qsharp
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));
```

<span data-ttu-id="feb26-163">Houd er rekening mee dat we de [`PI()`](xref:microsoft.quantum.math.pi) functie van de [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) naam ruimte gebruiken om de rotaties in termen van pi radialen te definiëren.</span><span class="sxs-lookup"><span data-stu-id="feb26-163">Note that we use the [`PI()`](xref:microsoft.quantum.math.pi) function from the [`Microsoft.Quantum.Math`](xref:microsoft.quantum.math) namespace to define the rotations in terms of pi radians.</span></span>
<span data-ttu-id="feb26-164">Daarnaast delen we door een `Double` (bijvoorbeeld), `2.0` omdat het delen door een geheel getal `2` een type fout genereert.</span><span class="sxs-lookup"><span data-stu-id="feb26-164">Additionally, we divide by a `Double` (e.g. `2.0`) because dividing by an integer `2` would throw a type error.</span></span> 

> [!TIP]
> <span data-ttu-id="feb26-165">`R1(π/2)`en `R1(π/4)` zijn gelijk aan de- `S` en- `T` bewerkingen (ook in `Microsoft.Quantum.Intrinsic` ).</span><span class="sxs-lookup"><span data-stu-id="feb26-165">`R1(π/2)` and `R1(π/4)` are equivalent to the `S` and `T` operations (also in `Microsoft.Quantum.Intrinsic`).</span></span>


<span data-ttu-id="feb26-166">Na het Toep assen van de relevante `H` bewerkingen en de beheerde draaiingen naar de tweede en derde qubits:</span><span class="sxs-lookup"><span data-stu-id="feb26-166">After applying the relevant `H` operations and controlled rotations to the second and third qubits:</span></span>

```qsharp
            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);
```

<span data-ttu-id="feb26-167">We hoeven alleen een [`SWAP`](xref:microsoft.quantum.intrinsic.swap) Gate toe te passen om het circuit te volt ooien:</span><span class="sxs-lookup"><span data-stu-id="feb26-167">we need only apply a [`SWAP`](xref:microsoft.quantum.intrinsic.swap) gate to complete the circuit:</span></span>

```qsharp
            SWAP(qs[2], qs[0]);
```

<span data-ttu-id="feb26-168">Dit is nodig omdat de aard van de Quantum Fourier-trans formatie de qubits in omgekeerde volg orde uitvoert, zodat de wissels een naadloze integratie van de subroutine tot grotere algoritmen mogelijk maakt.</span><span class="sxs-lookup"><span data-stu-id="feb26-168">This is necessary because the nature of the quantum Fourier transform outputs the qubits in reverse order, so the swaps allow for seamless integration of the subroutine into larger algorithms.</span></span>

<span data-ttu-id="feb26-169">Daarom hebben we de Qubit van de Quantum Fourier-trans formatie in onze Q #-bewerking voltooid:</span><span class="sxs-lookup"><span data-stu-id="feb26-169">Hence we have finished writing the qubit-level operations of the quantum Fourier transform into our Q# operation:</span></span>

<img src="./qft_full.PNG" alt="Three qubit quantum Fourier transform circuit diagram" width="600">

<span data-ttu-id="feb26-170">We kunnen de service echter nog maar een dag aanroepen.</span><span class="sxs-lookup"><span data-stu-id="feb26-170">However, we can't call it a day just yet.</span></span>
<span data-ttu-id="feb26-171">Onze qubits stond in de status $ \ket {0} $ toen we ze hebben toegewezen, en in de loop van de tijd, in Q #, moeten we alles op dezelfde manier hebben gevonden (of beter!).</span><span class="sxs-lookup"><span data-stu-id="feb26-171">Our qubits were in state $\ket{0}$ when we allocated them, and much like in life, in Q# we should leave things the same way we found them (or better!).</span></span>

### <a name="deallocate-qubits"></a><span data-ttu-id="feb26-172">Toewijzing qubits ongedaan maken</span><span class="sxs-lookup"><span data-stu-id="feb26-172">Deallocate qubits</span></span>

<span data-ttu-id="feb26-173">We bellen [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) opnieuw om de status na bewerking weer te geven en zijn [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) van toepassing op het Qubit-REGI ster om de qubits opnieuw in te stellen op $ \ket {0} $ voordat u de bewerking voltooit:</span><span class="sxs-lookup"><span data-stu-id="feb26-173">We call [`DumpMachine()`](xref:microsoft.quantum.diagnostics.dumpmachine) again to see the post-operation state, and finally apply [`ResetAll`](xref:microsoft.quantum.intrinsic.resetall) to the qubit register to reset our qubits to $\ket{0}$ before completing the operation:</span></span>

```qsharp
            Message("After:");
            DumpMachine();

            ResetAll(qs);
```

<span data-ttu-id="feb26-174">Als u wilt dat alle niet-toegewezen qubits expliciet worden ingesteld op $ \ket {0} $ is een basis functie van Q #, omdat het mogelijk is dat andere bewerkingen hun status nauw keurig kennen wanneer ze dezelfde qubits (een schaarse resource) gaan gebruiken.</span><span class="sxs-lookup"><span data-stu-id="feb26-174">Requiring that all deallocated qubits be explicitly set to $\ket{0}$ is a basic feature of Q#, as it allows other operations to know their state precisely when they begin using those same qubits (a scarce resource).</span></span>
<span data-ttu-id="feb26-175">Bovendien zorgt dit ervoor dat ze niet Entangled zijn met andere qubits in het systeem.</span><span class="sxs-lookup"><span data-stu-id="feb26-175">Additionally, this assures that they not be entangled with any other qubits in the system.</span></span>
<span data-ttu-id="feb26-176">Als het opnieuw instellen niet wordt uitgevoerd aan het einde van een `using` toewijzings blok, wordt een runtime-fout gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="feb26-176">If the reset is not performed at the end of a `using` allocation block, a runtime error will be thrown.</span></span>

<span data-ttu-id="feb26-177">Uw volledige Q #-bestand moet er nu als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="feb26-177">Your full Q# file should now look like this:</span></span>

```qsharp
namespace NamespaceQFT {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;
    open Microsoft.Quantum.Math;
    open Microsoft.Quantum.Arrays;

    operation Perform3qubitQFT() : Unit {

        using (qs = Qubit[3]) {

            Message("Initial state |000>:");
            DumpMachine();

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("After:");
            DumpMachine();

            ResetAll(qs);
        }
    }
}
```


<span data-ttu-id="feb26-178">Als het bestand Q # en de bewerking is voltooid, kan ons Quantum programma worden aangeroepen en gesimuleerd.</span><span class="sxs-lookup"><span data-stu-id="feb26-178">With the Q# file and operation complete, our quantum program is ready to be called and simulated.</span></span>

## <a name="execute-the-program"></a><span data-ttu-id="feb26-179">Het programma uitvoeren</span><span class="sxs-lookup"><span data-stu-id="feb26-179">Execute the program</span></span>

<span data-ttu-id="feb26-180">Nadat u de Q #-bewerking in een `.qs` bestand hebt gedefinieerd, moet u deze bewerking nu aanroepen en de geretourneerde klassieke gegevens bekijken.</span><span class="sxs-lookup"><span data-stu-id="feb26-180">Having defined our Q# operation in a `.qs` file, we now need to call that operation and observe any returned classical data.</span></span>
<span data-ttu-id="feb26-181">Er wordt nu niets geretourneerd (terugvallen op basis van de hierboven gedefinieerde bewerking `Unit` ), maar wanneer we de Q #-bewerking later wijzigen om een matrix met meet resultaten te retour neren ( `Result[]` ), zullen we dit aanpakken.</span><span class="sxs-lookup"><span data-stu-id="feb26-181">For now, there isn't anything returned (recall that our operation defined above returns `Unit`), but when we later modify the Q# operation to return an array of measurement results (`Result[]`), we will address this.</span></span>

<span data-ttu-id="feb26-182">Hoewel het programma Q # alomtegenwoordige is in de omgevingen die worden gebruikt om het te aanroepen, is de manier waarop u dit kunt doen, afhankelijk van elkaar.</span><span class="sxs-lookup"><span data-stu-id="feb26-182">While the Q# program is ubiquitous across the environments used to call it, the manner of doing so will of course vary.</span></span> <span data-ttu-id="feb26-183">Volg de instructies in het tabblad dat overeenkomt met uw installatie: werken vanuit de Q #-opdracht regel toepassing of een host-programma in Python of C#.</span><span class="sxs-lookup"><span data-stu-id="feb26-183">As such, simply follow the instructions in the tab corresponding to your setup: working from the Q# command line application or using a host program in Python or C#.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="feb26-184">Opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="feb26-184">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="feb26-185">Voor het uitvoeren van het programma Q # vanaf de opdracht regel is slechts een kleine wijziging van het Q #-bestand vereist.</span><span class="sxs-lookup"><span data-stu-id="feb26-185">Running the Q# program from the command line requires only a small change to the Q# file.</span></span>

<span data-ttu-id="feb26-186">Voeg simpelweg toe `@EntryPoint()` aan een regel voor de bewerkings definitie:</span><span class="sxs-lookup"><span data-stu-id="feb26-186">Simply add `@EntryPoint()` to a line preceding the operation definition:</span></span>

```qsharp
    @EntryPoint()
    operation Perform3qubitQFT() : Unit {
        // ...
```

<span data-ttu-id="feb26-187">Als u het programma wilt uitvoeren, opent u de terminal in de map van het project en voert u</span><span class="sxs-lookup"><span data-stu-id="feb26-187">To run the program, open the terminal in the folder of your project and enter</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="feb26-188">Na de uitvoering ziet u de `Message` onderstaande en `DumpMachine` afgedrukte uitvoer in uw-console.</span><span class="sxs-lookup"><span data-stu-id="feb26-188">Upon execution, you should see the `Message` and `DumpMachine` outputs below printed in your console.</span></span>


#### <a name="python"></a>[<span data-ttu-id="feb26-189">Python</span><span class="sxs-lookup"><span data-stu-id="feb26-189">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="feb26-190">Een python-hostbestand maken: `host.py` .</span><span class="sxs-lookup"><span data-stu-id="feb26-190">Create a Python host file: `host.py`.</span></span>

<span data-ttu-id="feb26-191">Het hostbestand is als volgt samengesteld:</span><span class="sxs-lookup"><span data-stu-id="feb26-191">The host file is constructed as follows:</span></span> 
1. <span data-ttu-id="feb26-192">Eerst importeren we de `qsharp` module, die de module lader voor Q #-interoperabiliteit registreert.</span><span class="sxs-lookup"><span data-stu-id="feb26-192">First, we import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="feb26-193">Op deze manier kunnen Q # naam ruimten (zoals de `NamespaceQFT` in ons Q #-bestand gedefinieerde) worden weer gegeven als python-modules, van waaruit we de bewerkingen van q # kunnen importeren.</span><span class="sxs-lookup"><span data-stu-id="feb26-193">This allows Q# namespaces (e.g. the `NamespaceQFT` we defined in our Q# file) to appear as Python modules, from which we can import Q# operations.</span></span>
2. <span data-ttu-id="feb26-194">Importeer vervolgens de Q #-bewerkingen die in dit geval direct---worden aangeroepen `Perform3qubitQFT` .</span><span class="sxs-lookup"><span data-stu-id="feb26-194">Then, import the Q# operations which we will directly invoke---in this case, `Perform3qubitQFT`.</span></span>
    <span data-ttu-id="feb26-195">Het invoer punt hoeft alleen te worden geïmporteerd naar een Q #-programma (dat wil zeggen _geen_ bewerkingen zoals `H` en `R1` , die worden aangeroepen door andere Q #-bewerkingen, maar nooit door de klassieke host).</span><span class="sxs-lookup"><span data-stu-id="feb26-195">We need only import the entry point into a Q# program (i.e. _not_ operations like `H` and `R1`, which are called by other Q# operations but never by the classical host).</span></span>
3. <span data-ttu-id="feb26-196">Bij het simuleren van Q #-bewerkingen of-functies gebruikt u het formulier `<Q#callable>.simulate(<args>)` om ze op de doel computer uit te voeren `QuantumSimulator()` .</span><span class="sxs-lookup"><span data-stu-id="feb26-196">In simulating Q# operations or functions, use the form `<Q#callable>.simulate(<args>)` to run them on the `QuantumSimulator()` target machine.</span></span> 

> [!NOTE]
> <span data-ttu-id="feb26-197">Als we de bewerking willen aanroepen op een andere computer, bijvoorbeeld de `ResourceEstimator()` , zou u gewoon gebruiken `<Q#callable>.estimate_resources(<args>)` .</span><span class="sxs-lookup"><span data-stu-id="feb26-197">If we wanted to call the operation on a different machine, for example the `ResourceEstimator()`, we would simply use `<Q#callable>.estimate_resources(<args>)`.</span></span>
> <span data-ttu-id="feb26-198">Over het algemeen worden Q #-bewerkingen neutraal naar de machines waarop ze worden uitgevoerd, maar sommige functies, zoals `DumpMachine` mogelijk, kunnen zich anders gedragen.</span><span class="sxs-lookup"><span data-stu-id="feb26-198">In general, Q# operations are agnostic to the machines on which they're run, but some features such as `DumpMachine` may behave differently.</span></span>

4. <span data-ttu-id="feb26-199">Bij het uitvoeren van de simulatie retourneert de bewerkings aanroep waarden zoals gedefinieerd in het bestand Q #.</span><span class="sxs-lookup"><span data-stu-id="feb26-199">Upon performing the simulation, the operation call will return values as defined in the Q# file.</span></span>
    <span data-ttu-id="feb26-200">Er wordt op dit moment niets geretourneerd, maar er wordt later een voor beeld weer gegeven van het toewijzen en verwerken van deze waarden.</span><span class="sxs-lookup"><span data-stu-id="feb26-200">For now there is nothing returned, but later on we will see an example of assigning and processing these values.</span></span>
    <span data-ttu-id="feb26-201">Met de resulterende gegevens in onze handen en volledig klassiek kunnen we alles doen wat we graag doen.</span><span class="sxs-lookup"><span data-stu-id="feb26-201">With the resultant data in our hands and totally classical, we can do whatever we'd like with it.</span></span>

<span data-ttu-id="feb26-202">Het volledige `host.py` bestand moet dit zijn:</span><span class="sxs-lookup"><span data-stu-id="feb26-202">Your full `host.py` file should be this:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3qubitQFT

Perform3qubitQFT.simulate()
```

<span data-ttu-id="feb26-203">Voer het python-bestand uit en druk af in uw-console. Hieronder ziet u de `Message` onderstaande en- `DumpMachine` uitvoer.</span><span class="sxs-lookup"><span data-stu-id="feb26-203">Run the Python file, and printed in your console you should see the `Message` and `DumpMachine` outputs below.</span></span> 


#### <a name="c"></a>[<span data-ttu-id="feb26-204">C#</span><span class="sxs-lookup"><span data-stu-id="feb26-204">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="feb26-205">Volg de instructies in de [installatie handleiding](xref:microsoft.quantum.install.cs)om een C#-hostbestand te maken en de naam ervan te wijzigen in `host.cs` .</span><span class="sxs-lookup"><span data-stu-id="feb26-205">Following the same instructions as in the [install guide](xref:microsoft.quantum.install.cs), create a C# host file, and rename it to `host.cs`.</span></span>

<span data-ttu-id="feb26-206">De C#-host heeft vier onderdelen:</span><span class="sxs-lookup"><span data-stu-id="feb26-206">The C# host has four parts:</span></span>
1. <span data-ttu-id="feb26-207">Bouw een kwantumsimulator.</span><span class="sxs-lookup"><span data-stu-id="feb26-207">Construct a quantum simulator.</span></span>
    <span data-ttu-id="feb26-208">In de onderstaande code is dit de variabele `qsim` .</span><span class="sxs-lookup"><span data-stu-id="feb26-208">In the code below, this is the variable `qsim`.</span></span>
2. <span data-ttu-id="feb26-209">Bereken de argumenten die vereist zijn voor het kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="feb26-209">Compute any arguments required for the quantum algorithm.</span></span>
    <span data-ttu-id="feb26-210">Er zijn geen in dit voor beeld.</span><span class="sxs-lookup"><span data-stu-id="feb26-210">There are none in this example.</span></span>
3. <span data-ttu-id="feb26-211">Voer het kwantumalgoritme uit.</span><span class="sxs-lookup"><span data-stu-id="feb26-211">Run the quantum algorithm.</span></span> 
    <span data-ttu-id="feb26-212">Elke Q#-bewerking genereert een C#-klasse met dezelfde naam.</span><span class="sxs-lookup"><span data-stu-id="feb26-212">Each Q# operation generates a C# class with the same name.</span></span> 
    <span data-ttu-id="feb26-213">Deze klasse heeft een methode `Run` die de bewerking **asynchroon** uitvoert.</span><span class="sxs-lookup"><span data-stu-id="feb26-213">This class has a `Run` method that **asynchronously** executes the operation.</span></span>
    <span data-ttu-id="feb26-214">De uitvoering is asynchroon, omdat de uitvoering op feitelijke hardware asynchroon is.</span><span class="sxs-lookup"><span data-stu-id="feb26-214">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> 
    <span data-ttu-id="feb26-215">Omdat de `Run` methode asynchroon is, wordt de `Wait()` methode aangeroepen. Hiermee wordt de uitvoering geblokkeerd totdat de taak is voltooid en het resultaat synchroon wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="feb26-215">Because the `Run` method is asynchronous, we call the `Wait()` method; this blocks execution until the task completes and returns the result synchronously.</span></span> 
4. <span data-ttu-id="feb26-216">Het geretourneerde resultaat van de bewerking verwerken.</span><span class="sxs-lookup"><span data-stu-id="feb26-216">Process the returned result of the operation.</span></span>
    <span data-ttu-id="feb26-217">Voor nu retourneert de bewerking niets.</span><span class="sxs-lookup"><span data-stu-id="feb26-217">For now, the operation returns nothing.</span></span>


```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                Perform3QubitQFT.Run(qsim).Wait();
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}

```
<span data-ttu-id="feb26-218">Voer de toepassing uit en de uitvoer moet overeenkomen met die hieronder.</span><span class="sxs-lookup"><span data-stu-id="feb26-218">Run the application, and your output should match that below.</span></span>
<span data-ttu-id="feb26-219">Het programma wordt afgesloten nadat u op een toets hebt gedrukt.</span><span class="sxs-lookup"><span data-stu-id="feb26-219">The program will exit after you press a key.</span></span>
***

```Output
Initial state |000>:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
After:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
```

<span data-ttu-id="feb26-220">Wanneer de Full-State Simulator wordt aangeroepen, `DumpMachine()` biedt deze Multiple-representaties van de Wavefunction van de Quantum status.</span><span class="sxs-lookup"><span data-stu-id="feb26-220">When called on the full-state simulator, `DumpMachine()` provides these mutliple representations of the quantum state's wavefunction.</span></span> <span data-ttu-id="feb26-221">De mogelijke statussen van een $n $-Qubit-systeem kunnen worden voorgesteld door $2 ^ n $ Computation-basis statussen, elk met een bijbehorende complexe coëfficiënt (gewoon een amplitude en een fase).</span><span class="sxs-lookup"><span data-stu-id="feb26-221">The possible states of an $n$-qubit system can be represented by $2^n$ computational basis states, each with a corresponding complex coefficient (simply an amplitude and a phase).</span></span>
<span data-ttu-id="feb26-222">De reken kundige basis statussen komen overeen met alle mogelijke binaire teken reeksen van de lengte $n $---dat wil zeggen alle mogelijke combi Naties van Qubit Staten $ \ket {0} $ en $ \ket {1} $, waarbij elk binair cijfer overeenkomt met een afzonderlijke Qubit.</span><span class="sxs-lookup"><span data-stu-id="feb26-222">The computational basis states correspond to all the possible binary strings of length $n$---that is, all the possible combinations of qubit states $\ket{0}$ and $\ket{1}$, where each binary digit corresponds to an individual qubit.</span></span>

<span data-ttu-id="feb26-223">De eerste rij bevat een opmerking met de Id's van de bijbehorende qubits in hun significante volg orde.</span><span class="sxs-lookup"><span data-stu-id="feb26-223">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="feb26-224">Qubit is `2` de ' meest significante ' betekent dat u in de binaire weer gave van basis status vector $ \ket{i} $ de status Qubit `2` overeenkomt met het meest linkse cijfer.</span><span class="sxs-lookup"><span data-stu-id="feb26-224">Qubit `2` being the "most significant" simply means that in the binary representation of basis state vector $\ket{i}$, the state of qubit `2` corresponds to the left-most digit.</span></span> <span data-ttu-id="feb26-225">Bijvoorbeeld: $ \ket {6} = \ket {110} $ omvat qubits `2` en `1` beide in $ \ket {1} $ en Qubit `0` in $ \ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="feb26-225">For example, $\ket{6} = \ket{110}$ comprises qubits `2` and `1` both in $\ket{1}$ and qubit `0` in $\ket{0}$.</span></span>


<span data-ttu-id="feb26-226">De rest van de rijen beschrijven de waarschijnlijke amplitude van het meten van de basis status vector $ \ket{i} $ in zowel Cartesisch als polaire indeling.</span><span class="sxs-lookup"><span data-stu-id="feb26-226">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{i}$ in both Cartesian and polar formats.</span></span>
<span data-ttu-id="feb26-227">Gedetailleerd voor de eerste rij van de invoer status $ \ket {000} $:</span><span class="sxs-lookup"><span data-stu-id="feb26-227">In detail for the first row of our input state $\ket{000}$:</span></span>
* <span data-ttu-id="feb26-228">**`|0>:`** deze rij komt overeen met de verwerkings `0` status van de berekening (op voor hand dat onze initiële status post-Allocation $ \ket {000} $ is. dit wordt verwacht dat dit de enige status met een waarschijnlijkheids amplitude op dit punt is).</span><span class="sxs-lookup"><span data-stu-id="feb26-228">**`|0>:`** this row corresponds to the `0` computational basis state (given that our initial state post-allocation was $\ket{000}$, we would expect this to be the only state with probability amplitude at this point).</span></span>
* <span data-ttu-id="feb26-229">**`1.000000 +  0.000000 i`**: de waarschijnlijke amplitude in Cartesisch formaat.</span><span class="sxs-lookup"><span data-stu-id="feb26-229">**`1.000000 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="feb26-230">**` == `**: het `equal` teken scheidt beide equivalente verklaringen.</span><span class="sxs-lookup"><span data-stu-id="feb26-230">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="feb26-231">**`********************`**: Een grafische weer gave van de omvang, het aantal `*` is evenredig met de kans dat deze status vector wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="feb26-231">**`********************`**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span> 
* <span data-ttu-id="feb26-232">**`[ 1.000000 ]`**: de numerieke waarde van de grootte</span><span class="sxs-lookup"><span data-stu-id="feb26-232">**`[ 1.000000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="feb26-233">**`    ---`**: Een grafische weer gave van de fase van de amplitude.</span><span class="sxs-lookup"><span data-stu-id="feb26-233">**`    ---`**: A graphical representation of the amplitude's phase.</span></span>
* <span data-ttu-id="feb26-234">**`[ 0.0000 rad ]`**: de numerieke waarde van de fase (in radialen).</span><span class="sxs-lookup"><span data-stu-id="feb26-234">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="feb26-235">Zowel de grootte als de fase worden weer gegeven met een grafische weer gave.</span><span class="sxs-lookup"><span data-stu-id="feb26-235">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="feb26-236">De weer gave met de grootte is eenvoudig: er wordt een balk van weer gegeven `*` , en hoe hoger de kans, hoe groter de balk is.</span><span class="sxs-lookup"><span data-stu-id="feb26-236">The magnitude representation is straightforward: it shows a bar of `*`, and the higher the probability, the larger the bar will be.</span></span> <span data-ttu-id="feb26-237">Voor de-fase raadpleegt u de sectie DumpMachine [hier](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions) voor de mogelijke symbool representaties op basis van de bereik hoek.</span><span class="sxs-lookup"><span data-stu-id="feb26-237">For the phase, see the DumpMachine section [here](xref:microsoft.quantum.techniques.testing-and-debugging#dump-functions) for the possible symbol representations based on angle ranges.</span></span>


<span data-ttu-id="feb26-238">De gedrukte uitvoer illustreert dus dat onze geprogrammeerde Gates onze staat hebben getransformeerd van</span><span class="sxs-lookup"><span data-stu-id="feb26-238">So, the printed output is illustrating that our programmed gates transformed our state from</span></span>

<span data-ttu-id="feb26-239">$ $ \ket{\psi} \_ {begin} = \ket {000} $ $</span><span class="sxs-lookup"><span data-stu-id="feb26-239">$$ \ket{\psi}\_{initial} = \ket{000} $$</span></span>

<span data-ttu-id="feb26-240">tot</span><span class="sxs-lookup"><span data-stu-id="feb26-240">to</span></span> 

<span data-ttu-id="feb26-241">$ $ \begin{align} \ket{\psi} \_ {Final} &= \frac {1} {\sqrt {8} } \left (\ket {000} + \ket {001} + \ket {010} + \ket {011} + \ket {100} + \ket {101} + \ket {110} + \ket {111} \right) \\ \\ &= \frac {1} {\sqrt{2 ^ n}} \sum \_ {j = 0} ^ {2 ^ n-1} \ket{j}, \end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="feb26-241">$$ \begin{align} \ket{\psi}\_{final} &= \frac{1}{\sqrt{8}} \left( \ket{000} + \ket{001} + \ket{010} + \ket{011} + \ket{100} + \ket{101} + \ket{110} + \ket{111}  \right) \\\\ &= \frac{1}{\sqrt{2^n}}\sum\_{j=0}^{2^n-1} \ket{j}, \end{align} $$</span></span>

<span data-ttu-id="feb26-242">Dit is precies het gedrag van de 3-qubite Fourier-trans formatie.</span><span class="sxs-lookup"><span data-stu-id="feb26-242">which is precisely the behavior of the 3-qubit Fourier transform.</span></span> 

<span data-ttu-id="feb26-243">Als u wilt weten hoe andere invoer Staten worden beïnvloed, raden we u aan om te spelen met het Toep assen van Qubit-bewerkingen vóór de trans formatie.</span><span class="sxs-lookup"><span data-stu-id="feb26-243">If you are curious about how other input states are affected, we encourage you to play around with applying qubit operations before the transform.</span></span>

## <a name="adding-measurements"></a><span data-ttu-id="feb26-244">Metingen toevoegen</span><span class="sxs-lookup"><span data-stu-id="feb26-244">Adding measurements</span></span>

<span data-ttu-id="feb26-245">Helaas vertelt een hoek steen van Quantum monteurs dat een echt Quantum systeem een dergelijke functie niet kan hebben `DumpMachine` .</span><span class="sxs-lookup"><span data-stu-id="feb26-245">Unfortunately, a cornerstone of quantum mechanics tells us that a real quantum system cannot have such a `DumpMachine` function.</span></span> <span data-ttu-id="feb26-246">In plaats daarvan worden gegevens geëxtraheerd door middel van metingen, wat in het algemeen niet alleen de volledige Quantum status biedt, maar kan het systeem zelf ook drastisch wijzigen.</span><span class="sxs-lookup"><span data-stu-id="feb26-246">Instead, we're forced to extract information through measurements, which in general not only fail to provide us the full quantum state, but can also drastically alter the system itself.</span></span>
<span data-ttu-id="feb26-247">Er zijn veel sorteringen van Quantum metingen, maar we richten ons op het meest Basic: uitstekende metingen op één qubits.</span><span class="sxs-lookup"><span data-stu-id="feb26-247">There are many sorts of quantum measurements, but we will focus on the most basic: projective measurements on single qubits.</span></span>
<span data-ttu-id="feb26-248">Bij meting in een gegeven (bijvoorbeeld de berekening van de verrekenings wijze $ \{ \ket {0} , \ket {1} \} $), wordt de status van het Qubit geprojecteerd op basis van de geschatte status, hetgeen wordt gemeten---, waardoor een wille keurige positie tussen de twee wordt vernietigd.</span><span class="sxs-lookup"><span data-stu-id="feb26-248">Upon measurement in a given basis (e.g. the computational basis $ \{ \ket{0}, \ket{1} \} $), the qubit state is projected onto whichever basis state was measured---hence destroying any superposition between the two.</span></span>

<span data-ttu-id="feb26-249">Voor het implementeren van metingen binnen een Q #-programma gebruiken we de `M` bewerking (uit `Microsoft.Quantum.Intrinsic` ), die een `Result` type retourneert.</span><span class="sxs-lookup"><span data-stu-id="feb26-249">To implement measurements within a Q# program, we use the `M` operation (from `Microsoft.Quantum.Intrinsic`), which returns a `Result` type.</span></span>

<span data-ttu-id="feb26-250">Eerst wijzigen we onze `Perform3QubitQFT` bewerking om een matrix met meet resultaten te retour neren, `Result[]` in plaats van `Unit` .</span><span class="sxs-lookup"><span data-stu-id="feb26-250">First, we modify our `Perform3QubitQFT` operation to return an array of measurement results, `Result[]`, instead of `Unit`.</span></span>

```qsharp
    operation Perform3QubitQFT() : Result[] {
```

#### <a name="define-and-initialize-result-array"></a><span data-ttu-id="feb26-251">Matrix definiëren en initialiseren `Result[]`</span><span class="sxs-lookup"><span data-stu-id="feb26-251">Define and initialize `Result[]` array</span></span>

<span data-ttu-id="feb26-252">Voordat u qubits (bijvoorbeeld vóór de instructie) toewijst `using` , declareren en verbindt u deze lengte-3 matrix (één `Result` voor elke qubit):</span><span class="sxs-lookup"><span data-stu-id="feb26-252">Before even allocating qubits (i.e. before the `using` statement), we declare and bind this length-3 array (one `Result` for each qubit):</span></span> 

```qsharp
        mutable resultArray = new Result[3];
```

<span data-ttu-id="feb26-253">`mutable`Met het tref woord `resultArray` wordt de variabele naar een later tijdstip in de code---afhankelijk van het toevoegen van onze meet resultaten.</span><span class="sxs-lookup"><span data-stu-id="feb26-253">The `mutable` keyword prefacing `resultArray` allows the variable to be rebound later in the code---for example, when adding our measurement results.</span></span>

#### <a name="perform-measurements-in-a-for-loop-and-add-results-to-array"></a><span data-ttu-id="feb26-254">Metingen uitvoeren in een `for` lus en resultaten toevoegen aan een matrix</span><span class="sxs-lookup"><span data-stu-id="feb26-254">Perform measurements in a `for` loop and add results to array</span></span>

<span data-ttu-id="feb26-255">Na de Fourier-transformatie bewerkingen binnen het `using` blok voert u de volgende code in:</span><span class="sxs-lookup"><span data-stu-id="feb26-255">After the Fourier transform operations inside the `using` block, insert the following code:</span></span>

```qsharp
            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }
```
<span data-ttu-id="feb26-256">De [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) functie die wordt aangeroepen in een matrix (bijvoorbeeld onze matrix van qubits `qs` ) retourneert een bereik over de indices van de matrix.</span><span class="sxs-lookup"><span data-stu-id="feb26-256">The [`IndexRange`](xref:microsoft.quantum.arrays.indexrange) function called on an array (e.g. our array of qubits, `qs`) returns a range over the indices of the array.</span></span> <span data-ttu-id="feb26-257">Hier gebruiken we dit in onze `for` lus om elke qubit achtereenvolgens te meten met behulp van de- `M(qs[i])` instructie.</span><span class="sxs-lookup"><span data-stu-id="feb26-257">Here, we use it in our `for` loop to sequentially measure each qubit using the `M(qs[i])` statement.</span></span>
<span data-ttu-id="feb26-258">Elk gemeten `Result` type ( `Zero` of `One` ) wordt vervolgens toegevoegd aan de bijbehorende index positie in `resultArray` met een update-en-reassign-instructie.</span><span class="sxs-lookup"><span data-stu-id="feb26-258">Each measured `Result` type (either `Zero` or `One`) is then added to the corresponding index position in `resultArray` with an update-and-reassign statement.</span></span>

> [!NOTE]
> <span data-ttu-id="feb26-259">De syntaxis van deze instructie is uniek voor Q #, maar komt overeen met de nieuwe hertoewijzing van een variabele `resultArray[i] <- M(qs[i])` die in andere talen wordt weer gegeven, zoals F # en R.</span><span class="sxs-lookup"><span data-stu-id="feb26-259">The syntax of this statement is unique to Q#, but corresponds to the similar variable reassignment `resultArray[i] <- M(qs[i])` seen in other languages such as F# and R.</span></span>

<span data-ttu-id="feb26-260">Het sleutel woord `set` wordt altijd gebruikt voor het opnieuw toewijzen van variabelen die zijn gekoppeld met `mutable` .</span><span class="sxs-lookup"><span data-stu-id="feb26-260">The keyword `set` is always used to reassign variables bound using `mutable`.</span></span>

#### <a name="return-resultarray"></a><span data-ttu-id="feb26-261">Opvragen`resultArray`</span><span class="sxs-lookup"><span data-stu-id="feb26-261">Return `resultArray`</span></span>

<span data-ttu-id="feb26-262">Met alle drie qubits gemeten en de resultaten die worden toegevoegd aan `resultArray` , kunnen we de qubits als voorheen opnieuw instellen en de toewijzing ervan ongedaan maken.</span><span class="sxs-lookup"><span data-stu-id="feb26-262">With all three qubits measured and the results added to `resultArray`, we are safe to reset and deallocate the qubits as before.</span></span>
<span data-ttu-id="feb26-263">Invoegen nadat de `using` blok kering is gesloten</span><span class="sxs-lookup"><span data-stu-id="feb26-263">After the `using` block's close, insert</span></span>

```qsharp
        return resultArray;
```
<span data-ttu-id="feb26-264">uiteindelijk de uitvoer van de bewerking te retour neren.</span><span class="sxs-lookup"><span data-stu-id="feb26-264">to ultimately return the output of our operation.</span></span> 

### <a name="understanding-the-effects-of-measurement"></a><span data-ttu-id="feb26-265">Meer informatie over de gevolgen van meting</span><span class="sxs-lookup"><span data-stu-id="feb26-265">Understanding the effects of measurement</span></span>

<span data-ttu-id="feb26-266">Laten we de plaatsing van onze `DumpMachine` functies wijzigen zodat de status wordt uitgevoerd vóór en na de metingen.</span><span class="sxs-lookup"><span data-stu-id="feb26-266">Let's change the placement of our `DumpMachine` functions to output the state before and after the measurements.</span></span>
<span data-ttu-id="feb26-267">De uiteindelijke bewerkings code moet er als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="feb26-267">The final operation code should look like:</span></span> 

```qsharp
    operation Perform3QubitQFT() : Result[] {

        mutable resultArray = new Result[3];

        using (qs = Qubit[3]) {

            //QFT:
            //first qubit:
            H(qs[0]);
            Controlled R1([qs[1]], (PI()/2.0, qs[0]));
            Controlled R1([qs[2]], (PI()/4.0, qs[0]));

            //second qubit:
            H(qs[1]);
            Controlled R1([qs[2]], (PI()/2.0, qs[1]));

            //third qubit:
            H(qs[2]);

            SWAP(qs[2], qs[0]);

            Message("Before measurement: ");
            DumpMachine();

            for(i in IndexRange(qs)) {
                set resultArray w/= i <- M(qs[i]);
            }

            Message("After measurement: ");
            DumpMachine();

            ResetAll(qs);
        }
        return resultArray;
    }
}
```

<span data-ttu-id="feb26-268">Als u vanaf de opdracht regel werkt, wordt de geretourneerde matrix gewoon direct naar de console afgedrukt aan het einde van de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="feb26-268">If you are working from the command line, the returned array will simply be printed directly to the console at the end of the execution.</span></span>
<span data-ttu-id="feb26-269">Werk anders uw host-programma bij om de geretourneerde matrix te verwerken.</span><span class="sxs-lookup"><span data-stu-id="feb26-269">Otherwise, update your host program to process the returned array.</span></span>

#### <a name="command-line"></a>[<span data-ttu-id="feb26-270">Opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="feb26-270">Command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="feb26-271">Om meer te weten te komen over de geretourneerde matrix die in de-console zal worden afgedrukt, kunnen we nog een nieuwe `Message` in het Q #-bestand toevoegen net vóór de `return` instructie:</span><span class="sxs-lookup"><span data-stu-id="feb26-271">To have more understanding of the returned array which will be printed in the console, we can add another `Message` in the Q# file just before the `return` statement:</span></span>

```qsharp
        Message("Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
        return resultArray;
```

<span data-ttu-id="feb26-272">Voer het project uit en de uitvoer moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="feb26-272">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]
```

#### <a name="python"></a>[<span data-ttu-id="feb26-273">Python</span><span class="sxs-lookup"><span data-stu-id="feb26-273">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="feb26-274">Werk uw python-programma bij naar het volgende:</span><span class="sxs-lookup"><span data-stu-id="feb26-274">Update your Python program to the following:</span></span>

```python
import qsharp
from NamespaceQFT import Perform3QubitQFT

measurementResult = Perform3QubitQFT.simulate()
print("\n")
print("Measured post-QFT state: [qubit0, qubit1, qubit2]")
print(measurementResult)

# reversing order to show corresponding basis state in binary form
binaryCompBasisState = ""
for i in measurementResult:
    binaryCompBasisState = str(i) + binaryCompBasisState
print("Corresponding basis state in binary:")
print("|" + binaryCompBasisState + ">")
```

<span data-ttu-id="feb26-275">Voer het bestand uit en de uitvoer moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="feb26-275">Run the file, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[1, 1, 0]

Corresponding basis state in binary:
|011>
```

#### <a name="c"></a>[<span data-ttu-id="feb26-276">C#</span><span class="sxs-lookup"><span data-stu-id="feb26-276">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="feb26-277">Nu de bewerking een resultaat retourneert, vervangt u de methode aanroep door `Wait()` de eigenschap op te halen `Result` .</span><span class="sxs-lookup"><span data-stu-id="feb26-277">Now that our operation is returning a result, replace the method call `Wait()` with fetching the `Result` property.</span></span> <span data-ttu-id="feb26-278">Dit heeft nog steeds hetzelfde Synchronicity dat eerder is besproken en we kunnen deze waarde rechtstreeks aan de variabele binden `measurementResult` .</span><span class="sxs-lookup"><span data-stu-id="feb26-278">This still accomplishes the same synchronicity discussed earlier, and we can directly bind this value to the variable `measurementResult`.</span></span>

```csharp
using System;

using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace NamespaceQFT
{
    class Driver
    {
        static void Main(string[] args)
        {
            using (var qsim = new QuantumSimulator())
            {
                var measurementResult = Perform3QubitQFT.Run(qsim).Result;
                System.Console.WriteLine(
                    $"Post-QFT measurement results [qubit0, qubit1, qubit2]: ");
                System.Console.WriteLine(
                    measurementResult);

                // reversing order to show corresponding basis state in binary form
                string binaryCompBasisState = String.Empty;

                foreach (Result i in measurementResult)
                {
                    string iString = i.ToString();
                    binaryCompBasisState = iString + binaryCompBasisState;
                }
                binaryCompBasisState = "|" + binaryCompBasisState + ">";
                System.Console.WriteLine(
                    $"Corresponding basis state in binary:");
                System.Console.WriteLine(
                    binaryCompBasisState);
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="feb26-279">Voer het project uit en de uitvoer moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="feb26-279">Run the project, and your output should look similar to the following:</span></span>

```Output
Before measurement: 
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|1>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|2>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|3>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|4>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|5>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|6>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
|7>:     0.353553 +  0.000000 i  ==     ***                  [ 0.125000 ]     --- [  0.00000 rad ]
After measurement:
# wave function for qubits with ids (least to most significant): 0;1;2
|0>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|1>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|2>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|3>:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
|4>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|5>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|6>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]
|7>:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]

Post-QFT measurement results [qubit0, qubit1, qubit2]: 
[One,One,Zero]

Corresponding basis state in binary:
|ZeroOneOne>

Press any key to continue...
```
***

<span data-ttu-id="feb26-280">In deze uitvoer ziet u een aantal verschillende dingen:</span><span class="sxs-lookup"><span data-stu-id="feb26-280">This output illustrates a few different things:</span></span>
1. <span data-ttu-id="feb26-281">Als vergelijking van het geretourneerde resultaat naar de voor meting `DumpMachine` , illustreert het duidelijk _niet_ de post-QFT-positie boven basis status.</span><span class="sxs-lookup"><span data-stu-id="feb26-281">Comparing the returned result to the pre-measurement `DumpMachine`, it clearly does _not_ illustrate the post-QFT superposition over basis states.</span></span>
    <span data-ttu-id="feb26-282">Een meting retourneert slechts één basis status, met een waarschijnlijkheid die is bepaald door de amplitude van die staat in de Wavefunction van het systeem.</span><span class="sxs-lookup"><span data-stu-id="feb26-282">A measurement only returns a single basis state, with a probability determined by the amplitude of that state in the system's wavefunction.</span></span>
2. <span data-ttu-id="feb26-283">Vanuit de post-meting `DumpMachine` zien we dat de status zelf wordt _gewijzigd_ en dat deze wordt geprojecteerd van de oorspronkelijke superpositie in de basis status en de enkelvoudige basis staat die overeenkomt met de gemeten waarde.</span><span class="sxs-lookup"><span data-stu-id="feb26-283">From the post-measurement `DumpMachine`, we see that measurement _changes_ the state itself, projecting it from the initial superposition over basis states to the single basis state that corresponds to the measured value.</span></span>

<span data-ttu-id="feb26-284">Als we deze bewerking meermaals moeten herhalen, zien we dat de resultaat statistieken beginnen met de gelijkmatig gewogen superpositie van de post-QFT-status, die resulteert in een wille keurig resultaat op elke afbeelding.</span><span class="sxs-lookup"><span data-stu-id="feb26-284">If we were to repeat this operation many times, we would see the result statistics begin to illustrate the equally weighted superposition of the post-QFT state that gives rise to a random result on each shot.</span></span>
<span data-ttu-id="feb26-285">Afgezien van inefficiënte en nog niet-perfecte, zou dit _echter_toch alleen de relatieve amplitudes van de basis status, niet de relatieve fasen ertussen, reproduceren.</span><span class="sxs-lookup"><span data-stu-id="feb26-285">_However_, besides being inefficient and still imperfect, this would nevertheless only reproduce the relative amplitudes of the basis states, not the relative phases between them.</span></span>
<span data-ttu-id="feb26-286">In dit voor beeld is dit geen probleem, maar we zien dat relatieve fasen worden weer gegeven als een complexere invoer wordt gegeven aan de QFT dan $ \ket {000} $.</span><span class="sxs-lookup"><span data-stu-id="feb26-286">The latter is not an issue in this example, but we would see relative phases appear if given a more complex input to the QFT than $\ket{000}$.</span></span>

#### <a name="partial-measurements"></a><span data-ttu-id="feb26-287">Gedeeltelijke metingen</span><span class="sxs-lookup"><span data-stu-id="feb26-287">Partial measurements</span></span> 
<span data-ttu-id="feb26-288">Als u wilt weten hoe alleen bepaalde qubits van de kassa van invloed kunnen zijn op de status van het systeem, voegt u het volgende toe in de `for` lus, na de meet lijn:</span><span class="sxs-lookup"><span data-stu-id="feb26-288">To explore how measuring only some qubits of the register can affect the system's state, try adding the following inside the `for` loop, after the measurement line:</span></span>
```qsharp
                let iString = IntAsString(i);
                Message("After measurement of qubit " + iString + ":");
                DumpMachine();
```

<span data-ttu-id="feb26-289">Houd er rekening mee dat `IntAsString` u toegang hebt tot de functie die u moet toevoegen</span><span class="sxs-lookup"><span data-stu-id="feb26-289">Note that to access the `IntAsString` function you will have to add</span></span> 
```qsharp
    open Microsoft.Quantum.Convert;
```
<span data-ttu-id="feb26-290">met de rest van de naam ruimte- `open` instructies.</span><span class="sxs-lookup"><span data-stu-id="feb26-290">with the rest of the namespace `open` statements.</span></span>

<span data-ttu-id="feb26-291">In de resulterende uitvoer ziet u de geleidelijke projectie in subruimten wanneer elke qubit wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="feb26-291">In the resulting output, you will see the gradual projection into subspaces as each qubit is measured.</span></span>


## <a name="use-the-q-libraries"></a><span data-ttu-id="feb26-292">De Q #-bibliotheken gebruiken</span><span class="sxs-lookup"><span data-stu-id="feb26-292">Use the Q# libraries</span></span>
<span data-ttu-id="feb26-293">Zoals we vermeld hebben in de inleiding, is veel Q # de kracht van de stroom, zodat u de zorgen over kunt samen stellen voor het afhandelen van afzonderlijke qubits.</span><span class="sxs-lookup"><span data-stu-id="feb26-293">As we mentioned in the introduction, much of Q#'s power rests in the fact that it allows you to abstract-away the worries of dealing with individual qubits.</span></span>
<span data-ttu-id="feb26-294">Als u de juiste, toepasselijke Quantum Program ma's wilt ontwikkelen, moet u er wel voor zorgen dat een bewerking wordt uitgevoerd `H` vóór of na een bepaalde rotatie.</span><span class="sxs-lookup"><span data-stu-id="feb26-294">Indeed, if you want to develop full-scale, applicable quantum programs, worrying about whether an `H` operation goes before or after a particular rotation would only slow you down.</span></span> 

<span data-ttu-id="feb26-295">De Q #-bibliotheken bevatten de [QFT](xref:microsoft.quantum.canon.qft) -bewerking, die u gewoon kunt uitvoeren en Toep assen voor een wille keurig aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="feb26-295">The Q# libraries contain the [QFT](xref:microsoft.quantum.canon.qft) operation, which you can simply take and apply for any number of qubits.</span></span>
<span data-ttu-id="feb26-296">Als u een try wilt opgeven, definieert u een nieuwe bewerking in uw Q #-bestand met dezelfde inhoud `Perform3QubitQFT` , maar met alles van de eerste `H` tot de `SWAP` vervangen door twee eenvoudige lijnen:</span><span class="sxs-lookup"><span data-stu-id="feb26-296">To give it a try, define a new operation in your Q# file which has the same contents of `Perform3QubitQFT`, but with everything from the first `H` to the `SWAP` replaced by two easy lines:</span></span>
```qsharp
            let register = BigEndian(qs);    //from Microsoft.Quantum.Arithmetic
            QFT(register);                   //from Microsoft.Quantum.Canon
```
<span data-ttu-id="feb26-297">De eerste regel maakt simpelweg een [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expressie van de toegewezen matrix van qubits, `qs` die de [QFT](xref:microsoft.quantum.canon.qft) -bewerking als argument gebruikt.</span><span class="sxs-lookup"><span data-stu-id="feb26-297">The first line simply creates a [`BigEndian`](xref:microsoft.quantum.arithmetic.bigendian) expression of the allocated array of qubits, `qs`, which is what the [QFT](xref:microsoft.quantum.canon.qft) operation takes as an argument.</span></span>
<span data-ttu-id="feb26-298">Dit komt overeen met de index volgorde van de qubits in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="feb26-298">This corresponds to index ordering of the qubits in the register.</span></span>

<span data-ttu-id="feb26-299">Als u toegang wilt hebben tot deze bewerkingen, voegt u `open` instructies toe voor de bijbehorende naam ruimten aan het begin van het Q #-bestand:</span><span class="sxs-lookup"><span data-stu-id="feb26-299">To have access to these operations, add `open` statements for their respective namespaces at the beginning of the Q# file:</span></span>
```qsharp
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Arithmetic;
```

<span data-ttu-id="feb26-300">Pas nu uw hostprogramma aan om de naam van uw nieuwe bewerking aan te roepen (bijvoorbeeld `PerformIntrinsicQFT` ) en geef het een uitproberen.</span><span class="sxs-lookup"><span data-stu-id="feb26-300">Now, adjust your host program to call the name of your new operation (e.g. `PerformIntrinsicQFT`), and give it a whirl.</span></span>

<span data-ttu-id="feb26-301">Als u het werkelijke voor deel van het gebruik van de Q #-bibliotheek bewerkingen wilt zien, wijzigt u het aantal qubits in iets anders dan `3` :</span><span class="sxs-lookup"><span data-stu-id="feb26-301">To see the real benefit of using the Q# library operations, change the number of qubits to something other than `3`:</span></span>
```qsharp
        mutable resultArray = new Result[4]; 

        using (qs = Qubit[4]) {
            //...
        }
```
<span data-ttu-id="feb26-302">U kunt de juiste QFT voor elk gegeven aantal qubits Toep assen, zonder dat u zich zorgen hoeft te maken over de rommel van nieuwe `H` bewerkingen en draaiingen op elke qubit.</span><span class="sxs-lookup"><span data-stu-id="feb26-302">You can thus apply the proper QFT for any given number of qubits, without having to worry about the mess of new `H` operations and rotations on each qubit.</span></span>

<span data-ttu-id="feb26-303">Houd er rekening mee dat de Quantum Simulator meer tijd in beslag neemt, omdat u het aantal qubits nauw keuriger kunt verg Roten---om precies te kijken wat er gebeurt.</span><span class="sxs-lookup"><span data-stu-id="feb26-303">Note that the quantum simulator takes exponentially more time to run as you increase the number of qubits---precisely why we look forward to real quantum hardware!</span></span>













