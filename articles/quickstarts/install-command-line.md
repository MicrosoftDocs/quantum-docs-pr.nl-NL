---
title: Ontwikkelen met Q#-toepassingen in een IDE
description: Meer informatie over hoe u een Q#-toepassing maakt die wordt uitgevoerd vanuit de opdrachtprompt.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: quickstart
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 3e4f1e97477ecb0547b1586b1c7603c8a9954584
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844323"
---
# <a name="develop-with-no-locq-applications-in-an-ide"></a><span data-ttu-id="67628-103">Ontwikkelen met Q#-toepassingen in een IDE</span><span class="sxs-lookup"><span data-stu-id="67628-103">Develop with Q# applications in an IDE</span></span>

<span data-ttu-id="67628-104">Q#-programma's kunnen zonder stuurprogramma zelfstandig worden uitgevoerd in een hosttaal als C#, F# of Python.</span><span class="sxs-lookup"><span data-stu-id="67628-104">Q# programs can run on their own, without a driver in a host language like C#, F#, or Python.</span></span> <span data-ttu-id="67628-105">U kunt Q#-toepassingen ontwikkelen in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces of in andere editors/IDE's en toepassingen uitvoeren vanuit de .NET-console.</span><span class="sxs-lookup"><span data-stu-id="67628-105">You can develop Q# applications in Visual Studio Code (VS Code), Visual Studio, Visual Studio Codespaces, or with any editor/IDE and run applications from the .NET console.</span></span> 

## <a name="prerequisites-for-all-environments"></a><span data-ttu-id="67628-106">Vereisten voor alle omgevingen</span><span class="sxs-lookup"><span data-stu-id="67628-106">Prerequisites for all environments</span></span>

