---
title: Een kwantumgenerator voor willekeurige getallen maken
description: U gaat een Q#-project bouwen waarin fundamentele kwantumconcepten, zoals superpositie, worden gedemonstreerd door een kwantumgenerator voor willekeurige getallen te maken.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: 18e8975e513a87c0a67a6dbb5586cc7dab5a93fb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274482"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="910cb-103">Zelfstudie: Een kwantumgenerator voor willekeurige getallen implementeren in Q\#</span><span class="sxs-lookup"><span data-stu-id="910cb-103">Tutorial: Implement a Quantum Random Number Generator in Q\#</span></span>

<span data-ttu-id="910cb-104">Een eenvoudig voorbeeld van een kwantumalgoritme dat is geschreven in Q# is een kwantumgenerator voor willekeurige getallen.</span><span class="sxs-lookup"><span data-stu-id="910cb-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="910cb-105">Dit algoritme maakt gebruik van de aard van kwantummechanismen om een willekeurig getal te produceren.</span><span class="sxs-lookup"><span data-stu-id="910cb-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="910cb-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="910cb-106">Prerequisites</span></span>

- <span data-ttu-id="910cb-107">De Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="910cb-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="910cb-108">Maak een Q#-project om [Q# vanaf de opdrachtregel te gebruiken](xref:microsoft.quantum.install.standalone), of met een [Python-hostprogramma](xref:microsoft.quantum.install.python) of [C#-hostprogramma](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="910cb-108">Create a Q# project for either [using Q# from the command line](xref:microsoft.quantum.install.standalone), or with a [Python host program](xref:microsoft.quantum.install.python) or [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="write-a-q-operation"></a><span data-ttu-id="910cb-109">Een Q#-bewerking schrijven</span><span class="sxs-lookup"><span data-stu-id="910cb-109">Write a Q# operation</span></span>

### <a name="q-operation-code"></a><span data-ttu-id="910cb-110">Q#-bewerkingscode</span><span class="sxs-lookup"><span data-stu-id="910cb-110">Q# operation code</span></span>

1. <span data-ttu-id="910cb-111">Vervang de inhoud van het bestand Program.qs door de volgende code:</span><span class="sxs-lookup"><span data-stu-id="910cb-111">Replace the contents of the Program.qs file with the following code:</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

<span data-ttu-id="910cb-112">Zoals vermeld in het artikel [Inzicht in kwantumcomputing](xref:microsoft.quantum.overview.understanding) is een qubit een eenheid van kwantuminformatie die in superpositie kan zijn.</span><span class="sxs-lookup"><span data-stu-id="910cb-112">As mentioned in our [Understanding quantum computing](xref:microsoft.quantum.overview.understanding) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="910cb-113">Bij meting kan een qubit alleen 0 of 1 zijn.</span><span class="sxs-lookup"><span data-stu-id="910cb-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="910cb-114">Tijdens de uitvoering vertegenwoordigt de toestand van de qubit echter de kans dat een meting een 0 of een 1 oplevert.</span><span class="sxs-lookup"><span data-stu-id="910cb-114">However, during execution the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="910cb-115">Deze waarschijnlijkheidstoestand staat bekend als superpositie.</span><span class="sxs-lookup"><span data-stu-id="910cb-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="910cb-116">We kunnen deze waarschijnlijkheid gebruiken voor het genereren van willekeurige getallen.</span><span class="sxs-lookup"><span data-stu-id="910cb-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="910cb-117">In onze Q#-bewerking introduceren we het gegevenstype `Qubit`, dat alleen wordt ondersteund in Q#.</span><span class="sxs-lookup"><span data-stu-id="910cb-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="910cb-118">We kunnen een `Qubit` alleen toewijzen met een `using`-instructie.</span><span class="sxs-lookup"><span data-stu-id="910cb-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="910cb-119">Wanneer een qubit wordt toegewezen, bevindt deze zich altijd in de toestand `Zero`.</span><span class="sxs-lookup"><span data-stu-id="910cb-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="910cb-120">Met behulp van de bewerking `H` kunnen we onze `Qubit` in superpositie plaatsen.</span><span class="sxs-lookup"><span data-stu-id="910cb-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="910cb-121">Als u een qubit wilt meten en de waarde ervan wilt lezen, gebruikt u de intrinsieke bewerking `M`.</span><span class="sxs-lookup"><span data-stu-id="910cb-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="910cb-122">Door onze `Qubit` in superpositie te plaatsen en vervolgens te meten, levert elke aanroep van de code een andere waarde op.</span><span class="sxs-lookup"><span data-stu-id="910cb-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span>

<span data-ttu-id="910cb-123">Wanneer de toewijzing van een `Qubit` ongedaan wordt gemaakt, moet deze expliciet weer worden ingesteld op de toestand `Zero`, anders rapporteert de simulator een runtime-fout.</span><span class="sxs-lookup"><span data-stu-id="910cb-123">When a `Qubit` is deallocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="910cb-124">Dit kan heel eenvoudig door `Reset` aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="910cb-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="910cb-125">De code visualiseren met de Blochbol</span><span class="sxs-lookup"><span data-stu-id="910cb-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="910cb-126">In de Blochbol vertegenwoordigt de noordpool de klassieke waarde **0** en de zuidpool de klassieke waarde **1**.</span><span class="sxs-lookup"><span data-stu-id="910cb-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="910cb-127">Elke superpositie kan worden weergegeven met een punt op de bol (aangeduid met een pijl).</span><span class="sxs-lookup"><span data-stu-id="910cb-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="910cb-128">Hoe dichter het einde van de pijl bij een pool is, hoe groter de kans is dat de qubit bij meting uiteenvalt in de klassieke waarde die aan die pool is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="910cb-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="910cb-129">De toestand van de qubit die wordt weergegeven door de rode pijl hieronder heeft bijvoorbeeld een hogere kans om de waarde **0** te retourneren als deze wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="910cb-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

