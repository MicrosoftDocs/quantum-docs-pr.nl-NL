---
title: Kennismaken met verstrengeling met Q#
description: Meer informatie over het schrijven van een kwantumprogramma in Q#. Een toepassing voor een Bell-toestand ontwikkelen met behulp van de Quantum Development Kit (QDK)
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 05/29/2020
ms.topic: tutorial
uid: microsoft.quantum.write-program
ms.openlocfilehash: 16c93b3dd17363c06602529cb34e8fc84aadc7a8
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415419"
---
# <a name="tutorial-explore-entanglement-with-q"></a><span data-ttu-id="c331e-104">Zelfstudie: kennismaken met verstrengeling met Q#\#</span><span class="sxs-lookup"><span data-stu-id="c331e-104">Tutorial: Explore entanglement with Q\#</span></span>

<span data-ttu-id="c331e-105">In deze zelfstudie laten we u zien hoe u een Q#-programma schrijft dat qubits manipuleert en meet, en dat de effecten van superpositie en verstrengeling demonstreert.</span><span class="sxs-lookup"><span data-stu-id="c331e-105">In this tutorial, we show you how to write a Q# program that manipulates and measures qubits and demonstrates the effects of superposition and entanglement.</span></span>

<span data-ttu-id="c331e-106">U gaat een toepassing schrijven met de naam Bell om kwantumverstrengeling te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="c331e-106">You will write an application called Bell to demonstrate quantum entanglement.</span></span>
<span data-ttu-id="c331e-107">De naam Bell is een verwijzing naar de Bell-toestanden, wat specifieke kwantumtoestanden van twee qubits zijn die worden gebruikt om de eenvoudigste voorbeelden van superpositie en kwantumverstrengeling voor te stellen.</span><span class="sxs-lookup"><span data-stu-id="c331e-107">The name Bell is in reference to Bell states, which are specific quantum states of two qubits that are used to represent the simplest examples of superposition and quantum entanglement.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="c331e-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="c331e-108">Pre-requisites</span></span>

<span data-ttu-id="c331e-109">Als u klaar bent om te gaan coderen, voert u deze stappen uit voordat u verdergaat:</span><span class="sxs-lookup"><span data-stu-id="c331e-109">If you are ready to start coding, follow these steps before proceeding:</span></span> 

* <span data-ttu-id="c331e-110">[Installeer](xref:microsoft.quantum.install) de Quantum Development Kit met uw voorkeurs taal en-ontwikkelings omgeving.</span><span class="sxs-lookup"><span data-stu-id="c331e-110">[Install](xref:microsoft.quantum.install) the Quantum Development Kit using your  preferred language and development environment.</span></span>
* <span data-ttu-id="c331e-111">Als u de QDK al hebt geïnstalleerd, controleert u of uw versie is [bijgewerkt](xref:microsoft.quantum.update) naar de nieuwste versie</span><span class="sxs-lookup"><span data-stu-id="c331e-111">If you already have the QDK installed, make sure you have [updated](xref:microsoft.quantum.update) to the latest version</span></span>

<span data-ttu-id="c331e-112">U kunt ook de oplossing volgen zonder de QDK te installeren en de overzichten van de Q #-programmeer taal en de eerste concepten van quantum computing te bekijken.</span><span class="sxs-lookup"><span data-stu-id="c331e-112">You can also follow along with the narrative without installing the QDK, reviewing  the overviews of the Q# programming language and the first concepts of quantum computing.</span></span>

## <a name="in-this-tutorial-youll-learn-how-to"></a><span data-ttu-id="c331e-113">In deze zelfstudie leert u het volgende:</span><span class="sxs-lookup"><span data-stu-id="c331e-113">In this tutorial, you'll learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="c331e-114">Bewerkingen in Q maken en combi neren\#</span><span class="sxs-lookup"><span data-stu-id="c331e-114">Create and combine operations in Q\#</span></span>
> * <span data-ttu-id="c331e-115">Maak bewerkingen om qubits toe te voegen aan de superpositie, entangle en meet ze te meten.</span><span class="sxs-lookup"><span data-stu-id="c331e-115">Create operations to put qubits in superposition, entangle and measure them.</span></span>
> * <span data-ttu-id="c331e-116">Laat Quantum Entanglement zien met een Q #-programma dat wordt uitgevoerd in een simulator.</span><span class="sxs-lookup"><span data-stu-id="c331e-116">Demonstrate quantum entanglement with a Q# program run in a simulator.</span></span> 

## <a name="demonstrating-qubit-behavior-with-the-qdk"></a><span data-ttu-id="c331e-117">Een demonstratie van het gedrag van Qubit met de QDK</span><span class="sxs-lookup"><span data-stu-id="c331e-117">Demonstrating qubit behavior with the QDK</span></span>

