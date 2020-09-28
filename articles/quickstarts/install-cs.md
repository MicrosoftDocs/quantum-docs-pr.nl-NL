---
title: Ontwikkelen met Q# en .NET
description: Meer informatie over hoe u een Q#-toepassing maakt met .NET-talen.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: e8733918daa02afaea0fc1994d5f0851d4be9b93
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834326"
---
# <a name="develop-with-no-locq-and-net"></a><span data-ttu-id="be2d6-103">Ontwikkelen met Q# en .NET</span><span class="sxs-lookup"><span data-stu-id="be2d6-103">Develop with Q# and .NET</span></span>

<span data-ttu-id="be2d6-104">Q# is gebouwd om prettig te kunnen werken met .NET-talen als C# en F#.</span><span class="sxs-lookup"><span data-stu-id="be2d6-104">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="be2d6-105">In deze handleiding wordt uitgelegd hoe u Q# gebruikt in combinatie met een hostprogramma dat is geschreven in een .NET-taal.</span><span class="sxs-lookup"><span data-stu-id="be2d6-105">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="be2d6-106">Eerst maken we de Q#-toepassing en .NET-host, en vervolgens laten we zien hoe u Q# aanroept vanaf de host.</span><span class="sxs-lookup"><span data-stu-id="be2d6-106">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="be2d6-107">Vereisten</span><span class="sxs-lookup"><span data-stu-id="be2d6-107">Prerequisites</span></span>

- <span data-ttu-id="be2d6-108">Installeer de Quantum Development Kit [voor Q#-projecten](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="be2d6-108">Install the Quantum Development Kit [for use with Q# projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-no-locq-library-and-a-net-host"></a><span data-ttu-id="be2d6-109">Een Q#-bibliotheek en een .NET-host maken</span><span class="sxs-lookup"><span data-stu-id="be2d6-109">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="be2d6-110">De eerste stap bestaat uit het maken van projecten voor uw Q#-bibliotheek en voor de .NET-host die de bewerkingen en functies aanroept die in de Q#-bibliotheek zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="be2d6-110">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="be2d6-111">Volg de instructies op het tabblad dat hoort bij de ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="be2d6-111">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="be2d6-112">Als u een andere editor gebruikt dan Visual Studio of VS Code, volgt u gewoon de stappen voor de opdrachtprompt.</span><span class="sxs-lookup"><span data-stu-id="be2d6-112">If you are using an editor other than Visual Studio or VS Code, simply follow the command prompt steps.</span></span>

### <a name="visual-studio-code-or-command-prompt"></a>[<span data-ttu-id="be2d6-113">Visual Studio Code of opdrachtprompt</span><span class="sxs-lookup"><span data-stu-id="be2d6-113">Visual Studio Code or command prompt</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="be2d6-114">Een nieuwe Q#-bibliotheek maken</span><span class="sxs-lookup"><span data-stu-id="be2d6-114">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="be2d6-115">Maak een nieuw C#- or F#-consoleproject</span><span class="sxs-lookup"><span data-stu-id="be2d6-115">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="be2d6-116">Voeg vanaf uw hostprogramma de Q#-bibliotheek toe als referentie</span><span class="sxs-lookup"><span data-stu-id="be2d6-116">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="be2d6-117">[Optioneel] Maak een oplossing voor beide projecten</span><span class="sxs-lookup"><span data-stu-id="be2d6-117">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="be2d6-118">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="be2d6-118">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="be2d6-119">Een nieuwe Q#-bibliotheek maken</span><span class="sxs-lookup"><span data-stu-id="be2d6-119">Create a new Q# library</span></span>
  - <span data-ttu-id="be2d6-120">Ga naar **Bestand** -> **Nieuw** -> **Project**</span><span class="sxs-lookup"><span data-stu-id="be2d6-120">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="be2d6-121">Typ Q# in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="be2d6-121">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="be2d6-122">Selecteer **Q#-bibliotheek**</span><span class="sxs-lookup"><span data-stu-id="be2d6-122">Select **Q# Library**</span></span>
  - <span data-ttu-id="be2d6-123">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="be2d6-123">Select **Next**</span></span>
  - <span data-ttu-id="be2d6-124">Kies een naam en een locatie voor uw bibliotheek</span><span class="sxs-lookup"><span data-stu-id="be2d6-124">Choose a name and location for your library</span></span>
  - <span data-ttu-id="be2d6-125">Zorg ervoor dat 'project en oplossing in dezelfde map plaatsen' is **uitgeschakeld**</span><span class="sxs-lookup"><span data-stu-id="be2d6-125">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="be2d6-126">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="be2d6-126">Select **Create**</span></span>
- <span data-ttu-id="be2d6-127">Maak een nieuw C#- of F#-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="be2d6-127">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="be2d6-128">Ga naar **Bestand** → **Nieuw** → **Project**</span><span class="sxs-lookup"><span data-stu-id="be2d6-128">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="be2d6-129">Selecteer 'Consoletoepassing (.NET Core)' voor C# of F#</span><span class="sxs-lookup"><span data-stu-id="be2d6-129">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="be2d6-130">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="be2d6-130">Select **Next**</span></span>
  - <span data-ttu-id="be2d6-131">Selecteer onder *oplossing* de optie 'aan oplossing toevoegen'</span><span class="sxs-lookup"><span data-stu-id="be2d6-131">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="be2d6-132">Kies een naam voor uw hostprogramma</span><span class="sxs-lookup"><span data-stu-id="be2d6-132">Choose a name for your host program</span></span>
  - <span data-ttu-id="be2d6-133">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="be2d6-133">Select **Create**</span></span>

***

## <a name="calling-into-no-locq-from-net"></a><span data-ttu-id="be2d6-134">Q# aanroepen vanuit .NET</span><span class="sxs-lookup"><span data-stu-id="be2d6-134">Calling into Q# from .NET</span></span>

<span data-ttu-id="be2d6-135">Nadat u de projecten hebt ingesteld, moet u de bovenstaande instructies volgen om Q# aan te roepen vanuit de .NET-consoletoepassing.</span><span class="sxs-lookup"><span data-stu-id="be2d6-135">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="be2d6-136">De Q#-compiler maakt .NET-klassen voor elke Q#-bewerking en -functie waarmee u uw kwantumprogramma's in een simulator kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="be2d6-136">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="be2d6-137">Zo bevat het [.NET-interoperabiliteitsvoorbeeld](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) het volgende voorbeeld van een Q#-bewerking:</span><span class="sxs-lookup"><span data-stu-id="be2d6-137">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="be2d6-138">Als u deze bewerking vanuit .NET wilt aanroepen in een kwantumsimulator, kunt u de `Run`-methode gebruiken van de `RunAlgorithm` .NET-klasse die is gegenereerd door de Q#-compiler:</span><span class="sxs-lookup"><span data-stu-id="be2d6-138">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="be2d6-139">C#</span><span class="sxs-lookup"><span data-stu-id="be2d6-139">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="be2d6-140">F#</span><span class="sxs-lookup"><span data-stu-id="be2d6-140">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="be2d6-141">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="be2d6-141">Next steps</span></span>

<span data-ttu-id="be2d6-142">Nu u de Quantum Development Kit hebt ingesteld voor Q#-toepassingen en interoperabiliteit met .NET, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="be2d6-142">Now that you have the Quantum Development Kit set up for both Q# applications and interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
