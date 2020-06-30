---
title: Ontwikkelen met Q# en .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 2b0b16bdd9fccc3b668036e6df2b20e11b32f8b6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274051"
---
# <a name="develop-with-q-and-net"></a><span data-ttu-id="80e12-102">Ontwikkelen met Q# en .NET</span><span class="sxs-lookup"><span data-stu-id="80e12-102">Develop with Q# and .NET</span></span>

<span data-ttu-id="80e12-103">Q# is gebouwd om prettig te kunnen werken met .NET-talen, zoals C# en F#.</span><span class="sxs-lookup"><span data-stu-id="80e12-103">Q# is built to play well with .NET languages such as C# and F#.</span></span>
<span data-ttu-id="80e12-104">In deze handleiding wordt uitgelegd hoe u Q# gebruikt in combinatie met een hostprogramma dat is geschreven in een .NET-taal.</span><span class="sxs-lookup"><span data-stu-id="80e12-104">In this guide, we'll demonstrate how to use Q# with a host program written in a .NET language.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="80e12-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="80e12-105">Prerequisites</span></span>

- <span data-ttu-id="80e12-106">Installeer de Quantum Development Kit [voor Q#-opdrachtregelprojecten](xref:microsoft.quantum.install.standalone).</span><span class="sxs-lookup"><span data-stu-id="80e12-106">Install the Quantum Development Kit [for use with Q# command-line projects](xref:microsoft.quantum.install.standalone).</span></span>

## <a name="creating-a-q-library-and-a-net-host"></a><span data-ttu-id="80e12-107">Een Q#-bibliotheek en een .NET-host maken</span><span class="sxs-lookup"><span data-stu-id="80e12-107">Creating a Q# library and a .NET host</span></span>

<span data-ttu-id="80e12-108">De eerste stap is het maken van projecten voor uw Q#-bibliotheek en voor de .NET-host die de bewerkingen en functies aanroept die in uw Q#-bibliotheek zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="80e12-108">The first step is to create projects for your Q# library, and for the .NET host that will call into the operations and functions defined in your Q# library.</span></span>

### <a name="visual-studio-2019"></a>[<span data-ttu-id="80e12-109">Visual Studio 2019</span><span class="sxs-lookup"><span data-stu-id="80e12-109">Visual Studio 2019</span></span>](#tab/tabid-vs2019)

- <span data-ttu-id="80e12-110">Maak een nieuwe Q#-bibliotheek</span><span class="sxs-lookup"><span data-stu-id="80e12-110">Create a new Q# library</span></span>
  - <span data-ttu-id="80e12-111">Ga naar **Bestand** -> **Nieuw** -> **Project**</span><span class="sxs-lookup"><span data-stu-id="80e12-111">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="80e12-112">Typ 'Q#' in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="80e12-112">Type "Q#" in the search box</span></span>
  - <span data-ttu-id="80e12-113">Selecteer **Q#-bibliotheek**</span><span class="sxs-lookup"><span data-stu-id="80e12-113">Select **Q# Library**</span></span>
  - <span data-ttu-id="80e12-114">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="80e12-114">Select **Next**</span></span>
  - <span data-ttu-id="80e12-115">Kies een naam en een locatie voor uw bibliotheek</span><span class="sxs-lookup"><span data-stu-id="80e12-115">Choose a name and location for your library</span></span>
  - <span data-ttu-id="80e12-116">Zorg ervoor dat 'project en oplossing in dezelfde map plaatsen' is **uitgeschakeld**</span><span class="sxs-lookup"><span data-stu-id="80e12-116">Make sure that "place project and solution in same directory" is **unchecked**</span></span>
  - <span data-ttu-id="80e12-117">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="80e12-117">Select **Create**</span></span>
- <span data-ttu-id="80e12-118">Maak een nieuw C#- of F#-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="80e12-118">Create a new C# or F# host program</span></span>
  - <span data-ttu-id="80e12-119">Ga naar **Bestand** → **Nieuw** → **Project**</span><span class="sxs-lookup"><span data-stu-id="80e12-119">Go to **File** → **New** → **Project**</span></span>
  - <span data-ttu-id="80e12-120">Selecteer 'Consoletoepassing (.NET Core)' voor C# of F#</span><span class="sxs-lookup"><span data-stu-id="80e12-120">Select "Console App (.NET Core")" for either C# or F#</span></span>
  - <span data-ttu-id="80e12-121">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="80e12-121">Select **Next**</span></span>
  - <span data-ttu-id="80e12-122">Selecteer onder *oplossing* de optie 'aan oplossing toevoegen'</span><span class="sxs-lookup"><span data-stu-id="80e12-122">Under *solution*, select "add to solution"</span></span>
  - <span data-ttu-id="80e12-123">Kies een naam voor uw hostprogramma</span><span class="sxs-lookup"><span data-stu-id="80e12-123">Choose a name for your host program</span></span>
  - <span data-ttu-id="80e12-124">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="80e12-124">Select **Create**</span></span>

### <a name="visual-studio-code-or-command-line"></a>[<span data-ttu-id="80e12-125">Visual Studio Code of opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="80e12-125">Visual Studio Code or Command Line</span></span>](#tab/tabid-cmdline)

- <span data-ttu-id="80e12-126">Maak een nieuwe Q#-bibliotheek</span><span class="sxs-lookup"><span data-stu-id="80e12-126">Create a new Q# library</span></span>

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- <span data-ttu-id="80e12-127">Maak een nieuw C#- or F#-consoleproject</span><span class="sxs-lookup"><span data-stu-id="80e12-127">Create a new C# or F# console project</span></span>

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- <span data-ttu-id="80e12-128">Voeg uw Q#-bibliotheek toe als referentie van uw hostprogramma</span><span class="sxs-lookup"><span data-stu-id="80e12-128">Add your Q# library as a reference from your host program</span></span>

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- <span data-ttu-id="80e12-129">[Optioneel] Maak een oplossing voor beide projecten</span><span class="sxs-lookup"><span data-stu-id="80e12-129">[Optional] Create a solution for both projects</span></span>

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a><span data-ttu-id="80e12-130">Q# aanroepen vanuit .NET</span><span class="sxs-lookup"><span data-stu-id="80e12-130">Calling into Q# from .NET</span></span>

<span data-ttu-id="80e12-131">Nadat u uw projecten hebt ingesteld, moet u de bovenstaande instructies volgen om Q# aan te roepen vanuit uw .NET-consoletoepassing.</span><span class="sxs-lookup"><span data-stu-id="80e12-131">Once you have your projects set up following the above instructions, you can call into Q# from your .NET console application.</span></span>
<span data-ttu-id="80e12-132">De Q#-compiler maakt .NET-klassen voor elke Q#-bewerking en -functie waarmee u uw kwantumprogramma's in een simulator kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="80e12-132">The Q# compiler will create .NET classes for each Q# operation and function that allow you to run your quantum programs on a simulator.</span></span>

<span data-ttu-id="80e12-133">Zo bevat het [.NET-interoperabiliteitsvoorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) het volgende voorbeeld van een Q#-bewerking:</span><span class="sxs-lookup"><span data-stu-id="80e12-133">For example, the [.NET interoperability sample](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) includes the following example of a Q# operation:</span></span>

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

<span data-ttu-id="80e12-134">Als u deze bewerking vanuit .NET wilt aanroepen in een kwantumsimulator, kunt u de `Run`-methode gebruiken van de `RunAlgorithm` .NET-klasse die is gegenereerd door de Q#-compiler:</span><span class="sxs-lookup"><span data-stu-id="80e12-134">To call this operation from .NET on a quantum simulator, you can use the `Run` method of the `RunAlgorithm` .NET class generated by the Q# compiler:</span></span>

### <a name="c"></a>[<span data-ttu-id="80e12-135">C#</span><span class="sxs-lookup"><span data-stu-id="80e12-135">C#</span></span>](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[<span data-ttu-id="80e12-136">F#</span><span class="sxs-lookup"><span data-stu-id="80e12-136">F#</span></span>](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a><span data-ttu-id="80e12-137">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="80e12-137">Next steps</span></span>

<span data-ttu-id="80e12-138">Nu u de Quantum Development Kit hebt ingesteld voor Q#-opdrachtregelprogramma's en interoperabiliteit met .NET, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="80e12-138">Now that you have Quantum Development Kit set up for both Q# command-line programs, and for interoperability with .NET, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
