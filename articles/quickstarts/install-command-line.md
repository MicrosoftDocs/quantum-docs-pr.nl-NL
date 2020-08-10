---
title: Ontwikkelen met Q#-opdrachtregeltoepassingen
author: KittyYeungQ
ms.author: kitty
ms.date: 4/24/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.standalone
no-loc:
- Q#
- $$v
ms.openlocfilehash: 630dc7b8acf2dd8f258eb27dfbc367b812cd1c19
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87867604"
---
# <a name="develop-with-no-locq-command-line-applications"></a><span data-ttu-id="729b1-102">Ontwikkelen met Q#-opdrachtregeltoepassingen</span><span class="sxs-lookup"><span data-stu-id="729b1-102">Develop with Q# command line applications</span></span>

<span data-ttu-id="729b1-103">Q#-programma's kunnen zonder stuurprogramma zelfstandig worden uitgevoerd in een hosttaal als C#, F# of Python.</span><span class="sxs-lookup"><span data-stu-id="729b1-103">Q# programs can be executed on their own, without a driver in a host language like C#, F#, or Python.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="729b1-104">Vereisten</span><span class="sxs-lookup"><span data-stu-id="729b1-104">Prerequisites</span></span>

- [<span data-ttu-id="729b1-105">.NET Core SDK 3.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="729b1-105">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

## <a name="installation"></a><span data-ttu-id="729b1-106">Installatie</span><span class="sxs-lookup"><span data-stu-id="729b1-106">Installation</span></span>

<span data-ttu-id="729b1-107">Hoewel u Q#-opdrachtregeltoepassingen in een IDE kunt maken, raden we u aan om Visual Studio Code (VS Code) of Visual Studio IDE te gebruiken als u uw Q#-toepassingen lokaal wilt ontwikkelen.</span><span class="sxs-lookup"><span data-stu-id="729b1-107">While you can build Q# command line applications in any IDE, we recommend using Visual Studio Code (VS Code) or Visual Studio IDE for developing your Q# applications locally.</span></span> <span data-ttu-id="729b1-108">Als u uw toepassingen in de cloud wilt ontwikkelen via de webbrowser, raden we Visual Studio Codespaces aan.</span><span class="sxs-lookup"><span data-stu-id="729b1-108">For developing in the Cloud via the web browser, we recommend Visual Studio Codespaces.</span></span> <span data-ttu-id="729b1-109">Ontwikkelen in deze omgevingen omvat de uitgebreide functies van de QDK-extensie, waaronder waarschuwingen, markeren van syntaxis, projectsjablonen, en meer.</span><span class="sxs-lookup"><span data-stu-id="729b1-109">Developing in these environments includes the rich functionality of the QDK extension, which includes warnings, syntax highlighting, project templates, and more.</span></span> 

<span data-ttu-id="729b1-110">Ga als volgt te werk om VS Code te configureren:</span><span class="sxs-lookup"><span data-stu-id="729b1-110">To configure VS Code:</span></span>

1. <span data-ttu-id="729b1-111">Download en installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).</span><span class="sxs-lookup"><span data-stu-id="729b1-111">Download and install [VS Code](https://code.visualstudio.com/download) (Windows, Linux and Mac).</span></span>
2. <span data-ttu-id="729b1-112">Installeer de [Microsoft QDK voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span><span class="sxs-lookup"><span data-stu-id="729b1-112">Install the [Microsoft QDK for VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).</span></span>

<span data-ttu-id="729b1-113">Ga als volgt te werk om Visual Studio te configureren:</span><span class="sxs-lookup"><span data-stu-id="729b1-113">To configure Visual Studio:</span></span>

1. <span data-ttu-id="729b1-114">Download en installeer [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 of hoger, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="729b1-114">Download and install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3 or greater, with the .NET Core cross-platform development workload enabled.</span></span>
2. <span data-ttu-id="729b1-115">Download en installeer de [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span><span class="sxs-lookup"><span data-stu-id="729b1-115">Download and install the [Microsoft QDK](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit).</span></span>

<span data-ttu-id="729b1-116">Voor de configuratie van Visual Studio Codespaces gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="729b1-116">To configure Visual Studio Codespaces:</span></span>

1. <span data-ttu-id="729b1-117">Maak een [Azure-account](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="729b1-117">Create an [Azure account](https://azure.microsoft.com/free/).</span></span>
2. <span data-ttu-id="729b1-118">Maak een Codespaces-omgeving.</span><span class="sxs-lookup"><span data-stu-id="729b1-118">Create a Codespaces environment.</span></span> <span data-ttu-id="729b1-119">Volg de [quickstart-gids](https://docs.microsoft.com/visualstudio/online/quickstarts/browser).</span><span class="sxs-lookup"><span data-stu-id="729b1-119">Please follow the [quickstart guide](https://docs.microsoft.com/visualstudio/online/quickstarts/browser).</span></span> <span data-ttu-id="729b1-120">We raden u aan om bij het maken van de Codespace `microsoft/Quantum` in te voeren in het veld Git-opslagplaats om QDK-specifieke instellingen te laden.</span><span class="sxs-lookup"><span data-stu-id="729b1-120">When creating the Codespace, we recommend to enter `microsoft/Quantum` in the "Git Repository" field to load QDK-specific settings.</span></span>
3. <span data-ttu-id="729b1-121">Nu kunt u uw nieuwe omgeving starten en beginnen met ontwikkelen in de browser via de [VS Codespaces cloud-IDE](https://online.visualstudio.com/environments).</span><span class="sxs-lookup"><span data-stu-id="729b1-121">You can now launch your new environment and start developing in the browser via the [VS Codespaces Cloud IDE](https://online.visualstudio.com/environments).</span></span> <span data-ttu-id="729b1-122">Het is ook mogelijk om uw lokale installatie van VS Code te gebruiken en Codespaces te gebruiken als een [externe omgeving](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span><span class="sxs-lookup"><span data-stu-id="729b1-122">Alternatively, it is possible to use your local installation of VS Code and use Codespaces as a [remote environment](https://docs.microsoft.com/visualstudio/online/how-to/vscode).</span></span>


<span data-ttu-id="729b1-123">Als u de QDK wilt installeren in een andere omgeving, voert u het volgende in de opdrachtregel in:</span><span class="sxs-lookup"><span data-stu-id="729b1-123">To install the QDK for another environment, enter in the command line:</span></span>

```dotnetcli
dotnet new -i Microsoft.Quantum.ProjectTemplates
```

## <a name="develop-with-no-locq"></a><span data-ttu-id="729b1-124">Ontwikkelen met Q#</span><span class="sxs-lookup"><span data-stu-id="729b1-124">Develop with Q#</span></span>

<span data-ttu-id="729b1-125">Volg de instructies op het tabblad dat hoort bij de omgeving.</span><span class="sxs-lookup"><span data-stu-id="729b1-125">Follow the instructions at the tab corresponding to your environment.</span></span>

### <a name="vs-code"></a>[<span data-ttu-id="729b1-126">VS-code</span><span class="sxs-lookup"><span data-stu-id="729b1-126">VS Code</span></span>](#tab/tabid-vscode)

<span data-ttu-id="729b1-127">Ga als volgt te werk om een nieuw project te maken:</span><span class="sxs-lookup"><span data-stu-id="729b1-127">To create a new project:</span></span>

1. <span data-ttu-id="729b1-128">Klik op **Weergave** -> **Opdrachtpallet** en selecteer **Q#: Nieuw project maken**.</span><span class="sxs-lookup"><span data-stu-id="729b1-128">Click **View** -> **Command Palette** and select **Q#: Create New Project**.</span></span>
2. <span data-ttu-id="729b1-129">Klik op **Zelfstandige consoletoepassing**.</span><span class="sxs-lookup"><span data-stu-id="729b1-129">Click **Standalone console application**.</span></span>
3. <span data-ttu-id="729b1-130">Ga naar de locatie waar het project moet worden opgeslagen en klik op **Project maken**.</span><span class="sxs-lookup"><span data-stu-id="729b1-130">Navigate to the location to save the project and click **Create Project**.</span></span>
4. <span data-ttu-id="729b1-131">Klik rechtsonder op **Nieuw project openen...** als het project is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="729b1-131">When the project is successfully created, click **Open new project...** in the lower right.</span></span>
        
<span data-ttu-id="729b1-132">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="729b1-132">Inspect the project.</span></span> <span data-ttu-id="729b1-133">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="729b1-133">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="729b1-134">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="729b1-134">To run the application:</span></span>
1. <span data-ttu-id="729b1-135">Klik op **Terminal** -> **Nieuwe terminal**.</span><span class="sxs-lookup"><span data-stu-id="729b1-135">Click **Terminal** -> **New Terminal**.</span></span>
2. <span data-ttu-id="729b1-136">Voer bij de terminalprompt `dotnet run` in.</span><span class="sxs-lookup"><span data-stu-id="729b1-136">At the terminal prompt, enter `dotnet run`.</span></span>
3. <span data-ttu-id="729b1-137">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="729b1-137">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> <span data-ttu-id="729b1-138">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de VS Code Q#-extensie.</span><span class="sxs-lookup"><span data-stu-id="729b1-138">Workspaces with multiple root folders are not currently supported by the VS Code Q# extension.</span></span> <span data-ttu-id="729b1-139">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="729b1-139">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

### <a name="visual-studio"></a>[<span data-ttu-id="729b1-140">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="729b1-140">Visual Studio</span></span>](#tab/tabid-vs)

<span data-ttu-id="729b1-141">Controleer uw Visual Studio-installatie door een Q# `Hello World`-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="729b1-141">Verify your Visual Studio installation by creating a Q# `Hello World` application.</span></span>

<span data-ttu-id="729b1-142">Een nieuwe Q#-toepassing maken:</span><span class="sxs-lookup"><span data-stu-id="729b1-142">To create a new Q# application:</span></span>
1. <span data-ttu-id="729b1-143">Open Visual Studio en klik op **Bestand** -> **Nieuw** -> **Project**.</span><span class="sxs-lookup"><span data-stu-id="729b1-143">Open Visual Studio and click **File** -> **New** -> **Project**.</span></span>
2. <span data-ttu-id="729b1-144">Typ `Q#` in het zoekvak, selecteer **Q#-toepassing** en klik op **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="729b1-144">Type `Q#` in the search box, select **Q# Application** and click **Next**.</span></span>
3. <span data-ttu-id="729b1-145">Geef een naam en een locatie op voor uw toepassing en klik op **Maken**.</span><span class="sxs-lookup"><span data-stu-id="729b1-145">Enter a name and location for your application and click **Create**.</span></span>


<span data-ttu-id="729b1-146">Controleer het project.</span><span class="sxs-lookup"><span data-stu-id="729b1-146">Inspect the project.</span></span> <span data-ttu-id="729b1-147">Als het goed is, ziet u een bronbestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="729b1-147">You should see a source file named `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

<span data-ttu-id="729b1-148">De toepassing uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="729b1-148">To run the application:</span></span>
1. <span data-ttu-id="729b1-149">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**.</span><span class="sxs-lookup"><span data-stu-id="729b1-149">Select **Debug** -> **Start Without Debugging**.</span></span>
2. <span data-ttu-id="729b1-150">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="729b1-150">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> <span data-ttu-id="729b1-151">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="729b1-151">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its sub-folders.</span></span>  

### <a name="other-editors-with-the-command-line"></a>[<span data-ttu-id="729b1-152">Andere editors met de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="729b1-152">Other editors with the command line</span></span>](#tab/tabid-cmdline)

<span data-ttu-id="729b1-153">Controleer de installatie door een Q# `Hello World`-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="729b1-153">Verify your installation by creating a Q# `Hello World` application.</span></span>

1. <span data-ttu-id="729b1-154">Installeer de projectsjablonen.</span><span class="sxs-lookup"><span data-stu-id="729b1-154">Install the project templates.</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="729b1-155">Een nieuwe toepassing maken:</span><span class="sxs-lookup"><span data-stu-id="729b1-155">Create a new application:</span></span>
    ```dotnetcli
    dotnet new console -lang Q# -o runSayHello
    ```

1. <span data-ttu-id="729b1-156">Navigeer naar de toepassingsmap:</span><span class="sxs-lookup"><span data-stu-id="729b1-156">Navigate to the application directory:</span></span>
    ```dotnetcli
    cd runSayHello
    ```

    <span data-ttu-id="729b1-157">De map bevat nu een bestand met de naam `Program.qs`. Dit is een Q#-programma dat een eenvoudige bewerking definieert waarmee een bericht in de console wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="729b1-157">This directory should now contain a file `Program.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span> <span data-ttu-id="729b1-158">U kunt deze sjabloon wijzigen met een teksteditor en overschrijven met uw eigen kwantumtoepassingen.</span><span class="sxs-lookup"><span data-stu-id="729b1-158">You can modfiy this template with a text editor and overwrite it with your own quantum applications.</span></span> 

1. <span data-ttu-id="729b1-159">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="729b1-159">Run the program:</span></span>
    ```dotnetcli
    dotnet run
    ```

1. <span data-ttu-id="729b1-160">U ziet nu de volgende tekst: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="729b1-160">You should see the following text printed: `Hello quantum world!`</span></span>

***

## <a name="next-steps"></a><span data-ttu-id="729b1-161">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="729b1-161">Next steps</span></span>

<span data-ttu-id="729b1-162">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="729b1-162">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.quickstarts.qrng).</span></span>
