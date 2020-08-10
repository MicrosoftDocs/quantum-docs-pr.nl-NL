---
title: Ontwikkelen met Q# en .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 13d73bdf0287941c89e03ba63869095e5fca4e70
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867553"
---
# <a name="develop-with-no-locq-and-net"></a><span data-ttu-id="731cf-102">Ontwikkelen met Q# en .NET</span><span class="sxs-lookup"><span data-stu-id="731cf-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="731cf-103">Q# is gebouwd om prettig te kunnen werken met .NET-talen als C# en F#.</span><span class="sxs-lookup"><span data-stu-id="731cf-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="731cf-104">In deze handleiding wordt uitgelegd hoe u Q# gebruikt in combinatie met een hostprogramma dat is geschreven in een .NET-taal.</span><span class="sxs-lookup"><span data-stu-id="731cf-104">In this guide, we demonstrate how to use Q# with a host program written in a .NET language.</span></span>

<span data-ttu-id="731cf-105">Eerst maken we de Q#-toepassing en .NET-host, en vervolgens laten we zien hoe u Q# aanroept vanaf de host.</span><span class="sxs-lookup"><span data-stu-id="731cf-105">First we create the Q# application and .NET host, and then demonstrate how to call to Q# from the host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="731cf-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="731cf-106">Prerequisites</span></span>

- <span data-ttu-id="731cf-107">Installeer de Quantum Development Kit [voor Q#-opdrachtregelprojecten](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="731cf-107">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-no-locq-library-and-a-net-host"></a><span data-ttu-id="731cf-108">Een Q#-bibliotheek en een .NET-host maken</span><span class="sxs-lookup"><span data-stu-id="731cf-108">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="731cf-109">De eerste stap bestaat uit het maken van projecten voor uw Q#-bibliotheek en voor de .NET-host die de bewerkingen en functies aanroept die in de Q#-bibliotheek zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="731cf-109">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

<span data-ttu-id="731cf-110">Volg de instructies op het tabblad dat hoort bij de ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="731cf-110">Follow the instructions in the tab corresponding to your development environment.</span></span>
<span data-ttu-id="731cf-111">Als u een andere editor gebruikt dan Visual Studio of VS Code, volgt u gewoon de stappen voor de opdrachtregel.</span><span class="sxs-lookup"><span data-stu-id="731cf-111">If you are using an editor other than Visual Studio or VS Code, simply follow the command line steps.</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="731cf-112">Visual Studio Code of opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="731cf-112">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="731cf-113">Een nieuwe Q#-bibliotheek maken</span><span class="sxs-lookup"><span data-stu-id="731cf-113">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="731cf-114">Maak een nieuw C#- or F#-consoleproject</span><span class="sxs-lookup"><span data-stu-id="731cf-114">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="731cf-115">Voeg vanaf uw hostprogramma de Q#-bibliotheek toe als referentie</span><span class="sxs-lookup"><span data-stu-id="731cf-115">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="731cf-116">[Optioneel] Maak een oplossing voor beide projecten</span><span class="sxs-lookup"><span data-stu-id="731cf-116">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[<span data-ttu-id="731cf-117">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="731cf-117">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="731cf-118">Een nieuwe Q#-bibliotheek maken</span><span class="sxs-lookup"><span data-stu-id="731cf-118">Create a new Q# library</span></span>
  - <span data-ttu-id="731cf-119">Ga naar **Bestand** -> **Nieuw** -> **Project**</span><span class="sxs-lookup"><span data-stu-id="731cf-119">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="731cf-120">Typ Q# in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="731cf-120">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="731cf-121">Selecteer **Q#-bibliotheek**</span><span class="sxs-lookup"><span data-stu-id="731cf-121">Select **Q# Library**</span></span>
  - <span data-ttu-id="731cf-122">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="731cf-122">Select **Next**</span></span>
  - <span data-ttu-id="731cf-123">Kies een naam en een locatie voor uw bibliotheek</span><span class="sxs-lookup"><span data-stu-id="731cf-123">Choose a name and location for your library</span></span>
  - <span data-ttu-id="731cf-124">Zorg ervoor dat 'project en oplossing in dezelfde map plaatsen' is **uitgeschakeld**</span><span class="sxs-lookup"><span data-stu-id="731cf-124">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="731cf-125">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="731cf-125">Select **Create**</span></span>
- <span data-ttu-id="731cf-126">Maak een nieuw C#- of F#-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="731cf-126">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="731cf-127">Ga naar **Bestand** → **Nieuw** → **Project**</span><span class="sxs-lookup"><span data-stu-id="731cf-127">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="731cf-128">Selecteer 'Consoletoepassing (.NET Core)' voor C# of F#</span><span class="sxs-lookup"><span data-stu-id="731cf-128">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="731cf-129">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="731cf-129">Select **Next**</span></span>
  - <span data-ttu-id="731cf-130">Selecteer onder *oplossing* de optie 'aan oplossing toevoegen'</span><span class="sxs-lookup"><span data-stu-id="731cf-130">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="731cf-131">Kies een naam voor uw hostprogramma</span><span class="sxs-lookup"><span data-stu-id="731cf-131">Choose a name for your host program</span></span>
  - <span data-ttu-id="731cf-132">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="731cf-132">Select **Create**</span></span>

***

## <a name="calling-into-no-locq-from-net"></a><span data-ttu-id="731cf-133">Q# aanroepen vanuit .NET</span><span class="sxs-lookup"><span data-stu-id="731cf-133">Calling into Q# from .NET</span></span>

<span data-ttu-id="731cf-134">Nadat u de projecten hebt ingesteld, moet u de bovenstaande instructies volgen om Q# aan te roepen vanuit de .NET-consoletoepassing.</span><span class="sxs-lookup"><span data-stu-id="731cf-134">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="731cf-135">De Q#-compiler maakt .NET-klassen voor elke Q#-bewerking en -functie waarmee u uw kwantumprogramma's in een simulator kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="731cf-135">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="731cf-136">Zo bevat het [.NET-interoperabiliteitsvoorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) het volgende voorbeeld van een Q#-bewerking:</span><span class="sxs-lookup"><span data-stu-id="731cf-136">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="731cf-137">Als u deze bewerking vanuit .NET wilt aanroepen in een kwantumsimulator, kunt u de `Run`-methode gebruiken van de `RunAlgorithm` .NET-klasse die is gegenereerd door de Q#-compiler:</span><span class="sxs-lookup"><span data-stu-id="731cf-137">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="731cf-138">C#</span><span class="sxs-lookup"><span data-stu-id="731cf-138">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="731cf-139">F#</span><span class="sxs-lookup"><span data-stu-id="731cf-139">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="731cf-140">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="731cf-140">Next steps</span></span>

<span data-ttu-id="731cf-141">Nu u de Quantum Development Kit hebt ingesteld voor Q#-opdrachtregelprogramma's en interoperabiliteit met .NET, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="731cf-141">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
