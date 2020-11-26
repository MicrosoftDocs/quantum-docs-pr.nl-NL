---
title: Manieren om een programma uit te voeren Q#
description: Overzicht van de verschillende manieren om Program ma's uit te voeren Q# . Vanaf de opdracht prompt, Q# Jupyter-notebooks en klassieke host-Program ma's in Python of een .net-taal.
author: gillenhaalb
ms.author: a-gibec
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 2c5bdebc826bb85f6d7e0ade6232e15e29e8fb19
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231686"
---
# <a name="ways-to-run-a-no-locq-program"></a><span data-ttu-id="58f5c-104">Manieren om een programma uit te voeren Q#</span><span class="sxs-lookup"><span data-stu-id="58f5c-104">Ways to run a Q# program</span></span>

<span data-ttu-id="58f5c-105">Een van de grootste sterke punten van de Quantum Development Kit is de flexibiliteit tussen platforms en ontwikkel omgevingen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="58f5c-106">Dit betekent echter ook dat nieuwe Q# gebruikers zichzelf kunnen vinden of worden overspoeld door de talloze opties die in de [installatie handleiding](xref:microsoft.quantum.install)worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="58f5c-106">However, this also means that new Q# users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="58f5c-107">Op deze pagina wordt uitgelegd wat er gebeurt wanneer een Q# programma wordt uitgevoerd en kunt u de verschillende manieren vergelijken waarop gebruikers dit kunnen doen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-107">On this page, we explain what happens when a Q# program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="58f5c-108">Een primair onderscheid is dat Q# kan worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="58f5c-108">A primary distinction is that Q# can be run:</span></span>
- <span data-ttu-id="58f5c-109">als zelfstandige toepassing, waarbij de Q# enige taal betrokken is en het programma rechtstreeks wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-109">as a standalone application, where Q# is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="58f5c-110">In deze categorie vallen twee methoden daad werkelijk:</span><span class="sxs-lookup"><span data-stu-id="58f5c-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="58f5c-111">de opdracht regel interface</span><span class="sxs-lookup"><span data-stu-id="58f5c-111">the command-line interface</span></span>
  - <span data-ttu-id="58f5c-112">Q# Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="58f5c-112">Q# Jupyter Notebooks</span></span>
- <span data-ttu-id="58f5c-113">met een extra *hostprogramma*, geschreven in Python of een .net-taal (bijvoorbeeld C# of F #), die vervolgens het programma aanroept en de geretourneerde resultaten verder kan verwerken.</span><span class="sxs-lookup"><span data-stu-id="58f5c-113">with an additional *host program*, written in Python or a .NET language (for example, C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="58f5c-114">Voor een beter begrip van deze processen en hun verschillen, kunt u een eenvoudig Q# programma overwegen en de manieren vergelijken waarop het kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-114">To best understand these processes and their differences, we consider a simple Q# program and compare the ways it can be run.</span></span>

## <a name="basic-no-locq-program"></a><span data-ttu-id="58f5c-115">Basic- Q# programma</span><span class="sxs-lookup"><span data-stu-id="58f5c-115">Basic Q# program</span></span>

<span data-ttu-id="58f5c-116">Een basis Quantum programma kan bestaan uit het voorbereiden van een Qubit in een gelijke superpositie van Staten $ \ket {0} $ en $ \ket {1} $, het meten ervan en het retour neren van het resultaat, dat wille keurig een van beide statussen met een gelijke kans is.</span><span class="sxs-lookup"><span data-stu-id="58f5c-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="58f5c-117">Dit proces is inderdaad de kern van de versnelde Generator van de [Quantum wille keurige getallen](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="58f5c-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="58f5c-118">In Q# wordt dit uitgevoerd met de volgende code:</span><span class="sxs-lookup"><span data-stu-id="58f5c-118">In Q#, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="58f5c-119">Deze code kan echter alleen worden uitgevoerd door Q# .</span><span class="sxs-lookup"><span data-stu-id="58f5c-119">However, this code alone can't be run by Q#.</span></span>
<span data-ttu-id="58f5c-120">Hiervoor moet de hoofd tekst van een [bewerking](xref:microsoft.quantum.qsharp.operationsandfunctions)worden ingesteld, die vervolgens wordt uitgevoerd wanneer---rechtstreeks of door een andere bewerking wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.qsharp.operationsandfunctions), which is then run when called---either directly or by another operation.</span></span> <span data-ttu-id="58f5c-121">Daarom kunt u een bewerking van het volgende formulier schrijven:</span><span class="sxs-lookup"><span data-stu-id="58f5c-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="58f5c-122">U hebt een bewerking gedefinieerd, `MeasureSuperposition` die geen invoer heeft en een waarde van het type [resultaat](xref:microsoft.quantum.qsharp.typesystem-index#available-types)retourneert.</span><span class="sxs-lookup"><span data-stu-id="58f5c-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.qsharp.typesystem-index#available-types).</span></span>

<span data-ttu-id="58f5c-123">Naast bewerkingen Q# kan ook deterministische berekeningen in functies worden ingekapseld.</span><span class="sxs-lookup"><span data-stu-id="58f5c-123">In addition to operations, Q# also allows to encapsulate deterministic computations into functions.</span></span> <span data-ttu-id="58f5c-124">Afgezien van de determinism-garantie dat impliceert dat berekeningen die op qubits handelen, moeten worden ingekapseld in bewerkingen in plaats van functies, is er weinig verschil tussen bewerkingen en functie.</span><span class="sxs-lookup"><span data-stu-id="58f5c-124">Aside from the determinism guarantee that implies that computations that act on qubits need to be encapsulated into operations rather than functions, there is little difference between operations and function.</span></span> <span data-ttu-id="58f5c-125">We verwijzen ernaar gezamenlijk als *callables*.</span><span class="sxs-lookup"><span data-stu-id="58f5c-125">We refer to them collectively as *callables*.</span></span>

### <a name="callable-defined-in-a-no-locq-file"></a><span data-ttu-id="58f5c-126">Aanroepable gedefinieerd in een Q# bestand</span><span class="sxs-lookup"><span data-stu-id="58f5c-126">Callable defined in a Q# file</span></span>

<span data-ttu-id="58f5c-127">De aanroep zou precies worden aangeroepen en worden uitgevoerd door Q# .</span><span class="sxs-lookup"><span data-stu-id="58f5c-127">The callable is precisely what's called and run by Q#.</span></span>
<span data-ttu-id="58f5c-128">Er zijn echter enkele extra toevoegingen vereist om een volledig bestand te vormen `*.qs` Q# .</span><span class="sxs-lookup"><span data-stu-id="58f5c-128">However, it requires a few more additions to comprise a full `*.qs` Q# file.</span></span>

