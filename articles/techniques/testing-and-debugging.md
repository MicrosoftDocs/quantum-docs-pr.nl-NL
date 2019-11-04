---
title: 'Q # technieken-testen en fout opsporing | Microsoft Docs'
description: 'Q # technieken-testen en fout opsporing'
author: tcNickolas
ms.author: mamykhai@microsoft.com
uid: microsoft.quantum.techniques.testing-and-debugging
ms.date: 12/11/2017
ms.topic: article
ms.openlocfilehash: 25679331f1bed9f98b86c6eb20f511c891bac1af
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73183485"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="92593-103">Testen en fout opsporing</span><span class="sxs-lookup"><span data-stu-id="92593-103">Testing and Debugging</span></span>

<span data-ttu-id="92593-104">Net als bij het klassieke Program meren is het essentieel om te controleren of Quantum Program ma's functioneren zoals bedoeld en om te kunnen vaststellen of een Quantum programma onjuist is.</span><span class="sxs-lookup"><span data-stu-id="92593-104">As with classical programming, it is essential to be able to check that quantum programs act as intended, and to be able to diagnose a quantum program that is incorrect.</span></span>
<span data-ttu-id="92593-105">In deze sectie hebben we de hulp middelen die worden aangeboden door Q # voor het testen en opsporen van fouten in Quantum Program ma's.</span><span class="sxs-lookup"><span data-stu-id="92593-105">In this section, we cover the tools offered by Q# for testing and debugging quantum programs.</span></span>

## <a name="unit-tests"></a><span data-ttu-id="92593-106">Eenheids tests</span><span class="sxs-lookup"><span data-stu-id="92593-106">Unit Tests</span></span>

<span data-ttu-id="92593-107">Een veelvoorkomende aanpak voor het testen van klassieke Program ma's is het schrijven van kleine Program ma's, de naam *eenheid testen* , die code uitvoeren in een bibliotheek en de uitvoer vergelijkt met een verwachte uitvoer.</span><span class="sxs-lookup"><span data-stu-id="92593-107">One common approach to testing classical programs is to write small programs called *unit tests* which run code in a library and compare its output to some expected output.</span></span>
<span data-ttu-id="92593-108">We willen er bijvoorbeeld voor zorgen dat `Square(2)` `4`retourneert, omdat we *een priori* weten dat $2 ^ 2 = $4.</span><span class="sxs-lookup"><span data-stu-id="92593-108">For instance, we may want to ensure that `Square(2)` returns `4`, since we know *a priori* that $2^2 = 4$.</span></span>

<span data-ttu-id="92593-109">Q # ondersteunt het maken van eenheids tests voor Quantum-Program ma's en die kunnen worden uitgevoerd als tests in het Framework van de [xUnit](https://xunit.github.io/) -analyse-eenheid.</span><span class="sxs-lookup"><span data-stu-id="92593-109">Q# supports creating unit tests for quantum programs, and which can be executed as tests within the [xUnit](https://xunit.github.io/) unit testing framework.</span></span>

### <a name="creating-a-test-project"></a><span data-ttu-id="92593-110">Een test project maken</span><span class="sxs-lookup"><span data-stu-id="92593-110">Creating a Test Project</span></span>

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="92593-111">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="92593-111">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="92593-112">Open Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="92593-112">Open Visual Studio 2019.</span></span> <span data-ttu-id="92593-113">Ga naar het menu `File` en selecteer `New` > `Project...`.</span><span class="sxs-lookup"><span data-stu-id="92593-113">Go to the `File` menu and select `New` > `Project...`.</span></span>
<span data-ttu-id="92593-114">Selecteer in de project-sjabloon Verkenner onder `Installed` > `Visual C#`de sjabloon `Q# Test Project`.</span><span class="sxs-lookup"><span data-stu-id="92593-114">In the project template explorer, under `Installed` > `Visual C#`, select the `Q# Test Project` template.</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="92593-115">Opdracht regel/Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="92593-115">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="92593-116">Voer vanuit uw favoriete opdracht regel de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="92593-116">From your favorite command line, run the following command:</span></span>
```bash
$ dotnet new xunit -lang Q# -o Tests
$ cd Tests
$ code . # To open in Visual Studio Code
```

****

<span data-ttu-id="92593-117">In beide gevallen heeft het nieuwe project twee bestanden geopend.</span><span class="sxs-lookup"><span data-stu-id="92593-117">In either case, your new project will have two files open.</span></span>
<span data-ttu-id="92593-118">Het eerste bestand, `Tests.qs`, biedt een handige plaats om nieuwe Q #-eenheids tests te definiëren.</span><span class="sxs-lookup"><span data-stu-id="92593-118">The first file, `Tests.qs`, provides a convenient place to define new Q# unit tests.</span></span>
<span data-ttu-id="92593-119">In eerste instantie bevat dit bestand een test voor een voorbeeld eenheid `AllocateQubitTest` die controleert of een nieuw toegewezen Qubit zich in de $ \ket{0}$ status bevindt en een bericht afdrukt:</span><span class="sxs-lookup"><span data-stu-id="92593-119">Initially this file contains one sample unit test `AllocateQubitTest` which checks that a newly allocated qubit is in the $\ket{0}$ state and prints a message:</span></span>

