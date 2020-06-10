---
title: Testen en foutopsporing
description: Meer informatie over het gebruik van eenheids testen, feiten en beweringen en dump functies om Quantum-Program ma's te testen en fout opsporing uit te voeren.
author: tcNickolas
ms.author: mamykhai@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
ms.openlocfilehash: dd6c7ae8a016423f26c37f3eedf0ae9c1d126b78
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630035"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="26918-103">Testen en foutopsporing</span><span class="sxs-lookup"><span data-stu-id="26918-103">Testing and debugging</span></span>

<span data-ttu-id="26918-104">Net als bij het klassieke Program meren is het essentieel om te controleren of Quantum Program ma's functioneren zoals bedoeld en om te kunnen vaststellen of een Quantum programma onjuist is.</span><span class="sxs-lookup"><span data-stu-id="26918-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="26918-105">In deze sectie hebben we de hulp middelen die worden aangeboden door Q # voor het testen en opsporen van fouten in Quantum Program ma's.</span><span class="sxs-lookup"><span data-stu-id="26918-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="26918-106">Eenheids tests</span><span class="sxs-lookup"><span data-stu-id="26918-106">Unit Tests</span></span>

<span data-ttu-id="26918-107">Een veelvoorkomende aanpak voor het testen van klassieke Program ma's is het schrijven van kleine Program ma's, de naam *eenheid testen* , die code uitvoeren in een bibliotheek en de uitvoer vergelijkt met een verwachte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="26918-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="26918-108">Het is bijvoorbeeld mogelijk dat we willen dat er wordt geadviseerd `Square(2)` `4` , omdat we *een priori* weten dat $2 ^ 2 = $4.</span><span class="sxs-lookup"><span data-stu-id="26918-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="26918-109">Q # ondersteunt het maken van eenheids tests voor Quantum-Program ma's en die kunnen worden uitgevoerd als tests in het Framework van de [xUnit](https://xunit.github.io/) -analyse-eenheid.</span><span class="sxs-lookup"><span data-stu-id="26918-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="26918-110">Een test project maken</span><span class="sxs-lookup"><span data-stu-id="26918-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="26918-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="26918-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="26918-112">Open Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="26918-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="26918-113">Ga naar het `File` menu en selecteer `New`  >  `Project...` .</span><span class="sxs-lookup"><span data-stu-id="26918-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="26918-114">Zoek in de rechter bovenhoek `Q#` de sjabloon en selecteer deze `Q# Test Project` .</span><span class="sxs-lookup"><span data-stu-id="26918-114">In the upper right corner, search for `Q#`, and select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="26918-115">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="26918-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="26918-116">Voer vanuit uw favoriete opdracht regel de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="26918-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="26918-117">Het nieuwe project heeft één bestand `Tests.qs` , dat een handige plaats biedt om nieuwe Q #-eenheids tests te definiëren.</span><span class="sxs-lookup"><span data-stu-id="26918-117">Your new project will have a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="26918-118">In eerste instantie bevat dit bestand één voor beeld van een eenheids test `AllocateQubit` waarmee wordt gecontroleerd of een nieuw toegewezen Qubit zich in de status $ \ket $ bevindt {0} en een bericht afdrukt:</span><span class="sxs-lookup"><span data-stu-id="26918-118">Initially this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            Assert([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="26918-119">: Nieuw: elke Q #-bewerking of-functie die een argument van het type `Unit` en retourneert, `Unit` kan worden gemarkeerd als een eenheids test via het `@Test("...")` kenmerk.</span><span class="sxs-lookup"><span data-stu-id="26918-119">:new: Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="26918-120">Het argument voor dat kenmerk `"QuantumSimulator"` hierboven geeft het doel aan waarop de test wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="26918-120">The argument to that attribute, `"QuantumSimulator"` above, specifies the target on which the test is executed.</span></span> <span data-ttu-id="26918-121">Eén test kan op meerdere doelen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="26918-121">A single test can be executed on multiple targets.</span></span> <span data-ttu-id="26918-122">Voeg bijvoorbeeld hierboven een kenmerk toe `@Test("ResourcesEstimator")` `AllocateQubit` .</span><span class="sxs-lookup"><span data-stu-id="26918-122">For example, add an attribute `@Test("ResourcesEstimator")` above `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="26918-123">Sla het bestand op en voer alle tests uit.</span><span class="sxs-lookup"><span data-stu-id="26918-123">Save the file and execute all tests.</span></span> <span data-ttu-id="26918-124">Er moeten nu twee eenheids tests worden uitgevoerd, één waarbij AllocateQubit op de QuantumSimulator-server wordt verwerkt en een waar deze wordt uitgevoerd in de ResourceEstimator.</span><span class="sxs-lookup"><span data-stu-id="26918-124">There should now be two unit tests, one where AllocateQubit is executed on the QuantumSimulator, and one where it is executed in the ResourceEstimator.</span></span> 