<span data-ttu-id="58f5c-129">Alle Q# typen en callables (zowel die u hebt gedefinieerd als de ingebouwde taal) worden gedefinieerd in *naam ruimten*, die elke volledige naam geven waarnaar vervolgens kan worden verwezen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-129">All Q# types and callables (both those you define and those intrinsic to the language) are defined within *namespaces*, which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="58f5c-130">De [`H`](xref:Microsoft.Quantum.Intrinsic.H) bewerkingen en zijn bijvoorbeeld te [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) vinden in de [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) naam ruimten en (onderdeel van de [ Q# standaard bibliotheken](xref:microsoft.quantum.libraries.standard.intro)).</span><span class="sxs-lookup"><span data-stu-id="58f5c-130">For example, the [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) and [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) namespaces (part of the [Q# Standard Libraries](xref:microsoft.quantum.libraries.standard.intro)).</span></span>
<span data-ttu-id="58f5c-131">Zo kunnen ze altijd worden aangeroepen via hun *volledige* naam `Microsoft.Quantum.Intrinsic.H(<qubit>)` en `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` , maar dit wordt altijd wel tot zeer ruime code.</span><span class="sxs-lookup"><span data-stu-id="58f5c-131">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="58f5c-132">In plaats daarvan `open` kunnen met behulp van de instructies callables worden gerefereerd aan een beknoptere steno, zoals in de bovenstaande hoofd tekst is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-132">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="58f5c-133">Het volledige Q# bestand met onze bewerking zou daarom bestaan uit het definiëren van onze eigen naam ruimte, het openen van de naam ruimten voor de callables die door onze bewerking worden gebruikt, en de bewerking:</span><span class="sxs-lookup"><span data-stu-id="58f5c-133">The full Q# file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

> [!NOTE]
> <span data-ttu-id="58f5c-134">Naam ruimten kunnen ook worden *gealiasd* wanneer deze worden geopend. Dit kan handig zijn als er sprake is van aanroep bare/type namen in twee naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="58f5c-134">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="58f5c-135">We kunnen bijvoorbeeld in plaats daarvan `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` hierboven gebruiken en vervolgens aanroepen `H` via `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-135">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="58f5c-136">Een uitzonde ring op dit is de [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) naam ruimte, die altijd automatisch wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="58f5c-136">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="58f5c-137">Daarom kan callables bijvoorbeeld [`Length`](xref:Microsoft.Quantum.Core.Length) altijd rechtstreeks worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="58f5c-137">Therefore, callables like [`Length`](xref:Microsoft.Quantum.Core.Length) can always be used directly.</span></span>

### <a name="running-on-target-machines"></a><span data-ttu-id="58f5c-138">Uitvoeren op doel computers</span><span class="sxs-lookup"><span data-stu-id="58f5c-138">Running on target machines</span></span>

<span data-ttu-id="58f5c-139">Het algemene model voor het uitvoeren van een Q# programma wordt nu duidelijk.</span><span class="sxs-lookup"><span data-stu-id="58f5c-139">Now the general run model of a Q# program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt="Q# program execution diagram" width="400">

<span data-ttu-id="58f5c-140">De specifieke aanroepable die moet worden uitgevoerd, heeft eerst toegang tot alle andere callables en typen die in dezelfde naam ruimte zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-140">Firstly, the specific callable to be run has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="58f5c-141">U kunt ook toegang krijgen tot die van een van de [ Q# bibliotheken](xref:microsoft.quantum.libraries), maar deze moeten worden gerefereerd via de volledige naam of door middel van het gebruik van de `open` hierboven beschreven instructies.</span><span class="sxs-lookup"><span data-stu-id="58f5c-141">It also access those from any of the [Q# libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="58f5c-142">De aanroepable zelf wordt vervolgens uitgevoerd op een *[doel computer](xref:microsoft.quantum.machines)*.</span><span class="sxs-lookup"><span data-stu-id="58f5c-142">The callable itself is then run on a *[target machine](xref:microsoft.quantum.machines)*.</span></span>
<span data-ttu-id="58f5c-143">Dergelijke doel computers kunnen echte Quantum hardware zijn of de meerdere simulatoren die beschikbaar zijn als onderdeel van de QDK.</span><span class="sxs-lookup"><span data-stu-id="58f5c-143">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="58f5c-144">Voor onze doel einden is de meest nuttige doel computer een exemplaar van de [Full-State Simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` waarmee het gedrag van het programma wordt berekend alsof het wordt uitgevoerd op een quantum computer zonder ruis.</span><span class="sxs-lookup"><span data-stu-id="58f5c-144">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being run on a noise-free quantum computer.</span></span>

<span data-ttu-id="58f5c-145">Tot nu toe hebben we beschreven wat er gebeurt wanneer een specifieke Q# aanroepable wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-145">So far, we've described what happens when a specific Q# callable is being run.</span></span>
<span data-ttu-id="58f5c-146">Ongeacht of het wordt Q# gebruikt in een zelfstandige toepassing of met een gast programma, is dit algemene proces meer of minder hetzelfde---dus de flexibiliteit van QDK.</span><span class="sxs-lookup"><span data-stu-id="58f5c-146">Regardless of whether Q# is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="58f5c-147">De verschillen tussen de manieren van aanroepen in de Quantum Development Kit geven daarom duidelijk aan *hoe* die Q# aanroep bare wordt uitgevoerd en op welke manier de resultaten worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-147">The differences between the ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that Q# callable is called to be run, and in what manner any results are returned.</span></span>
<span data-ttu-id="58f5c-148">Meer in het bijzonder zijn de verschillen van belang om:</span><span class="sxs-lookup"><span data-stu-id="58f5c-148">More specifically, the differences revolve around:</span></span>

- <span data-ttu-id="58f5c-149">Geeft Q# aan welke aanroepable moet worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="58f5c-149">Indicating which Q# callable is to be run</span></span>
- <span data-ttu-id="58f5c-150">Hoe mogelijke aanroep bare argumenten worden gegeven</span><span class="sxs-lookup"><span data-stu-id="58f5c-150">How potential callable arguments are provided</span></span>
- <span data-ttu-id="58f5c-151">De doel computer opgeven waarop de machine moet worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="58f5c-151">Specifying the target machine on which to run it</span></span>
- <span data-ttu-id="58f5c-152">Hoe worden de resultaten geretourneerd</span><span class="sxs-lookup"><span data-stu-id="58f5c-152">How any results are returned</span></span>

<span data-ttu-id="58f5c-153">Eerst bespreken we hoe dit wordt gedaan met de Q# zelfstandige toepassing vanaf de opdracht prompt en gaat u verder met het gebruik van python-en C#-host-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="58f5c-153">First, we discuss how this is done with the Q# standalone application from the command prompt, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="58f5c-154">We behouden de zelfstandige toepassing van Q# Jupyter-notebooks voor het laatst aan, omdat de primaire functionaliteit in tegens telling tot de eerste drie niet is gecentreerd rond een lokaal Q# bestand.</span><span class="sxs-lookup"><span data-stu-id="58f5c-154">We reserve the standalone application of Q# Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local Q# file.</span></span>

> [!NOTE]
> <span data-ttu-id="58f5c-155">Hoewel we dit niet in deze voor beelden illustreren, is een gemeen schappelijke methode tussen de run-methoden dat alle berichten die vanuit het programma worden afgedrukt Q# (via [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) of [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine) bijvoorbeeld), doorgaans altijd worden afgedrukt op de respectieve console.</span><span class="sxs-lookup"><span data-stu-id="58f5c-155">Although we don't illustrate it in these examples, one commonality between the run methods is that any messages printed from inside the Q# program (by way of [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) or [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="no-locq-from-the-command-prompt"></a><span data-ttu-id="58f5c-156">Q# vanaf de opdracht prompt</span><span class="sxs-lookup"><span data-stu-id="58f5c-156">Q# from the command prompt</span></span>
<span data-ttu-id="58f5c-157">Een van de eenvoudigste manieren om aan de slag te gaan met het schrijven Q# van Program ma's is om te voor komen dat u zich zorgen maakt over afzonderlijke bestanden en een tweede taal.</span><span class="sxs-lookup"><span data-stu-id="58f5c-157">One of the easiest ways to get started writing Q# programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="58f5c-158">Het gebruik van Visual Studio code of Visual Studio met de QDK-extensie biedt een naadloze werk stroom waarbij we Q# callables uit slechts één Q# bestand uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="58f5c-158">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run Q# callables from only a single Q# file.</span></span>

