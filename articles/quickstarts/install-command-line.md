---
title: Ontwikkelen met Q#-toepassingen
description: Meer informatie over hoe u een Q#-toepassing maakt die wordt uitgevoerd vanuit de opdrachtprompt.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 68f530d80e5c5f40dc2bcbb185879c3cb6f93f91
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834411"
---
# <a name="develop-with-no-locq-applications"></a><span data-ttu-id="3e2fd-103">Ontwikkelen met Q#-toepassingen</span><span class="sxs-lookup"><span data-stu-id="3e2fd-103">Develop with Q# applications</span></span>

<span data-ttu-id="3e2fd-104">Volg de instructies op het tabblad dat hoort bij de omgeving.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-104">Follow the instructions at the tab corresponding to your environment.</span></span>

<span data-ttu-id="3e2fd-105">Q#-programma's kunnen zonder stuurprogramma zelfstandig worden uitgevoerd in een hosttaal als C#, F# of Python.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-105">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3e2fd-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="3e2fd-106">Prerequisites</span></span>

- [<span data-ttu-id="3e2fd-107">.NET Core SDK 3.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="3e2fd-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="3e2fd-108">Installatie</span><span class="sxs-lookup"><span data-stu-id="3e2fd-108">Installation</span></span>

<span data-ttu-id="3e2fd-109">Hoewel u Q#-toepassingen in een IDE kunt maken, raden we u aan om Visual Studio Code (VS Code) of Visual Studio IDE te gebruiken als u uw Q#-toepassingen lokaal wilt ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="3e2fd-110">Als u uw toepassingen in de cloud wilt ontwikkelen via de webbrowser, raden we Visual Studio Codespaces aan.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="3e2fd-111">Ontwikkelen in deze omgevingen omvat de uitgebreide functies van de QDK-extensie, waaronder waarschuwingen, markeren van syntaxis, projectsjablonen, en meer.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-111">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="3e2fd-112">Ga als volgt te werk om VS Code te configureren:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-112">To configure VS Code:</span></span>

1. <span data-ttu-id="3e2fd-113">Download en installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).</span><span class="sxs-lookup"><span data-stu-id="3e2fd-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="3e2fd-114">Installeer de [Microsoft QDK voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="3e2fd-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="3e2fd-115">Ga als volgt te werk om Visual Studio te configureren:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-115">To configure Visual Studio:</span></span>

1. <span data-ttu-id="3e2fd-116">Download en installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 of hoger, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="3e2fd-117">Download en installeer de [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="3e2fd-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="3e2fd-118">Voor de configuratie van Visual Studio Codespaces gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-118">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="3e2fd-119">Maak een [Azure-account](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="3e2fd-119">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="3e2fd-120">Maak een Codespaces-omgeving.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-120">Create a Codespaces environment.</span></span> <span data-ttu-id="3e2fd-121">Volg de [quickstart-gids](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="3e2fd-121">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="3e2fd-122">We raden u aan om bij het maken van de Codespace `microsoft/Quantum` in te voeren in het veld Git-opslagplaats om QDK-specifieke instellingen te laden.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-122">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="3e2fd-123">Nu kunt u uw nieuwe omgeving starten en beginnen met ontwikkelen in de browser via de [VS Codespaces cloud-IDE](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="3e2fd-123">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="3e2fd-124">Het is ook mogelijk om uw lokale installatie van VS Code te gebruiken en Codespaces te gebruiken als een [externe omgeving](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="3e2fd-124">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="3e2fd-125">Als u de QDK wilt installeren in een andere omgeving, voert u het volgende bij de opdrachtprompt in:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-125">To install the QDK for another environment, enter the following at the command prompt:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a><span data-ttu-id="3e2fd-126">Ontwikkelen met Q#</span><span class="sxs-lookup"><span data-stu-id="3e2fd-126">Develop with Q#</span></span>

<span data-ttu-id="3e2fd-127">Volg de instructies op het tabblad dat hoort bij de omgeving.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-127">Follow the instructions on the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="3e2fd-128">VS-code</span><span class="sxs-lookup"><span data-stu-id="3e2fd-128">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="3e2fd-129">Ga als volgt te werk om een nieuw project te maken:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-129">To create a new project:</span></span>

1. <span data-ttu-id="3e2fd-130">Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-130">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="3e2fd-131">Klik op **Zelfstandige consoletoepassing**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-131">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="3e2fd-132">Ga naar de locatie waar het project moet worden opgeslagen en klik op **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-132">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="3e2fd-133">Klik rechtsonder op **Nieuw project openen...** als het project is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-133">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="3e2fd-134">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-134">Inspect the project.</span></span> <span data-ttu-id="3e2fd-135">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-135">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="3e2fd-136">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-136">To run the application:</span></span>

1. <span data-ttu-id="3e2fd-137">Klik op **Terminal** -> **Nieuwe terminal**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-137">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="3e2fd-138">Voer bij de terminalprompt `dotnet run` in.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-138">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="3e2fd-139">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="3e2fd-139">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="3e2fd-140">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de VS Code Q#-extensie.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-140">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="3e2fd-141">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-141">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="3e2fd-142">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3e2fd-142">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="3e2fd-143">Controleer uw Visual Studio-installatie door een Q# `Hello World`-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-143">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="3e2fd-144">Een nieuwe Q#-toepassing maken:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-144">To create a new Q# application:</span></span>

1. <span data-ttu-id="3e2fd-145">Open Visual Studio en klik op **Bestand** -> **Nieuw** -> **Project**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-145">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="3e2fd-146">Typ `Q#` in het zoekvak, selecteer **Q#-toepassing** en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-146">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="3e2fd-147">Geef een naam en een locatie op voor uw toepassing en klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-147">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="3e2fd-148">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-148">Inspect the project.</span></span> <span data-ttu-id="3e2fd-149">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-149">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="3e2fd-150">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-150">To run the application:</span></span>

1. <span data-ttu-id="3e2fd-151">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-151">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="3e2fd-152">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-152">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="3e2fd-153">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-153">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="3e2fd-154">Andere editors met de opdrachtprompt</span><span class="sxs-lookup"><span data-stu-id="3e2fd-154">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="3e2fd-155">Controleer de installatie door een Q# `Hello World`-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-155">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="3e2fd-156">Installeer de projectsjablonen.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-156">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="3e2fd-157">Een nieuwe toepassing maken:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-157">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="3e2fd-158">Navigeer naar de toepassingsmap:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-158">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="3e2fd-159">De map bevat nu een bestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-159">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="3e2fd-160">U kunt deze sjabloon wijzigen met een teksteditor en overschrijven met uw eigen kwantumtoepassingen.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-160">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="3e2fd-161">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="3e2fd-161">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="3e2fd-162">U ziet nu de volgende tekst: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="3e2fd-162">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="3e2fd-163">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="3e2fd-163">Next steps</span></span>

<span data-ttu-id="3e2fd-164">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="3e2fd-164">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
