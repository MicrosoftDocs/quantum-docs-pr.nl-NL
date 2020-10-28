---
title: 'Manieren om een programma uit te voeren :::no-loc(Q#):::'
description: "Overzicht van de verschillende manieren om Program ma's uit te voeren :::no-loc(Q#)::: . Vanaf de opdracht prompt, :::no-loc(Q#)::: Jupyter-notebooks en klassieke host-Program ma's in Python of een .net-taal."
author: gillenhaalb
ms.author: a-gibec
ms.date: 05/15/2020
ms.topic: article
uid: microsoft.quantum.guide.host-programs
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: f1a4ef0616a8a3f1548b7a7207cf8cbb9dcc7260
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691703"
---
# <a name="ways-to-run-a-no-locq-program"></a><span data-ttu-id="12fad-104">Manieren om een programma uit te voeren :::no-loc(Q#):::</span><span class="sxs-lookup"><span data-stu-id="12fad-104">Ways to run a :::no-loc(Q#)::: program</span></span>

<span data-ttu-id="12fad-105">Een van de grootste sterke punten van de Quantum Development Kit is de flexibiliteit tussen platforms en ontwikkel omgevingen.</span><span class="sxs-lookup"><span data-stu-id="12fad-105">One of the Quantum Development Kit's greatest strengths is its flexibility across platforms and development environments.</span></span>
<span data-ttu-id="12fad-106">Dit betekent echter ook dat nieuwe :::no-loc(Q#)::: gebruikers zichzelf kunnen vinden of worden overspoeld door de talloze opties die in de [installatie handleiding](xref:microsoft.quantum.install)worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="12fad-106">However, this also means that new :::no-loc(Q#)::: users may find themselves confused or overwhelmed by the numerous options found in the [install guide](xref:microsoft.quantum.install).</span></span>
<span data-ttu-id="12fad-107">Op deze pagina wordt uitgelegd wat er gebeurt wanneer een :::no-loc(Q#)::: programma wordt uitgevoerd en kunt u de verschillende manieren vergelijken waarop gebruikers dit kunnen doen.</span><span class="sxs-lookup"><span data-stu-id="12fad-107">On this page, we explain what happens when a :::no-loc(Q#)::: program is run, and compare the different ways in which users can do so.</span></span>

<span data-ttu-id="12fad-108">Een primair onderscheid is dat :::no-loc(Q#)::: kan worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="12fad-108">A primary distinction is that :::no-loc(Q#)::: can be run:</span></span>
- <span data-ttu-id="12fad-109">als zelfstandige toepassing, waarbij de :::no-loc(Q#)::: enige taal betrokken is en het programma rechtstreeks wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="12fad-109">as a standalone application, where :::no-loc(Q#)::: is the only language involved and the program is invoked directly.</span></span> <span data-ttu-id="12fad-110">In deze categorie vallen twee methoden daad werkelijk:</span><span class="sxs-lookup"><span data-stu-id="12fad-110">Two methods actually fall in this category:</span></span>
  - <span data-ttu-id="12fad-111">de opdracht regel interface</span><span class="sxs-lookup"><span data-stu-id="12fad-111">the command-line interface</span></span>
  - <span data-ttu-id="12fad-112">:::no-loc(Q#)::: Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="12fad-112">:::no-loc(Q#)::: Jupyter Notebooks</span></span>
- <span data-ttu-id="12fad-113">met een extra *hostprogramma* , geschreven in Python of een .net-taal (bijvoorbeeld C# of F #), die vervolgens het programma aanroept en de geretourneerde resultaten verder kan verwerken.</span><span class="sxs-lookup"><span data-stu-id="12fad-113">with an additional *host program* , written in Python or a .NET language (for example, C# or F#), which then invokes the program and can further process returned results.</span></span>

<span data-ttu-id="12fad-114">Voor een beter begrip van deze processen en hun verschillen, kunt u een eenvoudig :::no-loc(Q#)::: programma overwegen en de manieren vergelijken waarop het kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-114">To best understand these processes and their differences, we consider a simple :::no-loc(Q#)::: program and compare the ways it can be run.</span></span>

## <a name="basic-no-locq-program"></a><span data-ttu-id="12fad-115">Basic- :::no-loc(Q#)::: programma</span><span class="sxs-lookup"><span data-stu-id="12fad-115">Basic :::no-loc(Q#)::: program</span></span>

<span data-ttu-id="12fad-116">Een basis Quantum programma kan bestaan uit het voorbereiden van een Qubit in een gelijke superpositie van Staten $ \ket {0} $ en $ \ket {1} $, het meten ervan en het retour neren van het resultaat, dat wille keurig een van beide statussen met een gelijke kans is.</span><span class="sxs-lookup"><span data-stu-id="12fad-116">A basic quantum program might consist of preparing a qubit in an equal superposition of states $\ket{0}$ and $\ket{1}$, measuring it, and returning the result, which will be randomly either one of these two states with equal probability.</span></span>
<span data-ttu-id="12fad-117">Dit proces is inderdaad de kern van de versnelde Generator van de [Quantum wille keurige getallen](xref:microsoft.quantum.quickstarts.qrng) .</span><span class="sxs-lookup"><span data-stu-id="12fad-117">Indeed, this process is at the core of the [quantum random number generator](xref:microsoft.quantum.quickstarts.qrng) quickstart.</span></span>

<span data-ttu-id="12fad-118">In :::no-loc(Q#)::: wordt dit uitgevoerd met de volgende code:</span><span class="sxs-lookup"><span data-stu-id="12fad-118">In :::no-loc(Q#):::, this would be performed by the following code:</span></span>

```qsharp
        using (q = Qubit()) {    // allocates qubit for use (automatically in |0>)
            H(q);                // puts qubit in superposition of |0> and |1>
            return MResetZ(q);   // measures qubit, returns result (and resets it to |0> before deallocation)
        }
```

<span data-ttu-id="12fad-119">Deze code kan echter alleen worden uitgevoerd door :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="12fad-119">However, this code alone can't be run by :::no-loc(Q#):::.</span></span>
<span data-ttu-id="12fad-120">Hiervoor moet de hoofd tekst van een [bewerking](xref:microsoft.quantum.guide.basics#q-operations-and-functions)worden ingesteld, die vervolgens wordt uitgevoerd wanneer---rechtstreeks of door een andere bewerking wordt genoemd.</span><span class="sxs-lookup"><span data-stu-id="12fad-120">For that, it needs to make up the body of an [operation](xref:microsoft.quantum.guide.basics#q-operations-and-functions), which is then run when called---either directly or by another operation.</span></span> <span data-ttu-id="12fad-121">Daarom kunt u een bewerking van het volgende formulier schrijven:</span><span class="sxs-lookup"><span data-stu-id="12fad-121">Hence, you can write an operation of the following form:</span></span>
```qsharp
    operation MeasureSuperposition() : Result {
        using (q = Qubit()) {
            H(q);
            return MResetZ(q);
        }
    }
```
<span data-ttu-id="12fad-122">U hebt een bewerking gedefinieerd, `MeasureSuperposition` die geen invoer heeft en een waarde van het type [resultaat](xref:microsoft.quantum.guide.types)retourneert.</span><span class="sxs-lookup"><span data-stu-id="12fad-122">You have defined an operation, `MeasureSuperposition`, which takes no inputs and returns a value of type [Result](xref:microsoft.quantum.guide.types).</span></span>

<span data-ttu-id="12fad-123">Hoewel de voor beelden op deze pagina alleen bestaan uit :::no-loc(Q#)::: *bewerkingen* , zijn alle concepten die we bespreken gelijk aan de :::no-loc(Q#)::: *functies* en daarom verwijzen ze gezamenlijk naar hun *callables* .</span><span class="sxs-lookup"><span data-stu-id="12fad-123">While the examples on this page only consist of :::no-loc(Q#)::: *operations* , all of the concepts we will discuss pertain equally to :::no-loc(Q#)::: *functions* , and therefore we refer to them collectively as *callables* .</span></span> <span data-ttu-id="12fad-124">Hun verschillen worden besproken op basis van het [ :::no-loc(Q#)::: volgende: bewerkingen en functies](xref:microsoft.quantum.guide.basics#q-operations-and-functions), en meer informatie over het definiëren van ze vindt u op [bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions).</span><span class="sxs-lookup"><span data-stu-id="12fad-124">Their differences are discussed at [:::no-loc(Q#)::: basics: operations and functions](xref:microsoft.quantum.guide.basics#q-operations-and-functions), and more details on defining them can be found at [Operations and functions](xref:microsoft.quantum.guide.operationsfunctions).</span></span>

### <a name="callable-defined-in-a-no-locq-file"></a><span data-ttu-id="12fad-125">Aanroepable gedefinieerd in een :::no-loc(Q#)::: bestand</span><span class="sxs-lookup"><span data-stu-id="12fad-125">Callable defined in a :::no-loc(Q#)::: file</span></span>

<span data-ttu-id="12fad-126">De aanroep zou precies worden aangeroepen en worden uitgevoerd door :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="12fad-126">The callable is precisely what's called and run by :::no-loc(Q#):::.</span></span>
<span data-ttu-id="12fad-127">Er zijn echter enkele extra toevoegingen vereist om een volledig bestand te vormen `*.qs` :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="12fad-127">However, it requires a few more additions to comprise a full `*.qs` :::no-loc(Q#)::: file.</span></span>

<span data-ttu-id="12fad-128">Alle :::no-loc(Q#)::: typen en callables (zowel die u hebt gedefinieerd als de ingebouwde taal) worden gedefinieerd in *naam ruimten* , die elke volledige naam geven waarnaar vervolgens kan worden verwezen.</span><span class="sxs-lookup"><span data-stu-id="12fad-128">All :::no-loc(Q#)::: types and callables (both those you define and those intrinsic to the language) are defined within *namespaces* , which provide each a full name that can then be referenced.</span></span>

<span data-ttu-id="12fad-129">De [`H`](xref:Microsoft.Quantum.Intrinsic.H) bewerkingen en zijn bijvoorbeeld te [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) vinden in de [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) naam ruimten en (onderdeel van de [ :::no-loc(Q#)::: standaard bibliotheken](xref:microsoft.quantum.qsharplibintro)).</span><span class="sxs-lookup"><span data-stu-id="12fad-129">For example, the [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`MResetZ`](xref:Microsoft.Quantum.Measurement.MResetZ) operations are found in the [`Microsoft.Quantum.Instrinsic`](xref:Microsoft.Quantum.Intrinsic) and [`Microsoft.Quantum.Measurement`](xref:Microsoft.Quantum.Measurement) namespaces (part of the [:::no-loc(Q#)::: Standard Libraries](xref:microsoft.quantum.qsharplibintro)).</span></span>
<span data-ttu-id="12fad-130">Zo kunnen ze altijd worden aangeroepen via hun *volledige* naam `Microsoft.Quantum.Intrinsic.H(<qubit>)` en `Microsoft.Quantum.Measurement.MResetZ(<qubit>)` , maar dit wordt altijd wel tot zeer ruime code.</span><span class="sxs-lookup"><span data-stu-id="12fad-130">As such, they can always be called via their *full* names, `Microsoft.Quantum.Intrinsic.H(<qubit>)` and `Microsoft.Quantum.Measurement.MResetZ(<qubit>)`, but always doing this would lead to very cluttered code.</span></span>

<span data-ttu-id="12fad-131">In plaats daarvan `open` kunnen met behulp van de instructies callables worden gerefereerd aan een beknoptere steno, zoals in de bovenstaande hoofd tekst is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-131">Instead, `open` statements allow callables to be referenced with more concise shorthand, as we've done in the operation body above.</span></span>
<span data-ttu-id="12fad-132">Het volledige :::no-loc(Q#)::: bestand met onze bewerking zou daarom bestaan uit het definiëren van onze eigen naam ruimte, het openen van de naam ruimten voor de callables die door onze bewerking worden gebruikt, en de bewerking:</span><span class="sxs-lookup"><span data-stu-id="12fad-132">The full :::no-loc(Q#)::: file containing our operation would therefore consist of defining our own namespace, opening the namespaces for those callables our operation uses, and then our operation:</span></span>

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
> <span data-ttu-id="12fad-133">Naam ruimten kunnen ook worden *gealiasd* wanneer deze worden geopend. Dit kan handig zijn als er sprake is van aanroep bare/type namen in twee naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="12fad-133">Namespaces can also be *aliased* when opened, which can be helpful if callable/type names in two namespaces conflict.</span></span>
> <span data-ttu-id="12fad-134">We kunnen bijvoorbeeld in plaats daarvan `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` hierboven gebruiken en vervolgens aanroepen `H` via `NamespaceWithH.H(<qubit>)` .</span><span class="sxs-lookup"><span data-stu-id="12fad-134">For example, we could instead use `open Microsoft.Quantum.Instrinsic as NamespaceWithH;` above, and then call `H` via `NamespaceWithH.H(<qubit>)`.</span></span>

> [!NOTE]
> <span data-ttu-id="12fad-135">Een uitzonde ring op dit is de [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) naam ruimte, die altijd automatisch wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="12fad-135">One exception to all of this is the [`Microsoft.Quantum.Core`](xref:Microsoft.Quantum.Core) namespace, which is always automatically opened.</span></span>
> <span data-ttu-id="12fad-136">Daarom kan callables bijvoorbeeld [`Length`](xref:Microsoft.Quantum.Core.Length) altijd rechtstreeks worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="12fad-136">Therefore, callables like [`Length`](xref:Microsoft.Quantum.Core.Length) can always be used directly.</span></span>

### <a name="running-on-target-machines"></a><span data-ttu-id="12fad-137">Uitvoeren op doel computers</span><span class="sxs-lookup"><span data-stu-id="12fad-137">Running on target machines</span></span>

<span data-ttu-id="12fad-138">Het algemene model voor het uitvoeren van een :::no-loc(Q#)::: programma wordt nu duidelijk.</span><span class="sxs-lookup"><span data-stu-id="12fad-138">Now the general run model of a :::no-loc(Q#)::: program becomes clear.</span></span>

<br/>
<img src="../media/hostprograms_general_execution_model.png" alt=":::no-loc(Q#)::: program execution diagram" width="400">

<span data-ttu-id="12fad-139">De specifieke aanroepable die moet worden uitgevoerd, heeft eerst toegang tot alle andere callables en typen die in dezelfde naam ruimte zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-139">Firstly, the specific callable to be run has access to any other callables and types defined in the same namespace.</span></span>
<span data-ttu-id="12fad-140">U kunt ook toegang krijgen tot die van een van de [ :::no-loc(Q#)::: bibliotheken](xref:microsoft.quantum.libraries), maar deze moeten worden gerefereerd via de volledige naam of door middel van het gebruik van de `open` hierboven beschreven instructies.</span><span class="sxs-lookup"><span data-stu-id="12fad-140">It also access those from any of the [:::no-loc(Q#)::: libraries](xref:microsoft.quantum.libraries), but those must be referenced either via their full name, or through the use of `open` statements described above.</span></span>

<span data-ttu-id="12fad-141">De aanroepable zelf wordt vervolgens uitgevoerd op een *[doel computer](xref:microsoft.quantum.machines)* .</span><span class="sxs-lookup"><span data-stu-id="12fad-141">The callable itself is then run on a *[target machine](xref:microsoft.quantum.machines)* .</span></span>
<span data-ttu-id="12fad-142">Dergelijke doel computers kunnen echte Quantum hardware zijn of de meerdere simulatoren die beschikbaar zijn als onderdeel van de QDK.</span><span class="sxs-lookup"><span data-stu-id="12fad-142">Such target machines can be actual quantum hardware or the multiple simulators available as part of the QDK.</span></span>
<span data-ttu-id="12fad-143">Voor onze doel einden is de meest nuttige doel computer een exemplaar van de [Full-State Simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator` waarmee het gedrag van het programma wordt berekend alsof het wordt uitgevoerd op een quantum computer zonder ruis.</span><span class="sxs-lookup"><span data-stu-id="12fad-143">For our purposes here, the most useful target machine is an instance of the [full-state simulator](xref:microsoft.quantum.machines.full-state-simulator), `QuantumSimulator`, which calculates the program's behavior as if it were being run on a noise-free quantum computer.</span></span>

<span data-ttu-id="12fad-144">Tot nu toe hebben we beschreven wat er gebeurt wanneer een specifieke :::no-loc(Q#)::: aanroepable wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-144">So far, we've described what happens when a specific :::no-loc(Q#)::: callable is being run.</span></span>
<span data-ttu-id="12fad-145">Ongeacht of het wordt :::no-loc(Q#)::: gebruikt in een zelfstandige toepassing of met een gast programma, is dit algemene proces meer of minder hetzelfde---dus de flexibiliteit van QDK.</span><span class="sxs-lookup"><span data-stu-id="12fad-145">Regardless of whether :::no-loc(Q#)::: is used in a standalone application or with a host program, this general process is more or less the same---hence the QDK's flexibility.</span></span>
<span data-ttu-id="12fad-146">De verschillen tussen de manieren van aanroepen in de Quantum Development Kit geven daarom duidelijk aan *hoe* die :::no-loc(Q#)::: aanroep bare wordt uitgevoerd en op welke manier de resultaten worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-146">The differences between the ways of calling into the Quantum Development Kit therefore reveal themselves in *how* that :::no-loc(Q#)::: callable is called to be run, and in what manner any results are returned.</span></span>
<span data-ttu-id="12fad-147">Meer in het bijzonder zijn de verschillen van belang om:</span><span class="sxs-lookup"><span data-stu-id="12fad-147">More specifically, the differences revolve around:</span></span>

- <span data-ttu-id="12fad-148">Geeft :::no-loc(Q#)::: aan welke aanroepable moet worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="12fad-148">Indicating which :::no-loc(Q#)::: callable is to be run</span></span>
- <span data-ttu-id="12fad-149">Hoe mogelijke aanroep bare argumenten worden gegeven</span><span class="sxs-lookup"><span data-stu-id="12fad-149">How potential callable arguments are provided</span></span>
- <span data-ttu-id="12fad-150">De doel computer opgeven waarop de machine moet worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="12fad-150">Specifying the target machine on which to run it</span></span>
- <span data-ttu-id="12fad-151">Hoe worden de resultaten geretourneerd</span><span class="sxs-lookup"><span data-stu-id="12fad-151">How any results are returned</span></span>

<span data-ttu-id="12fad-152">Eerst bespreken we hoe dit wordt gedaan met de :::no-loc(Q#)::: zelfstandige toepassing vanaf de opdracht prompt en gaat u verder met het gebruik van python-en C#-host-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="12fad-152">First, we discuss how this is done with the :::no-loc(Q#)::: standalone application from the command prompt, and then proceed to using Python and C# host programs.</span></span>
<span data-ttu-id="12fad-153">We behouden de zelfstandige toepassing van :::no-loc(Q#)::: Jupyter-notebooks voor het laatst aan, omdat de primaire functionaliteit in tegens telling tot de eerste drie niet is gecentreerd rond een lokaal :::no-loc(Q#)::: bestand.</span><span class="sxs-lookup"><span data-stu-id="12fad-153">We reserve the standalone application of :::no-loc(Q#)::: Jupyter Notebooks for last, because unlike the first three, it's primary functionality does not center around a local :::no-loc(Q#)::: file.</span></span>

> [!NOTE]
> <span data-ttu-id="12fad-154">Hoewel we dit niet in deze voor beelden illustreren, is een gemeen schappelijke methode tussen de run-methoden dat alle berichten die vanuit het programma worden afgedrukt :::no-loc(Q#)::: (via [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) of [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine) bijvoorbeeld), doorgaans altijd worden afgedrukt op de respectieve console.</span><span class="sxs-lookup"><span data-stu-id="12fad-154">Although we don't illustrate it in these examples, one commonality between the run methods is that any messages printed from inside the :::no-loc(Q#)::: program (by way of [`Message`](xref:Microsoft.Quantum.Intrinsic.Message) or [`DumpMachine`](xref:Microsoft.Quantum.Diagnostics.DumpMachine), for example) will typically always be printed to the respective console.</span></span>

## <a name="no-locq-from-the-command-prompt"></a><span data-ttu-id="12fad-155">:::no-loc(Q#)::: vanaf de opdracht prompt</span><span class="sxs-lookup"><span data-stu-id="12fad-155">:::no-loc(Q#)::: from the command prompt</span></span>
<span data-ttu-id="12fad-156">Een van de eenvoudigste manieren om aan de slag te gaan met het schrijven :::no-loc(Q#)::: van Program ma's is om te voor komen dat u zich zorgen maakt over afzonderlijke bestanden en een tweede taal.</span><span class="sxs-lookup"><span data-stu-id="12fad-156">One of the easiest ways to get started writing :::no-loc(Q#)::: programs is to avoid worrying about separate files and a second language altogether.</span></span>
<span data-ttu-id="12fad-157">Het gebruik van Visual Studio code of Visual Studio met de QDK-extensie biedt een naadloze werk stroom waarbij we :::no-loc(Q#)::: callables uit slechts één :::no-loc(Q#)::: bestand uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="12fad-157">Using Visual Studio Code or Visual Studio with the QDK extension allows for a seamless work flow in which we run :::no-loc(Q#)::: callables from only a single :::no-loc(Q#)::: file.</span></span>

<span data-ttu-id="12fad-158">Hiervoor voert u het programma uiteindelijk uit door het volgende in te voeren:</span><span class="sxs-lookup"><span data-stu-id="12fad-158">For this, we will ultimately run the program by entering</span></span>

```dotnetcli
dotnet run
```

<span data-ttu-id="12fad-159">bij de opdracht prompt.</span><span class="sxs-lookup"><span data-stu-id="12fad-159">at the command prompt.</span></span>
<span data-ttu-id="12fad-160">De eenvoudigste werk stroom is wanneer de locatie van de map van de Terminal gelijk is aan die van het :::no-loc(Q#)::: bestand, dat eenvoudig kan worden verwerkt naast het :::no-loc(Q#)::: bewerken van bestanden met behulp van de geïntegreerde terminal in VS code.</span><span class="sxs-lookup"><span data-stu-id="12fad-160">The simplest workflow is when the terminal's directory location is the same as the :::no-loc(Q#)::: file, which can be easily handled alongside :::no-loc(Q#)::: file editing by using the integrated terminal in VS Code, for example.</span></span>
<span data-ttu-id="12fad-161">De [ `dotnet run` opdracht](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepteert echter talloze opties en het programma kan ook worden uitgevoerd vanaf een andere locatie door simpelweg `--project <PATH>` de locatie van het bestand op te geven :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="12fad-161">However, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) accepts numerous options, and the program can also be run from a different location by simply providing `--project <PATH>` with the location of the :::no-loc(Q#)::: file.</span></span>


### <a name="add-entry-point-to-no-locq-file"></a><span data-ttu-id="12fad-162">Invoer punt toevoegen aan :::no-loc(Q#)::: bestand</span><span class="sxs-lookup"><span data-stu-id="12fad-162">Add entry point to :::no-loc(Q#)::: file</span></span>

<span data-ttu-id="12fad-163">De meeste :::no-loc(Q#)::: bestanden bevatten meer dan één aanroepable, dus we moeten er natuurlijk voor zorgen dat de compiler weet *welke* aanroep kan worden uitgevoerd wanneer we de `dotnet run` opdracht opgeven.</span><span class="sxs-lookup"><span data-stu-id="12fad-163">Most :::no-loc(Q#)::: files will contain more than one callable, so naturally we need to let the compiler know *which* callable to run when we provide the `dotnet run` command.</span></span>
<span data-ttu-id="12fad-164">Dit wordt gedaan met een eenvoudige wijziging in het :::no-loc(Q#)::: bestand zelf:</span><span class="sxs-lookup"><span data-stu-id="12fad-164">This is done with a simple change to the :::no-loc(Q#)::: file itself:</span></span> 
    - <span data-ttu-id="12fad-165">Voeg een regel toe met `@EntryPoint()` de direct voorafgaande oproep bare.</span><span class="sxs-lookup"><span data-stu-id="12fad-165">add a line with `@EntryPoint()` directly preceding the callable.</span></span>

<span data-ttu-id="12fad-166">Ons bestand van bovenstaande zou daarom worden</span><span class="sxs-lookup"><span data-stu-id="12fad-166">Our file from above would therefore become</span></span>
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

<span data-ttu-id="12fad-167">Nu wordt een aanroep van `dotnet run` vanaf de opdracht prompt om te `MeasureSuperposition` worden uitgevoerd en wordt de geretourneerde waarde vervolgens rechtstreeks naar de Terminal afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="12fad-167">Now, a call of `dotnet run` from the command prompt leads to `MeasureSuperposition` being run, and the returned value is then printed directly to the terminal.</span></span>
<span data-ttu-id="12fad-168">Daarom ziet u ofwel `One` of `Zero` afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="12fad-168">So, you will see either `One` or `Zero` printed.</span></span> 

<span data-ttu-id="12fad-169">Houd er rekening mee dat het niet van belang is dat er meer callables worden gedefinieerd, maar alleen `MeasureSuperposition` worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-169">Note that it doesn't matter if you have more callables defined below it, only `MeasureSuperposition` will be run.</span></span>
<span data-ttu-id="12fad-170">Daarnaast is het geen probleem als uw aanroep mogelijk [documentatie commentaar](xref:microsoft.quantum.guide.filestructure#documentation-comments) bevat vóór de declaratie van het `@EntryPoint()` kenmerk, maar dit kan eenvoudigweg worden geplaatst.</span><span class="sxs-lookup"><span data-stu-id="12fad-170">Additionally, it's no problem if your callable includes [documentation comments](xref:microsoft.quantum.guide.filestructure#documentation-comments) before its declaration, the `@EntryPoint()` attribute can be simply placed above them.</span></span>

### <a name="callable-arguments"></a><span data-ttu-id="12fad-171">Aanroep bare argumenten</span><span class="sxs-lookup"><span data-stu-id="12fad-171">Callable arguments</span></span>

<span data-ttu-id="12fad-172">Tot nu toe hebben we alleen een bewerking gezien die geen invoer heeft.</span><span class="sxs-lookup"><span data-stu-id="12fad-172">So far, we've only considered an operation that takes no inputs.</span></span>
<span data-ttu-id="12fad-173">Stel dat we een vergelijk bare bewerking willen uitvoeren, maar op meerdere qubits---het aantal dat als argument wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="12fad-173">Suppose we wanted to perform a similar operation, but on multiple qubits---the number of which is provided as an argument.</span></span>
<span data-ttu-id="12fad-174">Een dergelijke bewerking kan worden geschreven als</span><span class="sxs-lookup"><span data-stu-id="12fad-174">Such an operation could be written as</span></span>
```qsharp
    operation MeasureSuperpositionArray(n : Int) : Result[] {
        using (qubits = Qubit[n]) {              // allocate a register of n qubits
            ApplyToEach(H, qubits);              // apply H to each qubit in the register
            return ForEach(MResetZ, qubits);     // perform MResetZ on each qubit, returns the resulting array
        }
    }
```
<span data-ttu-id="12fad-175">waarbij de geretourneerde waarde een matrix is van de meet resultaten.</span><span class="sxs-lookup"><span data-stu-id="12fad-175">where the returned value is an array of the measurement results.</span></span>
<span data-ttu-id="12fad-176">Houd er rekening mee dat [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) en [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) zich in de en de naam ruimte bevindt [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) . hiervoor [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) moeten aanvullende instructies worden vereist `open` .</span><span class="sxs-lookup"><span data-stu-id="12fad-176">Note that [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) and [`ForEach`](xref:Microsoft.Quantum.Arrays.ForEach) are in the [`Microsoft.Quantum.Canon`](xref:Microsoft.Quantum.Canon) and [`Microsoft.Quantum.Arrays`](xref:Microsoft.Quantum.Arrays) namespaces, requiring additional `open` statements for each.</span></span>

<span data-ttu-id="12fad-177">Als we het `@EntryPoint()` kenmerk voorafgaand aan deze nieuwe bewerking verplaatsen (Houd er dan rekening mee dat er slechts één regel in een bestand kan worden uitgevoerd). er wordt geprobeerd deze uit te voeren met alleen `dotnet run` resultaten in een fout bericht dat aangeeft welke extra opdracht regel opties vereist zijn en hoe u deze kunt uitdrukken.</span><span class="sxs-lookup"><span data-stu-id="12fad-177">If we move the `@EntryPoint()` attribute to precede this new operation (note there can only be one such line in a file), attempting to run it with simply `dotnet run` results in an error message which indicates what additional command-line options are required, and how to express them.</span></span>

<span data-ttu-id="12fad-178">De algemene notatie voor de opdracht regel is in werkelijkheid `dotnet run [options]` en aanroep bare argumenten worden daar vermeld.</span><span class="sxs-lookup"><span data-stu-id="12fad-178">The general format for the command line is actually `dotnet run [options]`, and callable arguments are provided there.</span></span>
<span data-ttu-id="12fad-179">In dit geval ontbreekt het argument `n` en ziet u dat we de optie moeten opgeven `-n <n>` .</span><span class="sxs-lookup"><span data-stu-id="12fad-179">In this case, the argument `n` is missing, and it shows that we need to provide the option `-n <n>`.</span></span> <span data-ttu-id="12fad-180">Om uit te voeren `MeasureSuperpositionArray` voor `n=4` qubits, gebruiken we daarom</span><span class="sxs-lookup"><span data-stu-id="12fad-180">To run `MeasureSuperpositionArray` for `n=4` qubits, we therefore use</span></span>

```dotnetcli
dotnet run -n 4
```

<span data-ttu-id="12fad-181">levert een uitvoer op die vergelijkbaar is met</span><span class="sxs-lookup"><span data-stu-id="12fad-181">yielding an output similar to</span></span>

```output
[Zero,One,One,One]
```

<span data-ttu-id="12fad-182">Deze cursus wordt uitgebreid naar meerdere argumenten.</span><span class="sxs-lookup"><span data-stu-id="12fad-182">This of course extends to multiple arguments.</span></span>

> [!NOTE]
> <span data-ttu-id="12fad-183">Argument namen die zijn gedefinieerd in `camelCase` , worden enigszins gewijzigd door de compiler om te worden geaccepteerd als :::no-loc(Q#)::: invoer.</span><span class="sxs-lookup"><span data-stu-id="12fad-183">Argument names defined in `camelCase` are slightly altered by the compiler to be accepted as :::no-loc(Q#)::: inputs.</span></span> <span data-ttu-id="12fad-184">Als `n` we bijvoorbeeld de bovenstaande naam hebben gebruikt `numQubits` , wordt deze invoer opgegeven in de opdracht regel in `--num-qubits 4` plaats van `-n 4` .</span><span class="sxs-lookup"><span data-stu-id="12fad-184">For example, if instead of `n`, we used the name `numQubits` above, then this input would be provided in the command line via `--num-qubits 4` instead of `-n 4`.</span></span>

<span data-ttu-id="12fad-185">Het fout bericht bevat ook andere opties die kunnen worden gebruikt, met inbegrip van het wijzigen van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="12fad-185">The error message also provides other options which can be used, including how to change the target machine.</span></span>

### <a name="different-target-machines"></a><span data-ttu-id="12fad-186">Verschillende doel computers</span><span class="sxs-lookup"><span data-stu-id="12fad-186">Different target machines</span></span>

<span data-ttu-id="12fad-187">Omdat de uitvoer van onze activiteiten tot nu toe de verwachte resultaten van hun actie op echte qubits was, is het duidelijk dat de standaard doel computer van de opdracht regel de Full-State Quantum Simulator is `QuantumSimulator` .</span><span class="sxs-lookup"><span data-stu-id="12fad-187">As the outputs from our operations thus far have been the expected results of their action on real qubits, it's clear that the default target machine from the command line is the full-state quantum simulator, `QuantumSimulator`.</span></span>
<span data-ttu-id="12fad-188">We kunnen er echter voor zorgen dat callables worden uitgevoerd op een specifieke doel computer met de optie `--simulator` (of de steno `-s` ).</span><span class="sxs-lookup"><span data-stu-id="12fad-188">However, we can instruct callables to be run on a specific target machine with the option `--simulator` (or the shorthand `-s`).</span></span>

<span data-ttu-id="12fad-189">Dit kan bijvoorbeeld worden uitgevoerd op [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) :</span><span class="sxs-lookup"><span data-stu-id="12fad-189">For example, we could run it on [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator):</span></span>

```dotnetcli
dotnet run -n 4 -s ResourcesEstimator
```

<span data-ttu-id="12fad-190">De afgedrukte uitvoer wordt vervolgens</span><span class="sxs-lookup"><span data-stu-id="12fad-190">The printed output is then</span></span>

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

<span data-ttu-id="12fad-191">Zie [resource Estimator: metrische](xref:microsoft.quantum.machines.resources-estimator#metrics-reported)gegevens voor meer informatie over wat deze metrische gegevens aangeven.</span><span class="sxs-lookup"><span data-stu-id="12fad-191">For details on what these metrics indicate, see [Resource estimator: metrics reported](xref:microsoft.quantum.machines.resources-estimator#metrics-reported).</span></span>

### <a name="command-line-run-summary"></a><span data-ttu-id="12fad-192">Overzicht van uitvoering van opdracht regel</span><span class="sxs-lookup"><span data-stu-id="12fad-192">Command line run summary</span></span>
<br/>
<img src="../media/hostprograms_command_line_diagram.png" alt=":::no-loc(Q#)::: program from command line" width="700">

### <a name="non-no-locq-dotnet-run-options"></a><span data-ttu-id="12fad-193">Niet- :::no-loc(Q#)::: `dotnet run` Opties</span><span class="sxs-lookup"><span data-stu-id="12fad-193">Non-:::no-loc(Q#)::: `dotnet run` options</span></span>

<span data-ttu-id="12fad-194">Zoals hierboven hierboven vermeld met de `--project` optie, accepteert de [ `dotnet run` opdracht](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) ook opties die niet gerelateerd zijn aan de :::no-loc(Q#)::: aanroep bare argumenten.</span><span class="sxs-lookup"><span data-stu-id="12fad-194">As we briefly mentioned above with the `--project` option, the [`dotnet run` command](https://docs.microsoft.com/dotnet/core/tools/dotnet-run) also accepts options unrelated to the :::no-loc(Q#)::: callable arguments.</span></span>
<span data-ttu-id="12fad-195">Als u beide soorten opties opgeeft, `dotnet` moeten de specifieke opties eerst worden opgegeven, gevolgd door een delimiter `--` , en vervolgens de :::no-loc(Q#)::: -specifieke opties.</span><span class="sxs-lookup"><span data-stu-id="12fad-195">If providing both kinds of options, the `dotnet`-specific options must be provided first, followed by a delimeter `--`, and then the :::no-loc(Q#):::-specific options.</span></span>
<span data-ttu-id="12fad-196">U kunt bijvoorbeeld een pad opgeven dat samen met een aantal qubits voor de bovenstaande bewerking wordt uitgevoerd via `dotnet run --project <PATH> -- -n <n>` .</span><span class="sxs-lookup"><span data-stu-id="12fad-196">For example, specifying a path along with a number qubits for the operation above would be run via `dotnet run --project <PATH> -- -n <n>`.</span></span>

## <a name="no-locq-with-host-programs"></a><span data-ttu-id="12fad-197">:::no-loc(Q#)::: met host-Program ma's</span><span class="sxs-lookup"><span data-stu-id="12fad-197">:::no-loc(Q#)::: with host programs</span></span>

<span data-ttu-id="12fad-198">Met ons :::no-loc(Q#)::: bestand is een alternatief voor het aanroepen van een bewerking of functie rechtstreeks vanaf de opdracht prompt het gebruik van een *hostprogramma* in een andere klassieke taal.</span><span class="sxs-lookup"><span data-stu-id="12fad-198">With our :::no-loc(Q#)::: file in hand, an alternative to calling an operation or function directly from the command prompt is to use a *host program* in another classical language.</span></span> <span data-ttu-id="12fad-199">Dit kan met name worden gedaan met python of een .NET-taal, zoals C# of F # (in het geval van een beknopt overzicht van de informatie over C#.</span><span class="sxs-lookup"><span data-stu-id="12fad-199">Specifically, this can be done with either Python or a .NET language such as C# or F# (for the sake of brevity we will only detail C# here).</span></span>
<span data-ttu-id="12fad-200">Er zijn nog meer instellingen vereist om de interoperabiliteit in te scha kelen, maar u kunt deze details vinden in de [installatie handleidingen](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="12fad-200">A little more setup is required to enable the interoperability, but those details can be found in the [install guides](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="12fad-201">In een kort gezegd bevat de situatie nu een bestand voor het hostprogramma (bijvoorbeeld `*.py` of `*.cs` ) op dezelfde locatie als het :::no-loc(Q#)::: bestand.</span><span class="sxs-lookup"><span data-stu-id="12fad-201">In a nutshell, the situation now includes a host program file (for example, `*.py` or `*.cs`) in the same location as our :::no-loc(Q#)::: file.</span></span>
<span data-ttu-id="12fad-202">Het is nu het *hostprogramma* dat wordt uitgevoerd en wanneer het wordt uitgevoerd, kan het specifieke :::no-loc(Q#)::: bewerkingen en functies vanuit het bestand aanroepen :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="12fad-202">It's now the *host* program that gets run, and while it is running, it can call specific :::no-loc(Q#)::: operations and functions from the :::no-loc(Q#)::: file.</span></span>
<span data-ttu-id="12fad-203">De kern van de interoperabiliteit is gebaseerd op de :::no-loc(Q#)::: compiler die de inhoud van het :::no-loc(Q#)::: bestand toegankelijk maakt voor het hostprogramma, zodat deze kan worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="12fad-203">The core of the interoperability is based on the :::no-loc(Q#)::: compiler making the contents of the :::no-loc(Q#)::: file accessible to the host program so that they can be called.</span></span>

<span data-ttu-id="12fad-204">Een van de belangrijkste voor delen van het gebruik van een hostprogramma is dat de klassieke gegevens die door het :::no-loc(Q#)::: programma worden geretourneerd, vervolgens verder kunnen worden verwerkt in de taal van de host.</span><span class="sxs-lookup"><span data-stu-id="12fad-204">One of the main benefits of using a host program is that the classical data returned by the :::no-loc(Q#)::: program can then be further processed in the host language.</span></span>
<span data-ttu-id="12fad-205">Dit kan bestaan uit een aantal geavanceerde gegevens verwerking (bijvoorbeeld iets dat niet intern kan worden uitgevoerd :::no-loc(Q#)::: ) en vervolgens aanroepen van verdere :::no-loc(Q#)::: acties op basis van deze resultaten, of iets zo eenvoudig als het uitzetten van de :::no-loc(Q#)::: resultaten.</span><span class="sxs-lookup"><span data-stu-id="12fad-205">This could consist of some advanced data processing (for example, something that can't be performed internally in :::no-loc(Q#):::), and then calling further :::no-loc(Q#)::: actions based on those results, or something as simple as plotting the :::no-loc(Q#)::: results.</span></span>

<span data-ttu-id="12fad-206">Het algemene schema wordt hier weer gegeven en we bespreken de specifieke implementaties voor python en C# hieronder.</span><span class="sxs-lookup"><span data-stu-id="12fad-206">The general scheme is shown here, and we discuss the specific implementations for Python and C# below.</span></span> <span data-ttu-id="12fad-207">Een voor beeld van het gebruik van een F #-hostprogramma vindt u in de voor [beelden van .net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="12fad-207">A sample using an F# host program can be found at the [.NET interoperability samples](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

<br/>
<img src="../media/hostprograms_host_program_diagram.png" alt=":::no-loc(Q#)::: program from a host program" width="700">

> [!NOTE]
> <span data-ttu-id="12fad-208">Het `@EntryPoint()` kenmerk dat voor toepassingen wordt gebruikt, :::no-loc(Q#)::: kan niet worden gebruikt met host-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="12fad-208">The `@EntryPoint()` attribute used for :::no-loc(Q#)::: applications cannot be used with host programs.</span></span>
> <span data-ttu-id="12fad-209">Er wordt een fout gegenereerd als deze aanwezig is in het :::no-loc(Q#)::: bestand dat wordt aangeroepen door een host.</span><span class="sxs-lookup"><span data-stu-id="12fad-209">An error will be raised if it is present in the :::no-loc(Q#)::: file being called by a host.</span></span> 

<span data-ttu-id="12fad-210">Als u wilt werken met andere host-Program ma's, hoeft u geen wijzigingen aan te brengen in een `*.qs` :::no-loc(Q#)::: bestand.</span><span class="sxs-lookup"><span data-stu-id="12fad-210">To work with different host programs, there are no changes required to a `*.qs` :::no-loc(Q#)::: file.</span></span>
<span data-ttu-id="12fad-211">De volgende implementaties van een host-programma werken allemaal met hetzelfde :::no-loc(Q#)::: bestand:</span><span class="sxs-lookup"><span data-stu-id="12fad-211">The following host program implementations all work with the same :::no-loc(Q#)::: file:</span></span>

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

<span data-ttu-id="12fad-212">Selecteer het tabblad dat overeenkomt met de taal van uw host.</span><span class="sxs-lookup"><span data-stu-id="12fad-212">Select the tab corresponding to your host language of interest.</span></span>

### <a name="python"></a>[<span data-ttu-id="12fad-213">Python</span><span class="sxs-lookup"><span data-stu-id="12fad-213">Python</span></span>](#tab/tabid-python)
<span data-ttu-id="12fad-214">Een python-hostprogramma is als volgt samengesteld:</span><span class="sxs-lookup"><span data-stu-id="12fad-214">A Python host program is constructed as follows:</span></span>
1. <span data-ttu-id="12fad-215">Importeer de `qsharp` module, die de module lader voor interoperabiliteit registreert :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="12fad-215">Import the `qsharp` module, which registers the module loader for :::no-loc(Q#)::: interoperability.</span></span> 
    <span data-ttu-id="12fad-216">Op die manier kunnen :::no-loc(Q#)::: naam ruimten worden weer gegeven als python-modules, waaruit we callables kunnen importeren :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="12fad-216">This allows :::no-loc(Q#)::: namespaces to appear as Python modules, from which we can "import" :::no-loc(Q#)::: callables.</span></span>
    <span data-ttu-id="12fad-217">Houd er rekening mee dat het technisch gezien niet het :::no-loc(Q#)::: callables is dat wordt geïmporteerd, maar dat er python-stubs zijn waarmee ze kunnen worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="12fad-217">Note that it is technically not the :::no-loc(Q#)::: callables themselves which are imported, but rather Python stubs which allow calling into them.</span></span>
    <span data-ttu-id="12fad-218">Deze gedragen zich als objecten van python-klassen.</span><span class="sxs-lookup"><span data-stu-id="12fad-218">These behave as objects of Python classes.</span></span> <span data-ttu-id="12fad-219">We gebruiken methoden op deze objecten om de doel machines op te geven waarnaar we de bewerking verzenden wanneer het programma wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-219">We use methods on these objects to specify the target machines that we send the operation to when running the program.</span></span>

2. <span data-ttu-id="12fad-220">Importeer de :::no-loc(Q#)::: callables die in dit geval direct---worden aangeroepen, `MeasureSuperposition` en `MeasureSuperpositionArray` .</span><span class="sxs-lookup"><span data-stu-id="12fad-220">Import those :::no-loc(Q#)::: callables which we will directly invoke---in this case, `MeasureSuperposition` and `MeasureSuperpositionArray`.</span></span>
    ```python
    import qsharp
    from NamespaceName import MeasureSuperposition, MeasureSuperpositionArray
    ```
    <span data-ttu-id="12fad-221">Als de `qsharp` module is geïmporteerd, kunt u ook rechtstreeks vanuit de :::no-loc(Q#)::: bibliotheek naam ruimten callables importeren.</span><span class="sxs-lookup"><span data-stu-id="12fad-221">With the `qsharp` module imported, you can also import callables directly from the :::no-loc(Q#)::: library namespaces.</span></span>

3. <span data-ttu-id="12fad-222">Onder andere python-code kunt u deze callables op specifieke doel computers aanroepen en de bijbehorende retour waarden toewijzen aan variabelen (als ze een waarde Retour neren) voor verder gebruik.</span><span class="sxs-lookup"><span data-stu-id="12fad-222">Among any other Python code, you can now call those callables on specific target machines, and assign their returns to variables (if they return a value) for further use.</span></span>

#### <a name="specifying-target-machines"></a><span data-ttu-id="12fad-223">Doel machines opgeven</span><span class="sxs-lookup"><span data-stu-id="12fad-223">Specifying target machines</span></span>
<span data-ttu-id="12fad-224">Het aanroepen van een bewerking die moet worden uitgevoerd op een specifieke doel computer, wordt uitgevoerd via verschillende python-methoden voor het geïmporteerde object.</span><span class="sxs-lookup"><span data-stu-id="12fad-224">Calling an operation to be run on a specific target machine is done via different Python methods on the imported object.</span></span>
<span data-ttu-id="12fad-225">`.simulate(<args>)`Maakt bijvoorbeeld gebruik `QuantumSimulator` van de om de bewerking uit te voeren, terwijl dat `.estimate_resources(<args>)` wel het geval is `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="12fad-225">For example, `.simulate(<args>)`, uses the `QuantumSimulator` to run the operation, whereas `.estimate_resources(<args>)` does so on the `ResourcesEstimator`.</span></span>

#### <a name="passing-inputs-to-q"></a><span data-ttu-id="12fad-226">Invoer door geven aan Q\#</span><span class="sxs-lookup"><span data-stu-id="12fad-226">Passing inputs to Q\#</span></span>
<span data-ttu-id="12fad-227">Argumenten voor de :::no-loc(Q#)::: aanroepable moeten worden aangegeven in de vorm van een trefwoord argument, waarbij het sleutel woord de argument naam in de :::no-loc(Q#)::: aanroep bare definitie is.</span><span class="sxs-lookup"><span data-stu-id="12fad-227">Arguments for the :::no-loc(Q#)::: callable should be provided in the form of a keyword argument, where the keyword is the argument name in the :::no-loc(Q#)::: callable definition.</span></span>
<span data-ttu-id="12fad-228">Dat wil zeggen, `MeasureSuperpositionArray.simulate(n=4)` is geldig, terwijl `MeasureSuperpositionArray.simulate(4)` een fout optreedt.</span><span class="sxs-lookup"><span data-stu-id="12fad-228">That is, `MeasureSuperpositionArray.simulate(n=4)` is valid, whereas `MeasureSuperpositionArray.simulate(4)` would throw an error.</span></span>

<span data-ttu-id="12fad-229">Daarom wordt het python-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="12fad-229">Therefore, the Python host program</span></span> 

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

<span data-ttu-id="12fad-230">resulteert in een uitvoer zoals de volgende:</span><span class="sxs-lookup"><span data-stu-id="12fad-230">results in an output like the following:</span></span>

```output
Single qubit:
1
{'CNOT': 0, 'QubitClifford': 1, 'R': 0, 'Measure': 1, 'T': 0, 'Depth': 0, 'Width': 1, 'BorrowedWidth': 0}

Multiple qubits:
[0, 1, 1, 1]
{'CNOT': 0, 'QubitClifford': 4, 'R': 0, 'Measure': 4, 'T': 0, 'Depth': 0, 'Width': 4, 'BorrowedWidth': 0}
```

#### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="12fad-231">:::no-loc(Q#):::Code uit andere projecten of pakketten gebruiken</span><span class="sxs-lookup"><span data-stu-id="12fad-231">Using :::no-loc(Q#)::: code from other projects or packages</span></span>

<span data-ttu-id="12fad-232">Standaard `import qsharp` laadt de opdracht alle `.qs` bestanden in de huidige map en :::no-loc(Q#)::: worden de bewerkingen en functies beschikbaar voor gebruik in het python-script.</span><span class="sxs-lookup"><span data-stu-id="12fad-232">By default, the `import qsharp` command loads all of the `.qs` files in the current folder and makes their :::no-loc(Q#)::: operations and functions available for use from inside the Python script.</span></span>

<span data-ttu-id="12fad-233">Als u :::no-loc(Q#)::: code wilt laden vanuit een andere map, kan de [ `qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) worden gebruikt voor het toevoegen van een verwijzing naar een `.csproj` bestand voor een :::no-loc(Q#)::: project (dat wil zeggen een project waarnaar wordt verwezen `Microsoft.Quantum.Sdk` ).</span><span class="sxs-lookup"><span data-stu-id="12fad-233">To load :::no-loc(Q#)::: code from another folder, the [`qsharp.projects` API](https://docs.microsoft.com/python/qsharp-core/qsharp.projects.projects) can be used to add a reference to a `.csproj` file for a :::no-loc(Q#)::: project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span>
<span data-ttu-id="12fad-234">Met deze opdracht worden alle `.qs` bestanden in de map die de submappen bevat, gecompileerd `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="12fad-234">This command will compile any `.qs` files in the folder containing the `.csproj` and its subfolders.</span></span> <span data-ttu-id="12fad-235">Ook worden alle pakketten die via of projecten verwijzen waarnaar wordt `PackageReference` :::no-loc(Q#)::: verwezen `ProjectReference` in dat bestand, recursief geladen `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="12fad-235">It will also recursively load any packages referenced via `PackageReference` or :::no-loc(Q#)::: projects referenced via `ProjectReference` in that `.csproj` file.</span></span>

<span data-ttu-id="12fad-236">Met de volgende python-code wordt bijvoorbeeld een extern project geïmporteerd, dat verwijst naar het pad ten opzichte van de huidige map en wordt een van de :::no-loc(Q#)::: bewerkingen aangeroepen:</span><span class="sxs-lookup"><span data-stu-id="12fad-236">As an example, the following Python code imports an external project, referencing its path relative to the current folder, and invokes one of its :::no-loc(Q#)::: operations:</span></span>

```python
import qsharp
qsharp.projects.add("../qrng/Qrng.csproj")
from Qrng import SampleQuantumRandomNumberGenerator
print(f"Qrng result: {SampleQuantumRandomNumberGenerator.simulate()}")
```

<span data-ttu-id="12fad-237">Dit resulteert in uitvoer als de volgende:</span><span class="sxs-lookup"><span data-stu-id="12fad-237">This results in output like the following:</span></span>

```output
Adding reference to project: ../qrng/Qrng.csproj
Qrng result: 0
```

<span data-ttu-id="12fad-238">Als u externe pakketten wilt laden die :::no-loc(Q#)::: code bevatten, gebruikt u de [ `qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span><span class="sxs-lookup"><span data-stu-id="12fad-238">To load external packages containing :::no-loc(Q#)::: code, use the [`qsharp.packages` API](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages).</span></span>

<span data-ttu-id="12fad-239">Als de :::no-loc(Q#)::: code in de huidige map afhankelijk is van externe projecten of pakketten, kunnen er fouten optreden tijdens `import qsharp` de uitvoering, omdat de afhankelijkheden nog niet zijn geladen.</span><span class="sxs-lookup"><span data-stu-id="12fad-239">If the :::no-loc(Q#)::: code in the current folder depends on external projects or packages, you may see errors when running `import qsharp`, since the dependencies have not yet been loaded.</span></span>
<span data-ttu-id="12fad-240">Als u de vereiste externe pakketten of :::no-loc(Q#)::: projecten tijdens de opdracht wilt laden, moet u `import qsharp` ervoor zorgen dat de map met het python-script een `.csproj` bestand bevat waarnaar wordt verwezen `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="12fad-240">To load required external packages or :::no-loc(Q#)::: projects during the `import qsharp` command, ensure that the folder with the Python script contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="12fad-241">Voeg in dat `.csproj` de eigenschap toe `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` aan de `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="12fad-241">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="12fad-242">Dit geeft de instructie :::no-loc(Q#)::: om een of meer items te `ProjectReference` laden `PackageReference` die zijn gevonden in die `.csproj` tijdens de `import qsharp` opdracht.</span><span class="sxs-lookup"><span data-stu-id="12fad-242">This will instruct I:::no-loc(Q#)::: to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` during the `import qsharp` command.</span></span>

<span data-ttu-id="12fad-243">Dit is bijvoorbeeld een eenvoudig `.csproj` bestand dat ervoor zorgt dat :::no-loc(Q#)::: het pakket automatisch wordt geladen `Microsoft.Quantum.Chemistry` :</span><span class="sxs-lookup"><span data-stu-id="12fad-243">For example, here is a simple `.csproj` file that causes I:::no-loc(Q#)::: to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

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
> <span data-ttu-id="12fad-244">Deze aangepaste `<IQSharpLoadAutomatically>` eigenschap is momenteel vereist voor python-hosts, maar in de toekomst kan dit het standaard gedrag voor een bestand zijn dat `.csproj` zich in dezelfde map bevindt als het python-script.</span><span class="sxs-lookup"><span data-stu-id="12fad-244">Currently this custom `<IQSharpLoadAutomatically>` property is required by Python hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the Python script.</span></span>

> [!NOTE]
> <span data-ttu-id="12fad-245">Momenteel `<QsharpCompile>` wordt de instelling in de `.csproj` wordt genegeerd door python-hosts en `.qs` worden alle bestanden in de map `.csproj` (inclusief submappen) geladen en gecompileerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-245">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by Python hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="12fad-246">Ondersteuning voor `.csproj` instellingen wordt in de toekomst verbeterd (Zie [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) voor meer informatie).</span><span class="sxs-lookup"><span data-stu-id="12fad-246">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>


### <a name="c"></a>[<span data-ttu-id="12fad-247">C#</span><span class="sxs-lookup"><span data-stu-id="12fad-247">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="12fad-248">Een C#-hostprogramma heeft meerdere onderdelen en werkt zeer nauw samen met enkele onderdelen van de QDK, zoals de simulators die zelf zijn gebouwd op C#.</span><span class="sxs-lookup"><span data-stu-id="12fad-248">A C# host program has multiple components, and works very closely with some components of the QDK, such as the simulators, which are themselves built on C#.</span></span>

<span data-ttu-id="12fad-249">De :::no-loc(Q#)::: compiler werkt hier door een overeenkomende C#-naam ruimte te genereren uit de :::no-loc(Q#)::: naam ruimte in het :::no-loc(Q#)::: bestand.</span><span class="sxs-lookup"><span data-stu-id="12fad-249">The :::no-loc(Q#)::: compiler works here by generating an equivalently named C# namespace from the :::no-loc(Q#)::: namespace in our :::no-loc(Q#)::: file.</span></span>
<span data-ttu-id="12fad-250">Daarnaast wordt er een gelijkwaardige C#-klasse gegenereerd voor elk van de :::no-loc(Q#)::: callables of typen die daarin zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-250">It further generates an equivalently named C# class for each of the :::no-loc(Q#)::: callables or types defined therein.</span></span>

<span data-ttu-id="12fad-251">Eerst maken we de klassen die in ons hostprogramma worden gebruikt, beschikbaar met `using` instructies, die ongeveer analagous zijn voor de `open` instructies in ons :::no-loc(Q#)::: bestand:</span><span class="sxs-lookup"><span data-stu-id="12fad-251">First, we make any classes used in our host program available with `using` statements, which are roughly analagous to the `open` statements in our :::no-loc(Q#)::: file:</span></span>

```csharp
using System;
using System.Threading.Tasks;
using Microsoft.Quantum.Simulation.Simulators;    // contains the target machines (for example, QuantumSimulator, ResourcesEstimator)
using NamespaceName;                              // make the :::no-loc(Q#)::: namespace available
```

<span data-ttu-id="12fad-252">Vervolgens declareren we onze C#-naam ruimte, een paar andere bits en delen (Zie het volledige code blok hieronder) en vervolgens een klassieke programmering (bijvoorbeeld voor het berekenen van argumenten voor de :::no-loc(Q#)::: callables).</span><span class="sxs-lookup"><span data-stu-id="12fad-252">Next, we declare our C# namespace, a few other bits and pieces (see the full code block below), and then any classical programming we would like (for example, computing arguments for the :::no-loc(Q#)::: callables).</span></span>
<span data-ttu-id="12fad-253">Dit is niet nodig in ons geval, maar een voor beeld van een dergelijk gebruik is te vinden in het voor  [beeld van .net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span><span class="sxs-lookup"><span data-stu-id="12fad-253">The latter isn't necessary in our case, but an example of such usage can be found at the  [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet).</span></span>

#### <a name="target-machines"></a><span data-ttu-id="12fad-254">Doelcomputers</span><span class="sxs-lookup"><span data-stu-id="12fad-254">Target machines</span></span>

<span data-ttu-id="12fad-255">Als u terugkeert naar :::no-loc(Q#)::: , moeten we een instantie maken van de doel computer waarop we onze bewerkingen zullen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="12fad-255">Getting back to :::no-loc(Q#):::, we must create an instance of whatever target machine we will run our operations on.</span></span>

```csharp
            using var sim = new QuantumSimulator();
```

<span data-ttu-id="12fad-256">Het gebruik van andere doel machines is net zo eenvoudig als het instantiëren van een andere computer, hoewel de manier waarop u dit doet en het verwerken van de geretourneerde items iets anders kan zijn.</span><span class="sxs-lookup"><span data-stu-id="12fad-256">Using other target machines is as simple as instantiating a different one, although the manner of doing so and processing the returns can be slightly different.</span></span>
<span data-ttu-id="12fad-257">Voor het oog op de boog is het [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) nu van toepassing op de voor-en de voor beelden [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span><span class="sxs-lookup"><span data-stu-id="12fad-257">For brevity, we stick to the [`QuantumSimulator`](xref:microsoft.quantum.machines.full-state-simulator) for now, and include the [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) [below](#including-the-resources-estimator).</span></span>

<span data-ttu-id="12fad-258">Elke C#-klasse die is gegenereerd op basis van de :::no-loc(Q#)::: bewerkingen, heeft een `Run` methode, het eerste argument waarvan het doel computer exemplaar moet zijn.</span><span class="sxs-lookup"><span data-stu-id="12fad-258">Each C# class generated from the :::no-loc(Q#)::: operations have a `Run` method, the first argument of which must be the target machine instance.</span></span>
<span data-ttu-id="12fad-259">Daarom gebruiken we om uit te voeren `MeasureSuperposition` op de `QuantumSimulator` `MeasureSuperposition.Run(sim)` .</span><span class="sxs-lookup"><span data-stu-id="12fad-259">So, to run `MeasureSuperposition` on the `QuantumSimulator`, we use `MeasureSuperposition.Run(sim)`.</span></span>
<span data-ttu-id="12fad-260">De geretourneerde resultaten kunnen vervolgens worden toegewezen aan variabelen in C#:</span><span class="sxs-lookup"><span data-stu-id="12fad-260">The returned results can then be assigned to variables in C#:</span></span>

```csharp
            var singleQubitResult = await MeasureSuperposition.Run(sim);
```

> [!NOTE]
> <span data-ttu-id="12fad-261">De `Run` methode wordt asynchroon uitgevoerd, omdat dit het geval is voor echte Quantum hardware `await` . het sleutel woord blokkeert daarom verdere verwerking totdat de taak is voltooid.</span><span class="sxs-lookup"><span data-stu-id="12fad-261">The `Run` method is run asynchronously because this will be the case for real quantum hardware, and therefore the `await` keyword blocks further processing until the task completes.</span></span>

<span data-ttu-id="12fad-262">Als de :::no-loc(Q#)::: aanroep geen retour nering heeft (bijvoorbeeld het retour type `Unit` ), kan de uitvoering nog steeds op dezelfde manier worden uitgevoerd zonder deze aan een variabele toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="12fad-262">If the :::no-loc(Q#)::: callable does not have any returns (for example, it has return type `Unit`), then the run can still be done in the same manner without assigning it to a variable.</span></span>
<span data-ttu-id="12fad-263">In dat geval zou de volledige regel gewoon bestaan uit</span><span class="sxs-lookup"><span data-stu-id="12fad-263">In that case, the entire line would simply consist of</span></span> 
```csharp
await <callable>.Run(<simulator>);
```

#### <a name="arguments"></a><span data-ttu-id="12fad-264">Argumenten</span><span class="sxs-lookup"><span data-stu-id="12fad-264">Arguments</span></span>

<span data-ttu-id="12fad-265">Argumenten die kunnen worden :::no-loc(Q#)::: aangeroepen, worden eenvoudigweg door gegeven als aanvullende argumenten na de doel computer.</span><span class="sxs-lookup"><span data-stu-id="12fad-265">Any arguments to the :::no-loc(Q#)::: callable are simply passed as additional arguments after the target machine.</span></span>
<span data-ttu-id="12fad-266">Daarom worden de resultaten van `MeasureSuperpositionArray` op `n=4` qubits opgehaald via</span><span class="sxs-lookup"><span data-stu-id="12fad-266">Hence the results of `MeasureSuperpositionArray` on `n=4` qubits would fetched via</span></span> 

```csharp
            var multiQubitResult = await MeasureSuperpositionArray.Run(sim, 4);
```

<span data-ttu-id="12fad-267">Een volledig C#-hostprogramma kan er dus als volgt uitzien</span><span class="sxs-lookup"><span data-stu-id="12fad-267">A full C# host program could thus look like</span></span>

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

<span data-ttu-id="12fad-268">Op de locatie van het C#-bestand kan het host-programma worden uitgevoerd vanaf de opdracht prompt door het in te voeren</span><span class="sxs-lookup"><span data-stu-id="12fad-268">At the location of the C# file, the host program can be run from the command prompt by entering</span></span>
```dotnetcli
dotnet run
```
<span data-ttu-id="12fad-269">in dit geval ziet u uitvoer die is geschreven naar de-console, vergelijkbaar met</span><span class="sxs-lookup"><span data-stu-id="12fad-269">and in this case you will see output written to the console similar to</span></span> 
```output
Single qubit result: One
Multiple qubit result: [One,One,Zero,Zero]
```

> [!NOTE]
> <span data-ttu-id="12fad-270">Als gevolg van de interoperabiliteit van de compiler met naam ruimten, kunnen we een andere :::no-loc(Q#)::: callables beschikbaar maken zonder de `using NamespaceName;` -instructie, en alleen de naam van de C#-titel ruimte erop.</span><span class="sxs-lookup"><span data-stu-id="12fad-270">Due to the compiler's interoperability with namespaces, we could alternatively make our :::no-loc(Q#)::: callables available without the `using NamespaceName;` statement, and simply matching the C# namespace title to it.</span></span>
> <span data-ttu-id="12fad-271">Dat wil zeggen door te vervangen door `namespace host` `namespace NamespaceName` .</span><span class="sxs-lookup"><span data-stu-id="12fad-271">That is, by replacing `namespace host` with `namespace NamespaceName`.</span></span>

#### <a name="including-the-resources-estimator"></a><span data-ttu-id="12fad-272">Inclusief de bronnen estimator</span><span class="sxs-lookup"><span data-stu-id="12fad-272">Including the resources estimator</span></span>

<span data-ttu-id="12fad-273">[`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator)Er is een iets andere implementatie vereist om de uitvoer op te halen.</span><span class="sxs-lookup"><span data-stu-id="12fad-273">The [`ResourcesEstimator`](xref:microsoft.quantum.machines.resources-estimator) requires a slightly different implementation to retrieve the output.</span></span>

<span data-ttu-id="12fad-274">In plaats van ze als een variabele te instantiëren met een- `using` instructie (zoals we met de) hebben gedaan `QuantumSimulator` , kunnen we objecten van de klasse direct instantiëren via</span><span class="sxs-lookup"><span data-stu-id="12fad-274">Firstly, instead of instantiating them as a variable with a `using` statement (as we do with the `QuantumSimulator`), we more directly instantiate objects of the class via</span></span>

```csharp
            var estimatorSingleQ = new ResourcesEstimator();
            var estimatorMultiQ = new ResourcesEstimator();
```

<span data-ttu-id="12fad-275">U ziet dat in plaats van één doel-Simulator door meerdere bewerkingen wordt gebruikt :::no-loc(Q#)::: , er één voor elk wordt geïnstantieerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-275">Notice that instead of a single target simulator to be used by multiple :::no-loc(Q#)::: operations, we have instantiated one for each.</span></span> <span data-ttu-id="12fad-276">Dit komt doordat de objecten zelf worden gewijzigd wanneer ze worden gebruikt als doel machines en de resultaten ervan daarna kunnen worden opgehaald met de methode Class `.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="12fad-276">This is because the objects themselves are modified when used as target machines, and their results can then be retrieved afterwards with the class method `.ToTSV()`.</span></span>

<span data-ttu-id="12fad-277">Voor het uitvoeren van de bewerkingen op resource schattingen gebruiken we</span><span class="sxs-lookup"><span data-stu-id="12fad-277">To run the operations on the resource estimators, we use</span></span>

```csharp
            await MeasureSuperposition.Run(estimatorSingleQ);
            await MeasureSuperpositionArray.Run(estimatorMultiQ, 4);
```
<span data-ttu-id="12fad-278">Daarna haalt u de resultaten op als door tabs gescheiden waarden (TSV) met `estimatorSingleQ.ToTSV()` en `estimatorMultiQ.ToTSV()` .</span><span class="sxs-lookup"><span data-stu-id="12fad-278">and then fetch the results as tab-separated-values (TSV) with `estimatorSingleQ.ToTSV()` and `estimatorMultiQ.ToTSV()`.</span></span>

<span data-ttu-id="12fad-279">Een volledig C#-hostprogramma dat zowel het gebruik `QuantumSimulator` als `ResourcesEstimator` het formulier maakt, kan dan het volgende doen:</span><span class="sxs-lookup"><span data-stu-id="12fad-279">So, a full C# host program making use of both the `QuantumSimulator` and `ResourcesEstimator` could take the form:</span></span>

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


<span data-ttu-id="12fad-280">wat resulteert in uitvoer die vergelijkbaar is met</span><span class="sxs-lookup"><span data-stu-id="12fad-280">which would yield output similar to</span></span>

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

## <a name="no-locq-jupyter-notebooks"></a><span data-ttu-id="12fad-281">:::no-loc(Q#)::: Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="12fad-281">:::no-loc(Q#)::: Jupyter Notebooks</span></span>
<span data-ttu-id="12fad-282">:::no-loc(Q#)::: Jupyter-notebooks maken gebruik van de I :::no-loc(Q#)::: -kernel, waarmee u callables in één notitie blok kunt definiëren, compileren en uitvoeren :::no-loc(Q#)::: ---alle naast instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="12fad-282">:::no-loc(Q#)::: Jupyter Notebooks make use of the I:::no-loc(Q#)::: kernel, which allows you to define, compile, and run :::no-loc(Q#)::: callables in a single notebook---all alongside instructions, notes, and other content.</span></span>
<span data-ttu-id="12fad-283">Dit betekent dat hoewel het mogelijk is om de inhoud van bestanden te importeren en `*.qs` :::no-loc(Q#)::: te gebruiken, ze niet nodig zijn in het run model.</span><span class="sxs-lookup"><span data-stu-id="12fad-283">This means that while it is possible to import and use the contents of `*.qs` :::no-loc(Q#)::: files, they are not necessary in the run model.</span></span>

<span data-ttu-id="12fad-284">Hier wordt beschreven hoe u de :::no-loc(Q#)::: hierboven gedefinieerde bewerkingen uitvoert, maar een uitgebreidere inleiding tot het gebruik van :::no-loc(Q#)::: Jupyter-notebooks is beschikbaar op [Inleiding tot :::no-loc(Q#)::: en Jupyter-notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span><span class="sxs-lookup"><span data-stu-id="12fad-284">Here, we will detail how to run the :::no-loc(Q#)::: operations defined above, but a more broad introduction to using :::no-loc(Q#)::: Jupyter Notebooks is provided at [Intro to :::no-loc(Q#)::: and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb).</span></span>

### <a name="defining-operations"></a><span data-ttu-id="12fad-285">Bewerkingen definiëren</span><span class="sxs-lookup"><span data-stu-id="12fad-285">Defining operations</span></span>

<span data-ttu-id="12fad-286">In een :::no-loc(Q#)::: Jupyter notebook voert u code in op :::no-loc(Q#)::: dezelfde manier als in de naam ruimte van een :::no-loc(Q#)::: bestand.</span><span class="sxs-lookup"><span data-stu-id="12fad-286">In a :::no-loc(Q#)::: Jupyter Notebook, you enter :::no-loc(Q#)::: code just as we would from inside the namespace of a :::no-loc(Q#)::: file.</span></span>

<span data-ttu-id="12fad-287">Daarom kunnen we toegang tot callables van de [ :::no-loc(Q#)::: standaard bibliotheken](xref:microsoft.quantum.qsharplibintro) inschakelen met `open` instructies voor hun respectieve naam ruimten.</span><span class="sxs-lookup"><span data-stu-id="12fad-287">So, we can enable access to callables from the [:::no-loc(Q#)::: standard libraries](xref:microsoft.quantum.qsharplibintro) with `open` statements for their respective namespaces.</span></span>
<span data-ttu-id="12fad-288">Bij het uitvoeren van een cel met een dergelijke instructie zijn de definities van deze naam ruimten beschikbaar in de hele werk ruimte.</span><span class="sxs-lookup"><span data-stu-id="12fad-288">Upon running a cell with such a statement, the definitions from those namespaces are available throughout the workspace.</span></span>

> [!NOTE]
> <span data-ttu-id="12fad-289">Callables van [micro soft. Quantum. intrinsieke](xref:Microsoft.Quantum.Intrinsic) en [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon) (bijvoorbeeld [`H`](xref:Microsoft.Quantum.Intrinsic.H) en [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach) ) zijn automatisch beschikbaar voor bewerkingen die zijn gedefinieerd in cellen in :::no-loc(Q#)::: Jupyter-notebooks.</span><span class="sxs-lookup"><span data-stu-id="12fad-289">Callables from [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic) and [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon) (for example, [`H`](xref:Microsoft.Quantum.Intrinsic.H) and [`ApplyToEach`](xref:Microsoft.Quantum.Canon.ApplyToEach)) are automatically available to operations defined within cells in :::no-loc(Q#)::: Jupyter Notebooks.</span></span>
> <span data-ttu-id="12fad-290">Dit geldt echter niet voor code die wordt binnengebracht in vanuit externe :::no-loc(Q#)::: bron bestanden (een proces dat wordt weer gegeven bij [Inleiding tot :::no-loc(Q#)::: en Jupyter-notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span><span class="sxs-lookup"><span data-stu-id="12fad-290">However, this is not true for code brought in from external :::no-loc(Q#)::: source files (a process shown at [Intro to :::no-loc(Q#)::: and Jupyter Notebooks](https://github.com/microsoft/Quantum/blob/main/samples/getting-started/intro-to-iqsharp/Notebook.ipynb)).</span></span> 
> 

<span data-ttu-id="12fad-291">Op dezelfde manier hoeft u alleen maar de :::no-loc(Q#)::: code te schrijven en de cel uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="12fad-291">Similarly, defining operations requires only writing the :::no-loc(Q#)::: code and running the cell.</span></span>

<img src="../media/hostprograms_jupyter_op_def_crop.png" alt="Jupyter cell defining :::no-loc(Q#)::: operations" width="773">

<span data-ttu-id="12fad-292">De uitvoer vermeldt deze bewerkingen, die vervolgens kunnen worden aangeroepen vanuit toekomstige cellen.</span><span class="sxs-lookup"><span data-stu-id="12fad-292">The output then lists those operations, which can then be called from future cells.</span></span>

### <a name="target-machines"></a><span data-ttu-id="12fad-293">Doelcomputers</span><span class="sxs-lookup"><span data-stu-id="12fad-293">Target machines</span></span>

<span data-ttu-id="12fad-294">De functionaliteit voor het uitvoeren van bewerkingen op specifieke doel computers wordt gegeven via een [ :::no-loc(Q#)::: Magic-opdracht](xref:microsoft.quantum.guide.quickref.iqsharp).</span><span class="sxs-lookup"><span data-stu-id="12fad-294">The functionality to run operations on specific target machines is provided via [I:::no-loc(Q#)::: Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp).</span></span>
<span data-ttu-id="12fad-295">`%simulate`Maakt bijvoorbeeld gebruik van de `QuantumSimulator` , en maakt gebruik van `%estimate` `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="12fad-295">For example, `%simulate` makes use of the `QuantumSimulator`, and `%estimate` uses the `ResourcesEstimator`:</span></span>

<img src="../media/hostprograms_jupyter_no_args_sim_est_crop.png" alt="Jupyter cell simulating a :::no-loc(Q#)::: operation and running resource estimation" width="773">

### <a name="passing-inputs-to-functions-and-operations"></a><span data-ttu-id="12fad-296">Invoer door geven aan functies en bewerkingen</span><span class="sxs-lookup"><span data-stu-id="12fad-296">Passing inputs to functions and operations</span></span>

<span data-ttu-id="12fad-297">Als u invoer wilt door geven aan de :::no-loc(Q#)::: bewerkingen, kunnen de argumenten als paren worden door gegeven `key=value` aan de opdracht Magic run.</span><span class="sxs-lookup"><span data-stu-id="12fad-297">To pass inputs to the :::no-loc(Q#)::: operations, the arguments can be passed as `key=value` pairs to the run magic command.</span></span>
<span data-ttu-id="12fad-298">Om uit te voeren `MeasureSuperpositionArray` met vier qubits kunnen we de `%simulate MeasureSuperpositionArray n=4` volgende handelingen uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="12fad-298">So, to run `MeasureSuperpositionArray` with four qubits, we can run `%simulate MeasureSuperpositionArray n=4`:</span></span>

<img src="../media/hostprograms_jupyter_args_sim_crop.png" alt="Jupyter cell simulating a :::no-loc(Q#)::: operation with arguments" width="773">

<span data-ttu-id="12fad-299">Dit patroon kan worden gebruikt in combi natie met `%estimate` andere run-opdrachten.</span><span class="sxs-lookup"><span data-stu-id="12fad-299">This pattern can be used similarly with `%estimate` and other run commands.</span></span>

### <a name="using-no-locq-code-from-other-projects-or-packages"></a><span data-ttu-id="12fad-300">:::no-loc(Q#):::Code uit andere projecten of pakketten gebruiken</span><span class="sxs-lookup"><span data-stu-id="12fad-300">Using :::no-loc(Q#)::: code from other projects or packages</span></span>

<span data-ttu-id="12fad-301">Standaard worden in een :::no-loc(Q#)::: Jupyter notebook alle `.qs` bestanden in de huidige map geladen en :::no-loc(Q#)::: worden de bewerkingen en functies beschikbaar voor gebruik in het notitie blok.</span><span class="sxs-lookup"><span data-stu-id="12fad-301">By default, a :::no-loc(Q#)::: Jupyter Notebook loads all of the `.qs` files in the current folder and makes their :::no-loc(Q#)::: operations and functions available for use from inside the notebook.</span></span> <span data-ttu-id="12fad-302">De [ `%who` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.who) bevat een lijst met alle momenteel beschik bare :::no-loc(Q#)::: bewerkingen en functies.</span><span class="sxs-lookup"><span data-stu-id="12fad-302">The [`%who` magic command](xref:microsoft.quantum.iqsharp.magic-ref.who) lists all currently-available :::no-loc(Q#)::: operations and functions.</span></span>

<span data-ttu-id="12fad-303">Als u :::no-loc(Q#)::: code uit een andere map wilt laden, kunt u de [ `%project` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.project) gebruiken om een verwijzing naar een `.csproj` bestand voor een project toe te voegen :::no-loc(Q#)::: (dat wil zeggen, een project waarnaar wordt verwezen `Microsoft.Quantum.Sdk` ).</span><span class="sxs-lookup"><span data-stu-id="12fad-303">To load :::no-loc(Q#)::: code from another folder, the [`%project` magic command](xref:microsoft.quantum.iqsharp.magic-ref.project) can be used to add a reference to a `.csproj` file for a :::no-loc(Q#)::: project (that is, a project that references `Microsoft.Quantum.Sdk`).</span></span> <span data-ttu-id="12fad-304">Met deze opdracht worden alle `.qs` bestanden in de map met de `.csproj` (en submappen) gecompileerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-304">This command will compile any `.qs` files in the folder containing the `.csproj` (and subfolders).</span></span> <span data-ttu-id="12fad-305">Ook worden alle pakketten die via of projecten verwijzen waarnaar wordt `PackageReference` :::no-loc(Q#)::: verwezen `ProjectReference` in dat bestand, recursief geladen `.csproj` .</span><span class="sxs-lookup"><span data-stu-id="12fad-305">It will also recursively load any packages referenced via `PackageReference` or :::no-loc(Q#)::: projects referenced via `ProjectReference` in that `.csproj` file.</span></span> 

<span data-ttu-id="12fad-306">Zo simuleren de volgende cellen een :::no-loc(Q#)::: bewerking vanuit een extern project, waarbij naar het pad van het project wordt verwezen ten opzichte van de huidige map:</span><span class="sxs-lookup"><span data-stu-id="12fad-306">As an example, the following cells simulate a :::no-loc(Q#)::: operation from an external project, where the project path is referenced relative to the current folder:</span></span>

<img src="../media/hostprograms_jupyter_project_crop.png" alt="Jupyter cell simulating a :::no-loc(Q#)::: operation from an external project" width="773">

<span data-ttu-id="12fad-307">Als u externe pakketten met :::no-loc(Q#)::: code wilt laden, gebruikt u de [ `%package` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).</span><span class="sxs-lookup"><span data-stu-id="12fad-307">To load external packages containing :::no-loc(Q#)::: code, use the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="12fad-308">Als u een pakket laadt, worden ook aangepaste Magic-opdrachten beschikbaar of worden coderings Programma's weer gegeven die zijn opgenomen in alle assembly's die deel uitmaken van het pakket.</span><span class="sxs-lookup"><span data-stu-id="12fad-308">Loading a package will also make available any custom magic commands or display encoders that are contained in any assemblies that are part of the package.</span></span>

<span data-ttu-id="12fad-309">Als u wilt dat externe pakketten of :::no-loc(Q#)::: projecten op notebook intialization keer worden geladen, moet u ervoor zorgen dat de notitieblokmap een `.csproj` bestand bevat waarnaar wordt verwezen `Microsoft.Quantum.Sdk` .</span><span class="sxs-lookup"><span data-stu-id="12fad-309">To load external packages or :::no-loc(Q#)::: projects at notebook intialization time, ensure that the notebook folder contains a `.csproj` file which references `Microsoft.Quantum.Sdk`.</span></span> <span data-ttu-id="12fad-310">Voeg in dat `.csproj` de eigenschap toe `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` aan de `<PropertyGroup>` .</span><span class="sxs-lookup"><span data-stu-id="12fad-310">In that `.csproj`, add the property `<IQSharpLoadAutomatically>true</IQSharpLoadAutomatically>` to the `<PropertyGroup>`.</span></span> <span data-ttu-id="12fad-311">Dit geeft een instructie :::no-loc(Q#)::: om een of meer items te `ProjectReference` laden `PackageReference` die zijn gevonden in de `.csproj` laad tijd van notebooks.</span><span class="sxs-lookup"><span data-stu-id="12fad-311">This will instruct I:::no-loc(Q#)::: to recursively load any `ProjectReference` or `PackageReference` items found in that `.csproj` at notebook load time.</span></span>

<span data-ttu-id="12fad-312">Dit is bijvoorbeeld een eenvoudig `.csproj` bestand dat ervoor zorgt dat :::no-loc(Q#)::: het pakket automatisch wordt geladen `Microsoft.Quantum.Chemistry` :</span><span class="sxs-lookup"><span data-stu-id="12fad-312">For example, here is a simple `.csproj` file that causes I:::no-loc(Q#)::: to automatically load the `Microsoft.Quantum.Chemistry` package:</span></span>

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
> <span data-ttu-id="12fad-313">Deze aangepaste `<IQSharpLoadAutomatically>` eigenschap is momenteel vereist :::no-loc(Q#)::: voor Jupyter notebook hosts, maar in de toekomst kan dit het standaard gedrag voor een bestand zijn dat `.csproj` zich in dezelfde map bevindt als het notitie blok-bestand.</span><span class="sxs-lookup"><span data-stu-id="12fad-313">Currently this custom `<IQSharpLoadAutomatically>` property is required by :::no-loc(Q#)::: Jupyter Notebook hosts, but in the future, this may become the default behavior for a `.csproj` file located in the same folder as the notebook file.</span></span>

> [!NOTE]
> <span data-ttu-id="12fad-314">Momenteel `<QsharpCompile>` wordt de instelling in de `.csproj` wordt genegeerd door :::no-loc(Q#)::: Jupyter notebook-hosts en `.qs` worden alle bestanden in de map `.csproj` (inclusief submappen) geladen en gecompileerd.</span><span class="sxs-lookup"><span data-stu-id="12fad-314">Currently the `<QsharpCompile>` setting in the `.csproj` is ignored by :::no-loc(Q#)::: Jupyter Notebook hosts, and all `.qs` files in the folder of the `.csproj` (including subfolders) are loaded and compiled.</span></span> <span data-ttu-id="12fad-315">Ondersteuning voor `.csproj` instellingen wordt in de toekomst verbeterd (Zie [iqsharp # 277](https://github.com/microsoft/iqsharp/issues/277) voor meer informatie).</span><span class="sxs-lookup"><span data-stu-id="12fad-315">Support for `.csproj` settings will be improved in the future (see [iqsharp#277](https://github.com/microsoft/iqsharp/issues/277) for more details).</span></span>
