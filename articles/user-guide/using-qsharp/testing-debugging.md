---
title: Testen en foutopsporing
description: Meer informatie over het gebruik van eenheids testen, feiten en beweringen en dump functies om Quantum-Program ma's te testen en fout opsporing uit te voeren.
author: tcNickolas
ms.author: mamykhai
ms.date: 06/01/2020
ms.topic: article
uid: microsoft.quantum.guide.testingdebugging
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: 5505086c5efac89f6940cde1ecae2ce629cfeda5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690965"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="6303a-103">Testen en foutopsporing</span><span class="sxs-lookup"><span data-stu-id="6303a-103">Testing and debugging</span></span>

<span data-ttu-id="6303a-104">Net als bij klassiek Program meren is het essentieel om te controleren of Quantum-Program ma's functioneren zoals bedoeld en om te kunnen vaststellen of het probleem onjuist is.</span><span class="sxs-lookup"><span data-stu-id="6303a-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose incorrect behavior.</span></span>
<span data-ttu-id="6303a-105">In deze sectie hebben we de hulp middelen die worden aangeboden Q# voor het testen en opsporen van fouten in Quantum Program ma's.</span><span class="sxs-lookup"><span data-stu-id="6303a-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="6303a-106">Eenheids tests</span><span class="sxs-lookup"><span data-stu-id="6303a-106">Unit Tests</span></span>

