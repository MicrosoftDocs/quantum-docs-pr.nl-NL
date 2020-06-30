---
title: Ontwikkelen met Q#-opdrachtregeltoepassingen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: 4311ebf9f72254485a20ba721ea2ce19163f4371
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274065"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="339ff-102">Ontwikkelen met Q#-opdrachtregeltoepassingen</span><span class="sxs-lookup"><span data-stu-id="339ff-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="339ff-103">Q#-programma's kunnen zelfstandig worden uitgevoerd zonder een stuurprogramma in een hosttaal, zoals C#, F# of Python.</span><span class="sxs-lookup"><span data-stu-id="339ff-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="339ff-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="339ff-104">Prerequisites</span></span>

- [<span data-ttu-id="339ff-105">.NET Core SDK 3.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="339ff-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="339ff-106">Installatie</span><span class="sxs-lookup"><span data-stu-id="339ff-106">Installation</span></span>

<span data-ttu-id="339ff-107">Hoewel u Q#-opdrachtregeltoepassingen in elke IDE kunt maken, raden we u aan om Visual Studio Code (VS Code) of Visual Studio IDE te gebruiken voor uw Q#-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="339ff-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="339ff-108">Tijdens het ontwikkelen in deze hulpprogramma's hebt u de beschikking over een groot aantal functies.</span><span class="sxs-lookup"><span data-stu-id="339ff-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="339ff-109">Ga als volgt te werk om VS Code te configureren:</span><span class="sxs-lookup"><span data-stu-id="339ff-109">To configure VS Code:</span></span>

1. <span data-ttu-id="339ff-110">Download en installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).</span><span class="sxs-lookup"><span data-stu-id="339ff-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="339ff-111">Installeer de [Microsoft QDK voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="339ff-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="339ff-112">Ga als volgt te werk om Visual Studio te configureren:</span><span class="sxs-lookup"><span data-stu-id="339ff-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="339ff-113">Download en installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 of hoger, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="339ff-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="339ff-114">Download en installeer de [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="339ff-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="339ff-115">Ontwikkelen met Q#, met behulp van VS Code</span><span class="sxs-lookup"><span data-stu-id="339ff-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="339ff-116">Ga als volgt te werk om de Q#-projectsjablonen te installeren:</span><span class="sxs-lookup"><span data-stu-id="339ff-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="339ff-117">Open VS Code.</span><span class="sxs-lookup"><span data-stu-id="339ff-117">Open VS Code.</span></span>
2. <span data-ttu-id="339ff-118">Klik op **Weergave** -> **Opdrachtpalet**.</span><span class="sxs-lookup"><span data-stu-id="339ff-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="339ff-119">Selecteer **Q#: Installeer de projectsjablonen**.</span><span class="sxs-lookup"><span data-stu-id="339ff-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="339ff-120">Als de melding **Projectsjablonen zijn geïnstalleerd** wordt weergegeven, is de QDK klaar om te worden gebruikt met uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="339ff-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="339ff-121">Ga als volgt te werk om een nieuw project te maken:</span><span class="sxs-lookup"><span data-stu-id="339ff-121">To create a new project:</span></span>

1. <span data-ttu-id="339ff-122">Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken**.</span><span class="sxs-lookup"><span data-stu-id="339ff-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="339ff-123">Klik op **Zelfstandige consoletoepassing**.</span><span class="sxs-lookup"><span data-stu-id="339ff-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="339ff-124">Ga naar de locatie waar het project moet worden opgeslagen en klik op **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="339ff-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="339ff-125">Klik rechtsonder op **Nieuw project openen...** als het project is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="339ff-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="339ff-126">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="339ff-126">Inspect the project.</span></span> <span data-ttu-id="339ff-127">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="339ff-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="339ff-128">Ga als volgt te werk om de toepassing uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="339ff-128">To run the application:</span></span>
1. <span data-ttu-id="339ff-129">Klik op **Terminal** -> **Nieuwe terminal**.</span><span class="sxs-lookup"><span data-stu-id="339ff-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="339ff-130">Voer bij de terminalprompt `dotnet run` in.</span><span class="sxs-lookup"><span data-stu-id="339ff-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="339ff-131">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="339ff-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="339ff-132">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de VS Code Q#-extensie.</span><span class="sxs-lookup"><span data-stu-id="339ff-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="339ff-133">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="339ff-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="339ff-134">Ontwikkelen met Q# met behulp van Visual Studio</span><span class="sxs-lookup"><span data-stu-id="339ff-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="339ff-135">Controleer uw Visual Studio-installatie door een Q# `Hello World`-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="339ff-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="339ff-136">Ga als volgt te werk om een nieuwe Q#-toepassing te maken:</span><span class="sxs-lookup"><span data-stu-id="339ff-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="339ff-137">Open Visual Studio en klik op **Bestand** -> **Nieuw** -> **Project**.</span><span class="sxs-lookup"><span data-stu-id="339ff-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="339ff-138">Typ `Q#` in het zoekvak, selecteer **Q#-toepassing** en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="339ff-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="339ff-139">Geef een naam en een locatie op voor uw toepassing en klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="339ff-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="339ff-140">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="339ff-140">Inspect the project.</span></span> <span data-ttu-id="339ff-141">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="339ff-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="339ff-142">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="339ff-142">To run the application:</span></span>
1. <span data-ttu-id="339ff-143">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**.</span><span class="sxs-lookup"><span data-stu-id="339ff-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="339ff-144">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="339ff-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="339ff-145">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="339ff-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="339ff-146">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="339ff-146">Next steps</span></span>

<span data-ttu-id="339ff-147">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="339ff-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
