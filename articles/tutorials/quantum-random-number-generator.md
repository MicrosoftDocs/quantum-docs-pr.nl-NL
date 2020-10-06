---
title: Een kwantumgenerator voor willekeurige getallen maken
description: Bouw een Q# project waarin de fundamentele Quantum concepten zoals de superpositie worden gedemonstreerd door een generator voor wille keurige getallen te maken.
author: bromeg
ms.author: megbrow
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: cefe35a10dd89c14d2f1abc3080d52ab125236d1
ms.sourcegitcommit: d98190988ff03146d9ca2b0d325870cd717d729a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2020
ms.locfileid: "91771272"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a><span data-ttu-id="3a945-103">Zelfstudie: Een kwantumgenerator voor willekeurige getallen implementeren in Q\#</span><span class="sxs-lookup"><span data-stu-id="3a945-103">Tutorial: Implement a Quantum Random Number Generator in Q\#</span></span>

<span data-ttu-id="3a945-104">Een eenvoudig voor beeld van een genoteerd Quantum algoritme Q# is een Quantum ring van een wille keurig getal.</span><span class="sxs-lookup"><span data-stu-id="3a945-104">A simple example of a quantum algorithm written in Q# is a quantum random number generator.</span></span> <span data-ttu-id="3a945-105">Dit algoritme maakt gebruik van de aard van kwantummechanismen om een willekeurig getal te produceren.</span><span class="sxs-lookup"><span data-stu-id="3a945-105">This algorithm leverages the nature of quantum mechanics to produce a random number.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3a945-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3a945-106">Prerequisites</span></span>

- <span data-ttu-id="3a945-107">De Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="3a945-107">The Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).</span></span>
- <span data-ttu-id="3a945-108">Een Q# project maken voor een [ Q# toepassing](xref:microsoft.quantum.install.standalone), met een [python-hostprogramma](xref:microsoft.quantum.install.python)of een [C#-hostprogramma](xref:microsoft.quantum.install.cs).</span><span class="sxs-lookup"><span data-stu-id="3a945-108">Create a Q# project for either a [Q# application](xref:microsoft.quantum.install.standalone), with a [Python host program](xref:microsoft.quantum.install.python), or a [C# host program](xref:microsoft.quantum.install.cs).</span></span>

## <a name="write-a-no-locq-operation"></a><span data-ttu-id="3a945-109">Een Q# bewerking schrijven</span><span class="sxs-lookup"><span data-stu-id="3a945-109">Write a Q# operation</span></span>

### <a name="no-locq-operation-code"></a><span data-ttu-id="3a945-110">Q# bewerkings code</span><span class="sxs-lookup"><span data-stu-id="3a945-110">Q# operation code</span></span>

1. <span data-ttu-id="3a945-111">Vervang de inhoud van het bestand Program.qs door de volgende code:</span><span class="sxs-lookup"><span data-stu-id="3a945-111">Replace the contents of the Program.qs file with the following code:</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

<span data-ttu-id="3a945-112">Zoals vermeld in het artikel [Inzicht in kwantumcomputing](xref:microsoft.quantum.overview.understanding) is een qubit een eenheid van kwantuminformatie die in superpositie kan zijn.</span><span class="sxs-lookup"><span data-stu-id="3a945-112">As mentioned in our [Understanding quantum computing](xref:microsoft.quantum.overview.understanding) article, a qubit is a unit of quantum information that can be in superposition.</span></span> <span data-ttu-id="3a945-113">Bij meting kan een qubit alleen 0 of 1 zijn.</span><span class="sxs-lookup"><span data-stu-id="3a945-113">When measured, a qubit can only be either 0 or 1.</span></span> <span data-ttu-id="3a945-114">Vóór de meting vertegenwoordigt de status van de Qubit echter de kans dat een 0 of een 1 met een meting wordt gelezen.</span><span class="sxs-lookup"><span data-stu-id="3a945-114">However, before measurement, the state of the qubit represents the probability of reading either a 0 or a 1 with a measurement.</span></span> <span data-ttu-id="3a945-115">Deze waarschijnlijkheidstoestand staat bekend als superpositie.</span><span class="sxs-lookup"><span data-stu-id="3a945-115">This probabilistic state is known as superposition.</span></span> <span data-ttu-id="3a945-116">We kunnen deze waarschijnlijkheid gebruiken voor het genereren van willekeurige getallen.</span><span class="sxs-lookup"><span data-stu-id="3a945-116">We can use this probability to generate random numbers.</span></span>

<span data-ttu-id="3a945-117">In onze Q# bewerking introduceren we het `Qubit` Data type, systeem eigen naar Q# .</span><span class="sxs-lookup"><span data-stu-id="3a945-117">In our Q# operation, we introduce the `Qubit` datatype, native to Q#.</span></span> <span data-ttu-id="3a945-118">We kunnen een `Qubit` alleen toewijzen met een `using`-instructie.</span><span class="sxs-lookup"><span data-stu-id="3a945-118">We can only allocate a `Qubit` with a `using` statement.</span></span> <span data-ttu-id="3a945-119">Wanneer een qubit wordt toegewezen, bevindt deze zich altijd in de toestand `Zero`.</span><span class="sxs-lookup"><span data-stu-id="3a945-119">When it gets allocated, a qubit is always in the `Zero`  state.</span></span> 