```qsharp
    operation AllocateQubitTest () : Unit {
        using (q = Qubit()) {
            Assert([PauliZ], [q], Zero, "Newly allocated qubit must be in the |0⟩ state.");
        }
        
        Message("Test passed");
    }
```

<span data-ttu-id="92593-120">Een Q #-bewerking die compatibel is met het type `(Unit => Unit)` of functie die compatibel is met `(Unit -> Unit)` kan worden uitgevoerd als een eenheids test.</span><span class="sxs-lookup"><span data-stu-id="92593-120">Any Q# operation compatible with the type `(Unit => Unit)` or function compatible with `(Unit -> Unit)` can be executed as a unit test.</span></span> 

<span data-ttu-id="92593-121">Het tweede bestand `TestSuiteRunner.cs` bevat een methode die Q #-eenheids tests detecteert en uitvoert.</span><span class="sxs-lookup"><span data-stu-id="92593-121">The second file, `TestSuiteRunner.cs` contains a method that discovers and runs Q# unit tests.</span></span> <span data-ttu-id="92593-122">Dit is de methode `TestTarget` voorzien van een `OperationDriver` kenmerk.</span><span class="sxs-lookup"><span data-stu-id="92593-122">This is the method `TestTarget` annotated with `OperationDriver` attribute.</span></span>
<span data-ttu-id="92593-123">Het kenmerk `OperationDriver` maakt deel uit van de xUnit extension library micro soft. Quantum. simulatie. xUnit.</span><span class="sxs-lookup"><span data-stu-id="92593-123">The `OperationDriver` attribute is a part of the Xunit extension library Microsoft.Quantum.Simulation.Xunit.</span></span>
<span data-ttu-id="92593-124">Het Framework voor het testen van de eenheid roept `TestTarget` methode voor elke Q #-eenheids test op.</span><span class="sxs-lookup"><span data-stu-id="92593-124">The unit testing framework calls `TestTarget` method for every Q# unit test it has discovered.</span></span>
<span data-ttu-id="92593-125">In het raam werk wordt de beschrijving van de eenheids test door gegeven aan de methode via `op` argument.</span><span class="sxs-lookup"><span data-stu-id="92593-125">The framework passes the unit test description to the method through `op` argument.</span></span> <span data-ttu-id="92593-126">De volgende regel code:</span><span class="sxs-lookup"><span data-stu-id="92593-126">The following line of code:</span></span>
```csharp
op.TestOperationRunner(sim);
```
<span data-ttu-id="92593-127">Hiermee wordt de eenheids test uitgevoerd op `QuantumSimulator`.</span><span class="sxs-lookup"><span data-stu-id="92593-127">executes the unit test on `QuantumSimulator`.</span></span>

<span data-ttu-id="92593-128">Het test detectie mechanisme van de eenheid zoekt standaard naar alle Q #-functies of-bewerkingen van compatibele typen die voldoen aan de volgende eigenschappen:</span><span class="sxs-lookup"><span data-stu-id="92593-128">By default, the unit test discovery mechanism looks for all Q# functions or operations of compatible type that satisfy the following properties:</span></span>
* <span data-ttu-id="92593-129">Deze bevindt zich in dezelfde assembly als de methode die is gekoppeld aan het kenmerk `OperationDriver`.</span><span class="sxs-lookup"><span data-stu-id="92593-129">Located in the same assembly as the method annotated with the `OperationDriver` attribute.</span></span>
* <span data-ttu-id="92593-130">Bevindt zich in dezelfde naam ruimte als de methode die is gekoppeld aan het kenmerk `OperationDriver`.</span><span class="sxs-lookup"><span data-stu-id="92593-130">Located in the same namespace as the method annotated with the `OperationDriver` attribute.</span></span>
* <span data-ttu-id="92593-131">Heeft een naam die eindigt op `Test`.</span><span class="sxs-lookup"><span data-stu-id="92593-131">Has a name ending with `Test`.</span></span>

<span data-ttu-id="92593-132">Een assembly, een naam ruimte en een achtervoegsel voor de functies en bewerkingen voor de eenheids test kunnen worden ingesteld met behulp van optionele para meters van het kenmerk `OperationDriver`:</span><span class="sxs-lookup"><span data-stu-id="92593-132">An assembly, a namespace, and a suffix for unit test functions and operations can be set using optional parameters of the `OperationDriver` attribute:</span></span>
* <span data-ttu-id="92593-133">`AssemblyName` para meter wordt de naam van de assembly ingesteld waarnaar wordt gezocht op tests.</span><span class="sxs-lookup"><span data-stu-id="92593-133">`AssemblyName` parameter sets the name of the assembly which is being searched for tests.</span></span>
* <span data-ttu-id="92593-134">`TestNamespace` para meter wordt de naam van de naam ruimte die wordt doorzocht op tests ingesteld.</span><span class="sxs-lookup"><span data-stu-id="92593-134">`TestNamespace` parameter sets the name of the namespace which is being searched for tests.</span></span>
* <span data-ttu-id="92593-135">`Suffix` stelt het achtervoegsel in van de bewerkings-of functie namen die als eenheids testen worden beschouwd.</span><span class="sxs-lookup"><span data-stu-id="92593-135">`Suffix` sets the suffix of operation or function names that are considered to be unit tests.</span></span>