<span data-ttu-id="58f5c-159">Hiervoor voert u het programma uiteindelijk uit door het volgende in te voeren:</span><span class="sxs-lookup"><span data-stu-id="58f5c-159">For this, we will ultimately run the program by entering</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="58f5c-160">bij de opdracht prompt.</span><span class="sxs-lookup"><span data-stu-id="58f5c-160">at the command prompt.</span></span>
<span data-ttu-id="58f5c-161">De eenvoudigste werk stroom is wanneer de locatie van de map van de Terminal gelijk is aan die van het Q# bestand, dat eenvoudig kan worden verwerkt naast het Q# bewerken van bestanden met behulp van de geïntegreerde terminal in VS code.</span><span class="sxs-lookup"><span data-stu-id="58f5c-161">The simplest workflow is when the terminal's directory location is the same as the Q# file, which can be easily handled alongside Q# file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="58f5c-162">De [ `dotnet run` opdracht](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepteert echter talloze opties en het programma kan ook worden uitgevoerd vanaf een andere locatie door simpelweg `--project <PATH>` de locatie van het bestand op te geven Q# .</span><span class="sxs-lookup"><span data-stu-id="58f5c-162">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the Q# file.</span></span>


### <a name="add-entry-point-to-no-locq-file"></a><span data-ttu-id="58f5c-163">Invoer punt toevoegen aan Q# bestand</span><span class="sxs-lookup"><span data-stu-id="58f5c-163">Add entry point to Q# file</span></span>

<span data-ttu-id="58f5c-164">De meeste Q# bestanden bevatten meer dan één aanroepable, dus we moeten er natuurlijk voor zorgen dat de compiler weet *welke* aanroep kan worden uitgevoerd wanneer we de `dotnet run` opdracht opgeven.</span><span class="sxs-lookup"><span data-stu-id="58f5c-164">Most Q# files will contain more than one callable, so naturally we need to let the compiler know *which* callable to run when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="58f5c-165">Dit wordt gedaan met een eenvoudige wijziging in het Q# bestand zelf:</span><span class="sxs-lookup"><span data-stu-id="58f5c-165">This is done with a simple change to the Q# file itself:</span></span> 
    - <span data-ttu-id="58f5c-166">Voeg een regel toe met `@EntryPoint()` de direct voorafgaande oproep bare.</span><span class="sxs-lookup"><span data-stu-id="58f5c-166">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="58f5c-167">Ons bestand van bovenstaande zou daarom worden</span><span class="sxs-lookup"><span data-stu-id="58f5c-167">Our file from above would therefore become</span></span>
```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // for the H operation
    open Microsoft.Quantum.Measurement;   // for MResetZ

    @EntryPoint()
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }
}
```

<span data-ttu-id="58f5c-168">Nu wordt een aanroep van `dotnet run` vanaf de opdracht prompt om te `MeasureSuperposition` worden uitgevoerd en wordt de geretourneerde waarde vervolgens rechtstreeks naar de Terminal afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="58f5c-168">Now, a call of `dotnet run` from the command prompt leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="58f5c-169">Daarom ziet u ofwel `One` of `Zero` afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="58f5c-169">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="58f5c-170">Houd er rekening mee dat het niet van belang is dat er meer callables worden gedefinieerd, maar alleen `MeasureSuperposition` worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-170">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="58f5c-171">Daarnaast is het geen probleem als uw aanroep mogelijk [documentatie commentaar](xref:microsoft.quantum.qsharp.comments#documentation-comments) bevat vóór de declaratie van het `@EntryPoint()` kenmerk, maar dit kan eenvoudigweg worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="58f5c-171">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.qsharp.comments#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="58f5c-172">Aanroep bare argumenten</span><span class="sxs-lookup"><span data-stu-id="58f5c-172">Callable arguments</span></span>

<span data-ttu-id="58f5c-173">Tot nu toe hebben we alleen een bewerking gezien die geen invoer heeft.</span><span class="sxs-lookup"><span data-stu-id="58f5c-173">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="58f5c-174">Stel dat we een vergelijk bare bewerking willen uitvoeren, maar op meerdere qubits---het aantal dat als argument wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="58f5c-174">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="58f5c-175">Een dergelijke bewerking kan worden geschreven als</span><span class="sxs-lookup"><span data-stu-id="58f5c-175">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="58f5c-176">waarbij de geretourneerde waarde een matrix is van de meet resultaten.</span><span class="sxs-lookup"><span data-stu-id="58f5c-176">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="58f5c-177">Houd er rekening mee dat [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) en [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) zich in de en de naam ruimte bevindt [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) . hiervoor [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) moeten aanvullende instructies worden vereist `open` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-177">Note that [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) and [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) are in the [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) and [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="58f5c-178">Als we het `@EntryPoint()` kenmerk voorafgaand aan deze nieuwe bewerking verplaatsen (Houd er dan rekening mee dat er slechts één regel in een bestand kan worden uitgevoerd). er wordt geprobeerd deze uit te voeren met alleen `dotnet run` resultaten in een fout bericht dat aangeeft welke extra opdracht regel opties vereist zijn en hoe u deze kunt uitdrukken.</span><span class="sxs-lookup"><span data-stu-id="58f5c-178">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command-line options are required, and how to express them.</span></span>

<span data-ttu-id="58f5c-179">De algemene notatie voor de opdracht regel is in werkelijkheid `dotnet run [options]` en aanroep bare argumenten worden daar vermeld.</span><span class="sxs-lookup"><span data-stu-id="58f5c-179">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="58f5c-180">In dit geval ontbreekt het argument `n` en ziet u dat we de optie moeten opgeven `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-180">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="58f5c-181">Om uit te voeren `MeasureSuperpositionArray` voor `n=4` qubits, gebruiken we daarom</span><span class="sxs-lookup"><span data-stu-id="58f5c-181">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="58f5c-182">levert een uitvoer op die vergelijkbaar is met</span><span class="sxs-lookup"><span data-stu-id="58f5c-182">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="58f5c-183">Deze cursus wordt uitgebreid naar meerdere argumenten.</span><span class="sxs-lookup"><span data-stu-id="58f5c-183">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="58f5c-184">Argument namen die zijn gedefinieerd in `camelCase` , worden enigszins gewijzigd door de compiler om te worden geaccepteerd als Q# invoer.</span><span class="sxs-lookup"><span data-stu-id="58f5c-184">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as Q# inputs.</span></span> <span data-ttu-id="58f5c-185">Als `n` we bijvoorbeeld de bovenstaande naam hebben gebruikt `numQubits` , wordt deze invoer opgegeven in de opdracht regel in `--num-qubits 4` plaats van `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-185">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="58f5c-186">Het fout bericht bevat ook andere opties die kunnen worden gebruikt, met inbegrip van het wijzigen van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="58f5c-186">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="58f5c-187">Verschillende doel computers</span><span class="sxs-lookup"><span data-stu-id="58f5c-187">Different target machines</span></span>

<span data-ttu-id="58f5c-188">Omdat de uitvoer van onze activiteiten tot nu toe de verwachte resultaten van hun actie op echte qubits was, is het duidelijk dat de standaard doel computer van de opdracht regel de Full-State Quantum Simulator is `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-188">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quantum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="58f5c-189">We kunnen er echter voor zorgen dat callables worden uitgevoerd op een specifieke doel computer met de optie `--simulator` (of de steno `-s` ).</span><span class="sxs-lookup"><span data-stu-id="58f5c-189">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="58f5c-190">Dit kan bijvoorbeeld worden uitgevoerd op [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="58f5c-190">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="58f5c-191">De afgedrukte uitvoer wordt vervolgens</span><span class="sxs-lookup"><span data-stu-id="58f5c-191">The printed output is then</span></span>

```output
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

