---
title: Q#-programma's testen en debuggen
description: Leer hoe u eenheidstests, feiten en beweringen gebruiken en hoe u kwantumprogramma's testen en debuggen.
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: caf15b7273b7efed1da87a2edd62c06cd4357593
ms.sourcegitcommit: b6b8459eb654040f1e19f66411b29fc9e48e95c9
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "82030579"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="6a214-103">Testen en debuggen</span><span class="sxs-lookup"><span data-stu-id="6a214-103">Testing and Debugging</span></span>

<span data-ttu-id="6a214-104">Net als bij de klassieke programmering, is het essentieel om te kunnen controleren of quantum programma's handelen zoals bedoeld, en in staat zijn om een quantum programma dat onjuist is diagnosticeren.</span><span class="sxs-lookup"><span data-stu-id="6a214-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="6a214-105">In deze sectie behandelen we de tools die Q# biedt voor het testen en debuggen van kwantumprogramma's.</span><span class="sxs-lookup"><span data-stu-id="6a214-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="6a214-106">Eenheidstests</span><span class="sxs-lookup"><span data-stu-id="6a214-106">Unit Tests</span></span>

<span data-ttu-id="6a214-107">Een veel voorkomende benadering van het testen van klassieke programma's is het schrijven van kleine programma's genaamd *unit tests* die code uitvoeren in een bibliotheek en de output te vergelijken met een aantal verwachte output.</span><span class="sxs-lookup"><span data-stu-id="6a214-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="6a214-108">Bijvoorbeeld, kunnen we willen `Square(2)` ervoor `4`zorgen dat rendementen, omdat we weten *a priori* dat $ 2 ^ 2 = 4 $.</span><span class="sxs-lookup"><span data-stu-id="6a214-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="6a214-109">Q# ondersteunt het maken van eenheidstests voor quantumprogramma's en die kunnen worden uitgevoerd als tests binnen het [testkader van](https://xunit.github.io/) de xUnit-eenheid.</span><span class="sxs-lookup"><span data-stu-id="6a214-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="6a214-110">Een testproject maken</span><span class="sxs-lookup"><span data-stu-id="6a214-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6a214-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6a214-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="6a214-112">Open Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="6a214-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="6a214-113">Ga naar `File` het `New`  >  `Project...`menu en selecteer .</span><span class="sxs-lookup"><span data-stu-id="6a214-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="6a214-114">Zoek in de rechterbovenhoek `Q#`naar en `Q# Test Project` selecteer de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="6a214-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6a214-115">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6a214-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="6a214-116">Voer vanaf uw favoriete opdrachtregel de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="6a214-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="6a214-117">Uw nieuwe project heeft `Tests.qs`één bestand, dat een handige plek biedt om nieuwe Q#-eenheidstests te definiëren.</span><span class="sxs-lookup"><span data-stu-id="6a214-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="6a214-118">In eerste instantie bevat dit `AllocateQubit` bestand een voorbeeldeenheidstest die controleert of{0}een nieuw toegewezen qubit zich in de $\ket $ staat bevindt en een bericht afdrukt:</span><span class="sxs-lookup"><span data-stu-id="6a214-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