<span data-ttu-id="92593-136">Daarnaast kunt u met de optionele para meter `TestCasePrefix` een voor voegsel instellen voor de naam van de test case.</span><span class="sxs-lookup"><span data-stu-id="92593-136">In addition, the `TestCasePrefix` optional parameter lets you set a prefix for the name of the test case.</span></span> <span data-ttu-id="92593-137">Het voor voegsel voor de naam van de bewerking wordt weer gegeven in de lijst met test cases.</span><span class="sxs-lookup"><span data-stu-id="92593-137">The prefix in front of the operation name will appear in the list of test cases.</span></span> <span data-ttu-id="92593-138">`TestCasePrefix = "QSim:"` zal er bijvoorbeeld voor zorgen dat `AllocateQubitTest` als `QSim:AllocateQubitTest` worden weer gegeven in de lijst met gevonden tests.</span><span class="sxs-lookup"><span data-stu-id="92593-138">For example, `TestCasePrefix = "QSim:"` will cause `AllocateQubitTest` to appear as `QSim:AllocateQubitTest` in the list of found tests.</span></span> <span data-ttu-id="92593-139">Dit kan handig zijn om te bepalen welke Simulator wordt gebruikt om een test uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="92593-139">This can be useful to indicate, for instance, which simulator is used to run a test.</span></span>

### <a name="running-q-unit-tests"></a><span data-ttu-id="92593-140">Er worden Q #-eenheids tests uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="92593-140">Running Q# Unit Tests</span></span>

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="92593-141">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="92593-141">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="92593-142">Als eenmalige installatie per oplossing, gaat u naar `Test` menu en selecteert u `Test Settings` > `Default Processor Architecture` > `X64`.</span><span class="sxs-lookup"><span data-stu-id="92593-142">As a one-time per-solution setup, go to `Test` menu and select `Test Settings` > `Default Processor Architecture` > `X64`.</span></span>

> [!TIP]
> <span data-ttu-id="92593-143">De standaard instelling voor de architectuur van de processor voor Visual Studio wordt opgeslagen in het bestand met oplossings opties (`.suo`) voor elke oplossing.</span><span class="sxs-lookup"><span data-stu-id="92593-143">The default processor architecture setting for Visual Studio is stored in the solution options (`.suo`) file for each solution.</span></span>
> <span data-ttu-id="92593-144">Als u dit bestand verwijdert, moet u opnieuw `X64` selecteren als uw processor architectuur.</span><span class="sxs-lookup"><span data-stu-id="92593-144">If you delete this file, then you will need to select `X64` as your processor architecture again.</span></span>

<span data-ttu-id="92593-145">Bouw het project, ga naar het menu `Test` en selecteer `Windows` > `Test Explorer`.</span><span class="sxs-lookup"><span data-stu-id="92593-145">Build the project, go to the `Test` menu and select `Windows` > `Test Explorer`.</span></span> <span data-ttu-id="92593-146">`AllocateQubitTest` wordt weer gegeven in de lijst met tests in de `Not Run Tests` groep.</span><span class="sxs-lookup"><span data-stu-id="92593-146">`AllocateQubitTest` will show up in the list of tests in the `Not Run Tests` group.</span></span> <span data-ttu-id="92593-147">Selecteer `Run All` of voer deze afzonderlijke test uit en probeer het opnieuw.</span><span class="sxs-lookup"><span data-stu-id="92593-147">Select `Run All` or run this individual test, and it should pass!</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="92593-148">Opdracht regel/Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="92593-148">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="92593-149">Als u tests wilt uitvoeren, gaat u naar de projectmap (de map die `Tests.csproj`bevat) en voert u de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="92593-149">To run tests, navigate to the project folder (the folder which contains `Tests.csproj`), and execute the command:</span></span>

```bash
$ dotnet restore
$ dotnet test
```

<span data-ttu-id="92593-150">U ziet dat de uitvoer er ongeveer als volgt uitziet:</span><span class="sxs-lookup"><span data-stu-id="92593-150">You should get output similar to the following:</span></span>

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

***

## <a name="logging-and-assertions"></a><span data-ttu-id="92593-151">Logboek registratie en bevestigingen</span><span class="sxs-lookup"><span data-stu-id="92593-151">Logging and Assertions</span></span>

<span data-ttu-id="92593-152">Een belang rijk gevolg van het feit dat functies in Q # geen neven effecten hebben, is dat alle gevolgen van het uitvoeren van een functie waarvan het uitvoer type de lege tuple `()`, nooit in acht kunnen worden genomen vanuit een Q #-programma.</span><span class="sxs-lookup"><span data-stu-id="92593-152">One important consequence of the fact that functions in Q# have no side effects is that any effects of executing a function whose output type is the empty tuple `()` can never be observed from within a Q# program.</span></span>
<span data-ttu-id="92593-153">Dat wil zeggen dat een doel computer ervoor kiest geen functie uit te voeren die `()` retourneert met de garantie dat dit weglatings gedrag van de volgende Q #-code niet wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="92593-153">That is, a target machine can choose not to execute any function which returns `()` with the guarantee that this omission will not modify the behavior of any following Q# code.</span></span>
<span data-ttu-id="92593-154">Hiermee kunnen functies `()` een nuttig hulp programma voor het insluiten van beweringen en fout opsporing in Q #-Program ma's worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="92593-154">This makes functions returning `()` a useful tool for embedding assertions and debugging logic into Q# programs.</span></span> 