<span data-ttu-id="c331e-118">Waar klassieke bits één binaire waarde bevatten, zoals een 0 of een 1, kan de toestand van een [qubit](xref:microsoft.quantum.glossary#qubit) in een **superpositie** zijn van 0 en 1.</span><span class="sxs-lookup"><span data-stu-id="c331e-118">Where classical bits hold a single binary value such as a 0 or 1, the state of a [qubit](xref:microsoft.quantum.glossary#qubit) can be in a **superposition** of 0 and 1.</span></span>  <span data-ttu-id="c331e-119">In het algemeen kan de status van een Qubit worden beschouwd als een richting in een abstracte ruimte (ook wel een vector genoemd).</span><span class="sxs-lookup"><span data-stu-id="c331e-119">Conceptually, the state of a qubit can be thought of as a direction in an abstract space (also known as a vector).</span></span>  <span data-ttu-id="c331e-120">Een Qubit-status kan zich in een van de mogelijke richtingen bevindt.</span><span class="sxs-lookup"><span data-stu-id="c331e-120">A qubit state can be in any of the possible directions.</span></span> <span data-ttu-id="c331e-121">De twee **klassieke toestanden** zijn de twee richtingen, die een 100% kans vertegenwoordigen dat de meting 0 oplevert en een 100% kans dat de meting 1 oplevert.</span><span class="sxs-lookup"><span data-stu-id="c331e-121">The two **classical states** are the two directions; representing 100% chance of measuring 0 and 100% chance of measuring 1.</span></span>

<span data-ttu-id="c331e-122">De handeling van het meten produceert een binair resultaat en verandert de toestand van een qubit.</span><span class="sxs-lookup"><span data-stu-id="c331e-122">The act of measurement produces a binary result and changes a qubit state.</span></span>
<span data-ttu-id="c331e-123">Meting resulteert in een binaire waarde, 0 of 1.</span><span class="sxs-lookup"><span data-stu-id="c331e-123">Measurement  produces a binary value, either 0 or 1.</span></span>  <span data-ttu-id="c331e-124">De qubit gaat over van de toestand van superpositie (willekeurige richting) in een van de klassieke toestanden.</span><span class="sxs-lookup"><span data-stu-id="c331e-124">The qubit goes from being in superposition (any direction) to one of the classical states.</span></span>  <span data-ttu-id="c331e-125">Daarna levert herhaling van dezelfde meting zonder tussenliggende bewerkingen hetzelfde binaire resultaat op.</span><span class="sxs-lookup"><span data-stu-id="c331e-125">Thereafter, repeating the same measurement without any intervening operations produces the same binary result.</span></span>  

<span data-ttu-id="c331e-126">Meerdere qubits kunnen worden [**verstrengeld**](xref:microsoft.quantum.glossary#entanglement).</span><span class="sxs-lookup"><span data-stu-id="c331e-126">Multiple qubits can be [**entangled**](xref:microsoft.quantum.glossary#entanglement).</span></span>  <span data-ttu-id="c331e-127">Wanneer we een meting uitvoeren van één verstrengelde qubit, wordt onze kennis van de toestand van de andere qubit(s) ook bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="c331e-127">When we make a measurement of one entangled qubit, our knowledge of the state of the other(s) is updated as well.</span></span>

<span data-ttu-id="c331e-128">We laten nu zien hoe dit gedrag wordt uitgedrukt in Q#.</span><span class="sxs-lookup"><span data-stu-id="c331e-128">Now, we're ready to demonstrate how Q# expresses this behavior.</span></span>  <span data-ttu-id="c331e-129">U begint met het eenvoudigst mogelijke programma en bouwt dit op om kwantumsuperpositie en kwantumverstrengeling te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="c331e-129">You start with the simplest program possible and build it up to demonstrate quantum superposition and quantum entanglement.</span></span>

## <a name="creating-a-q-project"></a><span data-ttu-id="c331e-130">Een Q #-project maken</span><span class="sxs-lookup"><span data-stu-id="c331e-130">Creating a Q# project</span></span>

<span data-ttu-id="c331e-131">Het eerste wat u moet doen, is het maken van een nieuw Q #-project.</span><span class="sxs-lookup"><span data-stu-id="c331e-131">The first thing we have to do is to create a new Q# project.</span></span> <span data-ttu-id="c331e-132">In deze zelf studie gaan we de omgeving gebruiken op basis van de [opdracht regel toepassingen met VS code](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="c331e-132">In this tutorial we are going to use the environment based on [command line applications with VS Code](xref:microsoft.quantum.install.standalone).</span></span>

<span data-ttu-id="c331e-133">In VS code kunt u een nieuw project maken:</span><span class="sxs-lookup"><span data-stu-id="c331e-133">To create a new project, in VS Code:</span></span> 

1. <span data-ttu-id="c331e-134">Klik **View**op  ->  **opdracht palet** weer geven en selecteer **Q #: nieuw project maken**.</span><span class="sxs-lookup"><span data-stu-id="c331e-134">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="c331e-135">Klik op **zelfstandige console toepassing**.</span><span class="sxs-lookup"><span data-stu-id="c331e-135">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="c331e-136">Ga naar de locatie waar u het project wilt opslaan en klik op **project maken**.</span><span class="sxs-lookup"><span data-stu-id="c331e-136">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="c331e-137">Wanneer het project is gemaakt, klikt u op **Nieuw project openen...** in de rechter benedenhoek.</span><span class="sxs-lookup"><span data-stu-id="c331e-137">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="c331e-138">In dit geval wordt het project genoemd `Bell` .</span><span class="sxs-lookup"><span data-stu-id="c331e-138">In this case we called the project `Bell`.</span></span> <span data-ttu-id="c331e-139">Hiermee worden twee bestanden gegenereerd: `Bell.csproj` , het project bestand en `Program.qs` een sjabloon van een Q #-toepassing die we gaan gebruiken om onze toepassing te schrijven.</span><span class="sxs-lookup"><span data-stu-id="c331e-139">This generates two files: `Bell.csproj`, the project file and `Program.qs`, a template of a Q# application that we will use to write our application.</span></span> <span data-ttu-id="c331e-140">De inhoud van `Program.qs` moet het volgende zijn:</span><span class="sxs-lookup"><span data-stu-id="c331e-140">The content of `Program.qs` should be:</span></span>

```qsharp
   namespace Bell {

      open Microsoft.Quantum.Canon;
      open Microsoft.Quantum.Intrinsic;
    

      @EntryPoint()
      operation HelloQ() : Unit {
          Message("Hello quantum world!");
      }
   }
```

## <a name="write-the-q-application"></a><span data-ttu-id="c331e-141">De Q- \# toepassing schrijven</span><span class="sxs-lookup"><span data-stu-id="c331e-141">Write the Q\# application</span></span>
 
<span data-ttu-id="c331e-142">We willen twee qubits voorbereiden in een specifieke kwantumtoestand om te laten zien hoe u met Q# bewerkingen kunt uitvoeren op qubits om hun toestand te wijzigen en om de effecten van superpositie en verstrengeling te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="c331e-142">Our goal is to prepare two qubits in a specific quantum state, demonstrating how to operate on qubits with Q# to change their state and demonstrate the effects of superposition and entanglement.</span></span> <span data-ttu-id="c331e-143">We bouwen dit stuk per stuk om qubite Staten, bewerkingen en metingen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="c331e-143">We will build this up piece by piece to introduce qubit states, operations, and measurement.</span></span>

### <a name="initialize-qubit-using-measurement"></a><span data-ttu-id="c331e-144">Qubit initialiseren met meting</span><span class="sxs-lookup"><span data-stu-id="c331e-144">Initialize qubit using measurement</span></span>

<span data-ttu-id="c331e-145">In het eerste codevoorbeeld hieronder laten we u zien hoe u met qubits kunt werken in Q#.</span><span class="sxs-lookup"><span data-stu-id="c331e-145">In the first code below, we show you how to work with qubits in Q#.</span></span>  <span data-ttu-id="c331e-146">We voeren twee bewerkingen uit [`M`](xref:microsoft.quantum.intrinsic.m) en zorgen [`X`](xref:microsoft.quantum.intrinsic.x) dat de status van een Qubit wordt getransformeerd.</span><span class="sxs-lookup"><span data-stu-id="c331e-146">We’ll introduce two operations, [`M`](xref:microsoft.quantum.intrinsic.m) and [`X`](xref:microsoft.quantum.intrinsic.x) that transform the state of a qubit.</span></span> <span data-ttu-id="c331e-147">In dit codefragment wordt een bewerking `SetQubitState` gedefinieerd die een qubit als parameter accepteert, evenals een andere parameter, `desired`, die de gewenste toestand van de qubit aangeeft.</span><span class="sxs-lookup"><span data-stu-id="c331e-147">In this code snippet, an operation `SetQubitState` is defined that takes as a parameter a qubit and another parameter, `desired`, representing the state that we would like the qubit to be in.</span></span>  <span data-ttu-id="c331e-148">Met de bewerking `SetQubitState` wordt een meting uitgevoerd op de qubit met behulp van de bewerking `M`.</span><span class="sxs-lookup"><span data-stu-id="c331e-148">The operation `SetQubitState` performs a measurement on the qubit using the operation `M`.</span></span>  <span data-ttu-id="c331e-149">In Q # retourneert een Qubit-meting altijd `Zero` of `One` .</span><span class="sxs-lookup"><span data-stu-id="c331e-149">In Q#, a qubit measurement always returns either `Zero` or `One`.</span></span>  <span data-ttu-id="c331e-150">Als de meting een waarde retourneert die niet gelijk is aan de gewenste waarde, `SetQubitState` ' spiegelt ' de Qubit; dat wil zeggen, wordt een bewerking uitgevoerd. `X` Hiermee wordt de Qubit-status gewijzigd in een nieuwe status waarin de waarschijnlijkheid van een meting `Zero` wordt geretourneerd en `One` omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="c331e-150">If the measurement returns a value not equal to the desired value, `SetQubitState` “flips” the qubit; that is, it executes an `X` operation, which changes the qubit state to a new state in which the probabilities of a measurement returning `Zero` and `One` are reversed.</span></span> <span data-ttu-id="c331e-151">Op deze manier `SetQubitState` plaatst de doel-Qubit altijd de gewenste status.</span><span class="sxs-lookup"><span data-stu-id="c331e-151">This way, `SetQubitState` always puts the target qubit in the desired state.</span></span>

<span data-ttu-id="c331e-152">Vervang de inhoud van `Program.qs` door de volgende code:</span><span class="sxs-lookup"><span data-stu-id="c331e-152">Replace the contents of `Program.qs` with the following code:</span></span>


```qsharp
   namespace Bell {
       open Microsoft.Quantum.Intrinsic;
       open Microsoft.Quantum.Canon;

       operation SetQubitState(desired : Result, q1 : Qubit) : Unit {
           if (desired != M(q1)) {
               X(q1);
           }
       }
   }
```

<span data-ttu-id="c331e-153">Deze bewerking kan nu worden aangeroepen om een qubit in te stellen op een klassieke toestand, met in 100% van de gevallen `Zero` of `One` als resultaat.</span><span class="sxs-lookup"><span data-stu-id="c331e-153">This operation may now be called to set a qubit to a classical state, either returning `Zero` 100% of the time or returning `One` 100% of the time.</span></span>
<span data-ttu-id="c331e-154">`Zero` en `One` zijn constanten die de enige twee mogelijke resultaten van een meting van een qubit vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="c331e-154">`Zero` and `One` are constants that represent the only two possible results of a measurement of a qubit.</span></span>

<span data-ttu-id="c331e-155">Met de bewerking `SetQubitState` wordt de qubit gemeten.</span><span class="sxs-lookup"><span data-stu-id="c331e-155">The operation `SetQubitState` measures the qubit.</span></span> <span data-ttu-id="c331e-156">Als de qubit zich in de gewenste toestand bevindt, wordt de toestand ongewijzigd gelaten door `SetQubitState`. Als dat niet zo is, wordt de toestand van de qubit gewijzigd in de gewenste toestand door het uitvoeren van de bewerking `X`.</span><span class="sxs-lookup"><span data-stu-id="c331e-156">If the qubit is in the state we want, `SetQubitState` leaves it alone; otherwise, by executing the `X` operation, we change the qubit state to the desired state.</span></span>

#### <a name="about-q-operations"></a><span data-ttu-id="c331e-157">Q#-bewerkingen</span><span class="sxs-lookup"><span data-stu-id="c331e-157">About Q# operations</span></span>

<span data-ttu-id="c331e-158">Een Q#-bewerking is een kwantumsubroutine,</span><span class="sxs-lookup"><span data-stu-id="c331e-158">A Q# operation is a quantum subroutine.</span></span> <span data-ttu-id="c331e-159">Dat wil zeggen dat het een aanroep bare routine is die aanroepen naar andere Quantum bewerkingen bevat.</span><span class="sxs-lookup"><span data-stu-id="c331e-159">That is, it is a callable routine that contains calls to other quantum operations.</span></span>

<span data-ttu-id="c331e-160">De argumenten voor een bewerking worden tussen haakjes opgegeven als een tupel.</span><span class="sxs-lookup"><span data-stu-id="c331e-160">The arguments to an operation are specified as a tuple, within parentheses.</span></span>

<span data-ttu-id="c331e-161">Het retourtype van de bewerking wordt na een dubbele punt opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c331e-161">The return type of the operation is specified after a colon.</span></span> <span data-ttu-id="c331e-162">In dit geval heeft de bewerking `SetQubitState` geen retourwaarde, zodat deze is gemarkeerd als retourzending `Unit`.</span><span class="sxs-lookup"><span data-stu-id="c331e-162">In this case, the `SetQubitState` operation has no return, so it is marked as returning `Unit`.</span></span> <span data-ttu-id="c331e-163">Dit is het Q#-equivalent van `unit` in F#, dat ongeveer analoog is met `void` in C#, en een lege tupel (`Tuple[()]`) in Python.</span><span class="sxs-lookup"><span data-stu-id="c331e-163">This is the Q# equivalent of `unit` in F#, which is roughly analogous to `void` in C#, and an empty tuple (`Tuple[()]`) in Python.</span></span>

<span data-ttu-id="c331e-164">U hebt twee kwantumbewerkingen gebruikt in uw eerste Q#-bewerking:</span><span class="sxs-lookup"><span data-stu-id="c331e-164">You have used two quantum operations in your first Q# operation:</span></span>

* <span data-ttu-id="c331e-165">De [`M`](xref:microsoft.quantum.intrinsic.m) bewerking, waarmee de status van de Qubit wordt gemeten</span><span class="sxs-lookup"><span data-stu-id="c331e-165">The [`M`](xref:microsoft.quantum.intrinsic.m) operation, which measures the state of the qubit</span></span>
* <span data-ttu-id="c331e-166">De [`X`](xref:microsoft.quantum.intrinsic.x) bewerking, die de status van een Qubit spiegelt</span><span class="sxs-lookup"><span data-stu-id="c331e-166">The [`X`](xref:microsoft.quantum.intrinsic.x) operation, which flips the state of a qubit</span></span>

<span data-ttu-id="c331e-167">Een kwantumbewerking transformeert de toestand van een qubit.</span><span class="sxs-lookup"><span data-stu-id="c331e-167">A quantum operation transforms the state of a qubit.</span></span> <span data-ttu-id="c331e-168">Soms worden kwantumbewerkingen ook wel kwantumpoorten genoemd, analoog aan klassieke logische poorten.</span><span class="sxs-lookup"><span data-stu-id="c331e-168">Sometime people talk about quantum gates instead of operations, in analogy to classical logic gates.</span></span> <span data-ttu-id="c331e-169">Dit vindt zijn oorsprong in het begintijdperk van de kwantumcomputing, toen algoritmen niets meer waren dan een theoretische constructie en werden gevisualiseerd als schema's, vergelijkbaar met circuitschema's in klassieke computing.</span><span class="sxs-lookup"><span data-stu-id="c331e-169">This is rooted in the early days of quantum computing when algorithms were merely a theoretical construct and visualized as diagrams similarly to circuit diagrams in classical computing.</span></span>

### <a name="counting-measurement-outcomes"></a><span data-ttu-id="c331e-170">Resultaten van de meting tellen</span><span class="sxs-lookup"><span data-stu-id="c331e-170">Counting measurement outcomes</span></span>

<span data-ttu-id="c331e-171">Om het effect van de bewerking `SetQubitState` te demonstreren, wordt er vervolgens een bewerking `TestBellState` toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="c331e-171">To demonstrate the effect of the `SetQubitState` operation, a `TestBellState` operation is then added.</span></span> <span data-ttu-id="c331e-172">Deze bewerking krijgt als invoer een `Zero` of `One` en roept de bewerking `SetQubitState` een aantal keer aan met die invoer, en telt het aantal keren dat `Zero` het resultaat is van de meting van de qubit en het aantal keren dat `One` wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c331e-172">This operation takes as input a `Zero` or `One`, and calls the `SetQubitState` operation some number of times with that input, and counts the number of times that `Zero` was returned from the measurement of the qubit and the number of times that `One` was returned.</span></span> <span data-ttu-id="c331e-173">In deze eerste simulatie van de bewerking `TestBellState` verwachten we natuurlijk dat de uitvoer laat zien dat alle metingen van de qubit die is ingesteld met de parameterinvoer `Zero`, `Zero` oplevert en dat alle metingen van de qubit die is ingesteld met `One` als de parameterinvoer, `One` retourneert.</span><span class="sxs-lookup"><span data-stu-id="c331e-173">Of course, in this first simulation of the `TestBellState` operation, we expect that the output will show that all measurements of the qubit set with `Zero` as the parameter input will return `Zero`, and all measurements of a qubit set with `One` as the parameter input will return `One`.</span></span> <span data-ttu-id="c331e-174">Daarnaast voegen we code toe aan `TestBellState` om superpositie en entanglement te demonstreren.</span><span class="sxs-lookup"><span data-stu-id="c331e-174">Further on, we’ll add code to `TestBellState` to demonstrate superposition and entanglement.</span></span>

<span data-ttu-id="c331e-175">Voeg na het einde van bewerking `SetQubitState` de volgende bewerking toe aan `Bell.qs` bestand binnen de naamruimte:</span><span class="sxs-lookup"><span data-stu-id="c331e-175">Add the following operation to the `Bell.qs` file, inside the namespace, after the end of the `SetQubitState` operation:</span></span>

```qsharp
   operation TestBellState(count : Int, initial : Result) : (Int, Int) {

       mutable numOnes = 0;
       using (qubit = Qubit()) {

           for (test in 1..count) {
               SetQubitState(initial, qubit);
               let res = M(qubit);

               // Count the number of ones we saw:
               if (res == One) {
                   set numOnes += 1;
               }
           }
            
           SetQubitState(Zero, qubit);
       }

       // Return number of times we saw a |0> and number of times we saw a |1>
       Message("Test results (# of 0s, # of 1s): ");
       return (count - numOnes, numOnes);
   }
```
<span data-ttu-id="c331e-176">Houd er rekening mee dat er een regel is toegevoegd voor het `return` afdrukken van een verklarend bericht in de-console met de functie ( `Message` ) [micro soft. Quantum. intrinsiek. Message]</span><span class="sxs-lookup"><span data-stu-id="c331e-176">Note that we added a line before the `return` to print an explanatory message in the console with the function (`Message`)[microsoft.quantum.intrinsic.message]</span></span>

<span data-ttu-id="c331e-177">Deze bewerking (`TestBellState`) wordt gedurende `count` iteraties als een lus uitgevoerd, er wordt een opgegeven `initial`-waarde voor een qubit gedefinieerd en vervolgens wordt het resultaat, (`M`), gemeten.</span><span class="sxs-lookup"><span data-stu-id="c331e-177">This operation (`TestBellState`) will loop for `count` iterations, set a specified `initial` value on a qubit and then measure (`M`) the result.</span></span> <span data-ttu-id="c331e-178">Er worden statistieken verzameld over het aantal nullen en enen dat we hebben gemeten, waarna ze naar de aanroepende functie worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="c331e-178">It will gather statistics on how many zeros and ones we've measured and return them to the caller.</span></span> <span data-ttu-id="c331e-179">Er wordt nog een andere noodzakelijke bewerking uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c331e-179">It performs one other necessary operation.</span></span> <span data-ttu-id="c331e-180">De qubit wordt opnieuw ingesteld op een bekende toestand (`Zero`) voordat deze wordt geretourneerd, zodat anderen deze qubit een bekende toestand kunnen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="c331e-180">It resets the qubit to a known state (`Zero`) before returning it allowing others to allocate this qubit in a known state.</span></span> <span data-ttu-id="c331e-181">Dit wordt door de instructie `using` vereist.</span><span class="sxs-lookup"><span data-stu-id="c331e-181">This is required by the `using` statement.</span></span>

#### <a name="about-variables-in-q"></a><span data-ttu-id="c331e-182">Over variabelen in Q\#</span><span class="sxs-lookup"><span data-stu-id="c331e-182">About variables in Q\#</span></span>

<span data-ttu-id="c331e-183">Standaard zijn variabelen in Q# niet meer te veranderen. De waarde kan niet worden gewijzigd als de variabele gebonden is.</span><span class="sxs-lookup"><span data-stu-id="c331e-183">By default, variables in Q# are immutable; their value may not be changed after they are bound.</span></span> <span data-ttu-id="c331e-184">Het sleutelwoord `let` wordt gebruikt om de binding van een onveranderlijke variabele aan te geven.</span><span class="sxs-lookup"><span data-stu-id="c331e-184">The `let` keyword is used to indicate the binding of an immutable variable.</span></span> <span data-ttu-id="c331e-185">Bewerkingsargumenten zijn altijd onveranderbaar.</span><span class="sxs-lookup"><span data-stu-id="c331e-185">Operation arguments are always immutable.</span></span>

<span data-ttu-id="c331e-186">Als u een variabele nodig hebt waarvan de waarde kan worden gewijzigd, zoals `numOnes` in het voorbeeld, kunt u de variabele declareren met het sleutelwoord `mutable`.</span><span class="sxs-lookup"><span data-stu-id="c331e-186">If you need a variable whose value can change, such as `numOnes` in the example, you can declare the variable with the `mutable` keyword.</span></span> <span data-ttu-id="c331e-187">De waarde van een veranderlijke variabele kan worden gewijzigd met behulp van een `setQubitState`-instructie.</span><span class="sxs-lookup"><span data-stu-id="c331e-187">A mutable variable's value may be changed using a `setQubitState` statement.</span></span>

<span data-ttu-id="c331e-188">In beide gevallen wordt het type variabele door de compiler afgeleid.</span><span class="sxs-lookup"><span data-stu-id="c331e-188">In both cases, the type of a variable is inferred by the compiler.</span></span> <span data-ttu-id="c331e-189">Voor Q# zijn geen typeannotaties vereist voor variabelen.</span><span class="sxs-lookup"><span data-stu-id="c331e-189">Q# doesn't require any type annotations for variables.</span></span>

#### <a name="about-using-statements-in-q"></a><span data-ttu-id="c331e-190">`using`Instructies in Q\#</span><span class="sxs-lookup"><span data-stu-id="c331e-190">About `using` statements in Q\#</span></span>

<span data-ttu-id="c331e-191">De instructie `using` is ook speciaal in Q#.</span><span class="sxs-lookup"><span data-stu-id="c331e-191">The `using` statement is also special to Q#.</span></span> <span data-ttu-id="c331e-192">Deze wordt gebruikt om qubits toe te wijzen voor gebruik in een codeblok.</span><span class="sxs-lookup"><span data-stu-id="c331e-192">It is used to allocate qubits for use in a block of code.</span></span> <span data-ttu-id="c331e-193">In Q# worden alle qubits dynamisch toegewezen en vrijgegeven. Het zijn geen vaste resources die de gehele levensduur van een complex algoritme meegaan.</span><span class="sxs-lookup"><span data-stu-id="c331e-193">In Q#, all qubits are dynamically allocated and released, rather than being fixed resources that are there for the entire lifetime of a complex algorithm.</span></span> <span data-ttu-id="c331e-194">Een `using`-instructie wijst aan het begin een set qubits toe en geeft deze qubits aan het einde van het blok vrij.</span><span class="sxs-lookup"><span data-stu-id="c331e-194">A `using` statement allocates a set of qubits at the start, and releases those qubits at the end of the block.</span></span>

## <a name="execute-the-code-from-the-command-line"></a><span data-ttu-id="c331e-195">De code uitvoeren vanaf de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="c331e-195">Execute the code from the command line</span></span>

<span data-ttu-id="c331e-196">Als u de code wilt uitvoeren, moet u de compiler opgeven *die* kan worden uitgevoerd wanneer de opdracht wordt opgegeven `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="c331e-196">In order to run the code we need to specify the compiler *which* callable to run when we provide the `dotnet run` command.</span></span> <span data-ttu-id="c331e-197">Dit wordt gedaan met een eenvoudige wijziging in het Q #-bestand door een regel toe te voegen die `@EntryPoint()` direct voor de aanroep zou worden opgeroepen: de `TestBellState` bewerking in dit geval.</span><span class="sxs-lookup"><span data-stu-id="c331e-197">This is done with a simple change in the Q# file by adding a line with `@EntryPoint()` directly preceding the callable: the `TestBellState` operation in this case.</span></span> <span data-ttu-id="c331e-198">De volledige code moet zijn:</span><span class="sxs-lookup"><span data-stu-id="c331e-198">The full code should be:</span></span>

```qsharp
namespace Bell {
    open Microsoft.Quantum.Canon;
    open Microsoft.Quantum.Intrinsic;

    operation SetQubitState(desired : Result, target : Qubit) : Unit {
        if (desired != M(target)) {
            X(target);
        }
    }

    @EntryPoint()
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using (qubit = Qubit()) {

            for (test in 1..count) {
                SetQubitState(initial, qubit);
                let res = M(qubit);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, qubit);
        }

    // Return number of times we saw a |0> and number of times we saw a |1>
    Message("Test results (# of 0s, # of 1s): ");
    return (count - numOnes, numOnes);
    }
}
```

<span data-ttu-id="c331e-199">Als u het programma wilt uitvoeren, moet u argumenten opgeven voor `count` `initial` de opdracht regel.</span><span class="sxs-lookup"><span data-stu-id="c331e-199">To run the program we need to specify `count` and `initial` arguments from the command line.</span></span> <span data-ttu-id="c331e-200">Laten we de voor beelden `count = 1000` kiezen `initial = One` .</span><span class="sxs-lookup"><span data-stu-id="c331e-200">Let's choose for example `count = 1000` and `initial = One`.</span></span> <span data-ttu-id="c331e-201">Voer de volgende opdracht in:</span><span class="sxs-lookup"><span data-stu-id="c331e-201">Enter the following command:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

<span data-ttu-id="c331e-202">En u moet rekening houden met de volgende uitvoer:</span><span class="sxs-lookup"><span data-stu-id="c331e-202">And you should observe the following output:</span></span>

```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="c331e-203">Als u probeert met `initial = Zero` het volgende te weten:</span><span class="sxs-lookup"><span data-stu-id="c331e-203">If you try with `initial = Zero` you should observe:</span></span>

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

## <a name="prepare-superposition"></a><span data-ttu-id="c331e-204">Superpositie voorbereiden</span><span class="sxs-lookup"><span data-stu-id="c331e-204">Prepare superposition</span></span>

<span data-ttu-id="c331e-205">Laten we nu eens kijken hoe Q # de manieren krijgt om qubits te plaatsen in de superpositie.</span><span class="sxs-lookup"><span data-stu-id="c331e-205">Now let’s look at how Q# expresses ways to put qubits in superposition.</span></span>  <span data-ttu-id="c331e-206">Zoals eerder gezegd, kan de toestand van een qubit een superpositie zijn van 0 en 1.</span><span class="sxs-lookup"><span data-stu-id="c331e-206">Recall that the state of a qubit can be in a superposition of 0 and 1.</span></span>  <span data-ttu-id="c331e-207">We gaan de bewerking `Hadamard` gebruiken om dit te bereiken.</span><span class="sxs-lookup"><span data-stu-id="c331e-207">We’ll use the `Hadamard` operation to accomplish this.</span></span> <span data-ttu-id="c331e-208">Als de qubit zich in een van de klassieke toestanden bevindt (waarbij een meting altijd `Zero` of altijd `One` retourneert) wordt de qubit met de bewerking `Hadamard` of `H` in een toestand geplaatst waarin een meting van de qubit in 50% van de gevallen `Zero` retourneert en in 50% van de gevallen `One`.</span><span class="sxs-lookup"><span data-stu-id="c331e-208">If the qubit is in either of the classical states (where a measurement returns `Zero` always or `One` always), then the `Hadamard` or `H` operation will put the qubit in a state where a measurement of the qubit will return `Zero` 50% of the time and return `One` 50% of the time.</span></span>  <span data-ttu-id="c331e-209">Conceptueel gezien, kan de qubit worden beschouwd als halverwege tussen de `Zero` en `One`.</span><span class="sxs-lookup"><span data-stu-id="c331e-209">Conceputually, the qubit can be thought of as halfway between the `Zero` and `One`.</span></span>  <span data-ttu-id="c331e-210">Als we nu de bewerking `TestBellState` simuleren, zien we dat de resultaten na meting ongeveer een gelijk aantal keren `Zero` en `One` bevatten.</span><span class="sxs-lookup"><span data-stu-id="c331e-210">Now, when we simulate the `TestBellState` operation, we will see the results will return roughly an equal number of `Zero` and `One` after measurement.</span></span>  

### <a name="x-flips-qubit-state"></a><span data-ttu-id="c331e-211">`X`Hiermee wordt de status van Qubit gespiegeld</span><span class="sxs-lookup"><span data-stu-id="c331e-211">`X` flips qubit state</span></span>

<span data-ttu-id="c331e-212">Eerst proberen we de qubit te spiegelen (als de qubit zich in de toestand `Zero` bevindt, wordt deze gespiegeld naar `One` en omgekeerd).</span><span class="sxs-lookup"><span data-stu-id="c331e-212">First we'll just try to flip the qubit (if the qubit is in `Zero` state will flip to `One` and vice versa).</span></span> <span data-ttu-id="c331e-213">Dit wordt bereikt door een bewerking `X` uit te voeren voordat we de qubit meten in `TestBellState`:</span><span class="sxs-lookup"><span data-stu-id="c331e-213">This is accomplished by performing an `X` operation before we measure it in `TestBellState`:</span></span>

```qsharp
X(qubit);
let res = M(qubit);
```

<span data-ttu-id="c331e-214">De resultaten worden nu omgekeerd:</span><span class="sxs-lookup"><span data-stu-id="c331e-214">Now the results are reversed:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(1000, 0)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s):
(0, 1000)
```

<span data-ttu-id="c331e-215">Laten we nu de Quantum eigenschappen van de qubits verkennen.</span><span class="sxs-lookup"><span data-stu-id="c331e-215">Now let's explore the quantum properties of the qubits.</span></span>

### <a name="h-prepares-superposition"></a><span data-ttu-id="c331e-216">`H`voor bereiding van superpositie</span><span class="sxs-lookup"><span data-stu-id="c331e-216">`H` prepares superposition</span></span>

<span data-ttu-id="c331e-217">We hoeven alleen maar de bewerking `X` uit het vorige voorbeeld te vervangen door een bewerking `H` of Hadamard.</span><span class="sxs-lookup"><span data-stu-id="c331e-217">All we need to do is replace the `X` operation in the previous run with an `H` or Hadamard operation.</span></span> <span data-ttu-id="c331e-218">In plaats van de qubit te spiegelen van 0 naar 1, wordt deze slechts half gespiegeld.</span><span class="sxs-lookup"><span data-stu-id="c331e-218">Instead of flipping the qubit all the way from 0 to 1, we will only flip it halfway.</span></span> <span data-ttu-id="c331e-219">De vervangen regels in `TestBellState` zien er nu als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="c331e-219">The replaced lines in `TestBellState` now look like:</span></span>

```qsharp
H(qubit);
let res = M(qubit);
```

<span data-ttu-id="c331e-220">De resultaten worden nu interessanter:</span><span class="sxs-lookup"><span data-stu-id="c331e-220">Now the results get more interesting:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```

