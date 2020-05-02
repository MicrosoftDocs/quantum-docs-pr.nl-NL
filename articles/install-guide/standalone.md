---
title: "Q #-Program ma's uitvoeren zonder stuur programma en host-taal"
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e83acaf10af952da06abf4737ad2ec91f1cf1b8e
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/01/2020
ms.locfileid: "82706798"
---
# <a name="q-command-line-applications"></a><span data-ttu-id="fb137-102">Q # opdracht regel toepassingen</span><span class="sxs-lookup"><span data-stu-id="fb137-102">Q# Command Line Applications</span></span>

<span data-ttu-id="fb137-103">Q #-Program ma's kunnen zelfstandig worden uitgevoerd, zonder een stuur programma in een host-taal als C#, F # of python.</span><span class="sxs-lookup"><span data-stu-id="fb137-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="fb137-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="fb137-104">Pre-requisites</span></span>

- [<span data-ttu-id="fb137-105">.NET Core SDK 3,1 of hoger</span><span class="sxs-lookup"><span data-stu-id="fb137-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="fb137-106">Installatie</span><span class="sxs-lookup"><span data-stu-id="fb137-106">Installation</span></span>

<span data-ttu-id="fb137-107">Hoewel u Q # opdracht regel toepassingen in een IDE kunt maken, raden we u aan om Visual Studio code (VS code) of Visual Studio IDE te gebruiken voor uw Q #-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="fb137-107">While you can build Q# command line applications in any IDE, we highly recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="fb137-108">Door gebruik te maken van VS code of Visual Studio en de QDK Visual Studio code-extensie kunt u toegang krijgen tot uitgebreide functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="fb137-108">By using VS Code or Visual Studio and the QDK Visual Studio Code extension you gain access to richer functionality.</span></span>

- <span data-ttu-id="fb137-109">[VS-code](https://code.visualstudio.com/download) installeren (Windows, Linux en Mac)</span><span class="sxs-lookup"><span data-stu-id="fb137-109">Install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac)</span></span>
- <span data-ttu-id="fb137-110">De [QDK-uitbrei ding voor VS code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) installeren of</span><span class="sxs-lookup"><span data-stu-id="fb137-110">Install the [QDK extension for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode) OR</span></span>
- <span data-ttu-id="fb137-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="fb137-111">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>
- <span data-ttu-id="fb137-112">Down load en installeer de [Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="fb137-112">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="fb137-113">Ontwikkelen met Q # met behulp van VS code</span><span class="sxs-lookup"><span data-stu-id="fb137-113">Develop with Q# using VS Code</span></span>

<span data-ttu-id="fb137-114">Installeer de Quantum-projectsjablonen:</span><span class="sxs-lookup"><span data-stu-id="fb137-114">Install the Quantum project templates:</span></span>

- <span data-ttu-id="fb137-115">Ga naar het**opdracht palet** **weer geven** -> </span><span class="sxs-lookup"><span data-stu-id="fb137-115">Go to **View** -> **Command Palette**</span></span>
- <span data-ttu-id="fb137-116">Selecteer **Q #: Project sjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="fb137-116">Select **Q#: Install project templates**</span></span>

<span data-ttu-id="fb137-117">De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="fb137-117">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>
- <span data-ttu-id="fb137-118">Maak een nieuw project:</span><span class="sxs-lookup"><span data-stu-id="fb137-118">Create a new project:</span></span>
  - <span data-ttu-id="fb137-119">Ga naar het**opdracht palet** **weer geven** -> </span><span class="sxs-lookup"><span data-stu-id="fb137-119">Go to **View** -> **Command Palette**</span></span>
  - <span data-ttu-id="fb137-120">Selecteer **Q #: nieuw project maken**</span><span class="sxs-lookup"><span data-stu-id="fb137-120">Select **Q#: Create New Project**</span></span>
  - <span data-ttu-id="fb137-121">**Zelfstandige console toepassing** selecteren</span><span class="sxs-lookup"><span data-stu-id="fb137-121">Select **Standalone console application**</span></span>
  - <span data-ttu-id="fb137-122">Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken</span><span class="sxs-lookup"><span data-stu-id="fb137-122">Navigate to the location on the file system where you would like to create the application</span></span>
  - <span data-ttu-id="fb137-123">Klik op de knop **Nieuw project openen...** zodra het project is gemaakt</span><span class="sxs-lookup"><span data-stu-id="fb137-123">Click on the **Open new project...** button, once the project has been created</span></span>
        
- <span data-ttu-id="fb137-124">Controleer het project</span><span class="sxs-lookup"><span data-stu-id="fb137-124">Inspect the project</span></span>
  - <span data-ttu-id="fb137-125">U ziet dat een bestand wordt gemaakt `Program.qs` met de naam Create, een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="fb137-125">You should see that a file called `Program.qs` created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="fb137-126">Voer de toepassing uit:</span><span class="sxs-lookup"><span data-stu-id="fb137-126">Run the application:</span></span>
  - <span data-ttu-id="fb137-127">Ga naar **Terminal** -> **New Terminal**</span><span class="sxs-lookup"><span data-stu-id="fb137-127">Go to **Terminal** -> **New Terminal**</span></span>
  - <span data-ttu-id="fb137-128">Voer `dotnet run` in</span><span class="sxs-lookup"><span data-stu-id="fb137-128">Enter `dotnet run`</span></span>
  - <span data-ttu-id="fb137-129">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="fb137-129">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="fb137-130">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie.</span><span class="sxs-lookup"><span data-stu-id="fb137-130">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="fb137-131">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="fb137-131">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="fb137-132">Ontwikkelen met Q # met behulp van Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb137-132">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="fb137-133">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="fb137-133">Verify the installation by creating a `Hello World` application</span></span>

- <span data-ttu-id="fb137-134">Maak een nieuwe Q#-toepassing</span><span class="sxs-lookup"><span data-stu-id="fb137-134">Create a new Q# application</span></span>
  - <span data-ttu-id="fb137-135">Ga naar het **bestand** -> **Nieuw** -> **project**</span><span class="sxs-lookup"><span data-stu-id="fb137-135">Go to **File** -> **New** -> **Project**</span></span>
  - <span data-ttu-id="fb137-136">Typ `Q#` in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="fb137-136">Type `Q#` in the search box</span></span>
  - <span data-ttu-id="fb137-137">Selecteer **Q#-toepassing**</span><span class="sxs-lookup"><span data-stu-id="fb137-137">Select **Q# Application**</span></span>
  - <span data-ttu-id="fb137-138">Selecteer **volgende**</span><span class="sxs-lookup"><span data-stu-id="fb137-138">Select **Next**</span></span>
  - <span data-ttu-id="fb137-139">Kies een naam en een locatie voor uw toepassing</span><span class="sxs-lookup"><span data-stu-id="fb137-139">Choose a name and location for your application</span></span>
  - <span data-ttu-id="fb137-140">Selecteer **maken**</span><span class="sxs-lookup"><span data-stu-id="fb137-140">Select **Create**</span></span>

- <span data-ttu-id="fb137-141">Controleer het project</span><span class="sxs-lookup"><span data-stu-id="fb137-141">Inspect the project</span></span>
  - <span data-ttu-id="fb137-142">U ziet dat er een bestand met `Program.qs` de naam is gemaakt. Dit is een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="fb137-142">You should see that a file called `Program.qs` has been created, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

- <span data-ttu-id="fb137-143">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="fb137-143">Run the application</span></span>
  - <span data-ttu-id="fb137-144">Selecteer **fouten opsporen** -> **starten zonder fout opsporing**</span><span class="sxs-lookup"><span data-stu-id="fb137-144">Select **Debug** -> **Start Without Debugging**</span></span>
  - <span data-ttu-id="fb137-145">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="fb137-145">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="fb137-146">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="fb137-146">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  


## <a name="whats-next"></a><span data-ttu-id="fb137-147">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="fb137-147">What's next?</span></span>

<span data-ttu-id="fb137-148">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="fb137-148">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