<span data-ttu-id="58f5c-192">Zie [resource Estimator: metrische](xref:microsoft.quantum.machines.resources-estimator#metrics-reported)gegevens voor meer informatie over wat deze metrische gegevens aangeven.</span><span class="sxs-lookup"><span data-stu-id="58f5c-192">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-run-summary"></a><span data-ttu-id="58f5c-193">Overzicht van uitvoering van opdracht regel</span><span class="sxs-lookup"><span data-stu-id="58f5c-193">Command line run summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt="Q# program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a><span data-ttu-id="58f5c-194">Niet- Q# `dotnet run` Opties</span><span class="sxs-lookup"><span data-stu-id="58f5c-194">Non-Q# `dotnet run` options</span></span>

<span data-ttu-id="58f5c-195">Zoals hierboven hierboven vermeld met de `--project` optie, accepteert de [ `dotnet run` opdracht](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) ook opties die niet gerelateerd zijn aan de Q# aanroep bare argumenten.</span><span class="sxs-lookup"><span data-stu-id="58f5c-195">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the Q# callable arguments.</span></span>
<span data-ttu-id="58f5c-196">Als u beide soorten opties opgeeft, `dotnet` moeten de specifieke opties eerst worden opgegeven, gevolgd door een delimiter `--` , en vervolgens de Q# -specifieke opties.</span><span class="sxs-lookup"><span data-stu-id="58f5c-196">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the Q#-specific options.</span></span>
<span data-ttu-id="58f5c-197">U kunt bijvoorbeeld een pad opgeven dat samen met een aantal qubits voor de bovenstaande bewerking wordt uitgevoerd via `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-197">For example, specifying a path along with a number qubits for the operation above would be run via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="no-locq-with-host-programs"></a><span data-ttu-id="58f5c-198">Q# met host-Program ma's</span><span class="sxs-lookup"><span data-stu-id="58f5c-198">Q# with host programs</span></span>

<span data-ttu-id="58f5c-199">Met ons Q# bestand is een alternatief voor het aanroepen van een bewerking of functie rechtstreeks vanaf de opdracht prompt het gebruik van een *hostprogramma* in een andere klassieke taal.</span><span class="sxs-lookup"><span data-stu-id="58f5c-199">With our Q# file in hand, an alternative to calling an operation or function directly from the command prompt is to use a *host program* in another classical language.</span></span> <span data-ttu-id="58f5c-200">Dit kan met name worden gedaan met python of een .NET-taal, zoals C# of F # (in het geval van een beknopt overzicht van de informatie over C#.</span><span class="sxs-lookup"><span data-stu-id="58f5c-200">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="58f5c-201">Er zijn nog meer instellingen vereist om de interoperabiliteit in te scha kelen, maar u kunt deze details vinden in de [installatie handleidingen](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="58f5c-201">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="58f5c-202">In een kort gezegd bevat de situatie nu een bestand voor het hostprogramma (bijvoorbeeld `*.py` of `*.cs` ) op dezelfde locatie als het Q# bestand.</span><span class="sxs-lookup"><span data-stu-id="58f5c-202">In a nutshell, the situation now includes a host program file (for example, `*.py` or `*.cs`) in the same location as our Q# file.</span></span>
<span data-ttu-id="58f5c-203">Het is nu het *hostprogramma* dat wordt uitgevoerd en wanneer het wordt uitgevoerd, kan het specifieke Q# bewerkingen en functies vanuit het bestand aanroepen Q# .</span><span class="sxs-lookup"><span data-stu-id="58f5c-203">It's now the *host* program that gets run, and while it is running, it can call specific Q# operations and functions from the Q# file.</span></span>
<span data-ttu-id="58f5c-204">De kern van de interoperabiliteit is gebaseerd op de Q# compiler die de inhoud van het Q# bestand toegankelijk maakt voor het hostprogramma, zodat deze kan worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-204">The core of the interoperability is based on the Q# compiler making the contents of the Q# file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="58f5c-205">Een van de belangrijkste voor delen van het gebruik van een hostprogramma is dat de klassieke gegevens die door het Q# programma worden geretourneerd, vervolgens verder kunnen worden verwerkt in de taal van de host.</span><span class="sxs-lookup"><span data-stu-id="58f5c-205">One of the main benefits of using a host program is that the classical data returned by the Q# program can then be further processed in the host language.</span></span>
<span data-ttu-id="58f5c-206">Dit kan bestaan uit een aantal geavanceerde gegevens verwerking (bijvoorbeeld iets dat niet intern kan worden uitgevoerd Q# ) en vervolgens aanroepen van verdere Q# acties op basis van deze resultaten, of iets zo eenvoudig als het uitzetten van de Q# resultaten.</span><span class="sxs-lookup"><span data-stu-id="58f5c-206">This could consist of some advanced data processing (for example, something that can't be performed internally in Q#), and then calling further Q# actions based on those results, or something as simple as plotting the Q# results.</span></span>

<span data-ttu-id="58f5c-207">Het algemene schema wordt hier weer gegeven en we bespreken de specifieke implementaties voor python en C# hieronder.</span><span class="sxs-lookup"><span data-stu-id="58f5c-207">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="58f5c-208">Een voor beeld van het gebruik van een F #-hostprogramma vindt u in de voor [beelden van .net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="58f5c-208">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt="Q# program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="58f5c-209">Het `@EntryPoint()` kenmerk dat voor toepassingen wordt gebruikt, Q# kan niet worden gebruikt met host-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="58f5c-209">The `@EntryPoint()` attribute used for Q# applications cannot be used with host programs.</span></span>
> <span data-ttu-id="58f5c-210">Er wordt een fout gegenereerd als deze aanwezig is in het Q# bestand dat wordt aangeroepen door een host.</span><span class="sxs-lookup"><span data-stu-id="58f5c-210">An error will be raised if it is present in the Q# file being called by a host.</span></span> 

<span data-ttu-id="58f5c-211">Als u wilt werken met andere host-Program ma's, hoeft u geen wijzigingen aan te brengen in een `*.qs` Q# bestand.</span><span class="sxs-lookup"><span data-stu-id="58f5c-211">To work with different host programs, there are no changes required to a `*.qs` Q# file.</span></span>
<span data-ttu-id="58f5c-212">De volgende implementaties van een host-programma werken allemaal met hetzelfde Q# bestand:</span><span class="sxs-lookup"><span data-stu-id="58f5c-212">The following host program implementations all work with the same Q# file:</span></span>

```qsharp
namespace NamespaceName {
    open Microsoft.Quantum.Intrinsic;     // contains H
    open Microsoft.Quantum.Measurement;   // MResetZ
    open Microsoft.Quantum.Canon;         // ApplyToEach
    open Microsoft.Quantum.Arrays;        // ForEach

    operation MeasureSuperposition() : Result {
        using (q = Qubit()) { 
            H(q);
            return MResetZ(q);
        }
    }

    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {  
            ApplyToEach(H, qubits); 
            return ForEach(MResetZ, qubits);    
        }
    }
}
```

<span data-ttu-id="58f5c-213">Selecteer het tabblad dat overeenkomt met de taal van uw host.</span><span class="sxs-lookup"><span data-stu-id="58f5c-213">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="58f5c-214">Python</span><span class="sxs-lookup"><span data-stu-id="58f5c-214">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="58f5c-215">Een python-hostprogramma is als volgt samengesteld:</span><span class="sxs-lookup"><span data-stu-id="58f5c-215">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="58f5c-216">Importeer de `qsharp` module, die de module lader voor interoperabiliteit registreert Q# .</span><span class="sxs-lookup"><span data-stu-id="58f5c-216">Import the `qsharp` module, which registers the module loader for Q# interoperability.</span></span> 
    <span data-ttu-id="58f5c-217">Op die manier kunnen Q# naam ruimten worden weer gegeven als python-modules, waaruit we callables kunnen importeren Q# .</span><span class="sxs-lookup"><span data-stu-id="58f5c-217">This allows Q# namespaces to appear as Python modules, from which we can "import" Q# callables.</span></span>
    <span data-ttu-id="58f5c-218">Houd er rekening mee dat het technisch gezien niet het Q# callables is dat wordt geïmporteerd, maar dat er python-stubs zijn waarmee ze kunnen worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-218">Note that it is technically not the Q# callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="58f5c-219">Deze gedragen zich als objecten van python-klassen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-219">These behave as objects of Python classes.</span></span> <span data-ttu-id="58f5c-220">We gebruiken methoden op deze objecten om de doel machines op te geven waarnaar we de bewerking verzenden wanneer het programma wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-220">We use methods on these objects to specify the target machines that we send the operation to when running the program.</span></span>

2. <span data-ttu-id="58f5c-221">Importeer de Q# callables die in dit geval direct---worden aangeroepen, `MeasureSuperposition` en `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-221">Import those Q# callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="58f5c-222">Als de `qsharp` module is geïmporteerd, kunt u ook rechtstreeks vanuit de Q# bibliotheek naam ruimten callables importeren.</span><span class="sxs-lookup"><span data-stu-id="58f5c-222">With the `qsharp` module imported, you can also import callables directly from the Q# library namespaces.</span></span>