<span data-ttu-id="910cb-130">We kunnen deze voorstelling gebruiken om te visualiseren wat de code doet:</span><span class="sxs-lookup"><span data-stu-id="910cb-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="910cb-131">We beginnen met een qubit die is geïnitialiseerd in de toestand **0** en passen `H` toe om een superpositie te maken waarin de waarschijnlijkheid van **0** en **1** hetzelfde is.</span><span class="sxs-lookup"><span data-stu-id="910cb-131">First we start with a qubit initialized in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* <span data-ttu-id="910cb-132">Vervolgens meten we de qubit en slaan we de uitvoer op:</span><span class="sxs-lookup"><span data-stu-id="910cb-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

<span data-ttu-id="910cb-133">Aangezien het resultaat van de meting volledig willekeurig is, hebben we een willekeurige bit verkregen.</span><span class="sxs-lookup"><span data-stu-id="910cb-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="910cb-134">We kunnen deze bewerking meerdere keren aanroepen om gehele getallen te maken.</span><span class="sxs-lookup"><span data-stu-id="910cb-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="910cb-135">Als we de bewerking bijvoorbeeld drie keer aanroepen om drie willekeurige bits te verkrijgen, kunnen we willekeurige 3-bits getallen maken (dat wil zeggen, een willekeurig getal tussen 0 en 7).</span><span class="sxs-lookup"><span data-stu-id="910cb-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>


## <a name="creating-a-complete-random-number-generator"></a><span data-ttu-id="910cb-136">Een volledige generator van willekeurige getallen maken</span><span class="sxs-lookup"><span data-stu-id="910cb-136">Creating a complete random number generator</span></span>

<span data-ttu-id="910cb-137">Nu we een Q#-bewerking hebben die willekeurige bits genereert, kunnen we die gebruiken om een volledige generator van willekeurige getallen te bouwen.</span><span class="sxs-lookup"><span data-stu-id="910cb-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator.</span></span> <span data-ttu-id="910cb-138">We kunnen de Q#-opdrachtregeltoepassingen of een hostprogramma gebruiken.</span><span class="sxs-lookup"><span data-stu-id="910cb-138">We can use the Q# command line applications or use a host program.</span></span>



### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[<span data-ttu-id="910cb-139">Q#-opdrachtregeltoepassingen met Visual Studio of Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="910cb-139">Q# command line applications with Visual Studio or Visual Studio Code</span></span>](#tab/tabid-qsharp)

<span data-ttu-id="910cb-140">Als u de volledige Q#-opdrachtregeltoepassing wilt gebruiken, voegt u het volgende invoerpunt toe aan uw Q#-programma:</span><span class="sxs-lookup"><span data-stu-id="910cb-140">To create the full Q# command line application, add the following entry point to your Q# program:</span></span> 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

<span data-ttu-id="910cb-141">Het uitvoerbare bestand voert de bewerking of functie met het kenmerk `@EntryPoint()` uit in een simulator of resourceschatter, afhankelijk van de projectconfiguratie en opdrachtregelopties.</span><span class="sxs-lookup"><span data-stu-id="910cb-141">The executable will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

<span data-ttu-id="910cb-142">Druk in Visual Studio op Ctrl + F5 om het script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="910cb-142">In Visual Studio, simply press Ctrl + F5 to execute the script.</span></span>

<span data-ttu-id="910cb-143">Bouw in VS Code Program.qs voor de eerste keer door het onderstaande in de terminal in te voeren:</span><span class="sxs-lookup"><span data-stu-id="910cb-143">In VS Code, build the Program.qs the first time by typing the below in the terminal:</span></span>

```dotnetcli
dotnet build
```

<span data-ttu-id="910cb-144">Voor nieuwe uitvoeringen is het niet nodig om de build opnieuw te doen.</span><span class="sxs-lookup"><span data-stu-id="910cb-144">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="910cb-145">Typ de volgende opdracht en druk op enter om hem uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="910cb-145">To run it, type the following command and press enter:</span></span>

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-line"></a>[<span data-ttu-id="910cb-146">Python met Visual Studio Code of de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="910cb-146">Python with Visual Studio Code or the Command Line</span></span>](#tab/tabid-python)

<span data-ttu-id="910cb-147">Als u uw nieuwe Q#-programma wilt uitvoeren vanuit Python, slaat u de volgende code op als `host.py`:</span><span class="sxs-lookup"><span data-stu-id="910cb-147">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

<span data-ttu-id="910cb-148">U kunt vervolgens uw Python-hostprogramma uitvoeren vanaf de opdrachtregel:</span><span class="sxs-lookup"><span data-stu-id="910cb-148">You can then run your Python host program from the command line:</span></span>

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[<span data-ttu-id="910cb-149">C# met Visual Studio Code of Visual Studio</span><span class="sxs-lookup"><span data-stu-id="910cb-149">C# with Visual Studio Code or Visual Studio</span></span>](#tab/tabid-csharp)

<span data-ttu-id="910cb-150">Als u uw nieuwe Q#-programma wilt uitvoeren vanuit C#, wijzigt u `Driver.cs` om de volgende C#-code toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="910cb-150">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

<span data-ttu-id="910cb-151">U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdrachtregel (in Visual Studio moet u op F5 drukken):</span><span class="sxs-lookup"><span data-stu-id="910cb-151">You can then run your C# host program from the command line (in Visual Studio you should press F5):</span></span>

```bash
$ dotnet run
The random number generated is 42
```

***