<span data-ttu-id="3a945-120">Met behulp van de bewerking `H` kunnen we onze `Qubit` in superpositie plaatsen.</span><span class="sxs-lookup"><span data-stu-id="3a945-120">Using the `H` operation, we are able to put our `Qubit` in superposition.</span></span> <span data-ttu-id="3a945-121">Als u een qubit wilt meten en de waarde ervan wilt lezen, gebruikt u de intrinsieke bewerking `M`.</span><span class="sxs-lookup"><span data-stu-id="3a945-121">To measure a qubit and read its value, you use the `M` intrinsic operation.</span></span>

<span data-ttu-id="3a945-122">Door onze `Qubit` in superpositie te plaatsen en vervolgens te meten, levert elke aanroep van de code een andere waarde op.</span><span class="sxs-lookup"><span data-stu-id="3a945-122">By putting our `Qubit` in superposition and measuring it, our result will be a different value each time the code is invoked.</span></span>

<span data-ttu-id="3a945-123">Wanneer de toewijzing van een `Qubit` ongedaan wordt gemaakt, moet deze expliciet weer worden ingesteld op de toestand `Zero`, anders rapporteert de simulator een runtime-fout.</span><span class="sxs-lookup"><span data-stu-id="3a945-123">When a `Qubit` is deallocated it must be explicitly set back to the `Zero` state, otherwise the simulator will report a runtime error.</span></span> <span data-ttu-id="3a945-124">Dit kan heel eenvoudig door `Reset` aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="3a945-124">An easy way to achieve this is invoking `Reset`.</span></span>

### <a name="visualizing-the-code-with-the-bloch-sphere"></a><span data-ttu-id="3a945-125">De code visualiseren met de Blochbol</span><span class="sxs-lookup"><span data-stu-id="3a945-125">Visualizing the code with the Bloch sphere</span></span>

<span data-ttu-id="3a945-126">In de Blochbol vertegenwoordigt de noordpool de klassieke waarde **0** en de zuidpool de klassieke waarde **1**.</span><span class="sxs-lookup"><span data-stu-id="3a945-126">In the Bloch sphere, the north pole represents the classical value **0** and the south pole represents the classical value **1**.</span></span> <span data-ttu-id="3a945-127">Elke superpositie kan worden weergegeven met een punt op de bol (aangeduid met een pijl).</span><span class="sxs-lookup"><span data-stu-id="3a945-127">Any superposition can be represented by a point on the sphere (represented by an arrow).</span></span> <span data-ttu-id="3a945-128">Hoe dichter het einde van de pijl bij een pool is, hoe groter de kans is dat de qubit bij meting uiteenvalt in de klassieke waarde die aan die pool is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="3a945-128">The closer the end of the arrow to a pole the higher the probability the qubit collapses into the classical value assigned to that pole when measured.</span></span> <span data-ttu-id="3a945-129">De toestand van de qubit die wordt weergegeven door de rode pijl hieronder heeft bijvoorbeeld een hogere kans om de waarde **0** te retourneren als deze wordt gemeten.</span><span class="sxs-lookup"><span data-stu-id="3a945-129">For example, the qubit state represented by the red arrow below has a higher probability of giving the value **0** if we measure it.</span></span>

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

<span data-ttu-id="3a945-130">We kunnen deze voorstelling gebruiken om te visualiseren wat de code doet:</span><span class="sxs-lookup"><span data-stu-id="3a945-130">We can use this representation to visualize what the code is doing:</span></span>

* <span data-ttu-id="3a945-131">We beginnen met een qubit die is geïnitialiseerd in de toestand **0** en passen `H` toe om een superpositie te maken waarin de waarschijnlijkheid van **0** en **1** hetzelfde is.</span><span class="sxs-lookup"><span data-stu-id="3a945-131">First we start with a qubit initialized in the state **0** and apply `H` to create a superposition in which the probabilities for **0** and **1** are the same.</span></span>

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* <span data-ttu-id="3a945-132">Vervolgens meten we de qubit en slaan we de uitvoer op:</span><span class="sxs-lookup"><span data-stu-id="3a945-132">Then we measure the qubit and save the output:</span></span>

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

<span data-ttu-id="3a945-133">Aangezien het resultaat van de meting volledig willekeurig is, hebben we een willekeurige bit verkregen.</span><span class="sxs-lookup"><span data-stu-id="3a945-133">Since the outcome of the measurement is completely random, we have obtained a random bit.</span></span> <span data-ttu-id="3a945-134">We kunnen deze bewerking meerdere keren aanroepen om gehele getallen te maken.</span><span class="sxs-lookup"><span data-stu-id="3a945-134">We can call this operation several times to create integers.</span></span> <span data-ttu-id="3a945-135">Als we de bewerking bijvoorbeeld drie keer aanroepen om drie willekeurige bits te verkrijgen, kunnen we willekeurige 3-bits getallen maken (dat wil zeggen, een willekeurig getal tussen 0 en 7).</span><span class="sxs-lookup"><span data-stu-id="3a945-135">For example, if we call the operation three times to obtain three random bits, we can build random 3-bit numbers (that is, a random number between 0 and 7).</span></span>


