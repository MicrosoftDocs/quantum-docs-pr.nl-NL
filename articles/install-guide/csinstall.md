---
title: Ontwikkelen met Q# + C#
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 5bcb036b0b32e64d43f90e9a068d9dcc237890ba
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680170"
---
# <a name="using-q-with-c-and-f"></a><span data-ttu-id="45442-102">Q # gebruiken met C\# en F\#</span><span class="sxs-lookup"><span data-stu-id="45442-102">Using Q# with C\# and F\#</span></span>

<span data-ttu-id="45442-103">Q # is gebouwd om goed te kunnen spelen met .NET-talen zoals C# en F #.</span><span class="sxs-lookup"><span data-stu-id="45442-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="45442-104">In deze hand leiding wordt uitgelegd hoe u Q # gebruikt met een hostprogramma dat is geschreven in een .NET-taal.</span><span class="sxs-lookup"><span data-stu-id="45442-104">In this guide, we'll demonstrate how to use Q# with a host program written in a .NET language.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="45442-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="45442-105">Prerequisites</span></span>

- <span data-ttu-id="45442-106">Installeer de Quantum Development Kit [voor gebruik met Q #-opdracht regel projecten](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="45442-106">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="45442-107">Een Q #-bibliotheek en een .NET-host maken</span><span class="sxs-lookup"><span data-stu-id="45442-107">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="45442-108">De eerste stap is het maken van projecten voor uw Q #-bibliotheek en voor de .NET-host die de bewerkingen en functies bevat die in uw Q #-bibliotheek zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="45442-108">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

### <a name="visual-studio-2019"></a>[<span data-ttu-id="45442-109">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="45442-109">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="45442-110">Een nieuwe Q #-bibliotheek maken</span><span class="sxs-lookup"><span data-stu-id="45442-110">Create a new Q# library</span></span>
  - <span data-ttu-id="45442-111">Ga naar het **bestand** -> **Nieuw** -> **project**</span><span class="sxs-lookup"><span data-stu-id="45442-111">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="45442-112">Typ "Q #" in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="45442-112">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="45442-113">Selecteer **Q # Library**</span><span class="sxs-lookup"><span data-stu-id="45442-113">Select **Q# Library**</span></span>
  - <span data-ttu-id="45442-114">Selecteer **volgende**</span><span class="sxs-lookup"><span data-stu-id="45442-114">Select **Next**</span></span>
  - <span data-ttu-id="45442-115">Een naam en locatie voor uw bibliotheek kiezen</span><span class="sxs-lookup"><span data-stu-id="45442-115">Choose a name and location for your library</span></span>
  - <span data-ttu-id="45442-116">Zorg ervoor dat ' project en oplossing in dezelfde directory plaatsen ' is **uitgeschakeld**</span><span class="sxs-lookup"><span data-stu-id="45442-116">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="45442-117">Selecteer **maken**</span><span class="sxs-lookup"><span data-stu-id="45442-117">Select **Create**</span></span>
- <span data-ttu-id="45442-118">Een nieuw C#-of F #-host-programma maken</span><span class="sxs-lookup"><span data-stu-id="45442-118">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="45442-119">Ga naar **bestand** → **Nieuw** → **project**</span><span class="sxs-lookup"><span data-stu-id="45442-119">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="45442-120">Selecteer console-app (.NET core) voor C# of F #</span><span class="sxs-lookup"><span data-stu-id="45442-120">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="45442-121">Selecteer **volgende**</span><span class="sxs-lookup"><span data-stu-id="45442-121">Select **Next**</span></span>
  - <span data-ttu-id="45442-122">Onder *oplossing*selecteert u ' toevoegen aan oplossing '</span><span class="sxs-lookup"><span data-stu-id="45442-122">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="45442-123">Kies een naam voor uw hostprogramma</span><span class="sxs-lookup"><span data-stu-id="45442-123">Choose a name for your host program</span></span>
  - <span data-ttu-id="45442-124">Selecteer **maken**</span><span class="sxs-lookup"><span data-stu-id="45442-124">Select **Create**</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="45442-125">Visual Studio code of opdracht regel</span><span class="sxs-lookup"><span data-stu-id="45442-125">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="45442-126">Een nieuwe Q #-bibliotheek maken</span><span class="sxs-lookup"><span data-stu-id="45442-126">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="45442-127">Een nieuw C#-of F #-console project maken</span><span class="sxs-lookup"><span data-stu-id="45442-127">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="45442-128">Voeg uw Q #-bibliotheek toe als referentie van uw host-programma</span><span class="sxs-lookup"><span data-stu-id="45442-128">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="45442-129">Beschrijving Een oplossing maken voor beide projecten</span><span class="sxs-lookup"><span data-stu-id="45442-129">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="45442-130">Aanroepen van Q # vanuit .NET</span><span class="sxs-lookup"><span data-stu-id="45442-130">Calling into Q# from .NET</span></span>

<span data-ttu-id="45442-131">Nadat u uw projecten hebt ingesteld, volgt u de bovenstaande instructies, kunt u aan Q # bellen vanuit uw .NET-console toepassing.</span><span class="sxs-lookup"><span data-stu-id="45442-131">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="45442-132">De Q #-compiler maakt .NET-klassen voor elke Q #-bewerking en functie waarmee u uw Quantum Programma's in een Simulator kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="45442-132">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="45442-133">Het voor beeld van een [.net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) omvat bijvoorbeeld het volgende een Q #-bewerking:</span><span class="sxs-lookup"><span data-stu-id="45442-133">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="45442-134">U kunt deze bewerking vanuit .NET aanroepen op een Quantum Simulator door de `Run` methode van de `RunAlgorithm` .net-klasse te gebruiken die is gegenereerd door de Q #-compiler:</span><span class="sxs-lookup"><span data-stu-id="45442-134">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="45442-135">G #</span><span class="sxs-lookup"><span data-stu-id="45442-135">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="45442-136">Ls #</span><span class="sxs-lookup"><span data-stu-id="45442-136">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="whats-next"></a><span data-ttu-id="45442-137">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="45442-137">What's next?</span></span>

<span data-ttu-id="45442-138">Nu u de Quantum Development Kit hebt ingesteld voor zowel Q # opdracht regel Programma's als voor interoperabiliteit met .NET, kunt u [uw eerste Quantum programma](xref:microsoft.quantum.write-program)schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="45442-138">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