3. <span data-ttu-id="58f5c-223">Onder andere python-code kunt u deze callables op specifieke doel computers aanroepen en de bijbehorende retour waarden toewijzen aan variabelen (als ze een waarde Retour neren) voor verder gebruik.</span><span class="sxs-lookup"><span data-stu-id="58f5c-223">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="58f5c-224">Doel machines opgeven</span><span class="sxs-lookup"><span data-stu-id="58f5c-224">Specifying target machines</span></span>
<span data-ttu-id="58f5c-225">Het aanroepen van een bewerking die moet worden uitgevoerd op een specifieke doel computer, wordt uitgevoerd via verschillende python-methoden voor het geïmporteerde object.</span><span class="sxs-lookup"><span data-stu-id="58f5c-225">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="58f5c-226">`.simulate(<args>)`Maakt bijvoorbeeld gebruik `QuantumSimulator` van de om de bewerking uit te voeren, terwijl dat `.estimate_resources(<args>)` wel het geval is `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-226">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="58f5c-227">Invoer door geven aan Q\#</span><span class="sxs-lookup"><span data-stu-id="58f5c-227">Passing inputs to Q\#</span></span>
<span data-ttu-id="58f5c-228">Argumenten voor de Q# aanroepable moeten worden aangegeven in de vorm van een trefwoord argument, waarbij het sleutel woord de argument naam in de Q# aanroep bare definitie is.</span><span class="sxs-lookup"><span data-stu-id="58f5c-228">Arguments for the Q# callable should be provided in the form of a keyword argument, where the keyword is the argument name in the Q# callable definition.</span></span>
<span data-ttu-id="58f5c-229">Dat wil zeggen, `MeasureSuperpositionArray.simulate(n=4)` is geldig, terwijl `MeasureSuperpositionArray.simulate(4)` een fout optreedt.</span><span class="sxs-lookup"><span data-stu-id="58f5c-229">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="58f5c-230">Daarom wordt het python-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="58f5c-230">Therefore, the Python host program</span></span> 

```python
import qsharp
from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray

single_qubit_result = MeasureSuperposition.simulate()
single_qubit_resources = MeasureSuperposition.estimate_resources()

multi_qubit_result = MeasureSuperpositionArray.simulate(n=4)
multi_qubit_resources = MeasureSuperpositionArray.estimate_resources(n=4)

print('Single qubit:\n' + str(single_qubit_result))
print(single_qubit_resources)

print('\nMultiple qubits:\n' + str(multi_qubit_result))
print(multi_qubit_resources)
```

<span data-ttu-id="58f5c-231">resulteert in een uitvoer zoals de volgende:</span><span class="sxs-lookup"><span data-stu-id="58f5c-231">results in an output like the following:</span></span>

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="58f5c-232">Q#Code uit andere projecten of pakketten gebruiken</span><span class="sxs-lookup"><span data-stu-id="58f5c-232">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="58f5c-233">Standaard `import qsharp` laadt de opdracht alle `.qs` bestanden in de huidige map en Q# worden de bewerkingen en functies beschikbaar voor gebruik in het python-script.</span><span class="sxs-lookup"><span data-stu-id="58f5c-233">By default, the `import qsharp` command loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the Python script.</span></span>

<span data-ttu-id="58f5c-234">Als u Q# code wilt laden vanuit een andere map, kan de [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) worden gebruikt voor het toevoegen van een verwijzing naar een `.csproj` bestand voor een Q# project (dat wil zeggen een project waarnaar wordt verwezen `Microsoft.Quantum.Sdk` ).</span><span class="sxs-lookup"><span data-stu-id="58f5c-234">To load Q# code from another folder, the [`qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span>
<span data-ttu-id="58f5c-235">Met deze opdracht worden alle `.qs` bestanden in de map die de submappen bevat, gecompileerd `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-235">This command will compile any `.qs` files in the folder containing the `.csproj` and its subfolders.</span></span> <span data-ttu-id="58f5c-236">Ook worden alle pakketten die via of projecten verwijzen waarnaar wordt `PackageReference` Q# verwezen `ProjectReference` in dat bestand, recursief geladen `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-236">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span>

<span data-ttu-id="58f5c-237">Met de volgende python-code wordt bijvoorbeeld een extern project geïmporteerd, dat verwijst naar het pad ten opzichte van de huidige map en wordt een van de Q# bewerkingen aangeroepen:</span><span class="sxs-lookup"><span data-stu-id="58f5c-237">As an example, the following Python code imports an external project, referencing its path relative to the current folder, and invokes one of its Q# operations:</span></span>

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

<span data-ttu-id="58f5c-238">Dit resulteert in uitvoer als de volgende:</span><span class="sxs-lookup"><span data-stu-id="58f5c-238">This results in output like the following:</span></span>

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

<span data-ttu-id="58f5c-239">Als u externe pakketten wilt laden die Q# code bevatten, gebruikt u de [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span><span class="sxs-lookup"><span data-stu-id="58f5c-239">To load external packages containing Q# code, use the [`qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span></span>