## <a name="creating-a-complete-random-number-generator"></a><span data-ttu-id="3a945-136">Een volledige generator van willekeurige getallen maken</span><span class="sxs-lookup"><span data-stu-id="3a945-136">Creating a complete random number generator</span></span>

<span data-ttu-id="3a945-137">Nu we een bewerking hebben Q# die wille keurige bits genereert, kunnen we deze gebruiken om een volledige Quantum-generator voor wille keurige getallen te maken.</span><span class="sxs-lookup"><span data-stu-id="3a945-137">Now that we have a Q# operation that generates random bits, we can use it to build a complete quantum random number generator.</span></span> <span data-ttu-id="3a945-138">We kunnen een Q# toepassing gebruiken of een host-programma gebruiken.</span><span class="sxs-lookup"><span data-stu-id="3a945-138">We can use a Q# application or use a host program.</span></span>



### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>[<span data-ttu-id="3a945-139">Q# toepassingen met Visual Studio of Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="3a945-139">Q# applications with Visual Studio or Visual Studio Code</span></span>](#tab/tabid-qsharp)

<span data-ttu-id="3a945-140">Als u de volledige Q# toepassing wilt maken, voegt u het volgende toegangs punt toe aan het Q# programma:</span><span class="sxs-lookup"><span data-stu-id="3a945-140">To create the full Q# application, add the following entry point to your Q# program:</span></span> 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

<span data-ttu-id="3a945-141">De bewerking of functie die is gemarkeerd met het `@EntryPoint()` kenmerk op een Simulator-of resource-Estimator wordt uitgevoerd, afhankelijk van de project configuratie en opdracht regel opties.</span><span class="sxs-lookup"><span data-stu-id="3a945-141">The program will run the operation or function marked with the `@EntryPoint()` attribute on a simulator or resource estimator, depending on the project configuration and command-line options.</span></span>

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

<span data-ttu-id="3a945-142">Druk in Visual Studio op CTRL + F5 om het script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="3a945-142">In Visual Studio, simply press Ctrl + F5 to run the script.</span></span>

<span data-ttu-id="3a945-143">Bouw in VS Code Program.qs voor de eerste keer door het onderstaande in de terminal in te voeren:</span><span class="sxs-lookup"><span data-stu-id="3a945-143">In VS Code, build the Program.qs the first time by typing the below in the terminal:</span></span>

```dotnetcli
dotnet build
```

<span data-ttu-id="3a945-144">Voor nieuwe uitvoeringen is het niet nodig om de build opnieuw te doen.</span><span class="sxs-lookup"><span data-stu-id="3a945-144">For subsequent runs, there is no need to build it again.</span></span> <span data-ttu-id="3a945-145">Typ de volgende opdracht en druk op enter om hem uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="3a945-145">To run it, type the following command and press enter:</span></span>

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-prompt"></a>[<span data-ttu-id="3a945-146">Python met Visual Studio code of de opdracht prompt</span><span class="sxs-lookup"><span data-stu-id="3a945-146">Python with Visual Studio Code or the command prompt</span></span>](#tab/tabid-python)

<span data-ttu-id="3a945-147">Als u uw nieuwe Q# programma wilt uitvoeren vanuit Python, slaat u de volgende code op als `host.py` :</span><span class="sxs-lookup"><span data-stu-id="3a945-147">To run your new Q# program from Python, save the following code as `host.py`:</span></span>

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

<span data-ttu-id="3a945-148">U kunt vervolgens uw python-hostprogramma uitvoeren vanaf de opdracht prompt:</span><span class="sxs-lookup"><span data-stu-id="3a945-148">You can then run your Python host program from the command prompt:</span></span>

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[<span data-ttu-id="3a945-149">C# met Visual Studio Code of Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3a945-149">C# with Visual Studio Code or Visual Studio</span></span>](#tab/tabid-csharp)

<span data-ttu-id="3a945-150">Als u uw nieuwe Q# programma vanuit C# wilt uitvoeren, wijzigt `Driver.cs` u de volgende C#-code:</span><span class="sxs-lookup"><span data-stu-id="3a945-150">To run your new Q# program from C#, modify `Driver.cs` to include the following C# code:</span></span>

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

<span data-ttu-id="3a945-151">U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdracht prompt (in Visual Studio moet u op F5 drukken):</span><span class="sxs-lookup"><span data-stu-id="3a945-151">You can then run your C# host program from the command prompt (in Visual Studio you should press F5):</span></span>

```bash
$ dotnet run
The random number generated is 42
```

***