<span data-ttu-id="26918-125">De Q #-compiler herkent de ingebouwde doelen "QuantumSimulator", "ToffoliSimulator" en "ResourcesEstimator" als geldige uitvoerings doelen voor eenheids testen.</span><span class="sxs-lookup"><span data-stu-id="26918-125">The Q# compiler recognizes the built-in targets "QuantumSimulator", "ToffoliSimulator", and "ResourcesEstimator" as valid execution targets for unit tests.</span></span> <span data-ttu-id="26918-126">Het is ook mogelijk om een volledig gekwalificeerde naam op te geven voor het definiëren van een aangepast uitvoerings doel.</span><span class="sxs-lookup"><span data-stu-id="26918-126">It is also possible to specify any fully qualified name to define a custom execution target.</span></span> 

### <a name="running-q-unit-tests"></a><span data-ttu-id="26918-127">Er worden Q #-eenheids tests uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="26918-127">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="26918-128">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="26918-128">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="26918-129">Als eenmalige installatie per oplossing, gaat u naar `Test` menu en selecteert u `Test Settings`  >  `Default Processor Architecture`  >  `X64` .</span><span class="sxs-lookup"><span data-stu-id="26918-129">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="26918-130">De standaard instelling voor de architectuur van de processor voor Visual Studio wordt opgeslagen in het bestand met oplossings opties ( `.suo` ) voor elke oplossing.</span><span class="sxs-lookup"><span data-stu-id="26918-130">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="26918-131">Als u dit bestand verwijdert, moet u `X64` opnieuw als uw processor architectuur selecteren.</span><span class="sxs-lookup"><span data-stu-id="26918-131">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="26918-132">Bouw het project, ga naar het `Test` menu en selecteer `Windows`  >  `Test Explorer` .</span><span class="sxs-lookup"><span data-stu-id="26918-132">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="26918-133">`AllocateQubit`wordt weer gegeven in de lijst met tests in de `Not Run Tests` groep.</span><span class="sxs-lookup"><span data-stu-id="26918-133">`AllocateQubit` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="26918-134">Selecteer `Run All` of voer deze afzonderlijke test uit en probeer het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="26918-134">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="26918-135">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="26918-135">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="26918-136">Als u tests wilt uitvoeren, gaat u naar de projectmap (de map die bevat `Tests.csproj` ) en voert u de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="26918-136">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="26918-137">U ziet dat de uitvoer er ongeveer als volgt uitziet:</span><span class="sxs-lookup"><span data-stu-id="26918-137">You should get output similar to the following:</span></span>

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

<span data-ttu-id="26918-138">Eenheids tests kunnen worden gefilterd op basis van hun naam en/of het uitvoerings doel:</span><span class="sxs-lookup"><span data-stu-id="26918-138">Unit tests can be filtered according to their name and/or the execution target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


***