<span data-ttu-id="58f5c-240">Als de Q# code in de huidige map afhankelijk is van externe projecten of pakketten, kunnen er fouten optreden tijdens `import qsharp` de uitvoering, omdat de afhankelijkheden nog niet zijn geladen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-240">If the Q# code in the current folder depends on external projects or packages, you may see errors when running `import qsharp`, since the dependencies have not yet been loaded.</span></span>
<span data-ttu-id="58f5c-241">Als u de vereiste externe pakketten of Q# projecten tijdens de opdracht wilt laden, moet u `import qsharp` ervoor zorgen dat de map met het python-script een `.csproj` bestand bevat waarnaar wordt verwezen `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-241">To load required external packages or Q# projects during the `import qsharp` command, ensure that the folder with the Python script contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="58f5c-242">Voeg in dat `.csproj` de eigenschap toe `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` aan de `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-242">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="58f5c-243">Dit geeft de instructie Q# om een of meer items te `ProjectReference` laden `PackageReference` die zijn gevonden in die `.csproj` tijdens de `import qsharp` opdracht.</span><span class="sxs-lookup"><span data-stu-id="58f5c-243">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` during the `import qsharp` command.</span></span>

<span data-ttu-id="58f5c-244">Dit is bijvoorbeeld een eenvoudig `.csproj` bestand dat ervoor zorgt dat Q# het pakket automatisch wordt geladen `Microsoft.Quantum.Chemistry` :</span><span class="sxs-lookup"><span data-stu-id="58f5c-244">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="58f5c-245">Deze aangepaste `<IQSharpLoadAutomatically>` eigenschap is momenteel vereist voor python-hosts, maar in de toekomst kan dit het standaard gedrag voor een bestand zijn dat `.csproj` zich in dezelfde map bevindt als het python-script.</span><span class="sxs-lookup"><span data-stu-id="58f5c-245">Currently this custom `<IQSharpLoadAutomatically>` property is required by Python hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the Python script.</span></span>

> [!NOTE]
> <span data-ttu-id="58f5c-246">Momenteel `<QsharpCompile>` wordt de instelling in de `.csproj` wordt genegeerd door python-hosts en `.qs` worden alle bestanden in de map `.csproj` (inclusief submappen) geladen en gecompileerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-246">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Python hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="58f5c-247">Ondersteuning voor `.csproj` instellingen wordt in de toekomst verbeterd (Zie [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) voor meer informatie).</span><span class="sxs-lookup"><span data-stu-id="58f5c-247">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>


### <a name="c"></a>[<span data-ttu-id="58f5c-248">C#</span><span class="sxs-lookup"><span data-stu-id="58f5c-248">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="58f5c-249">Een C#-hostprogramma heeft meerdere onderdelen en werkt zeer nauw samen met enkele onderdelen van de QDK, zoals de simulators die zelf zijn gebouwd op C#.</span><span class="sxs-lookup"><span data-stu-id="58f5c-249">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="58f5c-250">De Q# compiler werkt hier door een overeenkomende C#-naam ruimte te genereren uit de Q# naam ruimte in het Q# bestand.</span><span class="sxs-lookup"><span data-stu-id="58f5c-250">The Q# compiler works here by generating an equivalently named C# namespace from the Q# namespace in our Q# file.</span></span>
<span data-ttu-id="58f5c-251">Daarnaast wordt er een gelijkwaardige C#-klasse gegenereerd voor elk van de Q# callables of typen die daarin zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-251">It further generates an equivalently named C# class for each of the Q# callables or types defined therein.</span></span>

<span data-ttu-id="58f5c-252">Eerst maken we de klassen die in ons hostprogramma worden gebruikt, beschikbaar met `using` instructies, die ongeveer analagous zijn voor de `open` instructies in ons Q# bestand:</span><span class="sxs-lookup"><span data-stu-id="58f5c-252">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our Q# file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (for example, QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the Q# namespace available
```

<span data-ttu-id="58f5c-253">Vervolgens declareren we onze C#-naam ruimte, een paar andere bits en delen (Zie het volledige code blok hieronder) en vervolgens een klassieke programmering (bijvoorbeeld voor het berekenen van argumenten voor de Q# callables).</span><span class="sxs-lookup"><span data-stu-id="58f5c-253">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (for example, computing arguments for the Q# callables).</span></span>
<span data-ttu-id="58f5c-254">Dit is niet nodig in ons geval, maar een voor beeld van een dergelijk gebruik is te vinden in het voor  [beeld van .net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="58f5c-254">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="58f5c-255">Doelcomputers</span><span class="sxs-lookup"><span data-stu-id="58f5c-255">Target machines</span></span>

<span data-ttu-id="58f5c-256">Als u terugkeert naar Q# , moeten we een instantie maken van de doel computer waarop we onze bewerkingen zullen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="58f5c-256">Getting back to Q#, we must create an instance of whatever target machine we will run our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="58f5c-257">Het gebruik van andere doel machines is net zo eenvoudig als het instantiëren van een andere computer, hoewel de manier waarop u dit doet en het verwerken van de geretourneerde items iets anders kan zijn.</span><span class="sxs-lookup"><span data-stu-id="58f5c-257">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="58f5c-258">Voor het oog op de boog is het [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) nu van toepassing op de voor-en de voor beelden [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span><span class="sxs-lookup"><span data-stu-id="58f5c-258">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="58f5c-259">Elke C#-klasse die is gegenereerd op basis van de Q# bewerkingen, heeft een `Run` methode, het eerste argument waarvan het doel computer exemplaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="58f5c-259">Each C# class generated from the Q# operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="58f5c-260">Daarom gebruiken we om uit te voeren `MeasureSuperposition` op de `QuantumSimulator` `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-260">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="58f5c-261">De geretourneerde resultaten kunnen vervolgens worden toegewezen aan variabelen in C#:</span><span class="sxs-lookup"><span data-stu-id="58f5c-261">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="58f5c-262">De `Run` methode wordt asynchroon uitgevoerd, omdat dit het geval is voor echte Quantum hardware `await` . het sleutel woord blokkeert daarom verdere verwerking totdat de taak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="58f5c-262">The `Run` method is run asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further processing until the task completes.</span></span>

<span data-ttu-id="58f5c-263">Als de Q# aanroep geen retour nering heeft (bijvoorbeeld het retour type `Unit` ), kan de uitvoering nog steeds op dezelfde manier worden uitgevoerd zonder deze aan een variabele toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-263">If the Q# callable does not have any returns (for example, it has return type `Unit`), then the run can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="58f5c-264">In dat geval zou de volledige regel gewoon bestaan uit</span><span class="sxs-lookup"><span data-stu-id="58f5c-264">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="58f5c-265">Argumenten</span><span class="sxs-lookup"><span data-stu-id="58f5c-265">Arguments</span></span>

<span data-ttu-id="58f5c-266">Argumenten die kunnen worden Q# aangeroepen, worden eenvoudigweg door gegeven als aanvullende argumenten na de doel computer.</span><span class="sxs-lookup"><span data-stu-id="58f5c-266">Any arguments to the Q# callable are simply passed as additional arguments after the target machine.</span></span>
<span data-ttu-id="58f5c-267">Daarom worden de resultaten van `MeasureSuperpositionArray` op `n=4` qubits opgehaald via</span><span class="sxs-lookup"><span data-stu-id="58f5c-267">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="58f5c-268">Een volledig C#-hostprogramma kan er dus als volgt uitzien</span><span class="sxs-lookup"><span data-stu-id="58f5c-268">A full C# host program could thus look like</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine($"Multiple qubit result: {multiQubitResult}");
        }
    }
}
```

<span data-ttu-id="58f5c-269">Op de locatie van het C#-bestand kan het host-programma worden uitgevoerd vanaf de opdracht prompt door het in te voeren</span><span class="sxs-lookup"><span data-stu-id="58f5c-269">At the location of the C# file, the host program can be run from the command prompt by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="58f5c-270">in dit geval ziet u uitvoer die is geschreven naar de-console, vergelijkbaar met</span><span class="sxs-lookup"><span data-stu-id="58f5c-270">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="58f5c-271">Als gevolg van de interoperabiliteit van de compiler met naam ruimten, kunnen we een andere Q# callables beschikbaar maken zonder de `using NamespaceName;` -instructie, en alleen de naam van de C#-titel ruimte erop.</span><span class="sxs-lookup"><span data-stu-id="58f5c-271">Due to the compiler's interoperability with namespaces, we could alternatively make our Q# callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="58f5c-272">Dat wil zeggen door te vervangen door `namespace host` `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-272">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="58f5c-273">Inclusief de bronnen estimator</span><span class="sxs-lookup"><span data-stu-id="58f5c-273">Including the resources estimator</span></span>