```output
Test results (# of 0s, # of 1s):
(496, 504)
```

```dotnetcli
dotnet run --count 1000 --initial Zero
```

```output
Test results (# of 0s, # of 1s):
(506, 494)
```

<span data-ttu-id="c331e-221">Telkens als we meten, vragen we om een klassieke waarde, maar de qubit bevindt zich halverwege tussen 0 en 1, zodat we de helft van de tijd (statistisch) 0 en de helft van de tijd 1 krijgen.</span><span class="sxs-lookup"><span data-stu-id="c331e-221">Every time we measure, we ask for a classical value, but the qubit is halfway between 0 and 1, so we get (statistically) 0 half the time and 1 half the time.</span></span>
<span data-ttu-id="c331e-222">Dit staat bekend als **superpositie** en geeft ons de eerste echte blik op een kwantumtoestand.</span><span class="sxs-lookup"><span data-stu-id="c331e-222">This is known as **superposition** and gives us our first real view into a quantum state.</span></span>

## <a name="prepare-entanglement"></a><span data-ttu-id="c331e-223">Verstrengeling voorbereiden</span><span class="sxs-lookup"><span data-stu-id="c331e-223">Prepare entanglement</span></span>

<span data-ttu-id="c331e-224">Laten we nu eens kijken welke manieren beschikbaar zijn in Q# om verstrengeling van qubits uit te drukken.</span><span class="sxs-lookup"><span data-stu-id="c331e-224">Now let’s look at how Q# expresses ways to entangle qubits.</span></span>
<span data-ttu-id="c331e-225">Eerst stellen we de eerste qubit in op de begintoestand en gebruiken we vervolgens de bewerking `H` om deze in superpositie te brengen.</span><span class="sxs-lookup"><span data-stu-id="c331e-225">First, we set the first qubit to the initial state and then use the `H` operation to put it into superposition.</span></span>  <span data-ttu-id="c331e-226">Voordat we de eerste Qubit meten, gebruiken we vervolgens een nieuwe bewerking ( `CNOT` ), die staat voor beheerd.</span><span class="sxs-lookup"><span data-stu-id="c331e-226">Then, before we measure the first qubit, we use a new operation (`CNOT`), which stands for Controlled-NOT.</span></span>  <span data-ttu-id="c331e-227">Het resultaat van het uitvoeren van deze bewerking op twee qubits is het spiegelen van de tweede qubit als de eerste qubit `One` is.</span><span class="sxs-lookup"><span data-stu-id="c331e-227">The result of executing this operation on two qubits is to flip the second qubit if the first qubit is `One`.</span></span>  <span data-ttu-id="c331e-228">Nu zijn de twee qubits verstrengeld.</span><span class="sxs-lookup"><span data-stu-id="c331e-228">Now, the two qubits are entangled.</span></span>  <span data-ttu-id="c331e-229">Onze statistieken voor de eerste qubit zijn niet gewijzigd (kans van 50% op een `Zero` of `One` na meting), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ de uitkomst die voor de eerste qubit is gemeten.</span><span class="sxs-lookup"><span data-stu-id="c331e-229">Our statistics for the first qubit haven't changed (50-50 chance of a `Zero` or a `One` after measurement), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit.</span></span> <span data-ttu-id="c331e-230">Onze `CNOT`-poort heeft de twee qubits verstrengeld, zodat wat er met de ene gebeurt, ook met de andere gebeurt.</span><span class="sxs-lookup"><span data-stu-id="c331e-230">Our `CNOT` has entangled the two qubits, so that whatever happens to one of them, happens to the other.</span></span> <span data-ttu-id="c331e-231">Als u de metingen omkeert (de tweede qubit vóór de eerste), zou zich hetzelfde voordoen.</span><span class="sxs-lookup"><span data-stu-id="c331e-231">If you reversed the measurements (did the second qubit before the first), the same thing would happen.</span></span> <span data-ttu-id="c331e-232">De eerste meting zal willekeurig zijn, waarna de tweede zich houdt aan wat voor de eerste is gedetecteerd.</span><span class="sxs-lookup"><span data-stu-id="c331e-232">The first measurement would be random and the second would be in lock step with whatever was discovered for the first.</span></span>

