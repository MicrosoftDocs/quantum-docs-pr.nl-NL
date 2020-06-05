---
title: Kennismaken met verstrengeling met Q#
description: Meer informatie over het schrijven van een kwantumprogramma in Q#. Een toepassing voor een Bell-toestand ontwikkelen met behulp van de Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 989080e7d9979bb87d14b2580d28732bb1092eb1
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327370"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="b6229-104">Zelfstudie: kennismaken met verstrengeling met Q#\#</span><span class="sxs-lookup"><span data-stu-id="b6229-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="b6229-105">In deze zelfstudie laten we u zien hoe u een Q#-programma schrijft dat qubits manipuleert en meet, en dat de effecten van superpositie en verstrengeling demonstreert.</span><span class="sxs-lookup"><span data-stu-id="b6229-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>
<span data-ttu-id="b6229-106">U krijgt instructies voor het installeren van de QDK, het bouwen van het programma en het uitvoeren van dat programma op een kwantumsimulator.</span><span class="sxs-lookup"><span data-stu-id="b6229-106">This guides you on installing the QDK, building the program and executing that program on a quantum simulator.</span></span>  

<span data-ttu-id="b6229-107">U gaat een toepassing schrijven met de naam Bell om kwantumverstrengeling te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="b6229-107">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="b6229-108">De naam Bell is een verwijzing naar de Bell-toestanden, wat specifieke kwantumtoestanden van twee qubits zijn die worden gebruikt om de eenvoudigste voorbeelden van superpositie en kwantumverstrengeling voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="b6229-108">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="b6229-109">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b6229-109">Pre-requisites</span></span>