:nieuw: <span data-ttu-id="6a214-119">elke Q#-bewerking of -functie `Unit` die `Unit` een argument van type `@Test("...")` en retouren gebruikt, kan worden gemarkeerd als een eenheidstest via het kenmerk.</span><span class="sxs-lookup"><span data-stu-id="6a214-119">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="6a214-120">Het argument van `"QuantumSimulator"` dat kenmerk geeft hierboven het doel aan waarop de test wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6a214-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="6a214-121">Eén test kan op meerdere doelen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6a214-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="6a214-122">Voeg bijvoorbeeld een `@Test("ResourcesEstimator")` kenmerk `AllocateQubit`toe boven .</span><span class="sxs-lookup"><span data-stu-id="6a214-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="6a214-123">Sla het bestand op en voer alle tests uit.</span><span class="sxs-lookup"><span data-stu-id="6a214-123">Save the file and execute all tests.</span></span> <span data-ttu-id="6a214-124">Er moeten nu twee unit tests, een waar AssignQubit wordt uitgevoerd op de QuantumSimulator, en een waar het wordt uitgevoerd in de ResourceEstimator.</span><span class="sxs-lookup"><span data-stu-id="6a214-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="6a214-125">De Q# compiler herkent de ingebouwde doelen "QuantumSimulator", "ToffoliSimulator" en "ResourcesEstimator" als geldige uitvoeringsdoelen voor eenheidstests.</span><span class="sxs-lookup"><span data-stu-id="6a214-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="6a214-126">Het is ook mogelijk om een volledig gekwalificeerde naam op te geven om een aangepaste uitvoeringsdoelstelling te definiëren.</span><span class="sxs-lookup"><span data-stu-id="6a214-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="6a214-127">Q#-eenheidstests uitvoeren</span><span class="sxs-lookup"><span data-stu-id="6a214-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6a214-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6a214-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="6a214-129">Ga als een malige installatie per `Test` oplossing naar `Test Settings`  >  `Default Processor Architecture`  >  `X64`het menu en selecteer .</span><span class="sxs-lookup"><span data-stu-id="6a214-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="6a214-130">De standaardinstelling voor processorarchitectuur voor Visual Studio`.suo`wordt opgeslagen in het bestand () voor elke oplossing ( ) bestand.</span><span class="sxs-lookup"><span data-stu-id="6a214-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="6a214-131">Als u dit bestand verwijdert, moet `X64` u opnieuw als uw processorarchitectuur selecteren.</span><span class="sxs-lookup"><span data-stu-id="6a214-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="6a214-132">Bouw het project, `Test` ga naar `Windows`  >  `Test Explorer`het menu en selecteer .</span><span class="sxs-lookup"><span data-stu-id="6a214-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="6a214-133">`AllocateQubit`wordt weergegeven in de lijst `Not Run Tests` met tests in de groep.</span><span class="sxs-lookup"><span data-stu-id="6a214-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="6a214-134">Selecteer `Run All` of voer deze individuele test uit, en het moet slagen!</span><span class="sxs-lookup"><span data-stu-id="6a214-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6a214-135">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6a214-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="6a214-136">Als u tests wilt uitvoeren, navigeert `Tests.csproj`u naar de projectmap (de map die bevat) en voert u de opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="6a214-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="6a214-137">U moet uitvoer krijgen die vergelijkbaar is met het volgende:</span><span class="sxs-lookup"><span data-stu-id="6a214-137">You should get output similar to the following:</span></span>

```
Build started, please wait...
Build completed.

Test run for C:\Users\chgranad.REDMOND\tmp\Tests\bin\Debug\netcoreapp2.0\Tests.dll(.NETCoreApp,Version=v2.0)
Microsoft (R) Test Execution Command Line Tool Version 15.3.0-preview-20170628-02
Copyright (c) Microsoft Corporation.  All rights reserved.

Starting test execution, please wait...
[xUnit.net 00:00:00.5864002]   Discovering: Tests
[xUnit.net 00:00:00.7073844]   Discovered:  Tests
[xUnit.net 00:00:00.7453826]   Starting:    Tests
[xUnit.net 00:00:00.9590439]   Finished:    Tests

Total tests: 1. Passed: 1. Failed: 0. Skipped: 0.
Test Run Successful.
Test execution time: 1.9607 Seconds
```

<span data-ttu-id="6a214-138">Eenheidstests kunnen worden gefilterd op basis van hun naam en/of het uitvoeringsdoel:</span><span class="sxs-lookup"><span data-stu-id="6a214-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="6a214-139">De intrinsieke <xref:microsoft.quantum.intrinsic.message> `(String -> Unit)` functie heeft type en maakt het mogelijk diagnostische berichten te maken.</span><span class="sxs-lookup"><span data-stu-id="6a214-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6a214-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6a214-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="6a214-141">Nadat u een test hebt uitgevoerd in Test Explorer en op de test hebt geklikt, verschijnt er een paneel met informatie over de uitvoering van de test: Geslaagd/Mislukt-status, verstreken tijd en een koppeling 'Uitvoer'.</span><span class="sxs-lookup"><span data-stu-id="6a214-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="6a214-142">Als u op de koppeling 'Uitvoer' klikt, wordt de testuitvoer in een nieuw venster geopend.</span><span class="sxs-lookup"><span data-stu-id="6a214-142">If you click the "Output" link, test output will open in a new window.</span></span>

![testuitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6a214-144">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6a214-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="6a214-145">De pass/fail-status voor elke test `dotnet test`wordt op de console afgedrukt door .</span><span class="sxs-lookup"><span data-stu-id="6a214-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="6a214-146">Voor falende tests worden de uitgangen ook afgedrukt op de console om de fout te diagnosticeren.</span><span class="sxs-lookup"><span data-stu-id="6a214-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="6a214-147">Feiten en beweringen</span><span class="sxs-lookup"><span data-stu-id="6a214-147">Facts and Assertions</span></span>

<span data-ttu-id="6a214-148">Omdat functies in Q# geen _logische_ bijwerkingen hebben, kunnen _andere soorten_ effecten van het `()` uitvoeren van een functie waarvan het uitvoertype de lege tuple is, nooit worden waargenomen vanuit een Q#-programma.</span><span class="sxs-lookup"><span data-stu-id="6a214-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="6a214-149">Dat wil zeggen, een doelmachine kan ervoor `()` kiezen om geen functie uit te voeren die terugkeert met de garantie dat deze omissie het gedrag van een volgende Q#-code niet zal wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6a214-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="6a214-150">Dit maakt `()` functies die terugkeren `Unit`(d.w.z. ) een handig hulpmiddel voor het insluiten van beweringen en het debuggen van logica in Q#-programma's.</span><span class="sxs-lookup"><span data-stu-id="6a214-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="6a214-151">Laten we eens kijken naar een eenvoudig voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="6a214-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="6a214-152">Hier geeft `fail` het trefwoord aan dat de berekening niet door mag gaan, waardoor een uitzondering wordt gemaakt in de doelmachine waarop het Q#-programma wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6a214-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="6a214-153">Per definitie kan een dergelijke fout niet worden waargenomen vanuit Q#, omdat `fail` er geen nieuwe Q#-code wordt uitgevoerd nadat een instructie is bereikt.</span><span class="sxs-lookup"><span data-stu-id="6a214-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="6a214-154">Dus, als we verder `PositivityFact`gaan dan een oproep aan , kunnen we worden verzekerd door dat de input positief was.</span><span class="sxs-lookup"><span data-stu-id="6a214-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="6a214-155">Houd er rekening mee dat `PositivityFact` we [`Fact`](xref:microsoft.quantum.diagnostics.fact) hetzelfde <xref:microsoft.quantum.diagnostics> gedrag kunnen implementeren als het gebruik van de functie vanuit de naamruimte:</span><span class="sxs-lookup"><span data-stu-id="6a214-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="6a214-156">*Beweringen worden daarentegen*op dezelfde manier gebruikt als feiten, maar kunnen afhankelijk zijn van de toestand van de doelmachine.</span><span class="sxs-lookup"><span data-stu-id="6a214-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="6a214-157">Overeenkomstig worden ze gedefinieerd als bewerkingen, terwijl feiten worden gedefinieerd als functies (zoals hierboven).</span><span class="sxs-lookup"><span data-stu-id="6a214-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="6a214-158">Om het onderscheid te begrijpen, overweeg dan het volgende gebruik van een feit in een bewering:</span><span class="sxs-lookup"><span data-stu-id="6a214-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="6a214-159">Hier gebruiken we de <xref:microsoft.quantum.environment.getqubitsavailabletouse> bewerking om het aantal qubits dat beschikbaar is voor gebruik terug te geven.</span><span class="sxs-lookup"><span data-stu-id="6a214-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="6a214-160">Aangezien dit duidelijk afhangt van de wereldwijde toestand van het `AssertQubitsAreAvailable` programma en de uitvoeringsomgeving, moet onze definitie van een operatie ook zijn.</span><span class="sxs-lookup"><span data-stu-id="6a214-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="6a214-161">We kunnen die globale status echter `Bool` gebruiken om een `Fact` eenvoudige waarde te leveren als input voor de functie.</span><span class="sxs-lookup"><span data-stu-id="6a214-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="6a214-162">Voortbouwend op deze ideeën, [de prelude](xref:microsoft.quantum.libraries.standard.prelude) <xref:microsoft.quantum.intrinsic.assert> biedt <xref:microsoft.quantum.intrinsic.assertprob> twee bijzonder nuttige `()`beweringen, en beide gemodelleerd als operaties op .</span><span class="sxs-lookup"><span data-stu-id="6a214-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="6a214-163">Deze beweringen nemen elk een Exploitant Pauli die een bepaalde meting van belang beschrijft, een quantumregister waarop een meting moet worden uitgevoerd, en een hypothetischresultaat.</span><span class="sxs-lookup"><span data-stu-id="6a214-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="6a214-164">Op doelmachines die werken door simulatie, zijn we niet gebonden aan [de stelling zonder klonen](https://en.wikipedia.org/wiki/No-cloning_theorem), en kunnen dergelijke metingen uitvoeren zonder het register te verstoren dat aan dergelijke beweringen wordt doorgegeven.</span><span class="sxs-lookup"><span data-stu-id="6a214-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="6a214-165">Een simulator kan dan, `PositivityFact` vergelijkbaar met de bovenstaande functie, de berekening afbreken als de hypothetische uitkomst in de praktijk niet zou worden waargenomen:</span><span class="sxs-lookup"><span data-stu-id="6a214-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

```qsharp
using (register = Qubit()) 
{
    H(register);
    Assert([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

<span data-ttu-id="6a214-166">Op fysieke kwantumhardware, waar de stelling zonder klonen onderzoek `Assert` van `AssertProb` kwantumtoestand `()` verhindert, keren de en operaties gewoon zonder ander effect terug.</span><span class="sxs-lookup"><span data-stu-id="6a214-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="6a214-167">De <xref:microsoft.quantum.diagnostics> naamruimte biedt nog `Assert` een aantal functies van de familie die ons in staat stellen om meer geavanceerde voorwaarden te controleren.</span><span class="sxs-lookup"><span data-stu-id="6a214-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="6a214-168">Dumpfuncties</span><span class="sxs-lookup"><span data-stu-id="6a214-168">Dump Functions</span></span>

<span data-ttu-id="6a214-169">Om quantumprogramma's <xref:microsoft.quantum.diagnostics> voor problemen op te lossen, biedt de naamruimte twee <xref:microsoft.quantum.diagnostics.dumpmachine> <xref:microsoft.quantum.diagnostics.dumpregister>functies die in een bestand de huidige status van de doelmachine kunnen dumpen: en .</span><span class="sxs-lookup"><span data-stu-id="6a214-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="6a214-170">De gegenereerde output van elk is afhankelijk van de doelmachine.</span><span class="sxs-lookup"><span data-stu-id="6a214-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="6a214-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="6a214-171">DumpMachine</span></span>

<span data-ttu-id="6a214-172">De full-state quantum simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [golffunctie](https://en.wikipedia.org/wiki/Wave_function) van het hele kwantumsysteem, als een eendimensionale array van complexe getallen, waarin elk element vertegenwoordigt de amplitude van de waarschijnlijkheid van het meten van de computationele basis staat $\ket{n}$, waar $\ket{n} = \ket{b_{n-1}... b_1b_0 voor bits\{b_i\}$.</span><span class="sxs-lookup"><span data-stu-id="6a214-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="6a214-173">Bijvoorbeeld, op een machine met slechts twee qubits toegewezen en in de quantum staat $${1}\begin{align} \ket{\psi} = \frac {\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ bellen <xref:microsoft.quantum.diagnostics.dumpmachine> genereert deze output:</span><span class="sxs-lookup"><span data-stu-id="6a214-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="6a214-174">De eerste rij geeft een opmerking met de id's van de bijbehorende qubits in hun significante volgorde.</span><span class="sxs-lookup"><span data-stu-id="6a214-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="6a214-175">De rest van de rijen beschrijven de waarschijnlijkheidsamplitude van het meten van de basisstatusvector $\ket{n}$ in zowel Cartesiaanse als polaire formaten.</span><span class="sxs-lookup"><span data-stu-id="6a214-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="6a214-176">In detail voor de eerste rij:</span><span class="sxs-lookup"><span data-stu-id="6a214-176">In detail for the first row:</span></span>

* <span data-ttu-id="6a214-177">**`∣0❭:`** deze rij komt `0` overeen met de computationele basisstatus</span><span class="sxs-lookup"><span data-stu-id="6a214-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="6a214-178">**`0.707107 +  0.000000 i`**: de waarschijnlijkheidsamplitude in Cartesiaans formaat.</span><span class="sxs-lookup"><span data-stu-id="6a214-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="6a214-179">**` == `**: `equal` het teken scheidt beide gelijkwaardige voorstellingen.</span><span class="sxs-lookup"><span data-stu-id="6a214-179">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="6a214-180">**`**********  `**: Een grafische weergave van de `*` omvang, het aantal is evenredig aan de waarschijnlijkheid van het meten van deze staat vector.</span><span class="sxs-lookup"><span data-stu-id="6a214-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="6a214-181">**`[ 0.500000 ]`**: de numerieke waarde van de magnitude</span><span class="sxs-lookup"><span data-stu-id="6a214-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="6a214-182">**`    ---`**: Een grafische weergave van de fase van de amplitude (zie hieronder).</span><span class="sxs-lookup"><span data-stu-id="6a214-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="6a214-183">**`[ 0.0000 rad ]`**: de numerieke waarde van de fase (in radialen).</span><span class="sxs-lookup"><span data-stu-id="6a214-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="6a214-184">Zowel de omvang als de fase worden weergegeven met een grafische weergave.</span><span class="sxs-lookup"><span data-stu-id="6a214-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="6a214-185">De magnitude representatie is rechttoe rechtaan: het toont een balk van `*`, hoe groter de kans hoe groter de bar zal zijn.</span><span class="sxs-lookup"><span data-stu-id="6a214-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="6a214-186">Voor de fase tonen we de volgende symbolen om de hoek weer te geven op basis van bereiken:</span><span class="sxs-lookup"><span data-stu-id="6a214-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

```
[ -π/16,   π/16)       ---
[  π/16,  3π/16)        /-
[ 3π/16,  5π/16)        / 
[ 5π/16,  7π/16)       +/ 
[ 7π/16,  9π/16)      ↑   
[ 8π/16, 11π/16)    \-    
[ 7π/16, 13π/16)    \     
[ 7π/16, 15π/16)   +\     
[15π/16, 19π/16)   ---    
[17π/16, 19π/16)   -/     
[19π/16, 21π/16)    /     
[21π/16, 23π/16)    /+    
[23π/16, 25π/16)      ↓   
[25π/16, 27π/16)       -\ 
[27π/16, 29π/16)        \ 
[29π/16, 31π/16)        \+
[31π/16,   π/16)       ---
```

<span data-ttu-id="6a214-187">De volgende voorbeelden `DumpMachine` tonen voor sommige gemeenschappelijke staten:</span><span class="sxs-lookup"><span data-stu-id="6a214-187">The following examples show `DumpMachine` for some common states:</span></span>

### `∣0❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

### `∣1❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣1❭:     1.000000 +  0.000000 i  ==     ******************** [ 1.000000 ]     --- [  0.00000 rad ]
```

### `∣+❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
```

### `∣-❭`

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]      --- [  0.00000 rad ]
∣1❭:    -0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]  ---     [  3.14159 rad ]
```


  > [!NOTE]
  > <span data-ttu-id="6a214-188">De id van een qubit wordt toegewezen tijdens runtime en is niet noodzakelijkerwijs afgestemd op de volgorde waarin de qubit is toegewezen of zijn positie binnen een qubit-register.</span><span class="sxs-lookup"><span data-stu-id="6a214-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6a214-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6a214-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="6a214-190">U een qubit-id in Visual Studio achterhalen door een breekpunt in uw code te plaatsen en de waarde van een qubit-variabele te inspecteren, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="6a214-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![qubit-id weergeven in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="6a214-192">de qubit `0` met `register2` index`3`op heeft id= `1` ,`2`de qubit met index heeft id= .</span><span class="sxs-lookup"><span data-stu-id="6a214-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6a214-193">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6a214-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="6a214-194">U een qubit-id <xref:microsoft.quantum.intrinsic.message> achterhalen met behulp van de functie en de qubit-variabele in het bericht doorgeven, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="6a214-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="6a214-195">die deze output zou kunnen genereren:</span><span class="sxs-lookup"><span data-stu-id="6a214-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="6a214-196">dit betekent dat de `0` qubit met index `register2` op id=`3`heeft, de qubit met index `1` id=`2`heeft.</span><span class="sxs-lookup"><span data-stu-id="6a214-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="6a214-197"><xref:microsoft.quantum.diagnostics.dumpmachine>maakt deel <xref:microsoft.quantum.diagnostics> uit van de naamruimte, dus om `open` deze te gebruiken moet u een instructie toevoegen:</span><span class="sxs-lookup"><span data-stu-id="6a214-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

```qsharp
namespace Samples {
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {
        using (qubits = Qubit[2]) {
            H(qubits[1]);
            DumpMachine("dump.txt");
        }
    }
}
```


### <a name="dumpregister"></a><span data-ttu-id="6a214-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="6a214-198">DumpRegister</span></span>

<span data-ttu-id="6a214-199"><xref:microsoft.quantum.diagnostics.dumpregister>werkt <xref:microsoft.quantum.diagnostics.dumpmachine>als , behalve dat er ook een array van qubits nodig is om de hoeveelheid informatie te beperken tot alleen die relevant zijn voor de bijbehorende qubits.</span><span class="sxs-lookup"><span data-stu-id="6a214-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="6a214-200">Net <xref:microsoft.quantum.diagnostics.dumpmachine>als bij , <xref:microsoft.quantum.diagnostics.dumpregister> de informatie gegenereerd door is afhankelijk van de doelmachine.</span><span class="sxs-lookup"><span data-stu-id="6a214-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="6a214-201">Voor de full-state quantum simulator schrijft in het bestand de golf functie tot een globale fase van de <xref:microsoft.quantum.diagnostics.dumpmachine>quantum sub-systeem gegenereerd door de verstrekte qubits in hetzelfde formaat als .</span><span class="sxs-lookup"><span data-stu-id="6a214-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="6a214-202">Bijvoorbeeld, neem opnieuw een machine met slechts twee{1}qubits toegewezen en in de quantum staat $$ \begin{align}{2}\ket{\psi} = \frac {\sqrt } \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ({1}(\frac {\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ oproep <xref:microsoft.quantum.diagnostics.dumpregister> voor `qubit[0]` genereert deze output:</span><span class="sxs-lookup"><span data-stu-id="6a214-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="6a214-203">en <xref:microsoft.quantum.diagnostics.dumpregister> het `qubit[1]` vragen om genereert deze output:</span><span class="sxs-lookup"><span data-stu-id="6a214-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="6a214-204">In het algemeen is de toestand van een register dat is verstrengeld met een ander register een gemengde staat in plaats van een zuivere staat.</span><span class="sxs-lookup"><span data-stu-id="6a214-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="6a214-205">In dit <xref:microsoft.quantum.diagnostics.dumpregister> geval wordt het volgende bericht weergegeven:</span><span class="sxs-lookup"><span data-stu-id="6a214-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="6a214-206">In het volgende voorbeeld ziet <xref:microsoft.quantum.diagnostics.dumpregister> u <xref:microsoft.quantum.diagnostics.dumpmachine> hoe u beide gebruiken en in uw Q#-code:</span><span class="sxs-lookup"><span data-stu-id="6a214-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

```qsharp
namespace app
{
    open Microsoft.Quantum.Intrinsic;
    open Microsoft.Quantum.Diagnostics;

    operation Operation () : Unit {

        using (qubits = Qubit[2]) {
            X(qubits[1]);
            H(qubits[1]);
            R1Frac(1, 2, qubits[1]);
            
            DumpMachine("dump.txt");
            DumpRegister("q0.txt", qubits[0..0]);
            DumpRegister("q1.txt", qubits[1..1]);

            ResetAll(qubits);
        }
    }
}
```

## <a name="debugging"></a><span data-ttu-id="6a214-207">Foutopsporing</span><span class="sxs-lookup"><span data-stu-id="6a214-207">Debugging</span></span>

<span data-ttu-id="6a214-208">`Assert` Naast en `Dump` functies en bewerkingen ondersteunt Q# een subset van standaard Visual Studio-foutopsporingsmogelijkheden: [lijnbreekpunten instellen,](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints) [code doorlopen met F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) en het inspecteren van waarden van klassieke [variabelen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) zijn allemaal mogelijk tijdens codeuitvoering op de simulator.</span><span class="sxs-lookup"><span data-stu-id="6a214-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="6a214-209">Foutopsporing in Visual Studio Code maakt gebruik van de foutopsporingsmogelijkheden die worden geboden door de C#for Visual Studio Code-extensie aangedreven door OmniSharp en vereist het installeren van de [nieuwste versie.](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)</span><span class="sxs-lookup"><span data-stu-id="6a214-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp).</span></span> 
