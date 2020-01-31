---
title: 'Ontwikkelen met Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 1fd829c684502092bb7491b0f46b5f690320c941
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831015"
---
# <a name="develop-with-q--c"></a><span data-ttu-id="a1df9-102">Ontwikkelen met Q # +C#</span><span class="sxs-lookup"><span data-stu-id="a1df9-102">Develop with Q# + C#</span></span>

<span data-ttu-id="a1df9-103">Installeer de QDK voor het C# ontwikkelen van host-Program Ma's om Q #-bewerkingen aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="a1df9-103">Install the QDK to develop C# host programs to call Q# operations.</span></span>

<span data-ttu-id="a1df9-104">Q # is gebouwd om goed te kunnen spelen met .NET-talen C#, met name.</span><span class="sxs-lookup"><span data-stu-id="a1df9-104">Q# is built to play well with .NET languages--specifically C#.</span></span> <span data-ttu-id="a1df9-105">U kunt in verschillende ontwikkel omgevingen met deze koppeling werken:</span><span class="sxs-lookup"><span data-stu-id="a1df9-105">You can work with this pairing inside different development environments:</span></span>

- [<span data-ttu-id="a1df9-106">Q # + C# met Visual Studio (Windows)</span><span class="sxs-lookup"><span data-stu-id="a1df9-106">Q# + C# using Visual Studio (Windows)</span></span>](#VS)
- [<span data-ttu-id="a1df9-107">Q # + C# met Visual Studio code (Windows, Linux en Mac)</span><span class="sxs-lookup"><span data-stu-id="a1df9-107">Q# + C# using Visual Studio Code (Windows, Linux and Mac)</span></span>](#VSC)
- [<span data-ttu-id="a1df9-108">Q # + C# met behulp van het `dotnet` opdracht regel programma</span><span class="sxs-lookup"><span data-stu-id="a1df9-108">Q# + C# using the `dotnet` command-line tool</span></span>](#command)

## <span data-ttu-id="a1df9-109">Ontwikkelen met Q # + C# met Visual Studio<a name="VS"></a></span><span class="sxs-lookup"><span data-stu-id="a1df9-109">Develop with Q# + C# using Visual Studio <a name="VS"></a></span></span>

<span data-ttu-id="a1df9-110">Visual Studio biedt een uitgebreide omgeving voor het ontwikkelen van Q #-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="a1df9-110">Visual Studio offers a rich environment for developing Q# programs.</span></span> <span data-ttu-id="a1df9-111">De Q # Visual Studio-extensie bevat sjablonen voor Q # bestanden en projecten, evenals syntaxis markeringen, het volt ooien van code en IntelliSense-ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="a1df9-111">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting, code completion and IntelliSense support.</span></span>


1. <span data-ttu-id="a1df9-112">Vereisten</span><span class="sxs-lookup"><span data-stu-id="a1df9-112">Pre-requisites</span></span>

    - <span data-ttu-id="a1df9-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="a1df9-113">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="a1df9-114">Installeer de Q# Visual Studio-extensie</span><span class="sxs-lookup"><span data-stu-id="a1df9-114">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="a1df9-115">Down load en installeer de [Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="a1df9-115">Download and install the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>

1. <span data-ttu-id="a1df9-116">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="a1df9-116">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="a1df9-117">Maak een nieuwe Q#-toepassing</span><span class="sxs-lookup"><span data-stu-id="a1df9-117">Create a new Q# application</span></span>

        - <span data-ttu-id="a1df9-118">Ga naar **Bestand** -> **Nieuw** -> **Project**</span><span class="sxs-lookup"><span data-stu-id="a1df9-118">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="a1df9-119">Typ `Q#` in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="a1df9-119">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="a1df9-120">Selecteer **Q#-toepassing**</span><span class="sxs-lookup"><span data-stu-id="a1df9-120">Select **Q# Application**</span></span>
        - <span data-ttu-id="a1df9-121">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="a1df9-121">Select **Next**</span></span>
        - <span data-ttu-id="a1df9-122">Kies een naam en een locatie voor uw toepassing</span><span class="sxs-lookup"><span data-stu-id="a1df9-122">Choose a name and location for your application</span></span>
        - <span data-ttu-id="a1df9-123">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="a1df9-123">Select **Create**</span></span>

    - <span data-ttu-id="a1df9-124">Controleer het project</span><span class="sxs-lookup"><span data-stu-id="a1df9-124">Inspect the project</span></span>

        <span data-ttu-id="a1df9-125">U ziet dat er twee bestanden zijn gemaakt: `Driver.cs`, de C#-hosttoepassing. en `Operation.qs`, een Q#-programma dat een eenvoudige bewerking definieert om een bericht naar de console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="a1df9-125">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="a1df9-126">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="a1df9-126">Run the application</span></span>

        - <span data-ttu-id="a1df9-127">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**</span><span class="sxs-lookup"><span data-stu-id="a1df9-127">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="a1df9-128">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="a1df9-128">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="a1df9-129">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="a1df9-129">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <span data-ttu-id="a1df9-130">Ontwikkelen met Q # + C# met Visual Studio code<a name="VSC"></a></span><span class="sxs-lookup"><span data-stu-id="a1df9-130">Develop with Q# + C# using Visual Studio Code <a name="VSC"></a></span></span>

<span data-ttu-id="a1df9-131">Visual Studio code (VS code) biedt een uitgebreide omgeving voor het ontwikkelen van Q #-Program ma's in Windows, Linux en Mac.</span><span class="sxs-lookup"><span data-stu-id="a1df9-131">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs on Windows, Linux and Mac.</span></span>  <span data-ttu-id="a1df9-132">De code-uitbrei ding Q # versus bevat ondersteuning voor Q #-syntaxis markering, code voltooiing en Q #-code fragmenten.</span><span class="sxs-lookup"><span data-stu-id="a1df9-132">The Q# VS Code extension includes support for Q# syntax highlighting, code completion, and Q# code snippets.</span></span>

1. <span data-ttu-id="a1df9-133">Vereisten</span><span class="sxs-lookup"><span data-stu-id="a1df9-133">Pre-requisites</span></span>

   - [<span data-ttu-id="a1df9-134">VS-code</span><span class="sxs-lookup"><span data-stu-id="a1df9-134">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="a1df9-135">.NET Core SDK 3,1 of hoger</span><span class="sxs-lookup"><span data-stu-id="a1df9-135">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="a1df9-136">Installeer de Quantum VS Code-extensie</span><span class="sxs-lookup"><span data-stu-id="a1df9-136">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="a1df9-137">Installeer de [VS Code-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span><span class="sxs-lookup"><span data-stu-id="a1df9-137">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="a1df9-138">Installeer de Quantum-projectsjablonen:</span><span class="sxs-lookup"><span data-stu-id="a1df9-138">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="a1df9-139">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="a1df9-139">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="a1df9-140">Selecteer **Q #: Project sjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="a1df9-140">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="a1df9-141">De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="a1df9-141">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="a1df9-142">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="a1df9-142">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="a1df9-143">Maak een nieuw project:</span><span class="sxs-lookup"><span data-stu-id="a1df9-143">Create a new project:</span></span>

        - <span data-ttu-id="a1df9-144">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="a1df9-144">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="a1df9-145">Selecteer **Q #: nieuw project maken**</span><span class="sxs-lookup"><span data-stu-id="a1df9-145">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="a1df9-146">**Zelfstandige console toepassing** selecteren</span><span class="sxs-lookup"><span data-stu-id="a1df9-146">Select **Standalone console application**</span></span>
        - <span data-ttu-id="a1df9-147">Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken</span><span class="sxs-lookup"><span data-stu-id="a1df9-147">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="a1df9-148">Klik op de knop **Nieuw project openen...** zodra het project is gemaakt</span><span class="sxs-lookup"><span data-stu-id="a1df9-148">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="a1df9-149">Als u de C# uitbrei ding voor VS-code nog niet hebt geïnstalleerd, wordt er een pop-upvenster weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="a1df9-149">If you don't already have the C# extension for VS Code installed, a pop-up will appear.</span></span> <span data-ttu-id="a1df9-150">Installeer de extensie.</span><span class="sxs-lookup"><span data-stu-id="a1df9-150">Install the extension.</span></span> 

    - <span data-ttu-id="a1df9-151">Voer de toepassing uit:</span><span class="sxs-lookup"><span data-stu-id="a1df9-151">Run the application:</span></span>

        - <span data-ttu-id="a1df9-152">Ga naar **terminal** -> **nieuwe terminal**</span><span class="sxs-lookup"><span data-stu-id="a1df9-152">Go to **Terminal** -> **New Terminal**</span></span>
        - <span data-ttu-id="a1df9-153">Voer `dotnet run` in</span><span class="sxs-lookup"><span data-stu-id="a1df9-153">Enter `dotnet run`</span></span>
        - <span data-ttu-id="a1df9-154">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="a1df9-154">You should see the following text in the output window `Hello quantum world!`</span></span>


> [!NOTE]
> * <span data-ttu-id="a1df9-155">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie.</span><span class="sxs-lookup"><span data-stu-id="a1df9-155">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="a1df9-156">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="a1df9-156">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <span data-ttu-id="a1df9-157">Ontwikkelen met Q # + C# met behulp van het opdracht regel programma `dotnet`<a name="command"></a></span><span class="sxs-lookup"><span data-stu-id="a1df9-157">Develop with Q# + C# using the `dotnet` command-line tool <a name="command"></a></span></span>

<span data-ttu-id="a1df9-158">Natuurlijk kunt u ook Q#-programma's schrijven en uitvoeren vanaf de opdrachtregel. U hoeft hiervoor alleen de .NET Core SDK en de QDK-projectsjablonen te installeren.</span><span class="sxs-lookup"><span data-stu-id="a1df9-158">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="a1df9-159">Vereisten</span><span class="sxs-lookup"><span data-stu-id="a1df9-159">Pre-requisites</span></span>

    - [<span data-ttu-id="a1df9-160">.NET Core SDK 3,1 of hoger</span><span class="sxs-lookup"><span data-stu-id="a1df9-160">.NET Core SDK 3.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="a1df9-161">Installeer de Quantum-projectsjablonen voor .NET</span><span class="sxs-lookup"><span data-stu-id="a1df9-161">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="a1df9-162">De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="a1df9-162">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="a1df9-163">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="a1df9-163">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="a1df9-164">Een nieuwe toepassing maken</span><span class="sxs-lookup"><span data-stu-id="a1df9-164">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="a1df9-165">Navigeer naar de nieuwe toepassingsmap</span><span class="sxs-lookup"><span data-stu-id="a1df9-165">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="a1df9-166">U ziet dat er twee bestanden zijn gemaakt, samen met de projectbestanden van de toepassing: een Q#-bestand (`Operation.qs`) en een C#-hostbestand (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="a1df9-166">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="a1df9-167">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="a1df9-167">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="a1df9-168">U ziet de volgende uitvoer: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="a1df9-168">You should see the following output: `Hello quantum world!`</span></span>

    
## <a name="whats-next"></a><span data-ttu-id="a1df9-169">En verder?</span><span class="sxs-lookup"><span data-stu-id="a1df9-169">What's next?</span></span>

<span data-ttu-id="a1df9-170">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a1df9-170">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