<span data-ttu-id="b6229-110">Als u klaar bent om te gaan coderen, voert u deze stappen uit voordat u verdergaat:</span><span class="sxs-lookup"><span data-stu-id="b6229-110">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="b6229-111">Installeer de Quantum Development Kit voor [Python](xref:microsoft.quantum.install.python) of [.NET](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="b6229-111">Install the Quantum Development Kit for [Python](xref:microsoft.quantum.install.python) or [.NET](xref:microsoft.quantum.install.cs).</span></span>
* <span data-ttu-id="b6229-112">Als u de QDK al hebt geïnstalleerd, controleert u of uw versie is [bijgewerkt](xref:microsoft.quantum.update) naar de nieuwste versie</span><span class="sxs-lookup"><span data-stu-id="b6229-112">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="b6229-113">U kunt de instructies ook volgen zonder de QDK te installeren, om een beeld te krijgen van de Q#-programmeertaal en de basisconcepten van kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="b6229-113">You can also follow along with the narrative without installing the QDK, reviewing the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="demonstrating-qubit-behavior-with-q"></a><span data-ttu-id="b6229-114">Gedrag van qubits demonstreren met Q#</span><span class="sxs-lookup"><span data-stu-id="b6229-114">Demonstrating qubit behavior with Q#</span></span>

<span data-ttu-id="b6229-115">Denk nog even terug aan onze eenvoudige [definitie van een qubit](xref:microsoft.quantum.overview.understanding).</span><span class="sxs-lookup"><span data-stu-id="b6229-115">Recall our simple [definition of a qubit](xref:microsoft.quantum.overview.understanding).</span></span>  <span data-ttu-id="b6229-116">Waar klassieke bits één binaire waarde bevatten, zoals een 0 of een 1, kan de toestand van een [qubit](xref:microsoft.quantum.glossary#qubit) in een **superpositie** zijn van 0 en 1.</span><span class="sxs-lookup"><span data-stu-id="b6229-116">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="b6229-117">Conceptueel gezien kan een qubit worden gezien als een richting in de ruimte (ook wel een vector genoemd).</span><span class="sxs-lookup"><span data-stu-id="b6229-117">Conceptually, a qubit can be thought of as a direction in space (also known as a vector).</span></span>  <span data-ttu-id="b6229-118">Een qubit kan zich in een van de mogelijke richtingen bevinden.</span><span class="sxs-lookup"><span data-stu-id="b6229-118">A qubit can be in any of the possible directions.</span></span> <span data-ttu-id="b6229-119">De twee **klassieke toestanden** zijn de twee richtingen, die een 100% kans vertegenwoordigen dat de meting 0 oplevert en een 100% kans dat de meting 1 oplevert.</span><span class="sxs-lookup"><span data-stu-id="b6229-119">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>  <span data-ttu-id="b6229-120">Deze voorstelling is ook formeel te visualiseren door de zogenaamde [Blochbol](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span><span class="sxs-lookup"><span data-stu-id="b6229-120">This representation is also more formally visualized by the [bloch sphere](/quantum/concepts/the-qubit#visualizing-qubits-and-transformations-using-the-bloch-sphere).</span></span>

<span data-ttu-id="b6229-121">De handeling van het meten produceert een binair resultaat en verandert de toestand van een qubit.</span><span class="sxs-lookup"><span data-stu-id="b6229-121">The act of measurement produces a binary result and changes a qubit state.</span></span> <span data-ttu-id="b6229-122">Meting resulteert in een binaire waarde, 0 of 1.</span><span class="sxs-lookup"><span data-stu-id="b6229-122">Measurement produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="b6229-123">De qubit gaat over van de toestand van superpositie (willekeurige richting) in een van de klassieke toestanden.</span><span class="sxs-lookup"><span data-stu-id="b6229-123">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="b6229-124">Daarna levert herhaling van dezelfde meting zonder tussenliggende bewerkingen hetzelfde binaire resultaat op.</span><span class="sxs-lookup"><span data-stu-id="b6229-124">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="b6229-125">Meerdere qubits kunnen worden [**verstrengeld**](xref:microsoft.quantum.glossary#entanglement).</span><span class="sxs-lookup"><span data-stu-id="b6229-125">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span> <span data-ttu-id="b6229-126">Wanneer we een meting uitvoeren van één verstrengelde qubit, wordt onze kennis van de toestand van de andere qubit(s) ook bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b6229-126">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="b6229-127">We laten nu zien hoe dit gedrag wordt uitgedrukt in Q#.</span><span class="sxs-lookup"><span data-stu-id="b6229-127">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="b6229-128">U begint met het eenvoudigst mogelijke programma en bouwt dit op om kwantumsuperpositie en kwantumverstrengeling te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="b6229-128">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="setup"></a><span data-ttu-id="b6229-129">Instellen</span><span class="sxs-lookup"><span data-stu-id="b6229-129">Setup</span></span>

<span data-ttu-id="b6229-130">In deze zelfstudie wordt gebruikgemaakt van een hostprogramma en de studie bestaat uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="b6229-130">This tutorial uses a host programs and consists of two parts:</span></span>

1. <span data-ttu-id="b6229-131">Een reeks kwantumalgoritmen, geïmplementeerd met behulp van de kwantumprogrammeertaal Q#.</span><span class="sxs-lookup"><span data-stu-id="b6229-131">A series of quantum algorithms, implemented using the Q# quantum programming language.</span></span>
1. <span data-ttu-id="b6229-132">Een hostprogramma, geïmplementeerd in Python of C#, die als het belangrijkste toegangspunt fungeert en Q#-bewerkingen aanroept om de kwantumalgoritmen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b6229-132">A host program, implemented in either Python or C#, that serves as the main entry point and invokes Q# operations to execute the quantum algorithms.</span></span>

#### <a name="python"></a>[<span data-ttu-id="b6229-133">Python</span><span class="sxs-lookup"><span data-stu-id="b6229-133">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="b6229-134">Een locatie kiezen voor uw toepassing</span><span class="sxs-lookup"><span data-stu-id="b6229-134">Choose a location for your application</span></span>

1. <span data-ttu-id="b6229-135">Maak een bestand met de naam `Bell.qs`.</span><span class="sxs-lookup"><span data-stu-id="b6229-135">Create a file called `Bell.qs`.</span></span> <span data-ttu-id="b6229-136">Dit bestand bevat uw Q#-code.</span><span class="sxs-lookup"><span data-stu-id="b6229-136">This file will contain your Q# code.</span></span>

1. <span data-ttu-id="b6229-137">Maak een bestand met de naam `host.py`.</span><span class="sxs-lookup"><span data-stu-id="b6229-137">Create a file called `host.py`.</span></span> <span data-ttu-id="b6229-138">Dit bestand bevat uw Python-hostcode.</span><span class="sxs-lookup"><span data-stu-id="b6229-138">This file will contain your Python host code.</span></span>

#### <a name="c-command-line"></a>[<span data-ttu-id="b6229-139">C#-opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="b6229-139">C# Command Line</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="b6229-140">Een nieuw Q#-project maken:</span><span class="sxs-lookup"><span data-stu-id="b6229-140">Create a new Q# project:</span></span>

    ```bash
    dotnet new console -lang Q# --output Bell
    cd Bell
    ```

    <span data-ttu-id="b6229-141">Als het goed is, ziet u een `.csproj`-bestand, een Q#-bestand met de naam `Operations.qs` en een hostprogrammabestand met de naam `Driver.cs`</span><span class="sxs-lookup"><span data-stu-id="b6229-141">You should see a `.csproj` file, a Q# file called `Operations.qs`, and a host program file called `Driver.cs`</span></span>

1. <span data-ttu-id="b6229-142">De naam van het Q#-bestand wijzigen</span><span class="sxs-lookup"><span data-stu-id="b6229-142">Rename the Q# file</span></span>

    ```bash
    mv Operation.qs Bell.qs
    ```

#### <a name="visual-studio"></a>[<span data-ttu-id="b6229-143">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6229-143">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="b6229-144">Een nieuw project maken</span><span class="sxs-lookup"><span data-stu-id="b6229-144">Create a new project</span></span>

   * <span data-ttu-id="b6229-145">Open Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6229-145">Open Visual Studio</span></span>
   * <span data-ttu-id="b6229-146">Ga naar het menu **Bestand** en selecteer **Nieuw** -> **Project...**</span><span class="sxs-lookup"><span data-stu-id="b6229-146">Go to the **File** menu and select **New** -> **Project...**</span></span>
   * <span data-ttu-id="b6229-147">Typ in de sjabloonverkenner `Q#` in het zoekveld en selecteer de sjabloon `Q# Application`</span><span class="sxs-lookup"><span data-stu-id="b6229-147">In the project template explorer, type `Q#` into the search field and select the `Q# Application` template</span></span>
   * <span data-ttu-id="b6229-148">Geef uw project de naam `Bell`</span><span class="sxs-lookup"><span data-stu-id="b6229-148">Give your project the name `Bell`</span></span>

1. <span data-ttu-id="b6229-149">De naam van het Q#-bestand wijzigen</span><span class="sxs-lookup"><span data-stu-id="b6229-149">Rename the Q# file</span></span>

   * <span data-ttu-id="b6229-150">Ga naar **Solution Explorer**</span><span class="sxs-lookup"><span data-stu-id="b6229-150">Navigate to the **Solution Explorer**</span></span>
   * <span data-ttu-id="b6229-151">Klik met de rechter muisknop op bestand `Operations.qs`</span><span class="sxs-lookup"><span data-stu-id="b6229-151">Right click on the `Operations.qs` file</span></span>
   * <span data-ttu-id="b6229-152">Wijzig de naam in `Bell.qs`</span><span class="sxs-lookup"><span data-stu-id="b6229-152">Rename it to `Bell.qs`</span></span>

* * *

## <a name="write-a-q-operation"></a><span data-ttu-id="b6229-153">Een Q#-bewerking schrijven</span><span class="sxs-lookup"><span data-stu-id="b6229-153">Write a Q# operation</span></span>

<span data-ttu-id="b6229-154">We willen twee qubits voorbereiden in een specifieke kwantumtoestand om te laten zien hoe u met Q# bewerkingen kunt uitvoeren op qubits om hun toestand te wijzigen en om de effecten van superpositie en verstrengeling te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="b6229-154">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="b6229-155">Dit alles wordt stukje voor stukje opgebouwd om qubittoestanden, bewerkingen en metingen te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="b6229-155">We will build this up piece by piece to demonstrate qubit states, operations, and measurement.</span></span>

<span data-ttu-id="b6229-156">**Overzicht:**  In het eerste codevoorbeeld hieronder laten we u zien hoe u met qubits kunt werken in Q#.</span><span class="sxs-lookup"><span data-stu-id="b6229-156">**Overview:**  In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="b6229-157">We introduceren twee bewerkingen, `M` en `X`, die de toestand van een qubit transformeren.</span><span class="sxs-lookup"><span data-stu-id="b6229-157">We’ll introduce two operations, `M` and `X` that transform the state of a qubit.</span></span> 

<span data-ttu-id="b6229-158">In dit codefragment wordt een bewerking `Set` gedefinieerd die een qubit als parameter accepteert, evenals een andere parameter, `desired`, die de gewenste toestand van de qubit aangeeft.</span><span class="sxs-lookup"><span data-stu-id="b6229-158">In this code snippet, an operation `Set` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="b6229-159">Met de bewerking `Set` wordt een meting uitgevoerd op de qubit met behulp van de bewerking `M`.</span><span class="sxs-lookup"><span data-stu-id="b6229-159">The operation `Set` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="b6229-160">In Q# levert een qubitmeting altijd `Zero` of `One` op.</span><span class="sxs-lookup"><span data-stu-id="b6229-160">In Q#, a qubit measurement always returns either  `Zero` or `One`.</span></span>  <span data-ttu-id="b6229-161">Als de meting een waarde oplevert die niet gelijk is aan een gewenste waarde, wordt de qubit 'gespiegeld' door Set. Dit houdt in dat er een bewerking `X` wordt uitgevoerd waardoor de toestand van de qubit wordt gewijzigd in een nieuwe toestand waarin de waarschijnlijkheid dat een meting `Zero` en `One` oplevert, wordt omgedraaid.</span><span class="sxs-lookup"><span data-stu-id="b6229-161">If the measurement returns a value not equal to a desired value, Set “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span>  <span data-ttu-id="b6229-162">Om het effect van de bewerking `Set` te demonstreren, wordt er vervolgens een bewerking `TestBellState` toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="b6229-162">To demonstrate the effect of the `Set` operation, a `TestBellState` operation is then added.</span></span>  <span data-ttu-id="b6229-163">Deze bewerking krijgt als invoer een `Zero` of `One` en roept de bewerking `Set` een aantal keer aan met die invoer, en telt het aantal keren dat `Zero` het resultaat is van de meting van de qubit en het aantal keren dat `One` wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="b6229-163">This operation takes as input a `Zero` or `One`, and calls the `Set` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="b6229-164">In deze eerste simulatie van de bewerking `TestBellState` verwachten we natuurlijk dat de uitvoer laat zien dat alle metingen van de qubit die is ingesteld met de parameterinvoer `Zero`, `Zero` oplevert en dat alle metingen van de qubit die is ingesteld met `One` als de parameterinvoer, `One` retourneert.</span><span class="sxs-lookup"><span data-stu-id="b6229-164">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span>  <span data-ttu-id="b6229-165">Later voegen we code toe aan `TestBellState` om de concepten van superpositie en verstrengeling te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="b6229-165">Further on, we’ll add code to `TestBellState` to demonstrating superposition and entanglement.</span></span>


### <a name="q-operation-code"></a><span data-ttu-id="b6229-166">Q#-bewerkingscode</span><span class="sxs-lookup"><span data-stu-id="b6229-166">Q# operation code</span></span>

1. <span data-ttu-id="b6229-167">Vervang de inhoud van het bestand Bell.qs door de volgende code:</span><span class="sxs-lookup"><span data-stu-id="b6229-167">Replace the contents of the Bell.qs file with the following code:</span></span>

    ```qsharp
    namespace Quantum.Bell {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation Set(desired : Result, q1 : Qubit) : Unit {
            if (desired != M(q1)) {
                X(q1);
            }
        }
    }
    ```

    <span data-ttu-id="b6229-168">Deze bewerking kan nu worden aangeroepen om een qubit in te stellen op een klassieke toestand, met in 100% van de gevallen `Zero` of `One` als resultaat.</span><span class="sxs-lookup"><span data-stu-id="b6229-168">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>  <span data-ttu-id="b6229-169">`Zero` en `One` zijn constanten die de enige twee mogelijke resultaten van een meting van een qubit vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="b6229-169">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

    <span data-ttu-id="b6229-170">Met de bewerking `Set` wordt de qubit gemeten.</span><span class="sxs-lookup"><span data-stu-id="b6229-170">The operation `Set` measures the qubit.</span></span>
    <span data-ttu-id="b6229-171">Als de qubit zich in de gewenste toestand bevindt, wordt de toestand ongewijzigd gelaten door `Set`. Als dat niet zo is, wordt de toestand van de qubit gewijzigd in de gewenste toestand door het uitvoeren van de bewerking `X`.</span><span class="sxs-lookup"><span data-stu-id="b6229-171">If the qubit is in the state we want, `Set` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

### <a name="about-q-operations"></a><span data-ttu-id="b6229-172">Q#-bewerkingen</span><span class="sxs-lookup"><span data-stu-id="b6229-172">About Q# operations</span></span>

<span data-ttu-id="b6229-173">Een Q#-bewerking is een kwantumsubroutine,</span><span class="sxs-lookup"><span data-stu-id="b6229-173">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="b6229-174">ofwel een aanroepbare routine die kwantumbewerkingen bevat.</span><span class="sxs-lookup"><span data-stu-id="b6229-174">That is, it is a callable routine that contains quantum operations.</span></span>

<span data-ttu-id="b6229-175">De argumenten voor een bewerking worden tussen haakjes opgegeven als een tupel.</span><span class="sxs-lookup"><span data-stu-id="b6229-175">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="b6229-176">Het retourtype van de bewerking wordt na een dubbele punt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="b6229-176">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="b6229-177">In dit geval heeft de bewerking `Set` geen retourwaarde, zodat deze is gemarkeerd als retourzending `Unit`.</span><span class="sxs-lookup"><span data-stu-id="b6229-177">In this case, the `Set` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="b6229-178">Dit is het Q#-equivalent van `unit` in F#, dat ongeveer analoog is met `void` in C#, en een lege tupel (`Tuple[()]`) in Python.</span><span class="sxs-lookup"><span data-stu-id="b6229-178">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="b6229-179">U hebt twee kwantumbewerkingen gebruikt in uw eerste Q#-bewerking:</span><span class="sxs-lookup"><span data-stu-id="b6229-179">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="b6229-180">De bewerking [M](xref:microsoft.quantum.intrinsic.m), waarmee de toestand van de qubit wordt gemeten</span><span class="sxs-lookup"><span data-stu-id="b6229-180">The [M](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="b6229-181">De bewerking [X](xref:microsoft.quantum.intrinsic.x), waarmee de toestand van een qubit wordt gespiegeld</span><span class="sxs-lookup"><span data-stu-id="b6229-181">The [X](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="b6229-182">Een kwantumbewerking transformeert de toestand van een qubit.</span><span class="sxs-lookup"><span data-stu-id="b6229-182">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="b6229-183">Soms worden kwantumbewerkingen ook wel kwantumpoorten genoemd, analoog aan klassieke logische poorten.</span><span class="sxs-lookup"><span data-stu-id="b6229-183">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="b6229-184">Dit vindt zijn oorsprong in het begintijdperk van de kwantumcomputing, toen algoritmen niets meer waren dan een theoretische constructie en werden gevisualiseerd als schema's, vergelijkbaar met circuitschema's in klassieke computing.</span><span class="sxs-lookup"><span data-stu-id="b6229-184">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="add-q-test-code"></a><span data-ttu-id="b6229-185">Q#-testcode toevoegen</span><span class="sxs-lookup"><span data-stu-id="b6229-185">Add Q# test code</span></span>

1. <span data-ttu-id="b6229-186">Voeg na het einde van bewerking `Set` de volgende bewerking toe aan `Bell.qs` bestand binnen de naamruimte:</span><span class="sxs-lookup"><span data-stu-id="b6229-186">Add the following operation to the `Bell.qs` file, inside the namespace, after the end of the `Set` operation:</span></span>

    ```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                Set(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            Set(Zero, qubit);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
    ```

    <span data-ttu-id="b6229-187">Deze bewerking (`TestBellState`) wordt gedurende `count` iteraties als een lus uitgevoerd, er wordt een opgegeven `initial`-waarde voor een qubit gedefinieerd en vervolgens wordt het resultaat, (`M`), gemeten.</span><span class="sxs-lookup"><span data-stu-id="b6229-187">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="b6229-188">Er worden statistieken verzameld over het aantal nullen en enen dat we hebben gemeten, waarna ze naar de aanroepende functie worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="b6229-188">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="b6229-189">Er wordt nog een andere noodzakelijke bewerking uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b6229-189">It performs one other necessary operation.</span></span> <span data-ttu-id="b6229-190">De qubit wordt opnieuw ingesteld op een bekende toestand (`Zero`) voordat deze wordt geretourneerd, zodat anderen deze qubit een bekende toestand kunnen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="b6229-190">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="b6229-191">Dit wordt door de instructie `using` vereist.</span><span class="sxs-lookup"><span data-stu-id="b6229-191">This is required by the `using` statement.</span></span>

### <a name="about-variables-in-q"></a><span data-ttu-id="b6229-192">Variabelen in Q#</span><span class="sxs-lookup"><span data-stu-id="b6229-192">About variables in Q#</span></span>

<span data-ttu-id="b6229-193">Standaard zijn variabelen in Q# niet meer te veranderen. De waarde kan niet worden gewijzigd als de variabele gebonden is.</span><span class="sxs-lookup"><span data-stu-id="b6229-193">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="b6229-194">Het sleutelwoord `let` wordt gebruikt om de binding van een onveranderlijke variabele aan te geven.</span><span class="sxs-lookup"><span data-stu-id="b6229-194">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="b6229-195">Bewerkingsargumenten zijn altijd onveranderbaar.</span><span class="sxs-lookup"><span data-stu-id="b6229-195">Operation arguments are always immutable.</span></span>

<span data-ttu-id="b6229-196">Als u een variabele nodig hebt waarvan de waarde kan worden gewijzigd, zoals `numOnes` in het voorbeeld, kunt u de variabele declareren met het sleutelwoord `mutable`.</span><span class="sxs-lookup"><span data-stu-id="b6229-196">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="b6229-197">De waarde van een veranderlijke variabele kan worden gewijzigd met behulp van een `set`-instructie.</span><span class="sxs-lookup"><span data-stu-id="b6229-197">A mutable variable's value may be changed using a `set` statement.</span></span>

<span data-ttu-id="b6229-198">In beide gevallen wordt het type variabele door de compiler afgeleid.</span><span class="sxs-lookup"><span data-stu-id="b6229-198">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="b6229-199">Voor Q# zijn geen typeannotaties vereist voor variabelen.</span><span class="sxs-lookup"><span data-stu-id="b6229-199">Q# doesn't require any type annotations for variables.</span></span>

### <a name="about-using-statements-in-q"></a><span data-ttu-id="b6229-200">`using`-instructies in Q#</span><span class="sxs-lookup"><span data-stu-id="b6229-200">About `using` statements in Q#</span></span>

<span data-ttu-id="b6229-201">De instructie `using` is ook speciaal in Q#.</span><span class="sxs-lookup"><span data-stu-id="b6229-201">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="b6229-202">Deze wordt gebruikt om qubits toe te wijzen voor gebruik in een codeblok.</span><span class="sxs-lookup"><span data-stu-id="b6229-202">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="b6229-203">In Q# worden alle qubits dynamisch toegewezen en vrijgegeven. Het zijn geen vaste resources die de gehele levensduur van een complex algoritme meegaan.</span><span class="sxs-lookup"><span data-stu-id="b6229-203">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="b6229-204">Een `using`-instructie wijst aan het begin een set qubits toe en geeft deze qubits aan het einde van het blok vrij.</span><span class="sxs-lookup"><span data-stu-id="b6229-204">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="create-the-host-application-code"></a><span data-ttu-id="b6229-205">De code van de hosttoepassing maken</span><span class="sxs-lookup"><span data-stu-id="b6229-205">Create the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="b6229-206">Python</span><span class="sxs-lookup"><span data-stu-id="b6229-206">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="b6229-207">Open bestand `host.py` en voeg de volgende code toe:</span><span class="sxs-lookup"><span data-stu-id="b6229-207">Open the `host.py` file and add the following code:</span></span>

    ```python
    import qsharp

    from qsharp import Result
    from Quantum.Bell import TestBellState

    initials = (Result.Zero, Result.One)

    for i in initials:
      res = TestBellState.simulate(count=1000, initial=i)
      (num_zeros, num_ones) = res
      print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4}')
    ```

#### <a name="c"></a>[<span data-ttu-id="b6229-208">C#</span><span class="sxs-lookup"><span data-stu-id="b6229-208">C#</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="b6229-209">Vervang de inhoud van bestand `Driver.cs` door de volgende code:</span><span class="sxs-lookup"><span data-stu-id="b6229-209">Replace the contents of the `Driver.cs` file with the following code:</span></span>

    ```csharp
    using System;

    using Microsoft.Quantum.Simulation.Core;
    using Microsoft.Quantum.Simulation.Simulators;

    namespace Quantum.Bell
    {
        class Driver
        {
            static void Main(string[] args)
            {
                using (var qsim = new QuantumSimulator())
                {
                    // Try initial values
                    Result[] initials = new Result[] { Result.Zero, Result.One };
                    foreach (Result initial in initials)
                    {
                        var res = TestBellState.Run(qsim, 1000, initial).Result;
                        var (numZeros, numOnes) = res;
                        System.Console.WriteLine(
                            $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4}");
                    }
                }

                System.Console.WriteLine("Press any key to continue...");
                Console.ReadKey();
            }
        }
    }
    ```

#### [](#tab/tabid-vs2019)

* * *

### <a name="about-the-host-application-code"></a><span data-ttu-id="b6229-210">De code van de hosttoepassing</span><span class="sxs-lookup"><span data-stu-id="b6229-210">About the host application code</span></span>

#### <a name="python"></a>[<span data-ttu-id="b6229-211">Python</span><span class="sxs-lookup"><span data-stu-id="b6229-211">Python</span></span>](#tab/tabid-python)

<span data-ttu-id="b6229-212">De Python-hosttoepassing kent drie onderdelen:</span><span class="sxs-lookup"><span data-stu-id="b6229-212">The Python host application has three parts:</span></span>

* <span data-ttu-id="b6229-213">Bereken de argumenten die vereist zijn voor het kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="b6229-213">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="b6229-214">In het voorbeeld wordt `count` vastgezet op 1000 en `initial` is de beginwaarde van de qubit.</span><span class="sxs-lookup"><span data-stu-id="b6229-214">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="b6229-215">Voer het kwantumalgoritme uit door methode `simulate()` van de geïmporteerde Q#-bewerking aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="b6229-215">Run the quantum algorithm by calling the `simulate()` method of the imported Q# operation.</span></span>
* <span data-ttu-id="b6229-216">Verwerk het resultaat van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="b6229-216">Process the result of the operation.</span></span> <span data-ttu-id="b6229-217">In het voorbeeld ontvangt `res` het resultaat van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="b6229-217">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="b6229-218">Hier is het resultaat een tupel van het aantal nullen (`num_zeros`) en het aantal enen (`num_ones`) dat door de simulator wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="b6229-218">Here the result is a tuple of the number of zeros (`num_zeros`) and number of ones (`num_ones`) measured by the simulator.</span></span> <span data-ttu-id="b6229-219">De tupel wordt gedeconstrueerd om de twee velden te krijgen en de resultaten worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="b6229-219">We deconstruct the tuple to get the two fields, and print the results.</span></span>

#### <a name="c"></a>[<span data-ttu-id="b6229-220">C#</span><span class="sxs-lookup"><span data-stu-id="b6229-220">C#</span></span>](#tab/tabid-csharp)

<span data-ttu-id="b6229-221">De C#-hosttoepassing bestaat uit vier delen:</span><span class="sxs-lookup"><span data-stu-id="b6229-221">The C# host application has four parts:</span></span>

* <span data-ttu-id="b6229-222">Bouw een kwantumsimulator.</span><span class="sxs-lookup"><span data-stu-id="b6229-222">Construct a quantum simulator.</span></span> <span data-ttu-id="b6229-223">In het voorbeeld is `qsim` de simulator.</span><span class="sxs-lookup"><span data-stu-id="b6229-223">In the example, `qsim` is the simulator.</span></span>
* <span data-ttu-id="b6229-224">Bereken de argumenten die vereist zijn voor het kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="b6229-224">Compute any arguments required for the quantum algorithm.</span></span> <span data-ttu-id="b6229-225">In het voorbeeld wordt `count` vastgezet op 1000 en `initial` is de beginwaarde van de qubit.</span><span class="sxs-lookup"><span data-stu-id="b6229-225">In the example, `count` is fixed at a 1000 and `initial` is the initial value of the qubit.</span></span>
* <span data-ttu-id="b6229-226">Voer het kwantumalgoritme uit.</span><span class="sxs-lookup"><span data-stu-id="b6229-226">Run the quantum algorithm.</span></span> <span data-ttu-id="b6229-227">Elke Q#-bewerking genereert een C#-klasse met dezelfde naam.</span><span class="sxs-lookup"><span data-stu-id="b6229-227">Each Q# operation generates a C# class with the same name.</span></span> <span data-ttu-id="b6229-228">Deze klasse heeft een methode `Run` die de bewerking **asynchroon** uitvoert.</span><span class="sxs-lookup"><span data-stu-id="b6229-228">This class has a `Run` method that **asynchronously** executes the operation.</span></span> <span data-ttu-id="b6229-229">De uitvoering is asynchroon, omdat de uitvoering op feitelijke hardware asynchroon is.</span><span class="sxs-lookup"><span data-stu-id="b6229-229">The execution is asynchronous because execution on actual hardware will be asynchronous.</span></span> <span data-ttu-id="b6229-230">Aangezien methode `Run` asynchroon is, wordt eigenschap `Result` opgehaald. Hiermee wordt de uitvoering geblokkeerd totdat de taak is voltooid en het resultaat synchroon wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="b6229-230">Because the `Run` method is asynchronous, we fetch the `Result` property; this blocks execution until the task completes and returns the result synchronously.</span></span>
* <span data-ttu-id="b6229-231">Verwerk het resultaat van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="b6229-231">Process the result of the operation.</span></span> <span data-ttu-id="b6229-232">In het voorbeeld ontvangt `res` het resultaat van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="b6229-232">In the example, `res` receives the result of the operation.</span></span> <span data-ttu-id="b6229-233">Hier is het resultaat een tupel van het aantal nullen (`numZeros`) en het aantal enen (`numOnes`) dat door de simulator wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="b6229-233">Here the result is a tuple of the number of zeros (`numZeros`) and number of ones (`numOnes`) measured by the simulator.</span></span> <span data-ttu-id="b6229-234">Dit wordt geretourneerd als een ValueTuple in C#.</span><span class="sxs-lookup"><span data-stu-id="b6229-234">This is returned as a ValueTuple in C#.</span></span> <span data-ttu-id="b6229-235">De tupel wordt gedeconstrueerd om de twee velden te krijgen, de resultaten worden afgedrukt en er wordt gewacht op het indrukken van een toets.</span><span class="sxs-lookup"><span data-stu-id="b6229-235">We deconstruct the tuple to get the two fields, print the results, and wait for a keypress.</span></span>

#### [](#tab/tabid-vs2019)

* * *

## <a name="build-and-run"></a><span data-ttu-id="b6229-236">Bouwen en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b6229-236">Build and run</span></span>

#### <a name="python"></a>[<span data-ttu-id="b6229-237">Python</span><span class="sxs-lookup"><span data-stu-id="b6229-237">Python</span></span>](#tab/tabid-python)

1. <span data-ttu-id="b6229-238">Voer de volgende opdracht uit via de terminal:</span><span class="sxs-lookup"><span data-stu-id="b6229-238">Run the following command at your terminal:</span></span>

    ```
    python host.py
    ```

    <span data-ttu-id="b6229-239">Met deze opdracht wordt de hosttoepassing uitgevoerd, waarmee de Q#-bewerking wordt gesimuleerd.</span><span class="sxs-lookup"><span data-stu-id="b6229-239">This command runs the host application, which simulates the Q# operation.</span></span>

<span data-ttu-id="b6229-240">De resultaten moeten zijn:</span><span class="sxs-lookup"><span data-stu-id="b6229-240">The results should be:</span></span>

```Output
Init:0    0s=1000 1s=0   
Init:1    0s=0    1s=1000
```

#### <a name="command-line--visual-studio-code"></a>[<span data-ttu-id="b6229-241">Opdrachtregel/Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="b6229-241">Command Line / Visual Studio Code</span></span>](#tab/tabid-csharp)

1. <span data-ttu-id="b6229-242">Voer het volgende uit op de terminal:</span><span class="sxs-lookup"><span data-stu-id="b6229-242">Run the following at your terminal:</span></span>

    ```bash
    dotnet run
    ```

    <span data-ttu-id="b6229-243">Met deze opdracht worden alle vereiste pakketten automatisch gedownload, wordt de toepassing gebouwd en vervolgens uitgevoerd op de opdrachtregel.</span><span class="sxs-lookup"><span data-stu-id="b6229-243">This command will automatically download all required packages, build the application, then run it at the command line.</span></span>

1. <span data-ttu-id="b6229-244">U kunt ook op **F1** drukken om het opdrachtpalet te openen en **Fouten opsporen: starten zonder foutopsporing** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="b6229-244">Alternatively, press **F1** to open the Command Palette and select **Debug: Start Without Debugging.**</span></span>
<span data-ttu-id="b6229-245">U wordt mogelijk gevraagd een nieuw bestand ``launch.json`` te maken waarin wordt beschreven hoe u het programma kunt starten.</span><span class="sxs-lookup"><span data-stu-id="b6229-245">You may be prompted to create a new ``launch.json`` file describing how to start the program.</span></span>
<span data-ttu-id="b6229-246">Het standaardbestand ``launch.json`` moet voor de meeste toepassingen goed werken.</span><span class="sxs-lookup"><span data-stu-id="b6229-246">The default ``launch.json`` should work well for most applications.</span></span>

<span data-ttu-id="b6229-247">De resultaten moeten zijn:</span><span class="sxs-lookup"><span data-stu-id="b6229-247">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

#### <a name="visual-studio"></a>[<span data-ttu-id="b6229-248">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b6229-248">Visual Studio</span></span>](#tab/tabid-vs2019)

1. <span data-ttu-id="b6229-249">Druk op `F5` om het programma te bouwen en uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b6229-249">Just hit `F5`, and your program should build and run!</span></span>

<span data-ttu-id="b6229-250">De resultaten moeten zijn:</span><span class="sxs-lookup"><span data-stu-id="b6229-250">The results should be:</span></span>

```Output
Init:Zero 0s=1000 1s=0
Init:One  0s=0    1s=1000
Press any key to continue...
```

<span data-ttu-id="b6229-251">Het programma wordt afgesloten nadat u op een toets hebt gedrukt.</span><span class="sxs-lookup"><span data-stu-id="b6229-251">The program will exit after you press a key.</span></span>

* * *

## <a name="prepare-superposition"></a><span data-ttu-id="b6229-252">Superpositie voorbereiden</span><span class="sxs-lookup"><span data-stu-id="b6229-252">Prepare superposition</span></span>

<span data-ttu-id="b6229-253">**Overzicht** Laten we nu eens kijken welke manieren beschikbaar zijn in Q# om qubits in superpositie te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="b6229-253">**Overview** Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="b6229-254">Zoals eerder gezegd, kan de toestand van een qubit een superpositie zijn van 0 en 1.</span><span class="sxs-lookup"><span data-stu-id="b6229-254">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="b6229-255">We gaan de bewerking `Hadamard` gebruiken om dit te bereiken.</span><span class="sxs-lookup"><span data-stu-id="b6229-255">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="b6229-256">Als de qubit zich in een van de klassieke toestanden bevindt (waarbij een meting altijd `Zero` of altijd `One` retourneert) wordt de qubit met de bewerking `Hadamard` of `H` in een toestand geplaatst waarin een meting van de qubit in 50% van de gevallen `Zero` retourneert en in 50% van de gevallen `One`.</span><span class="sxs-lookup"><span data-stu-id="b6229-256">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="b6229-257">Conceptueel gezien, kan de qubit worden beschouwd als halverwege tussen de `Zero` en `One`.</span><span class="sxs-lookup"><span data-stu-id="b6229-257">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="b6229-258">Als we nu de bewerking `TestBellState` simuleren, zien we dat de resultaten na meting ongeveer een gelijk aantal keren `Zero` en `One` bevatten.</span><span class="sxs-lookup"><span data-stu-id="b6229-258">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

<span data-ttu-id="b6229-259">Eerst proberen we de qubit te spiegelen (als de qubit zich in de toestand `Zero` bevindt, wordt deze gespiegeld naar `One` en omgekeerd).</span><span class="sxs-lookup"><span data-stu-id="b6229-259">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="b6229-260">Dit wordt bereikt door een bewerking `X` uit te voeren voordat we de qubit meten in `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="b6229-260">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="b6229-261">De resultaten (nadat u op `F5` hebt gedrukt) worden nu omgedraaid:</span><span class="sxs-lookup"><span data-stu-id="b6229-261">Now the results (after pressing `F5`) are reversed:</span></span>

```Output
Init:Zero 0s=0    1s=1000
Init:One  0s=1000 1s=0
```

<span data-ttu-id="b6229-262">Alles wat we tot nu toe hebben gezien, is echter klassiek.</span><span class="sxs-lookup"><span data-stu-id="b6229-262">However, everything we've seen so far is classical.</span></span> <span data-ttu-id="b6229-263">Laten we een kwantumresultaat ophalen.</span><span class="sxs-lookup"><span data-stu-id="b6229-263">Let's get a quantum result.</span></span> <span data-ttu-id="b6229-264">We hoeven alleen maar de bewerking `X` uit het vorige voorbeeld te vervangen door een bewerking `H` of Hadamard.</span><span class="sxs-lookup"><span data-stu-id="b6229-264">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="b6229-265">In plaats van de qubit te spiegelen van 0 naar 1, wordt deze slechts half gespiegeld.</span><span class="sxs-lookup"><span data-stu-id="b6229-265">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="b6229-266">De vervangen regels in `TestBellState` zien er nu als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="b6229-266">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="b6229-267">De resultaten worden nu interessanter:</span><span class="sxs-lookup"><span data-stu-id="b6229-267">Now the results get more interesting:</span></span>

```Output
Init:Zero 0s=484  1s=516
Init:One  0s=522  1s=478
```

<span data-ttu-id="b6229-268">Telkens als we meten, vragen we om een klassieke waarde, maar de qubit bevindt zich halverwege tussen 0 en 1, zodat we de helft van de tijd (statistisch) 0 en de helft van de tijd 1 krijgen.</span><span class="sxs-lookup"><span data-stu-id="b6229-268">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span> <span data-ttu-id="b6229-269">Dit staat bekend als __superpositie__ en geeft ons de eerste echte blik op een kwantumtoestand.</span><span class="sxs-lookup"><span data-stu-id="b6229-269">This is known as __superposition__ and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="b6229-270">Verstrengeling voorbereiden</span><span class="sxs-lookup"><span data-stu-id="b6229-270">Prepare entanglement</span></span>

<span data-ttu-id="b6229-271">**Overzicht:**  Laten we nu eens kijken welke manieren beschikbaar zijn in Q# om verstrengeling van qubits uit te drukken.</span><span class="sxs-lookup"><span data-stu-id="b6229-271">**Overview:**  Now let’s look at how Q# expresses ways to entangle qubits.</span></span>  <span data-ttu-id="b6229-272">Eerst stellen we de eerste qubit in op de begintoestand en gebruiken we vervolgens de bewerking `H` om deze in superpositie te brengen.</span><span class="sxs-lookup"><span data-stu-id="b6229-272">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="b6229-273">Vervolgens gebruiken we, voordat we de eerste qubit gaan meten, een nieuwe bewerking (`CNOT`), die staat voor Controlled-Not.</span><span class="sxs-lookup"><span data-stu-id="b6229-273">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-Not.</span></span>  <span data-ttu-id="b6229-274">Het resultaat van het uitvoeren van deze bewerking op twee qubits is het spiegelen van de tweede qubit als de eerste qubit `One` is.</span><span class="sxs-lookup"><span data-stu-id="b6229-274">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="b6229-275">Nu zijn de twee qubits verstrengeld.</span><span class="sxs-lookup"><span data-stu-id="b6229-275">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="b6229-276">Onze statistieken voor de eerste qubit zijn niet gewijzigd (kans van 50% op een `Zero` of `One` na meting), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ de uitkomst die voor de eerste qubit is gemeten.</span><span class="sxs-lookup"><span data-stu-id="b6229-276">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="b6229-277">Onze `CNOT`-poort heeft de twee qubits verstrengeld, zodat wat er met de ene gebeurt, ook met de andere gebeurt.</span><span class="sxs-lookup"><span data-stu-id="b6229-277">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="b6229-278">Als u de metingen omkeert (de tweede qubit vóór de eerste), zou zich hetzelfde voordoen.</span><span class="sxs-lookup"><span data-stu-id="b6229-278">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="b6229-279">De eerste meting zal willekeurig zijn, waarna de tweede zich houdt aan wat voor de eerste is gedetecteerd.</span><span class="sxs-lookup"><span data-stu-id="b6229-279">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="b6229-280">Het eerste wat we nu moeten doen, is twee qubits toewijzen in plaats van één in `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="b6229-280">The first thing we'll need to do is allocate 2 qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="b6229-281">Zo kunnen we een nieuwe bewerking (`CNOT`) toevoegen voordat we een meting (`M`) in `TestBellState` uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="b6229-281">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
Set(initial, q0);
Set(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="b6229-282">We hebben nog een andere `Set`-bewerking toegevoegd om de eerste qubit te initialiseren, zodat we zeker weten dat deze altijd in toestand `Zero` is wanneer we starten.</span><span class="sxs-lookup"><span data-stu-id="b6229-282">We've added another `Set` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="b6229-283">We moeten ook de tweede qubit opnieuw instellen voordat deze wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="b6229-283">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
Set(Zero, q0);
Set(Zero, q1);
```

<span data-ttu-id="b6229-284">De volledige routine ziet er nu als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="b6229-284">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set (initial, q0);
                Set (Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="b6229-285">Als we deze uitvoeren, krijgen we precies hetzelfde 50-50-resultaat dat we eerder hadden.</span><span class="sxs-lookup"><span data-stu-id="b6229-285">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="b6229-286">Het is echter belangrijk om te weten hoe de tweede qubit reageert op het meten van de eerste.</span><span class="sxs-lookup"><span data-stu-id="b6229-286">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="b6229-287">We voegen deze statistiek toe met een nieuwe versie van de `TestBellState`-bewerking:</span><span class="sxs-lookup"><span data-stu-id="b6229-287">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                Set(initial, q0);
                Set(Zero, q1);

                H(q0);
                CNOT(q0, q1);
                let res = M(q0);

                if (M(q1) == res) {
                    set agree += 1;
                }

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }
            
            Set(Zero, q0);
            Set(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="b6229-288">In de nieuwe retourwaarde (`agree`) wordt telkens bijgehouden als de meting van de eerste qubit overeenkomt met de meting van de tweede qubit.</span><span class="sxs-lookup"><span data-stu-id="b6229-288">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span> <span data-ttu-id="b6229-289">We moeten ook de hosttoepassing dienovereenkomstig bijwerken:</span><span class="sxs-lookup"><span data-stu-id="b6229-289">We also have to update the host application accordingly:</span></span>

#### <a name="python"></a>[<span data-ttu-id="b6229-290">Python</span><span class="sxs-lookup"><span data-stu-id="b6229-290">Python</span></span>](#tab/tabid-python)

```python
import qsharp

from qsharp import Result
from Quantum.Bell import TestBellState

initials = {Result.Zero, Result.One} 

for i in initials:
    res = TestBellState.simulate(count=1000, initial=i)
    (num_zeros, num_ones, agree) = res
    print(f'Init:{i: <4} 0s={num_zeros: <4} 1s={num_ones: <4} agree={agree: <4}')
```

#### <a name="c"></a>[<span data-ttu-id="b6229-291">C#</span><span class="sxs-lookup"><span data-stu-id="b6229-291">C#</span></span>](#tab/tabid-csharp)

```csharp
            using (var qsim = new QuantumSimulator())
            {
                // Try initial values
                Result[] initials = new Result[] { Result.Zero, Result.One };
                foreach (Result initial in initials)
                {
                    var res = TestBellState.Run(qsim, 1000, initial).Result;
                    var (numZeros, numOnes, agree) = res;
                    System.Console.WriteLine(
                        $"Init:{initial,-4} 0s={numZeros,-4} 1s={numOnes,-4} agree={agree,-4}");
                }
            }
            
            System.Console.WriteLine("Press any key to continue...");
            Console.ReadKey();
```

#### [](#tab/tabid-vs2019)

* * *

<span data-ttu-id="b6229-292">Wanneer we nu een uitvoering doen, krijgen we verbluffende uitkomst:</span><span class="sxs-lookup"><span data-stu-id="b6229-292">Now when we run, we get something pretty amazing:</span></span>

```Output
Init:Zero 0s=499  1s=501  agree=1000
Init:One  0s=490  1s=510  agree=1000
```

<span data-ttu-id="b6229-293">Zoals aangegeven in het overzicht, zijn onze statistieken voor de eerste qubit niet gewijzigd (kans van 50% op 0 of 1), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ dezelfde uitkomst als voor de eerste qubit, omdat ze namelijk verstrengeld zijn.</span><span class="sxs-lookup"><span data-stu-id="b6229-293">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

<span data-ttu-id="b6229-294">Gefeliciteerd, u hebt uw eerste kwantumprogramma geschreven.</span><span class="sxs-lookup"><span data-stu-id="b6229-294">Congratulations, you've written your first quantum program!</span></span>

## <a name="next-steps"></a><span data-ttu-id="b6229-295">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="b6229-295">Next steps</span></span>

<span data-ttu-id="b6229-296">De zelfstudie [Zoekalgoritme van Grover](xref:microsoft.quantum.quickstarts.search) laat zien hoe u een zoekalgoritme van Grover kunt bouwen en uitvoeren, een van de populairste algoritmen uit de kwantumcomputing en een goed voorbeeld van een Q#-programma dat kan worden gebruikt voor het oplossen van echte problemen met kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="b6229-296">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="b6229-297">In [Aan de slag met de Quantum Development Kit](xref:microsoft.quantum.welcome) vindt u meer manieren om te leren werken met Q# en kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="b6229-297">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>