<span data-ttu-id="c331e-233">Het eerste wat u moet doen, is twee qubits toewijzen in plaats van één in `TestBellState` :</span><span class="sxs-lookup"><span data-stu-id="c331e-233">The first thing we'll need to do is allocate two qubits instead of one in `TestBellState`:</span></span>

```qsharp
using ((q0, q1) = (Qubit(), Qubit())) {
```

<span data-ttu-id="c331e-234">Zo kunnen we een nieuwe bewerking (`CNOT`) toevoegen voordat we een meting (`M`) in `TestBellState` uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="c331e-234">This will allow us to add a new operation (`CNOT`) before we measure  (`M`) in `TestBellState`:</span></span>

```qsharp
SetQubitState(initial, q0);
SetQubitState(Zero, q1);

H(q0);
CNOT(q0, q1);
let res = M(q0);
```

<span data-ttu-id="c331e-235">We hebben nog een andere `SetQubitState`-bewerking toegevoegd om de eerste qubit te initialiseren, zodat we zeker weten dat deze altijd in toestand `Zero` is wanneer we starten.</span><span class="sxs-lookup"><span data-stu-id="c331e-235">We've added another `SetQubitState` operation to initialize the first qubit to make sure that it's always in the `Zero` state when we start.</span></span>

<span data-ttu-id="c331e-236">We moeten ook de tweede qubit opnieuw instellen voordat deze wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="c331e-236">We also need to reset the second qubit before releasing it.</span></span>