### <a name="logging"></a><span data-ttu-id="92593-155">Logboekregistratie</span><span class="sxs-lookup"><span data-stu-id="92593-155">Logging</span></span>

<span data-ttu-id="92593-156">De intrinsieke functie <xref:microsoft.quantum.intrinsic.message> is van het type `(String -> Unit)` en maakt het mogelijk diagnostische berichten te maken.</span><span class="sxs-lookup"><span data-stu-id="92593-156">The intrinsic function <xref:microsoft.quantum.intrinsic.message> has type `(String -> Unit)` and enables the creation of diagnostic messages.</span></span>

<span data-ttu-id="92593-157">De `onLog` actie van `QuantumSimulator` kan worden gebruikt om acties te definiëren die worden uitgevoerd wanneer Q #-code aanroepen `Message`.</span><span class="sxs-lookup"><span data-stu-id="92593-157">The `onLog` action of `QuantumSimulator` can be used to define actions performed when Q# code calls `Message`.</span></span> <span data-ttu-id="92593-158">Standaard worden logboek berichten afgedrukt op standaard uitvoer.</span><span class="sxs-lookup"><span data-stu-id="92593-158">By default logged messages are printed to standard output.</span></span>

<span data-ttu-id="92593-159">Bij het definiëren van een eenheids test suite kunnen de geregistreerde berichten worden omgeleid naar de test uitvoer.</span><span class="sxs-lookup"><span data-stu-id="92593-159">When defining a unit test suite, the logged messages can be directed to the test output.</span></span> <span data-ttu-id="92593-160">Wanneer een project wordt gemaakt op basis van Q # test project sjabloon, wordt deze omleiding vooraf geconfigureerd voor de suite en als volgt gemaakt:</span><span class="sxs-lookup"><span data-stu-id="92593-160">When a project is created from Q# Test Project template, this redirection is pre-configured for the suite and created by default as follows:</span></span>

```qsharp
using (var sim = new QuantumSimulator())
{
    // OnLog defines action(s) performed when Q# test calls operation Message
    sim.OnLog += (msg) => { output.WriteLine(msg); };
    op.TestOperationRunner(sim);
}
```

#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="92593-161">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="92593-161">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

<span data-ttu-id="92593-162">Nadat u een test in test Explorer hebt uitgevoerd en op de test hebt geklikt, wordt er een paneel weer gegeven met informatie over de test uitvoering: geslaagd/mislukt status, verstreken tijd en de koppeling uitvoer.</span><span class="sxs-lookup"><span data-stu-id="92593-162">After you execute a test in Test Explorer and click on the test, a panel will appear with information about test execution: Passed/Failed status, elapsed time and an "Output" link.</span></span> <span data-ttu-id="92593-163">Als u op de koppeling uitvoer klikt, wordt de test uitvoer in een nieuw venster geopend.</span><span class="sxs-lookup"><span data-stu-id="92593-163">If you click the "Output" link, test output will open in a new window.</span></span>

![test uitvoer](~/media/unit-test-output.png)

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="92593-165">Opdracht regel/Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="92593-165">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="92593-166">De status pass/fail voor elke test wordt op de-console afgedrukt door `dotnet test`.</span><span class="sxs-lookup"><span data-stu-id="92593-166">The pass/fail status for each test is printed to the console by `dotnet test`.</span></span>
<span data-ttu-id="92593-167">Voor mislukte tests worden de uitvoer die is geregistreerd als resultaat van de `output.WriteLine(msg)` bovenstaande aanroep ook naar de console afgedrukt om de fout te kunnen vaststellen.</span><span class="sxs-lookup"><span data-stu-id="92593-167">For failing tests, the outputs logged as a result of the `output.WriteLine(msg)` call above are also printed to the console to help diagnose the failure.</span></span>

***

### <a name="assertions"></a><span data-ttu-id="92593-168">Asserties</span><span class="sxs-lookup"><span data-stu-id="92593-168">Assertions</span></span>

<span data-ttu-id="92593-169">Dezelfde logica kan worden toegepast voor het implementeren van bevestigingen.</span><span class="sxs-lookup"><span data-stu-id="92593-169">The same logic can be applied to implementing assertions.</span></span> <span data-ttu-id="92593-170">Laten we eens een eenvoudig voor beeld bekijken:</span><span class="sxs-lookup"><span data-stu-id="92593-170">Let's consider a simple example:</span></span>

```qsharp
function AssertPositive(value : Double) : Unit 
{
    if (value <= 0) 
    {
        fail "Expected a positive number.";
    }
}
```