<span data-ttu-id="58f5c-274">[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Er is een iets andere implementatie vereist om de uitvoer op te halen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-274">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="58f5c-275">In plaats van ze als een variabele te instantiëren met een- `using` instructie (zoals we met de) hebben gedaan `QuantumSimulator` , kunnen we objecten van de klasse direct instantiëren via</span><span class="sxs-lookup"><span data-stu-id="58f5c-275">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="58f5c-276">U ziet dat in plaats van één doel-Simulator door meerdere bewerkingen wordt gebruikt Q# , er één voor elk wordt geïnstantieerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-276">Notice that instead of a single target simulator to be used by multiple Q# operations, we have instantiated one for each.</span></span> <span data-ttu-id="58f5c-277">Dit komt doordat de objecten zelf worden gewijzigd wanneer ze worden gebruikt als doel machines en de resultaten ervan daarna kunnen worden opgehaald met de methode Class `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-277">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="58f5c-278">Voor het uitvoeren van de bewerkingen op resource schattingen gebruiken we</span><span class="sxs-lookup"><span data-stu-id="58f5c-278">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="58f5c-279">Daarna haalt u de resultaten op als door tabs gescheiden waarden (TSV) met `estimatorSingleQ.ToTSV()` en `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-279">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="58f5c-280">Een volledig C#-hostprogramma dat zowel het gebruik `QuantumSimulator` als `ResourcesEstimator` het formulier maakt, kan dan het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="58f5c-280">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;
using NamespaceName;

namespace host
{
    static class Program
    {
        static async Task Main(string[] args)
        {
            using var sim = new QuantumSimulator();
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();

            var singleQubitResult = await MeasureSuperposition.Run(sim);
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);

            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);

            Console.WriteLine($"Single qubit result: {singleQubitResult}");
            Console.WriteLine("Single qubit resources:");
            Console.WriteLine(estimatorSingleQ.ToTSV());

            Console.WriteLine($"\nMultiple qubit result: {multiQubitResult}");
            Console.WriteLine("Multiple qubit resources:");
            Console.WriteLine(estimatorMultiQ.ToTSV());
        }
    }
}
```


<span data-ttu-id="58f5c-281">wat resulteert in uitvoer die vergelijkbaar is met</span><span class="sxs-lookup"><span data-stu-id="58f5c-281">which would yield output similar to</span></span>

```output
Single qubit result: One
Single qubit resources:
Metric          Sum
CNOT            0
QubitClifford   1
R               0
Measure         1
T               0
Depth           0
Width           1
BorrowedWidth   0

Multiple qubit result: [One,One,One,Zero]
Multiple qubit resources:
Metric          Sum
CNOT            0
QubitClifford   4
R               0
Measure         4
T               0
Depth           0
Width           4
BorrowedWidth   0
```

***

## <a name="no-locq-jupyter-notebooks"></a><span data-ttu-id="58f5c-282">Q# Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="58f5c-282">Q# Jupyter Notebooks</span></span>
<span data-ttu-id="58f5c-283">Q# Jupyter-notebooks maken gebruik van de I Q# -kernel, waarmee u callables in één notitie blok kunt definiëren, compileren en uitvoeren Q# ---alle naast instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="58f5c-283">Q# Jupyter Notebooks make use of the IQ# kernel, which allows you to define, compile, and run Q# callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="58f5c-284">Dit betekent dat hoewel het mogelijk is om de inhoud van bestanden te importeren en `*.qs` Q# te gebruiken, ze niet nodig zijn in het run model.</span><span class="sxs-lookup"><span data-stu-id="58f5c-284">This means that while it is possible to import and use the contents of `*.qs` Q# files, they are not necessary in the run model.</span></span>

<span data-ttu-id="58f5c-285">Hier wordt beschreven hoe u de Q# hierboven gedefinieerde bewerkingen uitvoert, maar een uitgebreidere inleiding tot het gebruik van Q# Jupyter-notebooks is beschikbaar op [Inleiding tot Q# en Jupyter-notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="58f5c-285">Here, we will detail how to run the Q# operations defined above, but a more broad introduction to using Q# Jupyter Notebooks is provided at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="58f5c-286">Bewerkingen definiëren</span><span class="sxs-lookup"><span data-stu-id="58f5c-286">Defining operations</span></span>

<span data-ttu-id="58f5c-287">In een Q# Jupyter notebook voert u code in op Q# dezelfde manier als in de naam ruimte van een Q# bestand.</span><span class="sxs-lookup"><span data-stu-id="58f5c-287">In a Q# Jupyter Notebook, you enter Q# code just as we would from inside the namespace of a Q# file.</span></span>

<span data-ttu-id="58f5c-288">Daarom kunnen we toegang tot callables van de [ Q# standaard bibliotheken](xref:microsoft.quantum.libraries.standard.intro) inschakelen met `open` instructies voor hun respectieve naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="58f5c-288">So, we can enable access to callables from the [Q# standard libraries](xref:microsoft.quantum.libraries.standard.intro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="58f5c-289">Bij het uitvoeren van een cel met een dergelijke instructie zijn de definities van deze naam ruimten beschikbaar in de hele werk ruimte.</span><span class="sxs-lookup"><span data-stu-id="58f5c-289">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="58f5c-290">Callables van [micro soft. Quantum. intrinsieke](xref:Microsoft.Quantum.Intrinsic) en [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon) (bijvoorbeeld [`H`](xref:Microsoft.Quantum.Intrinsic.H) en [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) ) zijn automatisch beschikbaar voor bewerkingen die zijn gedefinieerd in cellen in Q# Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="58f5c-290">Callables from [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic) and [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon) (for example, [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach)) are automatically available to operations defined within cells in Q# Jupyter Notebooks.</span></span>
> <span data-ttu-id="58f5c-291">Dit geldt echter niet voor code die wordt binnengebracht in vanuit externe Q# bron bestanden (een proces dat wordt weer gegeven bij [Inleiding tot Q# en Jupyter-notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span><span class="sxs-lookup"><span data-stu-id="58f5c-291">However, this is not true for code brought in from external Q# source files (a process shown at [Intro to Q# and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="58f5c-292">Op dezelfde manier hoeft u alleen maar de Q# code te schrijven en de cel uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="58f5c-292">Similarly, defining operations requires only writing the Q# code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining Q# operations" width="773">

<span data-ttu-id="58f5c-293">De uitvoer vermeldt deze bewerkingen, die vervolgens kunnen worden aangeroepen vanuit toekomstige cellen.</span><span class="sxs-lookup"><span data-stu-id="58f5c-293">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="58f5c-294">Doelcomputers</span><span class="sxs-lookup"><span data-stu-id="58f5c-294">Target machines</span></span>

<span data-ttu-id="58f5c-295">De functionaliteit voor het uitvoeren van bewerkingen op specifieke doel computers wordt gegeven via een [ Q# Magic-opdracht](xref:microsoft.quantum.guide.quickref.iqsharp).</span><span class="sxs-lookup"><span data-stu-id="58f5c-295">The functionality to run operations on specific target machines is provided via [IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="58f5c-296">`%simulate`Maakt bijvoorbeeld gebruik van de `QuantumSimulator` , en maakt gebruik van `%estimate` `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="58f5c-296">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a Q# operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="58f5c-297">Invoer door geven aan functies en bewerkingen</span><span class="sxs-lookup"><span data-stu-id="58f5c-297">Passing inputs to functions and operations</span></span>