<span data-ttu-id="26918-139">De intrinsieke functie <xref:microsoft.quantum.intrinsic.message> heeft type `(String -> Unit)` en maakt het mogelijk diagnostische berichten te maken.</span><span class="sxs-lookup"><span data-stu-id="26918-139">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="26918-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="26918-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="26918-141">Nadat u een test in test Explorer hebt uitgevoerd en op de test hebt geklikt, wordt er een paneel weer gegeven met informatie over de test uitvoering: geslaagd/mislukt status, verstreken tijd en de koppeling uitvoer.</span><span class="sxs-lookup"><span data-stu-id="26918-141">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="26918-142">Als u op de koppeling uitvoer klikt, wordt de test uitvoer in een nieuw venster geopend.</span><span class="sxs-lookup"><span data-stu-id="26918-142">If you click the "Output" link, test output will open in a new window.</span></span>

![test uitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="26918-144">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="26918-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="26918-145">De status pass/fail voor elke test wordt door gegeven aan de console `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="26918-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="26918-146">Voor mislukte tests worden ook de uitvoer naar de console afgedrukt om de fout te kunnen vaststellen.</span><span class="sxs-lookup"><span data-stu-id="26918-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

***

## <a name="facts-and-assertions"></a><span data-ttu-id="26918-147">Feiten en verklaringen</span><span class="sxs-lookup"><span data-stu-id="26918-147">Facts and Assertions</span></span>

<span data-ttu-id="26918-148">Omdat functies in Q # geen _logische_ neven effecten hebben, kunnen _andere soorten_ effecten van het uitvoeren van een functie waarvan het uitvoer type niet de lege tuple is, `()` nooit worden waargenomen vanuit een Q #-programma.</span><span class="sxs-lookup"><span data-stu-id="26918-148">Because functions in Q# have no _logical_ side effects, any _other kinds_ of effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="26918-149">Dat wil zeggen dat een doel computer ervoor kiest geen functie uit te voeren die wordt geretourneerd `()` met de garantie dat dit weglatings gedrag van een van de volgende Q #-code niet wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="26918-149">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="26918-150">Hiermee worden functies die `()` `Unit` een handig hulp middel voor het insluiten van beweringen en fout opsporing in Q #-Program ma's retour neren (dat wil zeggen).</span><span class="sxs-lookup"><span data-stu-id="26918-150">This makes functions returning `()` (i.e. `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="26918-151">Laten we eens een eenvoudig voor beeld bekijken:</span><span class="sxs-lookup"><span data-stu-id="26918-151">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="26918-152">Hier geeft het sleutel woord `fail` aan dat de berekening niet moet worden voortgezet, waardoor er een uitzonde ring wordt gegenereerd op de doel computer waarop het Q #-programma wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="26918-152">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="26918-153">Een fout in deze soort kan per definitie niet worden waargenomen, omdat er geen verdere Q #-code wordt uitgevoerd nadat een `fail` instructie is bereikt.</span><span class="sxs-lookup"><span data-stu-id="26918-153">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="26918-154">Daarom kunnen we er zeker van zijn dat, als we een gesprek tot stand brengen met `PositivityFact` , de invoer positief is.</span><span class="sxs-lookup"><span data-stu-id="26918-154">Thus, if we proceed past a call to `PositivityFact`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="26918-155">Houd er rekening mee dat we hetzelfde gedrag kunnen implementeren als `PositivityFact` het gebruik [`Fact`](xref:microsoft.quantum.diagnostics.fact) van de functie uit de <xref:microsoft.quantum.diagnostics> naam ruimte:</span><span class="sxs-lookup"><span data-stu-id="26918-155">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:microsoft.quantum.diagnostics.fact) function from the <xref:microsoft.quantum.diagnostics> namespace:</span></span>

```qsharp
    Fact(value <= 0, "Expected a positive number.");
```

<span data-ttu-id="26918-156">*Beweringen*, daarentegen, worden op dezelfde manier gebruikt als feiten, maar kunnen afhankelijk zijn van de status van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="26918-156">*Assertions*, on the other hand, are used similarly to facts, but may be dependent on the state of the target machine.</span></span> <span data-ttu-id="26918-157">Ze worden dienovereenkomstig gedefinieerd als bewerkingen, terwijl feiten worden gedefinieerd als functies (zoals hierboven).</span><span class="sxs-lookup"><span data-stu-id="26918-157">Correspondingly, they are defined as operations, whereas facts are defined as functions (as above).</span></span>
<span data-ttu-id="26918-158">Voor een beter begrip van het onderscheid moet u rekening houden met het volgende gebruik van een feit binnen een bewering:</span><span class="sxs-lookup"><span data-stu-id="26918-158">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="26918-159">Hier gebruiken we de bewerking <xref:microsoft.quantum.environment.getqubitsavailabletouse> voor het retour neren van het aantal beschik bare qubits dat kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="26918-159">Here, we are using the operation <xref:microsoft.quantum.environment.getqubitsavailabletouse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="26918-160">Zoals dit duidelijk is afhankelijk van de algemene status van het programma en de uitvoerings omgeving, moet onze definitie van `AssertQubitsAreAvailable` ook een bewerking zijn.</span><span class="sxs-lookup"><span data-stu-id="26918-160">As this clearly depends on the global state of the program and its execution environment, our definition of  `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="26918-161">We kunnen die globale status echter gebruiken om een eenvoudige `Bool` waarde te leveren als invoer voor de `Fact` functie.</span><span class="sxs-lookup"><span data-stu-id="26918-161">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="26918-162">Op basis van deze ideeën biedt [de prelude](xref:microsoft.quantum.libraries.standard.prelude) twee bijzonder nuttige beweringen <xref:microsoft.quantum.intrinsic.assert> en <xref:microsoft.quantum.intrinsic.assertprob> beide gemodelleerd als bewerkingen op `()` .</span><span class="sxs-lookup"><span data-stu-id="26918-162">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="26918-163">Deze beweringen maken elk deel uit van een Pauli-operator die een bepaalde waardering van belang beschrijft, een Quantum registratie waarop een meting moet worden uitgevoerd en een hypothetisch resultaat.</span><span class="sxs-lookup"><span data-stu-id="26918-163">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="26918-164">Op doel computers die door simulatie werken, zijn we niet gebonden aan [het niet-klonen van theorema](https://en.wikipedia.org/wiki/No-cloning_theorem)en kunnen deze metingen worden uitgevoerd zonder dat de registratie wordt verstoord die aan dergelijke verklaringen wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="26918-164">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="26918-165">Een Simulator kan vervolgens, net als de `PositivityFact` bovenstaande functie, de berekening afbreken als het hypothetische resultaat niet in de praktijk wordt waargenomen:</span><span class="sxs-lookup"><span data-stu-id="26918-165">A simulator can then, similar to the `PositivityFact` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="26918-166">In fysieke Quantum-hardware, waarbij het niet-klonen van theorema het onderzoek van de Quantum status voor komt, worden de `Assert` en- `AssertProb` bewerkingen gewoon `()` zonder ander effect geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="26918-166">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="26918-167">De <xref:microsoft.quantum.diagnostics> naam ruimte biedt een aantal meer functies van de `Assert` familie waarmee we meer geavanceerde voor waarden kunnen controleren.</span><span class="sxs-lookup"><span data-stu-id="26918-167">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="26918-168">Dump functies</span><span class="sxs-lookup"><span data-stu-id="26918-168">Dump Functions</span></span>

<span data-ttu-id="26918-169">Voor het oplossen van problemen met Quantum Program ma's <xref:microsoft.quantum.diagnostics> biedt de naam ruimte twee functies die in een bestand de huidige status van de doel computer kunnen dumpen: <xref:microsoft.quantum.diagnostics.dumpmachine> en <xref:microsoft.quantum.diagnostics.dumpregister> .</span><span class="sxs-lookup"><span data-stu-id="26918-169">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="26918-170">De gegenereerde uitvoer van beide is afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="26918-170">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="26918-171">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="26918-171">DumpMachine</span></span>

<span data-ttu-id="26918-172">De Full-State Quantum Simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [functie Wave](https://en.wikipedia.org/wiki/Wave_function) van het hele Quantum systeem, als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitude vormt van de kans op het meten van de berekenings basis status $ \ket{n} $, waarbij $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ voor bits $ \{ b_i \} $.</span><span class="sxs-lookup"><span data-stu-id="26918-172">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="26918-173">Bijvoorbeeld, op een computer met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} , \end{align} $ $ aanroepen, wordt <xref:microsoft.quantum.diagnostics.dumpmachine> deze uitvoer gegenereerd:</span><span class="sxs-lookup"><span data-stu-id="26918-173">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="26918-174">De eerste rij bevat een opmerking met de Id's van de bijbehorende qubits in hun significante volg orde.</span><span class="sxs-lookup"><span data-stu-id="26918-174">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="26918-175">De rest van de rijen beschrijven de waarschijnlijke amplitude van het meten van de basis status vector $ \ket{n} $ in zowel Cartesisch als polaire indeling.</span><span class="sxs-lookup"><span data-stu-id="26918-175">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="26918-176">Gedetailleerd voor de eerste rij:</span><span class="sxs-lookup"><span data-stu-id="26918-176">In detail for the first row:</span></span>

* <span data-ttu-id="26918-177">**`∣0❭:`** deze rij komt overeen met de status van de `0` reken kundige basis</span><span class="sxs-lookup"><span data-stu-id="26918-177">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="26918-178">**`0.707107 +  0.000000 i`**: de waarschijnlijke amplitude in Cartesisch formaat.</span><span class="sxs-lookup"><span data-stu-id="26918-178">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="26918-179">**` == `**: het `equal` teken scheidt beide equivalente verklaringen.</span><span class="sxs-lookup"><span data-stu-id="26918-179">**` == `**: the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="26918-180">**`**********  `**: Een grafische weer gave van de omvang, het aantal `*` is evenredig met de kans dat deze status vector wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="26918-180">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="26918-181">**`[ 0.500000 ]`**: de numerieke waarde van de grootte</span><span class="sxs-lookup"><span data-stu-id="26918-181">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="26918-182">**`    ---`**: Een grafische weer gave van de fase van de amplitude (zie hieronder).</span><span class="sxs-lookup"><span data-stu-id="26918-182">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="26918-183">**`[ 0.0000 rad ]`**: de numerieke waarde van de fase (in radialen).</span><span class="sxs-lookup"><span data-stu-id="26918-183">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="26918-184">Zowel de grootte als de fase worden weer gegeven met een grafische weer gave.</span><span class="sxs-lookup"><span data-stu-id="26918-184">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="26918-185">De weer gave met de grootte is direct vooruit: er wordt een balk van weer gegeven `*` , hoe groter de kans dat de balk groter wordt.</span><span class="sxs-lookup"><span data-stu-id="26918-185">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="26918-186">Voor de fase worden de volgende symbolen weer gegeven die de hoek aangeven op basis van bereiken:</span><span class="sxs-lookup"><span data-stu-id="26918-186">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="26918-187">In de volgende voor beelden ziet u `DumpMachine` een aantal algemene statussen:</span><span class="sxs-lookup"><span data-stu-id="26918-187">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="26918-188">De id van een Qubit wordt tijdens runtime toegewezen en is niet noodzakelijkerwijs uitgelijnd met de volg orde waarin de Qubit is toegewezen of hun positie binnen een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="26918-188">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="26918-189">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="26918-189">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="26918-190">U kunt een Qubit-id in Visual Studio uitzoeken door een onderbrekings punt in uw code te plaatsen en de waarde van een Qubit-variabele te controleren, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="26918-190">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Qubit-id weer geven in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="26918-192">de Qubit met index `0` op `register2` heeft id = `3` , de Qubit met index `1` heeft id = `2` .</span><span class="sxs-lookup"><span data-stu-id="26918-192">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="26918-193">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="26918-193">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="26918-194">U kunt een Qubit-id berekenen door de <xref:microsoft.quantum.intrinsic.message> functie te gebruiken en de variabele Qubit in het bericht door te geven, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="26918-194">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="26918-195">Dit kan deze uitvoer genereren:</span><span class="sxs-lookup"><span data-stu-id="26918-195">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="26918-196">Dit betekent dat de Qubit met index `0` op `register2` heeft id = `3` , de Qubit met index `1` heeft id = `2` .</span><span class="sxs-lookup"><span data-stu-id="26918-196">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="26918-197"><xref:microsoft.quantum.diagnostics.dumpmachine>maakt deel uit van de <xref:microsoft.quantum.diagnostics> naam ruimte, dus als u deze wilt gebruiken, moet u een `open` instructie toevoegen:</span><span class="sxs-lookup"><span data-stu-id="26918-197"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="26918-198">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="26918-198">DumpRegister</span></span>

<span data-ttu-id="26918-199"><xref:microsoft.quantum.diagnostics.dumpregister>werkt <xref:microsoft.quantum.diagnostics.dumpmachine> , behalve als het ook een matrix van qubits is om de hoeveelheid gegevens te beperken tot alleen die relevant voor de bijbehorende qubits.</span><span class="sxs-lookup"><span data-stu-id="26918-199"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="26918-200">Net als bij is <xref:microsoft.quantum.diagnostics.dumpmachine> de informatie die door wordt gegenereerd, <xref:microsoft.quantum.diagnostics.dumpregister> afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="26918-200">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="26918-201">Voor de volle Quantum Simulator schrijft het naar het bestand met de functie Wave tot een globale fase van het Quantum subsysteem dat wordt gegenereerd door de geleverde qubits in dezelfde indeling als <xref:microsoft.quantum.diagnostics.dumpmachine> .</span><span class="sxs-lookup"><span data-stu-id="26918-201">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="26918-202">Bijvoorbeeld: Voer een machine opnieuw uit met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} =-e ^ {-i \ Pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\frac{(1 + i)} {2} \ket {1} ) \otimes \frac{-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ aanroepen <xref:microsoft.quantum.diagnostics.dumpregister> voor `qubit[0]` genereert deze uitvoer:</span><span class="sxs-lookup"><span data-stu-id="26918-202">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="26918-203">en aanroepen <xref:microsoft.quantum.diagnostics.dumpregister> voor `qubit[1]` het genereren van deze uitvoer:</span><span class="sxs-lookup"><span data-stu-id="26918-203">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="26918-204">Over het algemeen is de status van een REGI ster dat Entangled met een ander REGI ster een gemengde status in plaats van een zuivere status.</span><span class="sxs-lookup"><span data-stu-id="26918-204">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="26918-205">In dit geval <xref:microsoft.quantum.diagnostics.dumpregister> voert het volgende bericht uit:</span><span class="sxs-lookup"><span data-stu-id="26918-205">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="26918-206">In het volgende voor beeld ziet u hoe u zowel <xref:microsoft.quantum.diagnostics.dumpregister> als <xref:microsoft.quantum.diagnostics.dumpmachine> in uw Q #-code kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="26918-206">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="26918-207">Foutopsporing</span><span class="sxs-lookup"><span data-stu-id="26918-207">Debugging</span></span>

<span data-ttu-id="26918-208">Naast `Assert` en `Dump` functions en Operations ondersteunt Q # een subset van de standaard functies voor het opsporen van problemen met Visual Studio: het [instellen van regel onderbrekingen](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), het [door lopen van code met behulp van F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) en het [controleren van waarden van klassieke variabelen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) is allemaal mogelijk tijdens het uitvoeren van code in de Simulator.</span><span class="sxs-lookup"><span data-stu-id="26918-208">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="26918-209">Fout opsporing in Visual Studio code maakt gebruik van de mogelijkheden voor fout opsporing die worden geboden door de C# voor Visual Studio code-extensie die wordt ondersteund door OmniSharp en waarvoor de [nieuwste versie](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)moet worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="26918-209">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