<span data-ttu-id="92593-171">Hier geeft het tref woord `fail` aan dat de berekening niet moet worden voortgezet, waardoor er een uitzonde ring wordt gegenereerd op de doel computer waarop het Q #-programma wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="92593-171">Here, the keyword `fail` indicates that the computation should not proceed, raising an exception in the target machine running the Q# program.</span></span>
<span data-ttu-id="92593-172">Een fout in deze soort kan per definitie niet worden waargenomen, omdat er geen verdere Q #-code wordt uitgevoerd nadat een `fail`-instructie is bereikt.</span><span class="sxs-lookup"><span data-stu-id="92593-172">By definition, a failure of this kind cannot be observed from within Q#, as no further Q# code is run after a `fail` statement is reached.</span></span>
<span data-ttu-id="92593-173">Daarom kunnen we er zeker van zijn dat de invoer van het `AssertPositive`positief is.</span><span class="sxs-lookup"><span data-stu-id="92593-173">Thus, if we proceed past a call to `AssertPositive`, we can be assured by that its input was positive.</span></span>

<span data-ttu-id="92593-174">Op basis van deze ideeën biedt [de prelude](xref:microsoft.quantum.libraries.standard.prelude) twee nuttige beweringen, <xref:microsoft.quantum.intrinsic.assert> en <xref:microsoft.quantum.intrinsic.assertprob> beide gemodelleerd als bewerkingen op `()`.</span><span class="sxs-lookup"><span data-stu-id="92593-174">Building on these ideas, [the prelude](xref:microsoft.quantum.libraries.standard.prelude) offers two especially useful assertions, <xref:microsoft.quantum.intrinsic.assert> and <xref:microsoft.quantum.intrinsic.assertprob> both modeled as operations onto `()`.</span></span> <span data-ttu-id="92593-175">Deze beweringen maken elk deel uit van een Pauli-operator die een bepaalde waardering van belang beschrijft, een Quantum registratie waarop een meting moet worden uitgevoerd en een hypothetisch resultaat.</span><span class="sxs-lookup"><span data-stu-id="92593-175">These assertions each take a Pauli operator describing a particular measurement of interest, a quantum register on which a measurement is to be performed, and a hypothetical outcome.</span></span>
<span data-ttu-id="92593-176">Op doel computers die door simulatie werken, zijn we niet gebonden aan [het niet-klonen van theorema](https://en.wikipedia.org/wiki/No-cloning_theorem)en kunnen deze metingen worden uitgevoerd zonder dat de registratie wordt verstoord die aan dergelijke verklaringen wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="92593-176">On target machines which work by simulation, we are not bound by [the no-cloning theorem](https://en.wikipedia.org/wiki/No-cloning_theorem), and can perform such measurements without disturbing the register passed to such assertions.</span></span>
<span data-ttu-id="92593-177">Een Simulator kan vervolgens, vergelijkbaar met de bovenstaande `AssertPositive` functie, de berekening afbreken als de hypothetische uitkomst niet in de praktijk wordt waargenomen:</span><span class="sxs-lookup"><span data-stu-id="92593-177">A simulator can then, similar to the `AssertPositive` function above, abort computation if the hypothetical outcome would not be observed in practice:</span></span>

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

<span data-ttu-id="92593-178">In fysieke Quantum hardware, waarbij het niet-klonen van theorema het onderzoek van de Quantum status voor komt, worden de `Assert`-en `AssertProb`-bewerkingen gewoon `()` zonder ander effect weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="92593-178">On physical quantum hardware, where the no-cloning theorem prevents examination of quantum state, the `Assert` and `AssertProb` operations simply return `()` with no other effect.</span></span>

<span data-ttu-id="92593-179">De <xref:microsoft.quantum.diagnostics>-naam ruimte biedt een aantal meer functies van de `Assert`-familie waarmee we meer geavanceerde voor waarden kunnen controleren.</span><span class="sxs-lookup"><span data-stu-id="92593-179">The <xref:microsoft.quantum.diagnostics> namespace provides several more functions of the `Assert` family which allow us to check more advanced conditions.</span></span> 

## <a name="dump-functions"></a><span data-ttu-id="92593-180">Dump functies</span><span class="sxs-lookup"><span data-stu-id="92593-180">Dump Functions</span></span>

<span data-ttu-id="92593-181">Voor het oplossen van problemen met Quantum Program ma's biedt de <xref:microsoft.quantum.diagnostics> naam ruimte twee functies die in een bestand kunnen dumpen van de huidige status van de doel computer: <xref:microsoft.quantum.diagnostics.dumpmachine> en <xref:microsoft.quantum.diagnostics.dumpregister>.</span><span class="sxs-lookup"><span data-stu-id="92593-181">To help troubleshooting quantum programs, the <xref:microsoft.quantum.diagnostics> namespace offers two functions that can dump into a file the current status of the target machine: <xref:microsoft.quantum.diagnostics.dumpmachine> and <xref:microsoft.quantum.diagnostics.dumpregister>.</span></span> <span data-ttu-id="92593-182">De gegenereerde uitvoer van beide is afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="92593-182">The generated output of each depends on the target machine.</span></span>

### <a name="dumpmachine"></a><span data-ttu-id="92593-183">DumpMachine</span><span class="sxs-lookup"><span data-stu-id="92593-183">DumpMachine</span></span>

<span data-ttu-id="92593-184">De Full-State Quantum Simulator gedistribueerd als onderdeel van de Quantum Development Kit schrijft in het bestand de [functie Wave](https://en.wikipedia.org/wiki/Wave_function) van het hele Quantum systeem, als een eendimensionale matrix van complexe getallen, waarbij elk element de amplitude van de de waarschijnlijkheid van het meten van de berekenings basis status $ \ket{n} $, waarbij $ \ket{n} = \ket{b_{n-1}... b_1b_0} $ voor bits $\{b_i\}$.</span><span class="sxs-lookup"><span data-stu-id="92593-184">The full-state quantum simulator distributed as part of the Quantum Development Kit writes into the file the [wave function](https://en.wikipedia.org/wiki/Wave_function) of the entire quantum system, as a one-dimensional array of complex numbers, in which each element represents the amplitude of the probability of measuring the computational basis state $\ket{n}$, where $\ket{n} = \ket{b_{n-1}...b_1b_0}$ for bits $\{b_i\}$.</span></span> <span data-ttu-id="92593-185">Bijvoorbeeld op een machine met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10}, \end{align} $ $ aanroepen <xref:microsoft.quantum.diagnostics.dumpmachine> deze uitvoer genereert :</span><span class="sxs-lookup"><span data-stu-id="92593-185">For example, on a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10}, \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpmachine> generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0;1
∣0❭:     0.707107 +  0.000000 i  ==     **********           [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
∣2❭:    -0.500000 + -0.500000 i  ==     **********           [ 0.500000 ]   /     [ -2.35619 rad ]
∣3❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="92593-186">De eerste rij bevat een opmerking met de Id's van de bijbehorende qubits in hun significante volg orde.</span><span class="sxs-lookup"><span data-stu-id="92593-186">The first row provides a comment with the IDs of the corresponding qubits in their significant order.</span></span>
<span data-ttu-id="92593-187">De rest van de rijen beschrijven de waarschijnlijke amplitude van het meten van de basis status vector $ \ket{n} $ in zowel Cartesisch als polaire indeling.</span><span class="sxs-lookup"><span data-stu-id="92593-187">The rest of the rows describe the probability amplitude of measuring the basis state vector $\ket{n}$ in both Cartesian and polar formats.</span></span> <span data-ttu-id="92593-188">Gedetailleerd voor de eerste rij:</span><span class="sxs-lookup"><span data-stu-id="92593-188">In detail for the first row:</span></span>

* <span data-ttu-id="92593-189">**`∣0❭:`** deze rij overeenkomt met de status van de `0` berekening</span><span class="sxs-lookup"><span data-stu-id="92593-189">**`∣0❭:`** this row corresponds to the `0` computational basis state</span></span>
* <span data-ttu-id="92593-190">**`0.707107 +  0.000000 i`** : de waarschijnlijke amplitude in Cartesisch formaat.</span><span class="sxs-lookup"><span data-stu-id="92593-190">**`0.707107 +  0.000000 i`**: the probability amplitude in Cartesian format.</span></span>
* <span data-ttu-id="92593-191">**` == `** : in het `equal`-teken worden beide equivalente verklaringen gescheiden.</span><span class="sxs-lookup"><span data-stu-id="92593-191">**` == `**: the `equal` sign seperates both equivalent representations.</span></span>
* <span data-ttu-id="92593-192">**`**********  `** : een grafische weer gave van de omvang, het aantal `*` is evenredig met de waarschijnlijkheid van het meten van deze status vector.</span><span class="sxs-lookup"><span data-stu-id="92593-192">**`**********  `**: A graphical representation of the magnitude, the number of `*` is proportionate to the probability of measuring this state vector.</span></span>
* <span data-ttu-id="92593-193">**`[ 0.500000 ]`** : de numerieke waarde van de grootte</span><span class="sxs-lookup"><span data-stu-id="92593-193">**`[ 0.500000 ]`**: the numeric value of the magnitude</span></span>
* <span data-ttu-id="92593-194">**`    ---`** : een grafische weer gave van de amplitude fase (zie hieronder).</span><span class="sxs-lookup"><span data-stu-id="92593-194">**`    ---`**: A graphical representation of the amplitude's phase (see below).</span></span>
* <span data-ttu-id="92593-195">**`[ 0.0000 rad ]`** : de numerieke waarde van de fase (in radialen).</span><span class="sxs-lookup"><span data-stu-id="92593-195">**`[ 0.0000 rad ]`**: the numeric value of the phase (in radians).</span></span>

<span data-ttu-id="92593-196">Zowel de grootte als de fase worden weer gegeven met een grafische weer gave.</span><span class="sxs-lookup"><span data-stu-id="92593-196">Both the magnitude and the phase are displayed with a graphical representation.</span></span> <span data-ttu-id="92593-197">De weer gave met de grootte is direct vooruit: er wordt een balk van `*`weer gegeven, hoe groter de kans dat de balk groter is.</span><span class="sxs-lookup"><span data-stu-id="92593-197">The magnitude representation is straight-forward: it shows a bar of `*`, the bigger the probability the bigger the bar will be.</span></span> <span data-ttu-id="92593-198">Voor de fase worden de volgende symbolen weer gegeven die de hoek aangeven op basis van bereiken:</span><span class="sxs-lookup"><span data-stu-id="92593-198">For the phase, we show the following symbols to represent the angle based on ranges:</span></span>

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

<span data-ttu-id="92593-199">In de volgende voor beelden ziet u `DumpMachine` voor een aantal algemene statussen:</span><span class="sxs-lookup"><span data-stu-id="92593-199">The following examples show `DumpMachine` for some common states:</span></span>

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
  > <span data-ttu-id="92593-200">De id van een Qubit wordt tijdens runtime toegewezen en is niet noodzakelijkerwijs uitgelijnd met de volg orde waarin de Qubit is toegewezen of hun positie binnen een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="92593-200">The id of a qubit is assigned at runtime and it's not necessarily aligned with the order in which the qubit was allocated or its position within a qubit register.</span></span>


#### <a name="visual-studio-2019tabtabid-vs2019"></a>[<span data-ttu-id="92593-201">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="92593-201">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

  > [!TIP]
  > <span data-ttu-id="92593-202">U kunt een Qubit-id in Visual Studio uitzoeken door een onderbrekings punt in uw code te plaatsen en de waarde van een Qubit-variabele te controleren, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="92593-202">You can figure out a qubit id in Visual Studio by putting a breakpoint in your code and inspecting the value of a qubit variable, for example:</span></span>
  > 
  > ![Qubit-id weer geven in Visual Studio](~/media/qubit_id.png)
  >
  > <span data-ttu-id="92593-204">de Qubit met index `0` op `register2` heeft id =`3`. de Qubit met index `1` heeft id =`2`.</span><span class="sxs-lookup"><span data-stu-id="92593-204">the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>

#### <a name="command-line--visual-studio-codetabtabid-vscode"></a>[<span data-ttu-id="92593-205">Opdracht regel/Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="92593-205">Command Line / Visual Studio Code</span></span>](#tab/tabid-vscode)

  > [!TIP]
  > <span data-ttu-id="92593-206">U kunt een Qubit-id berekenen met behulp van de functie <xref:microsoft.quantum.intrinsic.message> en de variabele Qubit in het bericht door geven, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="92593-206">You can figure out a qubit id by using the <xref:microsoft.quantum.intrinsic.message> function and passing the qubit variable in the message, for example:</span></span>
  >
  > ```qsharp
  > Message($"0={register2[0]}; 1={register2[1]}");
  > ```
  > 
  > <span data-ttu-id="92593-207">Dit kan deze uitvoer genereren:</span><span class="sxs-lookup"><span data-stu-id="92593-207">which could generate this output:</span></span>
  >```
  > 0=q:3; 1=q:2
  >```
  > <span data-ttu-id="92593-208">Dit betekent dat de Qubit met index `0` op `register2` een id =`3`heeft, de Qubit met index `1` een id =`2`heeft.</span><span class="sxs-lookup"><span data-stu-id="92593-208">which means that the qubit with index `0` on `register2` has id=`3`, the qubit with index `1` has id=`2`.</span></span>


***

<span data-ttu-id="92593-209"><xref:microsoft.quantum.diagnostics.dumpmachine> maakt deel uit van de <xref:microsoft.quantum.diagnostics> naam ruimte, dus als u deze wilt gebruiken, moet u een `open`-instructie toevoegen:</span><span class="sxs-lookup"><span data-stu-id="92593-209"><xref:microsoft.quantum.diagnostics.dumpmachine> is part of the  <xref:microsoft.quantum.diagnostics> namespace, so in order to use it you must add an `open` statement:</span></span>

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


### <a name="dumpregister"></a><span data-ttu-id="92593-210">DumpRegister</span><span class="sxs-lookup"><span data-stu-id="92593-210">DumpRegister</span></span>

<span data-ttu-id="92593-211"><xref:microsoft.quantum.diagnostics.dumpregister> werkt als <xref:microsoft.quantum.diagnostics.dumpmachine>, maar er wordt ook een matrix van qubits gebruikt om de hoeveelheid gegevens te beperken tot alleen die relevant voor de bijbehorende qubits.</span><span class="sxs-lookup"><span data-stu-id="92593-211"><xref:microsoft.quantum.diagnostics.dumpregister> works like <xref:microsoft.quantum.diagnostics.dumpmachine>, except it also takes an array of qubits to limit the amount of information to only that relevant to the corresponding qubits.</span></span>

<span data-ttu-id="92593-212">Net als bij <xref:microsoft.quantum.diagnostics.dumpmachine>is de informatie die door <xref:microsoft.quantum.diagnostics.dumpregister> wordt gegenereerd, afhankelijk van de doel computer.</span><span class="sxs-lookup"><span data-stu-id="92593-212">As with <xref:microsoft.quantum.diagnostics.dumpmachine>, the information generated by <xref:microsoft.quantum.diagnostics.dumpregister> depends on the target machine.</span></span> <span data-ttu-id="92593-213">Voor de volle Quantum Simulator schrijft het naar het bestand met de functie Wave tot een globale fase van het Quantum subsysteem dat wordt gegenereerd door de geleverde qubits in dezelfde indeling als <xref:microsoft.quantum.diagnostics.dumpmachine>.</span><span class="sxs-lookup"><span data-stu-id="92593-213">For the full-state quantum simulator it writes into the file the wave function up to a global phase of the quantum sub-system generated by the provided qubits in the same format as <xref:microsoft.quantum.diagnostics.dumpmachine>.</span></span>  <span data-ttu-id="92593-214">Neem bijvoorbeeld opnieuw een machine met slechts twee qubits toegewezen en in de Quantum status $ $ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00}-\frac{(1 + i)}{2} \ket{10} =-e ^ {-i \ Pi/4} ((\frac{1}{\sqrt{2}} \ Ket{0}-\frac{(1 + i)}{2} \ket{1}) \otimes \frac{-(1 + i)} {\sqrt{2}} \ket{0}), \end{align} $ $ die <xref:microsoft.quantum.diagnostics.dumpregister> aanroept voor `qubit[0]`, wordt deze uitvoer gegenereerd:</span><span class="sxs-lookup"><span data-stu-id="92593-214">For example, take again a machine with only two qubits allocated and in the quantum state $$ \begin{align} \ket{\psi} = \frac{1}{\sqrt{2}} \ket{00} - \frac{(1 + i)}{2} \ket{10} = - e^{-i\pi/4} ( (\frac{1}{\sqrt{2}} \ket{0} - \frac{(1 + i)}{2} \ket{1} ) \otimes \frac{-(1 + i)}{\sqrt{2}} \ket{0} ) , \end{align} $$ calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[0]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 0
∣0❭:    -0.707107 + -0.707107 i  ==     ******************** [ 1.000000 ]  /      [ -2.35619 rad ]
∣1❭:     0.000000 +  0.000000 i  ==                          [ 0.000000 ]                   
```

<span data-ttu-id="92593-215">en het aanroepen van <xref:microsoft.quantum.diagnostics.dumpregister> voor `qubit[1]` genereert deze uitvoer:</span><span class="sxs-lookup"><span data-stu-id="92593-215">and calling <xref:microsoft.quantum.diagnostics.dumpregister> for `qubit[1]` generates this output:</span></span>

```
# wave function for qubits with ids (least to most significant): 1
∣0❭:     0.707107 +  0.000000 i  ==     ***********          [ 0.500000 ]     --- [  0.00000 rad ]
∣1❭:    -0.500000 + -0.500000 i  ==     ***********          [ 0.500000 ]  /      [ -2.35619 rad ]
```

<span data-ttu-id="92593-216">Over het algemeen is de status van een REGI ster dat Entangled met een ander REGI ster een gemengde status in plaats van een zuivere status.</span><span class="sxs-lookup"><span data-stu-id="92593-216">In general, the state of a register that is entangled with another register is a mixed state rather than a pure state.</span></span> <span data-ttu-id="92593-217">In dit geval wordt <xref:microsoft.quantum.diagnostics.dumpregister> het volgende bericht uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="92593-217">In this case, <xref:microsoft.quantum.diagnostics.dumpregister> outputs the following message:</span></span>

```
Qubits provided (0;) are entangled with some other qubit.
```

<span data-ttu-id="92593-218">In het volgende voor beeld ziet u hoe u zowel <xref:microsoft.quantum.diagnostics.dumpregister> als <xref:microsoft.quantum.diagnostics.dumpmachine> kunt gebruiken in uw Q #-code:</span><span class="sxs-lookup"><span data-stu-id="92593-218">The following example shows you how you can use both <xref:microsoft.quantum.diagnostics.dumpregister> and <xref:microsoft.quantum.diagnostics.dumpmachine> in your Q# code:</span></span>

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

## <a name="debugging"></a><span data-ttu-id="92593-219">Foutopsporing</span><span class="sxs-lookup"><span data-stu-id="92593-219">Debugging</span></span>

<span data-ttu-id="92593-220">Op de `Assert`-en `Dump` functies en-bewerkingen ondersteunt Q # een subset van de standaard mogelijkheden voor Visual Studio-fout opsporing: [regel onderbrekingen instellen](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), de [code door lopen met behulp van F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) en [waarden van klassieke variabelen controleren ](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows)zijn allemaal mogelijk tijdens het uitvoeren van code in de Simulator.</span><span class="sxs-lookup"><span data-stu-id="92593-220">On top of `Assert` and `Dump` functions and operations, Q# supports a subset of standard Visual Studio debugging capabilities: [setting line breakpoints](https://docs.microsoft.com/visualstudio/debugger/using-breakpoints), [stepping through code using F10](https://docs.microsoft.com/visualstudio/debugger/navigating-through-code-with-the-debugger) and [inspecting values of classic variables](https://docs.microsoft.com/visualstudio/debugger/autos-and-locals-windows) are all possible during code execution on the simulator.</span></span>

<span data-ttu-id="92593-221">Fout opsporing in Visual Studio code wordt nog niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="92593-221">Debugging in Visual Studio Code is not yet supported.</span></span>