- [<span data-ttu-id="67628-107">.NET Core SDK 3.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="67628-107">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="67628-108">Installatie</span><span class="sxs-lookup"><span data-stu-id="67628-108">Installation</span></span>

<span data-ttu-id="67628-109">Hoewel u Q#-toepassingen in een IDE kunt maken, raden we u aan om Visual Studio Code (VS Code) of Visual Studio IDE te gebruiken als u uw Q#-toepassingen lokaal wilt ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="67628-109">While you can build Q# applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="67628-110">Als u uw toepassingen in de cloud wilt ontwikkelen via de webbrowser, raden we Visual Studio Codespaces aan.</span><span class="sxs-lookup"><span data-stu-id="67628-110">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="67628-111">Bij het ontwikkelen in deze omgevingen wordt gebruikgemaakt van de uitgebreide functies van de QDK-extensie, waaronder waarschuwingen, markeren van syntaxis, projectsjablonen, en meer.</span><span class="sxs-lookup"><span data-stu-id="67628-111">Developing in these environments leverages the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

### <a name="to-configure-for-vs-code"></a><span data-ttu-id="67628-112">Ga als volgt te werk om voor VS Code te configureren:</span><span class="sxs-lookup"><span data-stu-id="67628-112">To configure for VS Code:</span></span>

1. <span data-ttu-id="67628-113">Download en installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).</span><span class="sxs-lookup"><span data-stu-id="67628-113">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="67628-114">Installeer de [Microsoft QDK voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="67628-114">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

### <a name="to-configure-for-visual-studio"></a><span data-ttu-id="67628-115">Ga als volgt te werk om voor Visual Studio te configureren:</span><span class="sxs-lookup"><span data-stu-id="67628-115">To configure for Visual Studio:</span></span>

1. <span data-ttu-id="67628-116">Download en installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 of hoger, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="67628-116">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="67628-117">Download en installeer de [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="67628-117">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

### <a name="to-configure-for-another-environment"></a><span data-ttu-id="67628-118">Ga als volgt te werk als u voor een andere omgeving wilt configureren:</span><span class="sxs-lookup"><span data-stu-id="67628-118">To configure for another environment:</span></span> 

1. <span data-ttu-id="67628-119">Voer het volgende in de opdrachtprompt in</span><span class="sxs-lookup"><span data-stu-id="67628-119">Enter the following at the command prompt</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

### <a name="to-configure-for-visual-studio-codespaces"></a><span data-ttu-id="67628-120">Ga als volgt te werk als u voor Visual Studio Codespaces wilt configureren:</span><span class="sxs-lookup"><span data-stu-id="67628-120">To configure for Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="67628-121">Maak een [Azure-account](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="67628-121">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="67628-122">Maak een Codespaces-omgeving.</span><span class="sxs-lookup"><span data-stu-id="67628-122">Create a Codespaces environment.</span></span> <span data-ttu-id="67628-123">Volg de [quickstart-gids](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="67628-123">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/codespaces/quickstarts/browser).</span></span> <span data-ttu-id="67628-124">We raden u aan om bij het maken van de Codespace `microsoft/Quantum` in te voeren in het veld Git-opslagplaats om QDK-specifieke instellingen te laden.</span><span class="sxs-lookup"><span data-stu-id="67628-124">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="67628-125">Nu kunt u uw nieuwe omgeving starten en beginnen met ontwikkelen in de browser via de [VS Codespaces cloud-IDE](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="67628-125">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="67628-126">Het is ook mogelijk om uw lokale installatie van VS Code te gebruiken en Codespaces te gebruiken als een [externe omgeving](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="67628-126">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>

## <a name="develop-with-no-locq"></a><span data-ttu-id="67628-127">Ontwikkelen met Q#</span><span class="sxs-lookup"><span data-stu-id="67628-127">Develop with Q#</span></span>

<span data-ttu-id="67628-128">Volg de instructies op het tabblad dat hoort bij de ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="67628-128">Follow the instructions on the tab corresponding to your development environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="67628-129">VS-code</span><span class="sxs-lookup"><span data-stu-id="67628-129">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="67628-130">Ga als volgt te werk om een nieuw project te maken:</span><span class="sxs-lookup"><span data-stu-id="67628-130">To create a new project:</span></span>

1. <span data-ttu-id="67628-131">Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken**.</span><span class="sxs-lookup"><span data-stu-id="67628-131">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="67628-132">Klik op **Zelfstandige consoletoepassing**.</span><span class="sxs-lookup"><span data-stu-id="67628-132">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="67628-133">Navigeer naar de locatie om het project op te slaan.</span><span class="sxs-lookup"><span data-stu-id="67628-133">Navigate to the location to save the project.</span></span> <span data-ttu-id="67628-134">Voer de projectnaam in en klik op **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="67628-134">Enter the project name and click **Create Project**.</span></span>
4. <span data-ttu-id="67628-135">Klik rechtsonder op **Nieuw project openen...** als het project is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="67628-135">When the project is successfully created, click **Open new project...** in the lower right.</span></span>

<span data-ttu-id="67628-136">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="67628-136">Inspect the project.</span></span> <span data-ttu-id="67628-137">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="67628-137">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="67628-138">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="67628-138">To run the application:</span></span>

1. <span data-ttu-id="67628-139">Klik op **Terminal** -> **Nieuwe terminal**.</span><span class="sxs-lookup"><span data-stu-id="67628-139">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="67628-140">Voer bij de terminalprompt `dotnet run` in.</span><span class="sxs-lookup"><span data-stu-id="67628-140">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="67628-141">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="67628-141">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> <span data-ttu-id="67628-142">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de VS Code Q#-extensie.</span><span class="sxs-lookup"><span data-stu-id="67628-142">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="67628-143">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="67628-143">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="67628-144">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="67628-144">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="67628-145">Controleer uw Visual Studio-installatie door een Q# `Hello World`-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="67628-145">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="67628-146">Een nieuwe Q#-toepassing maken:</span><span class="sxs-lookup"><span data-stu-id="67628-146">To create a new Q# application:</span></span>

1. <span data-ttu-id="67628-147">Open Visual Studio en klik op **Bestand** -> **Nieuw** -> **Project**.</span><span class="sxs-lookup"><span data-stu-id="67628-147">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="67628-148">Typ `Q#` in het zoekvak, selecteer **Q#-toepassing** en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="67628-148">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="67628-149">Geef een naam en een locatie op voor uw toepassing en klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="67628-149">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="67628-150">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="67628-150">Inspect the project.</span></span> <span data-ttu-id="67628-151">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="67628-151">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="67628-152">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="67628-152">To run the application:</span></span>

1. <span data-ttu-id="67628-153">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**.</span><span class="sxs-lookup"><span data-stu-id="67628-153">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="67628-154">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="67628-154">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="67628-155">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="67628-155">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-prompt"></a>[<span data-ttu-id="67628-156">Andere editors met de opdrachtprompt</span><span class="sxs-lookup"><span data-stu-id="67628-156">Other editors with the command prompt</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="67628-157">Controleer de installatie door een Q# `Hello World`-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="67628-157">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="67628-158">Een nieuwe toepassing maken:</span><span class="sxs-lookup"><span data-stu-id="67628-158">Create a new application:</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="67628-159">Navigeer naar de toepassingsmap:</span><span class="sxs-lookup"><span data-stu-id="67628-159">Navigate to the application directory:</span></span>

    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="67628-160">De map bevat nu een bestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="67628-160">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="67628-161">U kunt deze sjabloon wijzigen met een teksteditor en overschrijven met uw eigen kwantumtoepassingen.</span><span class="sxs-lookup"><span data-stu-id="67628-161">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="67628-162">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="67628-162">Run the program:</span></span>

    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="67628-163">U ziet nu de volgende tekst: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="67628-163">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="67628-164">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="67628-164">Next steps</span></span>

<span data-ttu-id="67628-165">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="67628-165">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