```qsharp
SetQubitState(Zero, q0);
SetQubitState(Zero, q1);
```

<span data-ttu-id="c331e-237">De volledige routine ziet er nu als volgt uit:</span><span class="sxs-lookup"><span data-stu-id="c331e-237">The full routine now looks like this:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int) {

        mutable numOnes = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

                H(q0);
                CNOT(q0,q1);
                let res = M(q0);

                // Count the number of ones we saw:
                if (res == One) {
                    set numOnes += 1;
                }
            }

            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return number of times we saw a |0> and number of times we saw a |1>
        return (count-numOnes, numOnes);
    }
```

<span data-ttu-id="c331e-238">Als we deze uitvoeren, krijgen we precies hetzelfde 50-50-resultaat dat we eerder hadden.</span><span class="sxs-lookup"><span data-stu-id="c331e-238">If we run this, we'll get exactly the same 50-50 result we got before.</span></span> <span data-ttu-id="c331e-239">Het is echter belangrijk om te weten hoe de tweede qubit reageert op het meten van de eerste.</span><span class="sxs-lookup"><span data-stu-id="c331e-239">However, what we're interested in is how the second qubit reacts to the first being measured.</span></span> <span data-ttu-id="c331e-240">We voegen deze statistiek toe met een nieuwe versie van de `TestBellState`-bewerking:</span><span class="sxs-lookup"><span data-stu-id="c331e-240">We'll add this statistic with a new version of the `TestBellState` operation:</span></span>

```qsharp
    operation TestBellState(count : Int, initial : Result) : (Int, Int, Int) {
        mutable numOnes = 0;
        mutable agree = 0;
        using ((q0, q1) = (Qubit(), Qubit())) {
            for (test in 1..count) {
                SetQubitState(initial, q0);
                SetQubitState(Zero, q1);

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
            
            SetQubitState(Zero, q0);
            SetQubitState(Zero, q1);
        }

        // Return times we saw |0>, times we saw |1>, and times measurements agreed
        Message("Test results (# of 0s, # of 1s, # of agreements)");
        return (count-numOnes, numOnes, agree);
    }
```

<span data-ttu-id="c331e-241">In de nieuwe retourwaarde (`agree`) wordt telkens bijgehouden als de meting van de eerste qubit overeenkomt met de meting van de tweede qubit.</span><span class="sxs-lookup"><span data-stu-id="c331e-241">The new return value (`agree`) keeps track of every time the measurement from the first qubit matches the measurement of the second qubit.</span></span>

<span data-ttu-id="c331e-242">Het uitvoeren van de code die wij verkrijgen:</span><span class="sxs-lookup"><span data-stu-id="c331e-242">Running the code we obtain:</span></span>

```dotnetcli
dotnet run --count 1000 --initial One
```
```output
(505, 495, 1000)
```
```dotnetcli
dotnet run --count 1000 --initial Zero
```
```output
Test results (# of 0s, # of 1s, # of agreements)
(507, 493, 1000)
```

<span data-ttu-id="c331e-243">Zoals aangegeven in het overzicht, zijn onze statistieken voor de eerste qubit niet gewijzigd (kans van 50% op 0 of 1), maar wanneer we nu de tweede qubit meten, krijgen we __altijd__ dezelfde uitkomst als voor de eerste qubit, omdat ze namelijk verstrengeld zijn.</span><span class="sxs-lookup"><span data-stu-id="c331e-243">As stated in the overview, our statistics for the first qubit haven't changed (50-50 chance of a 0 or a 1), but now when we measure the second qubit, it is __always__ the same as what we measured for the first qubit, because they are entangled!</span></span>

## <a name="next-steps"></a><span data-ttu-id="c331e-244">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="c331e-244">Next steps</span></span>

<span data-ttu-id="c331e-245">De zelfstudie [Zoekalgoritme van Grover](xref:microsoft.quantum.quickstarts.search) laat zien hoe u een zoekalgoritme van Grover kunt bouwen en uitvoeren, een van de populairste algoritmen uit de kwantumcomputing en een goed voorbeeld van een Q#-programma dat kan worden gebruikt voor het oplossen van echte problemen met kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="c331e-245">The tutorial [Grover’s search](xref:microsoft.quantum.quickstarts.search) shows you how to build and run Grover search, one of the most popular quantum computing algorithms and offers a nice example of a Q# program that can be used to solve real problems with quantum computing.</span></span>  

<span data-ttu-id="c331e-246">In [Aan de slag met de Quantum Development Kit](xref:microsoft.quantum.welcome) vindt u meer manieren om te leren werken met Q# en kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="c331e-246">[Get Started with the Quantum Development Kit](xref:microsoft.quantum.welcome) recommends more ways to learn Q# and quantum programming.</span></span>