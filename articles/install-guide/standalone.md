---
title: 'Ontwikkelen met Q # opdracht regel toepassingen'
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
ms.openlocfilehash: e829862521951c50cb42eebf261c803071a95275
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426424"
---
# <a name="develop-with-q-command-line-applications"></a><span data-ttu-id="11e1e-102">Ontwikkelen met Q # opdracht regel toepassingen</span><span class="sxs-lookup"><span data-stu-id="11e1e-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="11e1e-103">Q #-Program ma's kunnen zelfstandig worden uitgevoerd, zonder een stuur programma in een host-taal als C#, F # of python.</span><span class="sxs-lookup"><span data-stu-id="11e1e-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="11e1e-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="11e1e-104">Pre-requisites</span></span>

- [<span data-ttu-id="11e1e-105">.NET Core SDK 3,1 of hoger</span><span class="sxs-lookup"><span data-stu-id="11e1e-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="11e1e-106">Installatie</span><span class="sxs-lookup"><span data-stu-id="11e1e-106">Installation</span></span>

<span data-ttu-id="11e1e-107">Hoewel u Q # opdracht regel toepassingen in een IDE kunt maken, raden we u aan om Visual Studio code (VS code) of Visual Studio IDE te gebruiken voor uw Q #-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="11e1e-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for your Q# applications.</span></span> <span data-ttu-id="11e1e-108">Het ontwikkelen van deze hulpprogram ma's biedt toegang tot uitgebreide functionaliteit.</span><span class="sxs-lookup"><span data-stu-id="11e1e-108">Developing in these tools provides access to rich functionality.</span></span>

<span data-ttu-id="11e1e-109">VS-code configureren:</span><span class="sxs-lookup"><span data-stu-id="11e1e-109">To configure VS Code:</span></span>

1. <span data-ttu-id="11e1e-110">Down load en Installeer [VS code](https://code.visualstudio.com/download) (Windows, Linux en Mac).</span><span class="sxs-lookup"><span data-stu-id="11e1e-110">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="11e1e-111">Installeer de [micro soft-QDK voor VS code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="11e1e-111">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="11e1e-112">Visual Studio configureren:</span><span class="sxs-lookup"><span data-stu-id="11e1e-112">To configure Visual Studio:</span></span>

1. <span data-ttu-id="11e1e-113">Down load en Installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16,3 of hoger met de .net core-werk belasting voor meerdere platform ontwikkeling ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="11e1e-113">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="11e1e-114">Down load en installeer de [micro soft-QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="11e1e-114">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>


## <a name="develop-with-q-using-vs-code"></a><span data-ttu-id="11e1e-115">Ontwikkelen met Q # met behulp van VS code</span><span class="sxs-lookup"><span data-stu-id="11e1e-115">Develop with Q# using VS Code</span></span>

<span data-ttu-id="11e1e-116">De Q # project-sjablonen installeren:</span><span class="sxs-lookup"><span data-stu-id="11e1e-116">Install the Q# project templates:</span></span>

1. <span data-ttu-id="11e1e-117">Open VS code.</span><span class="sxs-lookup"><span data-stu-id="11e1e-117">Open VS Code.</span></span>
2. <span data-ttu-id="11e1e-118">Klik **View**op  ->  **opdracht palet**weer geven.</span><span class="sxs-lookup"><span data-stu-id="11e1e-118">Click **View** -> **Command Palette**.</span></span>
3. <span data-ttu-id="11e1e-119">Selecteer **Q #: Project sjablonen installeren**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-119">Select **Q#: Install project templates**.</span></span>

<span data-ttu-id="11e1e-120">Wanneer de **geïnstalleerde project sjablonen** worden weer gegeven, is de QDK klaar voor gebruik met uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="11e1e-120">When **Project templates installed successfully** displays, the QDK is ready to use with your own applications and libraries.</span></span>

<span data-ttu-id="11e1e-121">Een nieuw project maken:</span><span class="sxs-lookup"><span data-stu-id="11e1e-121">To create a new project:</span></span>

1. <span data-ttu-id="11e1e-122">Klik **View**op  ->  **opdracht palet** weer geven en selecteer **Q #: nieuw project maken**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-122">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="11e1e-123">Klik op **zelfstandige console toepassing**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-123">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="11e1e-124">Ga naar de locatie waar u het project wilt opslaan en klik op **project maken**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-124">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="11e1e-125">Wanneer het project is gemaakt, klikt u op **Nieuw project openen...** in de rechter benedenhoek.</span><span class="sxs-lookup"><span data-stu-id="11e1e-125">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="11e1e-126">Inspecteer het project.</span><span class="sxs-lookup"><span data-stu-id="11e1e-126">Inspect the project.</span></span> <span data-ttu-id="11e1e-127">U ziet een bron bestand met de naam `Program.qs` , een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="11e1e-127">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="11e1e-128">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="11e1e-128">To run the application:</span></span>
1. <span data-ttu-id="11e1e-129">Klik op **Terminal**  ->  **New Terminal**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-129">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="11e1e-130">Voer op de terminal prompt in `dotnet run` .</span><span class="sxs-lookup"><span data-stu-id="11e1e-130">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="11e1e-131">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="11e1e-131">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="11e1e-132">Werk ruimten met meerdere hoofd mappen worden momenteel niet ondersteund door de extensie VS code Q #.</span><span class="sxs-lookup"><span data-stu-id="11e1e-132">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="11e1e-133">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="11e1e-133">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-q-using-visual-studio"></a><span data-ttu-id="11e1e-134">Ontwikkelen met Q # met behulp van Visual Studio</span><span class="sxs-lookup"><span data-stu-id="11e1e-134">Develop with Q# using Visual Studio</span></span>

<span data-ttu-id="11e1e-135">Controleer uw Visual Studio-installatie door een Q #-toepassing te maken `Hello World` .</span><span class="sxs-lookup"><span data-stu-id="11e1e-135">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="11e1e-136">Een nieuwe Q #-toepassing maken:</span><span class="sxs-lookup"><span data-stu-id="11e1e-136">To create a new Q# application:</span></span>
1. <span data-ttu-id="11e1e-137">Open Visual Studio en klik op **bestand**  ->  **Nieuw**  ->  **project**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-137">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="11e1e-138">Typ `Q#` in het zoekvak de optie **Q # toepassing** en klik op **volgende**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-138">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="11e1e-139">Voer een naam en locatie in voor uw toepassing en klik op **maken**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-139">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="11e1e-140">Inspecteer het project.</span><span class="sxs-lookup"><span data-stu-id="11e1e-140">Inspect the project.</span></span> <span data-ttu-id="11e1e-141">U ziet een bron bestand met de naam `Program.qs` , een Q #-programma dat een eenvoudige bewerking definieert om een bericht naar de-console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="11e1e-141">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="11e1e-142">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="11e1e-142">To run the application:</span></span>
1. <span data-ttu-id="11e1e-143">Selecteer **fout opsporing**  ->  **starten zonder fout opsporing**.</span><span class="sxs-lookup"><span data-stu-id="11e1e-143">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="11e1e-144">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="11e1e-144">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="11e1e-145">Als u meerdere projecten binnen één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="11e1e-145">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  


## <a name="next-steps"></a><span data-ttu-id="11e1e-146">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="11e1e-146">Next steps</span></span>

<span data-ttu-id="11e1e-147">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="11e1e-147">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