<span data-ttu-id="58f5c-298">Als u invoer wilt door geven aan de Q# bewerkingen, kunnen de argumenten als paren worden door gegeven `key=value` aan de opdracht Magic run.</span><span class="sxs-lookup"><span data-stu-id="58f5c-298">To pass inputs to the Q# operations, the arguments can be passed as `key=value` pairs to the run magic command.</span></span>
<span data-ttu-id="58f5c-299">Om uit te voeren `MeasureSuperpositionArray` met vier qubits kunnen we de `%simulate MeasureSuperpositionArray n=4` volgende handelingen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="58f5c-299">So, to run `MeasureSuperpositionArray` with four qubits, we can run `%simulate MeasureSuperpositionArray n=4`:</span></span>

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a Q# operation with arguments" width="773">

<span data-ttu-id="58f5c-300">Dit patroon kan worden gebruikt in combi natie met `%estimate` andere run-opdrachten.</span><span class="sxs-lookup"><span data-stu-id="58f5c-300">This pattern can be used similarly with `%estimate` and other run commands.</span></span>

### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="58f5c-301">Q#Code uit andere projecten of pakketten gebruiken</span><span class="sxs-lookup"><span data-stu-id="58f5c-301">Using Q# code from other projects or packages</span></span>

<span data-ttu-id="58f5c-302">Standaard worden in een Q# Jupyter notebook alle `.qs` bestanden in de huidige map geladen en Q# worden de bewerkingen en functies beschikbaar voor gebruik in het notitie blok.</span><span class="sxs-lookup"><span data-stu-id="58f5c-302">By default, a Q# Jupyter Notebook loads all of the `.qs` files in the current folder and makes their Q# operations and functions available for use from inside the notebook.</span></span> <span data-ttu-id="58f5c-303">De [ `%who` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.who) bevat een lijst met alle momenteel beschik bare Q# bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="58f5c-303">The [`%who` magic command](xref:microsoft.quantum.iqsharp.magic-ref.who) lists all currently-available Q# operations and functions.</span></span>

<span data-ttu-id="58f5c-304">Als u Q# code uit een andere map wilt laden, kunt u de [ `%project` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.project) gebruiken om een verwijzing naar een `.csproj` bestand voor een project toe te voegen Q# (dat wil zeggen, een project waarnaar wordt verwezen `Microsoft.Quantum.Sdk` ).</span><span class="sxs-lookup"><span data-stu-id="58f5c-304">To load Q# code from another folder, the [`%project` magic command](xref:microsoft.quantum.iqsharp.magic-ref.project) can be used to add a reference to a `.csproj` file for a Q# project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span> <span data-ttu-id="58f5c-305">Met deze opdracht worden alle `.qs` bestanden in de map met de `.csproj` (en submappen) gecompileerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-305">This command will compile any `.qs` files in the folder containing the `.csproj` (and subfolders).</span></span> <span data-ttu-id="58f5c-306">Ook worden alle pakketten die via of projecten verwijzen waarnaar wordt `PackageReference` Q# verwezen `ProjectReference` in dat bestand, recursief geladen `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-306">It will also recursively load any packages referenced via `PackageReference` or Q# projects referenced via `ProjectReference` in that `.csproj` file.</span></span> 

<span data-ttu-id="58f5c-307">Zo simuleren de volgende cellen een Q# bewerking vanuit een extern project, waarbij naar het pad van het project wordt verwezen ten opzichte van de huidige map:</span><span class="sxs-lookup"><span data-stu-id="58f5c-307">As an example, the following cells simulate a Q# operation from an external project, where the project path is referenced relative to the current folder:</span></span>

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a Q# operation from an external project" width="773">

<span data-ttu-id="58f5c-308">Als u externe pakketten met Q# code wilt laden, gebruikt u de [ `%package` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).</span><span class="sxs-lookup"><span data-stu-id="58f5c-308">To load external packages containing Q# code, use the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="58f5c-309">Als u een pakket laadt, worden ook aangepaste Magic-opdrachten beschikbaar of worden coderings Programma's weer gegeven die zijn opgenomen in alle assembly's die deel uitmaken van het pakket.</span><span class="sxs-lookup"><span data-stu-id="58f5c-309">Loading a package will also make available any custom magic commands or display encoders that are contained in any assemblies that are part of the package.</span></span>

<span data-ttu-id="58f5c-310">Als u wilt dat externe pakketten of Q# projecten op notebook intialization keer worden geladen, moet u ervoor zorgen dat de notitieblokmap een `.csproj` bestand bevat waarnaar wordt verwezen `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-310">To load external packages or Q# projects at notebook intialization time, ensure that the notebook folder contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="58f5c-311">Voeg in dat `.csproj` de eigenschap toe `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` aan de `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="58f5c-311">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="58f5c-312">Dit geeft een instructie Q# om een of meer items te `ProjectReference` laden `PackageReference` die zijn gevonden in de `.csproj` laad tijd van notebooks.</span><span class="sxs-lookup"><span data-stu-id="58f5c-312">This will instruct IQ# to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` at notebook load time.</span></span>

<span data-ttu-id="58f5c-313">Dit is bijvoorbeeld een eenvoudig `.csproj` bestand dat ervoor zorgt dat Q# het pakket automatisch wordt geladen `Microsoft.Quantum.Chemistry` :</span><span class="sxs-lookup"><span data-stu-id="58f5c-313">For example, here is a simple `.csproj` file that causes IQ# to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

```xml
<Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    <PropertyGroup>
        <OutputType>Library</OutputType>
        <TargetFramework>netstandard2.1</TargetFramework>
        <IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>
    </PropertyGroup>
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Chemistry" Version="0.12.20072031" />
    </ItemGroup>
</Project>
```

> [!NOTE]
> <span data-ttu-id="58f5c-314">Deze aangepaste `<IQSharpLoadAutomatically>` eigenschap is momenteel vereist Q# voor Jupyter notebook hosts, maar in de toekomst kan dit het standaard gedrag voor een bestand zijn dat `.csproj` zich in dezelfde map bevindt als het notitie blok-bestand.</span><span class="sxs-lookup"><span data-stu-id="58f5c-314">Currently this custom `<IQSharpLoadAutomatically>` property is required by Q# Jupyter Notebook hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the notebook file.</span></span>

> [!NOTE]
> <span data-ttu-id="58f5c-315">Momenteel `<QsharpCompile>` wordt de instelling in de `.csproj` wordt genegeerd door Q# Jupyter notebook-hosts en `.qs` worden alle bestanden in de map `.csproj` (inclusief submappen) geladen en gecompileerd.</span><span class="sxs-lookup"><span data-stu-id="58f5c-315">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Q# Jupyter Notebook hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="58f5c-316">Ondersteuning voor `.csproj` instellingen wordt in de toekomst verbeterd (Zie [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) voor meer informatie).</span><span class="sxs-lookup"><span data-stu-id="58f5c-316">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>