<span data-ttu-id="6303a-107">Een gemeen schappelijke aanpak voor het testen van klassieke Program ma's is het schrijven van kleine Program ma's met de naam *unit-tests* , waarmee code wordt uitgevoerd in een bibliotheek en de uitvoer ervan wordt vergeleken met een verwachte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="6303a-107">One common approach to testing classical programs is to write small programs called *unit tests* , which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="6303a-108">U kunt er bijvoorbeeld voor zorgen dat er `Square(2)` wordt geretourneerd, `4` omdat u *een priori* weet dat $2 ^ 2 = $4.</span><span class="sxs-lookup"><span data-stu-id="6303a-108">For example, you can ensure that `Square(2)` returns `4` since you know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="6303a-109">Q# biedt ondersteuning voor het maken van eenheids tests voor Quantum-Program ma's en die als tests kunnen worden uitgevoerd binnen het test raamwerk van de [xUnit](https://xunit.github.io/) -eenheid.</span><span class="sxs-lookup"><span data-stu-id="6303a-109">Q# supports creating unit tests for quantum programs, and which can run as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="6303a-110">Een test project maken</span><span class="sxs-lookup"><span data-stu-id="6303a-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6303a-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6303a-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="6303a-112">Open Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="6303a-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="6303a-113">Ga naar het menu **bestand** en selecteer **Nieuw > project...** . Zoek in de rechter bovenhoek `Q#` de **Q# test project** sjabloon en selecteer deze.</span><span class="sxs-lookup"><span data-stu-id="6303a-113">Go to the **File** menu and select **New > Project...** . In the upper right corner, search for `Q#`, and select the **Q# Test Project** template.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6303a-114">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6303a-114">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="6303a-115">Voer vanuit uw favoriete opdracht regel de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="6303a-115">From your favorite command line, run the following command:</span></span>
```dotnetcli
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="6303a-116">Het nieuwe project heeft één bestand `Tests.qs` , dat een handige plaats biedt om nieuwe Q# eenheids tests te definiëren.</span><span class="sxs-lookup"><span data-stu-id="6303a-116">Your new project has a single file `Tests.qs`, which provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="6303a-117">In eerste instantie bevat dit bestand één sample-eenheids test `AllocateQubit` waarmee wordt gecontroleerd of een nieuw toegewezen Qubit zich in de status $ \ket $ bevindt {0} en een bericht afdrukt:</span><span class="sxs-lookup"><span data-stu-id="6303a-117">Initially, this file contains one sample unit test `AllocateQubit` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    @Test("QuantumSimulator")
    operation AllocateQubit () : Unit {

        using (qubit = Qubit()) {
            AssertMeasurement([PauliZ], [qubit], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="6303a-118">Elke Q# bewerking of functie die een argument van het type `Unit` en retourneert, `Unit` kan worden gemarkeerd als een eenheids test via het `@Test("...")` kenmerk.</span><span class="sxs-lookup"><span data-stu-id="6303a-118">Any Q# operation or function that takes an argument of type `Unit` and returns `Unit` can be marked as a unit test via the `@Test("...")` attribute.</span></span> <span data-ttu-id="6303a-119">In het vorige voor beeld, het argument voor dat kenmerk, `"QuantumSimulator"` geeft het doel aan waarop de test wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6303a-119">In the previous example, the argument to that attribute, `"QuantumSimulator"`, specifies the target on which the test runs.</span></span> <span data-ttu-id="6303a-120">Eén test kan op meerdere doelen worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="6303a-120">A single test can run on multiple targets.</span></span> <span data-ttu-id="6303a-121">Voeg bijvoorbeeld eerst een kenmerk toe `@Test("ResourcesEstimator")` `AllocateQubit` .</span><span class="sxs-lookup"><span data-stu-id="6303a-121">For example, add an attribute `@Test("ResourcesEstimator")` before `AllocateQubit`.</span></span> 
```qsharp
    @Test("QuantumSimulator")
    @Test("ResourcesEstimator")
    operation AllocateQubit () : Unit {
        ...
```
<span data-ttu-id="6303a-122">Sla het bestand op en voer alle tests uit.</span><span class="sxs-lookup"><span data-stu-id="6303a-122">Save the file and run all tests.</span></span> <span data-ttu-id="6303a-123">Er moeten nu twee eenheids tests zijn, één waarbij `AllocateQubit` wordt uitgevoerd op de `QuantumSimulator` en een waar deze wordt uitgevoerd in de `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="6303a-123">There should now be two unit tests, one where `AllocateQubit` runs on the `QuantumSimulator`, and one where it runs in the `ResourcesEstimator`.</span></span> 

<span data-ttu-id="6303a-124">De Q# compiler herkent de ingebouwde doelen `"QuantumSimulator"` , `"ToffoliSimulator"` en `"ResourcesEstimator"` als geldige uitvoerings doelen voor eenheids testen.</span><span class="sxs-lookup"><span data-stu-id="6303a-124">The Q# compiler recognizes the built-in targets `"QuantumSimulator"`, `"ToffoliSimulator"`, and `"ResourcesEstimator"` as valid run targets for unit tests.</span></span> <span data-ttu-id="6303a-125">Het is ook mogelijk om een volledig gekwalificeerde naam op te geven voor het definiëren van een aangepast uitvoerings doel.</span><span class="sxs-lookup"><span data-stu-id="6303a-125">It is also possible to specify any fully qualified name to define a custom run target.</span></span> 

### <a name="running-no-locq-unit-tests"></a><span data-ttu-id="6303a-126">Actieve Q# eenheids tests</span><span class="sxs-lookup"><span data-stu-id="6303a-126">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6303a-127">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6303a-127">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="6303a-128">Als eenmalige installatie per oplossing, gaat u naar het menu **test** en selecteert u **instellingen testen > standaard processor architectuur > x64** .</span><span class="sxs-lookup"><span data-stu-id="6303a-128">As a one-time per-solution setup, go to the **Test** menu and select **Test Settings > Default Processor Architecture > X64** .</span></span>

> [!TIP]
> <span data-ttu-id="6303a-129">De standaard instelling voor de architectuur van de processor voor Visual Studio wordt opgeslagen in het bestand met oplossings opties ( `.suo` ) voor elke oplossing.</span><span class="sxs-lookup"><span data-stu-id="6303a-129">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="6303a-130">Als u dit bestand verwijdert, moet u opnieuw **x64** selecteren als uw processor architectuur.</span><span class="sxs-lookup"><span data-stu-id="6303a-130">If you delete this file, then you need to select **X64** as your processor architecture again.</span></span>

<span data-ttu-id="6303a-131">Bouw het project, open het menu **test** en selecteer **Windows > test Verkenner** .</span><span class="sxs-lookup"><span data-stu-id="6303a-131">Build the project, open the **Test** menu, and select **Windows > Test Explorer** .</span></span> <span data-ttu-id="6303a-132">**AllocateQubit** wordt weer gegeven in de lijst met tests in de groep **niet-uitgevoerde tests** .</span><span class="sxs-lookup"><span data-stu-id="6303a-132">**AllocateQubit** displays in the list of tests in the **Not Run Tests** group.</span></span> <span data-ttu-id="6303a-133">Selecteer **alles uitvoeren** of voer deze afzonderlijke test uit.</span><span class="sxs-lookup"><span data-stu-id="6303a-133">Select **Run All** or run this individual test.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6303a-134">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6303a-134">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="6303a-135">Als u tests wilt uitvoeren, gaat u naar de projectmap (de map die bevat `Tests.csproj` ) en voert u de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="6303a-135">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and run the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="6303a-136">U ziet dat de uitvoer er ongeveer als volgt uitziet:</span><span class="sxs-lookup"><span data-stu-id="6303a-136">You should get output similar to the following:</span></span>

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

<span data-ttu-id="6303a-137">Eenheids tests kunnen worden gefilterd op basis van de naam of het uitvoerings doel:</span><span class="sxs-lookup"><span data-stu-id="6303a-137">Unit tests can be filtered according to their name or the run target:</span></span>

```bash 
$ dotnet test --filter "Target=QuantumSimulator"
$ dotnet test --filter "Name=AllocateQubit"
```


<span data-ttu-id="6303a-138">\*\*_</span><span class="sxs-lookup"><span data-stu-id="6303a-138">\*\*_</span></span>

<span data-ttu-id="6303a-139">De intrinsieke functie <xref:Microsoft.Quantum.Intrinsic.Message> heeft type `(String -> Unit)` en maakt het mogelijk diagnostische berichten te maken.</span><span class="sxs-lookup"><span data-stu-id="6303a-139">The intrinsic function <xref:Microsoft.Quantum.Intrinsic.Message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6303a-140">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6303a-140">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="6303a-141">Nadat u een test in test Explorer hebt uitgevoerd en op de test hebt geklikt, wordt een deel venster weer gegeven met informatie over de test uitvoering: status van geslaagd/mislukt, verstreken tijd en een koppeling naar de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="6303a-141">After you run a test in Test Explorer and click on the test, a panel displays with information about test run: Pass/fail status, elapsed time, and a link to the output.</span></span> <span data-ttu-id="6303a-142">Klik op _ *uitvoer* \* om de test uitvoer in een nieuw venster te openen.</span><span class="sxs-lookup"><span data-stu-id="6303a-142">Click _ *Output* \* to open the test output in a new window.</span></span>

![test uitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6303a-144">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6303a-144">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="6303a-145">De status pass/fail voor elke test wordt door gegeven aan de console `dotnet test` .</span><span class="sxs-lookup"><span data-stu-id="6303a-145">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="6303a-146">Voor mislukte tests worden ook de uitvoer naar de console afgedrukt om de fout te kunnen vaststellen.</span><span class="sxs-lookup"><span data-stu-id="6303a-146">For failing tests, the outputs are also printed to the console to help diagnose the failure.</span></span>

<span data-ttu-id="6303a-147">\*\*_</span><span class="sxs-lookup"><span data-stu-id="6303a-147">\*\*_</span></span>

## <a name="facts-and-assertions"></a><span data-ttu-id="6303a-148">Feiten en verklaringen</span><span class="sxs-lookup"><span data-stu-id="6303a-148">Facts and Assertions</span></span>

<span data-ttu-id="6303a-149">Omdat functies in Q# geen _logische_ neven effecten hebben, kunt u nooit nagaan, vanuit een Q# programma, andere soorten effecten van het uitvoeren van een functie waarvan het uitvoer type de lege tuple is `()` .</span><span class="sxs-lookup"><span data-stu-id="6303a-149">Because functions in Q# have no _logical_ side effects, you can never observe, from within a Q# program, any other kinds of effects from running a function whose output type is the empty tuple `()`.</span></span>
<span data-ttu-id="6303a-150">Dat wil zeggen dat een doel computer ervoor kiest geen functie uit te voeren die wordt geretourneerd `()` met de garantie dat dit weglatings gedrag van de volgende code niet wordt gewijzigd Q# .</span><span class="sxs-lookup"><span data-stu-id="6303a-150">That is, a target machine can choose not to run any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="6303a-151">Dit gedrag zorgt ervoor dat functies die worden geretourneerd `()` (zoals `Unit` ) een handig hulp middel voor het insluiten van beweringen en het opsporen van fouten in Q# Program ma's.</span><span class="sxs-lookup"><span data-stu-id="6303a-151">This behavior makes functions returning `()` (such as `Unit`) a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

<span data-ttu-id="6303a-152">Laten we eens een eenvoudig voor beeld bekijken:</span><span class="sxs-lookup"><span data-stu-id="6303a-152">Let's consider a simple example:</span></span>

```qsharp
function PositivityFact(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="6303a-153">Hier geeft het sleutel woord `fail` aan dat de berekening niet moet worden voortgezet en wordt er een uitzonde ring gegenereerd op de doel computer waarop het programma wordt uitgevoerd Q# .</span><span class="sxs-lookup"><span data-stu-id="6303a-153">Here, the keyword `fail` indicates that the computation should not proceed, and raises an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="6303a-154">Op basis van de definitie kan een fout van dit soort niet worden waargenomen Q# , omdat de doel computer de code niet langer uitvoert Q# nadat een `fail` instructie is bereikt.</span><span class="sxs-lookup"><span data-stu-id="6303a-154">By definition, a failure of this kind cannot be observed from within Q#, as the target machine no longer runs the Q# code after reaching a `fail` statement.</span></span>
<span data-ttu-id="6303a-155">Daarom `PositivityFact` kunnen we er zeker van zijn dat de invoer van de gegevens positief is.</span><span class="sxs-lookup"><span data-stu-id="6303a-155">Thus, if we proceed past a call to `PositivityFact`, we can be assured that its input was positive.</span></span>

<span data-ttu-id="6303a-156">Houd er rekening mee dat we hetzelfde gedrag kunnen implementeren als `PositivityFact` het gebruik [`Fact`](xref:Microsoft.Quantum.Diagnostics.fact) van de functie uit de <xref:Microsoft.Quantum.Diagnostics> naam ruimte:</span><span class="sxs-lookup"><span data-stu-id="6303a-156">Note that we can implement the same behavior as `PositivityFact` using the [`Fact`](xref:Microsoft.Quantum.Diagnostics.fact) function from the <xref:Microsoft.Quantum.Diagnostics> namespace:</span></span>

```qsharp
    Fact(value > 0, "Expected a positive number.");
```

<span data-ttu-id="6303a-157">_Assertions \* worden daarentegen op dezelfde manier gebruikt als voor waarden, maar dit kan afhankelijk zijn van de status van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="6303a-157">_Assertions\*, on the other hand, are used similarly to facts but may depend on the state of the target machine.</span></span> <span data-ttu-id="6303a-158">Ze worden dienovereenkomstig gedefinieerd als bewerkingen, terwijl feiten worden gedefinieerd als functies (zoals in het vorige voor beeld).</span><span class="sxs-lookup"><span data-stu-id="6303a-158">Correspondingly, they are defined as operations, whereas facts are defined as functions (as in the previous example).</span></span>
<span data-ttu-id="6303a-159">Voor een beter begrip van het onderscheid moet u rekening houden met het volgende gebruik van een feit binnen een bewering:</span><span class="sxs-lookup"><span data-stu-id="6303a-159">To understand the distinction, consider the following use of a fact within an assertion:</span></span>

```qsharp
operation AssertQubitsAreAvailable() : Unit
{
     Fact(GetQubitsAvailableToUse() > 0, "No qubits were actually available");
}
```

<span data-ttu-id="6303a-160">Hier gebruiken we de bewerking <xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse> voor het retour neren van het aantal beschik bare qubits dat kan worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="6303a-160">Here, we are using the operation <xref:Microsoft.Quantum.Environment.GetQubitsAvailableToUse> to return the number of qubits available to use.</span></span>
<span data-ttu-id="6303a-161">Zoals dit afhankelijk is van de algemene status van het programma en de uitvoerings omgeving, moet de definitie van `AssertQubitsAreAvailable` ook een bewerking zijn.</span><span class="sxs-lookup"><span data-stu-id="6303a-161">As this depends on the global state of the program and its run environment, our definition of `AssertQubitsAreAvailable` must be an operation as well.</span></span>
<span data-ttu-id="6303a-162">We kunnen die globale status echter gebruiken om een eenvoudige `Bool` waarde te leveren als invoer voor de `Fact` functie.</span><span class="sxs-lookup"><span data-stu-id="6303a-162">However, we can use that global state to yield a simple `Bool` value as input to the `Fact` function.</span></span>

<span data-ttu-id="6303a-163">[De prelude](xref:microsoft.quantum.libraries.standard.prelude), die voortbouwt op deze ideeën, biedt twee bijzonder nuttige verklaringen <xref:Microsoft.Quantum.Diagnostics.AssertMeasurement> en <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> beide gemodelleerd als bewerkingen op `()` .</span><span class="sxs-lookup"><span data-stu-id="6303a-163">[The prelude](xref:microsoft.quantum.libraries.standard.prelude), building on these ideas, offers two especially useful assertions, <xref:Microsoft.Quantum.Diagnostics.AssertMeasurement> and <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> both modeled as operations onto `()`.</span></span> <span data-ttu-id="6303a-164">Deze beweringen maken elk deel uit van een Pauli-operator die een bepaalde meet waarde beschrijft, een Quantum registratie waarop een meting wordt uitgevoerd en een hypothetisch resultaat.</span><span class="sxs-lookup"><span data-stu-id="6303a-164">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="6303a-165">Doel computers die door simulatie werken, zijn niet gebonden aan [het niet-klonen theorema](https://en.wikipedia.org/wiki/No-cloning_theorem)en kunnen dergelijke metingen uitvoeren zonder de kassa te verstoren die aan dergelijke bevestigingen wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="6303a-165">Target machines which work by simulation are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register that passes to such assertions.</span></span>
<span data-ttu-id="6303a-166">Een Simulator kan vervolgens, net als bij de `PositivityFact` vorige functie, de berekening stoppen als het hypothetische resultaat in de praktijk niet wordt waargenomen:</span><span class="sxs-lookup"><span data-stu-id="6303a-166">A simulator can then, similar to the `PositivityFact` function previous, stop computation if the hypothetical outcome is not observed in practice:</span></span>

```qsharp
using (register = Qubit()) 
{
    H(register);
    AssertMeasurement([PauliX], [register], Zero);
    // Even though we do not have access to states in Q#,
    // we know by the anthropic principle that the state
    // of register at this point is |+〉.
}
```

<span data-ttu-id="6303a-167">In fysieke Quantum-hardware, waarbij het niet-klonen van theorema het onderzoek van een Quantum status voor komt, worden de `AssertMeasurement` en- `AssertMeasurementProbability` bewerkingen gewoon `()` zonder ander effect geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="6303a-167">On physical quantum hardware, where the no-cloning theorem prevents examination of a quantum state, the `AssertMeasurement` and `AssertMeasurementProbability` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="6303a-168">De <xref:Microsoft.Quantum.Diagnostics> naam ruimte bevat verschillende meer functies van de `Assert` familie, waarmee u meer geavanceerde voor waarden kunt controleren.</span><span class="sxs-lookup"><span data-stu-id="6303a-168">The <xref:Microsoft.Quantum.Diagnostics> namespace provides several more functions of the `Assert` family, with which you can check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="6303a-169">Dump functies</span><span class="sxs-lookup"><span data-stu-id="6303a-169">Dump Functions</span></span>

<span data-ttu-id="6303a-170">Voor het oplossen van problemen met Quantum Program ma's <xref:Microsoft.Quantum.Diagnostics> biedt de naam ruimte twee functies die in een bestand de huidige status van de doel computer kunnen dumpen: <xref:Microsoft.Quantum.Diagnostics.DumpMachine> en <xref:Microsoft.Quantum.Diagnostics.DumpRegister> .</span><span class="sxs-lookup"><span data-stu-id="6303a-170">To help troubleshooting quantum programs, the <xref:Microsoft.Quantum.Diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:Microsoft.Quantum.Diagnostics.DumpMachine> and <xref:Microsoft.Quantum.Diagnostics.DumpRegister>.</span></span> <span data-ttu-id="6303a-171">De gegenereerde uitvoer van beide is afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="6303a-171">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="6303a-172">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="6303a-172">DumpMachine</span></span>

<span data-ttu-id="6303a-173">De Full-State Quantum Simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [functie Wave](https://en.wikipedia.org/wiki/Wave_function) van het hele Quantum systeem, als een eendimensionale matrix met complexe getallen, waarbij elk element de amplitude vormt van de kans op het meten van de berekenings basis status $ \ket{n} $, waarbij $ \ket{n} = \ket{b_ {n-1}... b_1b_0} $ voor bits $ \{ b_i \} $.</span><span class="sxs-lookup"><span data-stu-id="6303a-173">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="6303a-174">Bijvoorbeeld, op een computer met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} , \end{align} $ $ aanroepen, wordt <xref:Microsoft.Quantum.Diagnostics.DumpMachine> deze uitvoer gegenereerd:</span><span class="sxs-lookup"><span data-stu-id="6303a-174">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:Microsoft.Quantum.Diagnostics.DumpMachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="6303a-175">De eerste rij bevat een opmerking met de id's van de bijbehorende qubits in hun significante volg orde.</span><span class="sxs-lookup"><span data-stu-id="6303a-175">The first row provides a comment with the ids of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="6303a-176">De rest van de rijen beschrijven de waarschijnlijke amplitude van het meten van de basis status vector $ \ket{n} $ in zowel Cartesisch als polaire indeling.</span><span class="sxs-lookup"><span data-stu-id="6303a-176">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="6303a-177">Gedetailleerd voor de eerste rij:</span><span class="sxs-lookup"><span data-stu-id="6303a-177">In detail for the first row:</span></span>

* <span data-ttu-id="6303a-178">**`∣0❭:`** deze rij komt overeen met de status van de `0` reken kundige basis</span><span class="sxs-lookup"><span data-stu-id="6303a-178">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="6303a-179">**`0.707107 +  0.000000 i`** : de waarschijnlijke amplitude in Cartesisch formaat.</span><span class="sxs-lookup"><span data-stu-id="6303a-179">**`0.707107 +  0.000000 i`** : the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="6303a-180">**` == `** : het `equal` teken scheidt beide equivalente verklaringen.</span><span class="sxs-lookup"><span data-stu-id="6303a-180">**` == `** : the `equal` sign separates both equivalent representations.</span></span>
* <span data-ttu-id="6303a-181">**`**********  `** : Een grafische weer gave van de omvang, het aantal `*` is evenredig met de kans dat deze status vector wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="6303a-181">**`**********  `** : A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="6303a-182">**`[ 0.500000 ]`** : de numerieke waarde van de grootte</span><span class="sxs-lookup"><span data-stu-id="6303a-182">**`[ 0.500000 ]`** : the numeric value of the magnitude</span></span>
* <span data-ttu-id="6303a-183">**`    ---`** : Een grafische weer gave van de fase van de amplitude (Zie de volgende uitvoer).</span><span class="sxs-lookup"><span data-stu-id="6303a-183">**`    ---`** : A graphical representation of the amplitude's phase (see the following output).</span></span>
* <span data-ttu-id="6303a-184">**`[ 0.0000 rad ]`** : de numerieke waarde van de fase (in radialen).</span><span class="sxs-lookup"><span data-stu-id="6303a-184">**`[ 0.0000 rad ]`** : the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="6303a-185">Zowel de grootte als de fase worden weer gegeven met een grafische weer gave.</span><span class="sxs-lookup"><span data-stu-id="6303a-185">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="6303a-186">De weer gave met de grootte is direct vooruit: er wordt een balk van weer gegeven `*` , hoe groter de kans dat de balk groter wordt.</span><span class="sxs-lookup"><span data-stu-id="6303a-186">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="6303a-187">Voor de fase worden de volgende symbolen weer gegeven die de hoek aangeven op basis van bereiken:</span><span class="sxs-lookup"><span data-stu-id="6303a-187">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="6303a-188">In de volgende voor beelden ziet u `DumpMachine` een aantal algemene statussen:</span><span class="sxs-lookup"><span data-stu-id="6303a-188">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="6303a-189">De id van een Qubit wordt tijdens runtime toegewezen en is niet noodzakelijkerwijs uitgelijnd met de volg orde waarin de Qubit is toegewezen of hun positie binnen een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="6303a-189">The id of a qubit is assigned at runtime and is not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019"></a>[<span data-ttu-id="6303a-190">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="6303a-190">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="6303a-191">U kunt een Qubit-id in Visual Studio vinden door een onderbrekings punt in uw code te plaatsen en de waarde van een Qubit-variabele te controleren, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="6303a-191">You can locate a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Qubit-id weer geven in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="6303a-193">de Qubit met index `0` op `register2` heeft id = `3` , de Qubit met index `1` heeft id = `2` .</span><span class="sxs-lookup"><span data-stu-id="6303a-193">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="6303a-194">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="6303a-194">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="6303a-195">U kunt een Qubit-id vinden door de <xref:Microsoft.Quantum.Intrinsic.Message> functie te gebruiken en de variabele Qubit in het bericht door te geven, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="6303a-195">You can locate a qubit id by using the <xref:Microsoft.Quantum.Intrinsic.Message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="6303a-196">Dit kan deze uitvoer genereren:</span><span class="sxs-lookup"><span data-stu-id="6303a-196">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="6303a-197">Dit betekent dat de Qubit met index `0` op `register2` heeft id = `3` , de Qubit met index `1` heeft id = `2` .</span><span class="sxs-lookup"><span data-stu-id="6303a-197">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


<span data-ttu-id="6303a-198">\*\*_</span><span class="sxs-lookup"><span data-stu-id="6303a-198">\*\*_</span></span>

<span data-ttu-id="6303a-199">Aangezien <xref:Microsoft.Quantum.Diagnostics.DumpMachine> u een deel van de  <xref:Microsoft.Quantum.Diagnostics> naam ruimte hebt, moet u een `open` instructie toevoegen om deze te openen:</span><span class="sxs-lookup"><span data-stu-id="6303a-199">Since <xref:Microsoft.Quantum.Diagnostics.DumpMachine> is part of the  <xref:Microsoft.Quantum.Diagnostics> namespace, you must add an `open` statement to access it:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="6303a-200">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="6303a-200">DumpRegister</span></span>

<span data-ttu-id="6303a-201"><xref:Microsoft.Quantum.Diagnostics.DumpRegister> werkt als <xref:Microsoft.Quantum.Diagnostics.DumpMachine> , behalve dat er ook een matrix met qubits wordt gebruikt om de hoeveelheid gegevens te beperken tot alleen die relevant voor de bijbehorende qubits.</span><span class="sxs-lookup"><span data-stu-id="6303a-201"><xref:Microsoft.Quantum.Diagnostics.DumpRegister> works like <xref:Microsoft.Quantum.Diagnostics.DumpMachine>, except that it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="6303a-202">Net als bij is <xref:Microsoft.Quantum.Diagnostics.DumpMachine> de informatie die door wordt gegenereerd, <xref:Microsoft.Quantum.Diagnostics.DumpRegister> afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="6303a-202">As with <xref:Microsoft.Quantum.Diagnostics.DumpMachine>, the information generated by <xref:Microsoft.Quantum.Diagnostics.DumpRegister> depends on the target machine.</span></span> <span data-ttu-id="6303a-203">Voor de volle Quantum Simulator schrijft het naar het bestand met de functie Wave tot een globale fase van het Quantum subsysteem dat wordt gegenereerd door de geleverde qubits in dezelfde indeling als <xref:Microsoft.Quantum.Diagnostics.DumpMachine> .</span><span class="sxs-lookup"><span data-stu-id="6303a-203">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:Microsoft.Quantum.Diagnostics.DumpMachine>.</span></span>  <span data-ttu-id="6303a-204">Bijvoorbeeld: Voer een machine opnieuw uit met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac {1} {\sqrt {2} } \ket {00} -\frac{(1 + i)} {2} \ket {10} =-e ^ {-i \ Pi/4} ((\frac {1} {\sqrt {2} } \ket {0} -\frac{(1 + i)} {2} \ket {1} ) \otimes \frac{-(1 + i)} {\sqrt {2} } \ket {0} ), \end{align} $ $ aanroepen <xref:Microsoft.Quantum.Diagnostics.DumpRegister> voor `qubit[0]` genereert deze uitvoer:</span><span class="sxs-lookup"><span data-stu-id="6303a-204">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:Microsoft.Quantum.Diagnostics.DumpRegister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     _******************* [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="6303a-205">en aanroepen <xref:Microsoft.Quantum.Diagnostics.DumpRegister> voor `qubit[1]` het genereren van deze uitvoer:</span><span class="sxs-lookup"><span data-stu-id="6303a-205">and calling <xref:Microsoft.Quantum.Diagnostics.DumpRegister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="6303a-206">Over het algemeen is de status van een REGI ster dat Entangled met een ander REGI ster een gemengde status in plaats van een zuivere status.</span><span class="sxs-lookup"><span data-stu-id="6303a-206">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="6303a-207">In dit geval <xref:Microsoft.Quantum.Diagnostics.DumpRegister> voert het volgende bericht uit:</span><span class="sxs-lookup"><span data-stu-id="6303a-207">In this case, <xref:Microsoft.Quantum.Diagnostics.DumpRegister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="6303a-208">In het volgende voor beeld ziet u hoe u zowel <xref:Microsoft.Quantum.Diagnostics.DumpRegister> als <xref:Microsoft.Quantum.Diagnostics.DumpMachine> in uw Q# code kunt gebruiken:</span><span class="sxs-lookup"><span data-stu-id="6303a-208">The following example shows you how you can use both <xref:Microsoft.Quantum.Diagnostics.DumpRegister> and <xref:Microsoft.Quantum.Diagnostics.DumpMachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="6303a-209">Foutopsporing</span><span class="sxs-lookup"><span data-stu-id="6303a-209">Debugging</span></span>

<span data-ttu-id="6303a-210">Onder `Assert` en `Dump` functions en Operations Q# ondersteunt een subset van de standaard functies voor het opsporen van fouten in Visual Studio: het [instellen van regel onderbrekingen](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), het [door lopen van code met behulp van F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger)en het [inspecteren van de waarden van klassieke variabelen](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) zijn allemaal mogelijk wanneer u uw code op de Simulator uitvoert.</span><span class="sxs-lookup"><span data-stu-id="6303a-210">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger), and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible when running your code on the simulator.</span></span>

<span data-ttu-id="6303a-211">Fout opsporing in Visual Studio code maakt gebruik van de mogelijkheden voor fout opsporing die worden geboden door de C# voor Visual Studio code-extensie die wordt ondersteund door OmniSharp en waarvoor de [nieuwste versie](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)moet worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="6303a-211">Debugging in Visual Studio Code leverages the debugging capabilities provided by the C# for Visual Studio Code extension powered by OmniSharp and requires installing the [latest version](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp).</span></span> 
