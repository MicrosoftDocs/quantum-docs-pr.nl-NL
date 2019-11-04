---
title: Meer informatie over het installeren van de Microsoft Quantum development kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 3ec53934436b47908fd4d794a98933010f6059a7
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035281"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="127af-102">De Microsoft Quantum development kit (QDK) installeren</span><span class="sxs-lookup"><span data-stu-id="127af-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="127af-103">Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="127af-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="127af-104">De QDK bestaat uit:</span><span class="sxs-lookup"><span data-stu-id="127af-104">The QDK consists of:</span></span>

- <span data-ttu-id="127af-105">de programmeertaal Q#</span><span class="sxs-lookup"><span data-stu-id="127af-105">the Q# programming language</span></span>
- <span data-ttu-id="127af-106">een set bibliotheken voor abstractie van complexe functionaliteit in Q#</span><span class="sxs-lookup"><span data-stu-id="127af-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="127af-107">een hosttoepassing (geschreven in Python of een .NET-taal) voor het uitvoeren van kwantumbewerkingen die zijn geschreven in Q#</span><span class="sxs-lookup"><span data-stu-id="127af-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="127af-108">hulpprogramma's om het ontwikkelen te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="127af-108">tools to facilitate your development</span></span>

<span data-ttu-id="127af-109">De installatiestappen kunnen verschillen, afhankelijk van de gekozen ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="127af-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="127af-110">Kies uw omgeving in de secties hieronder.</span><span class="sxs-lookup"><span data-stu-id="127af-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="127af-111">Ontwikkelen met Python</span><span class="sxs-lookup"><span data-stu-id="127af-111">Develop with Python</span></span>

1. <span data-ttu-id="127af-112">Vereisten</span><span class="sxs-lookup"><span data-stu-id="127af-112">Pre-requisites</span></span>

    - <span data-ttu-id="127af-113">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="127af-113">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="127af-114">Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="127af-114">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="127af-115">.NET Core SDK 2.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="127af-115">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="127af-116">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="127af-116">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="127af-117">Installeer het pakket `qsharp`</span><span class="sxs-lookup"><span data-stu-id="127af-117">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="127af-118">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="127af-118">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="127af-119">Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en er de volgende code aan toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="127af-119">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - <span data-ttu-id="127af-120">Maak een Python-programma met de naam `hello_world.py` om de Q#-bewerking `SayHello()` aan te roepen:</span><span class="sxs-lookup"><span data-stu-id="127af-120">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="127af-121">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="127af-121">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="127af-122">Controleer de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="127af-122">Verify the output.</span></span> <span data-ttu-id="127af-123">Met het programma worden de volgende regels uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="127af-123">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="127af-124">Ontwikkelen met Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="127af-124">Develop with Jupyter notebooks</span></span>

1. <span data-ttu-id="127af-125">Vereisten</span><span class="sxs-lookup"><span data-stu-id="127af-125">Pre-requisites</span></span>

    - <span data-ttu-id="127af-126">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="127af-126">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="127af-127">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="127af-127">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="127af-128">.NET Core SDK 2.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="127af-128">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="127af-129">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="127af-129">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="127af-130">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="127af-130">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="127af-131">Voer de volgende opdracht uit om de Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="127af-131">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="127af-132">Blader naar de URL die wordt weergegeven op de opdrachtregel.</span><span class="sxs-lookup"><span data-stu-id="127af-132">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="127af-133">Bijvoorbeeld: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="127af-133">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="127af-134">Maak een Jupyter Notebook met een Q#-kernel en voeg de volgende code toe aan de eerste Notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="127af-134">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="127af-135">Voer deze cel van het Notebook uit:</span><span class="sxs-lookup"><span data-stu-id="127af-135">Run this cell of the notebook:</span></span>

        ![Jupyter Notebook-cel](~/media/install-guide-jupyter.png)

        <span data-ttu-id="127af-137">U ziet `SayHello` in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="127af-137">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="127af-138">Wanneer u werkt met Jupyter Notebook, wordt de Q#-code gecompileerd en wordt de naam van de gevonden bewerking(en) geretourneerd in de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="127af-138">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="127af-139">Ontwikkelen met C# in Windows, met behulp van Visual Studio</span><span class="sxs-lookup"><span data-stu-id="127af-139">Develop with C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="127af-140">Vereisten</span><span class="sxs-lookup"><span data-stu-id="127af-140">Pre-requisites</span></span>

    - <span data-ttu-id="127af-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="127af-141">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="127af-142">Installeer de Q# Visual Studio-extensie</span><span class="sxs-lookup"><span data-stu-id="127af-142">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="127af-143">Download de [Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="127af-143">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="127af-144">Voeg de extensie toe aan Visual Studio</span><span class="sxs-lookup"><span data-stu-id="127af-144">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="127af-145">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="127af-145">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="127af-146">Maak een nieuwe Q#-toepassing</span><span class="sxs-lookup"><span data-stu-id="127af-146">Create a new Q# application</span></span>

        - <span data-ttu-id="127af-147">Ga naar **Bestand** -> **Nieuw** -> **Project**</span><span class="sxs-lookup"><span data-stu-id="127af-147">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="127af-148">Typ `Q#` in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="127af-148">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="127af-149">Selecteer **Q#-toepassing**</span><span class="sxs-lookup"><span data-stu-id="127af-149">Select **Q# Application**</span></span>
        - <span data-ttu-id="127af-150">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="127af-150">Select **Next**</span></span>
        - <span data-ttu-id="127af-151">Kies een naam en een locatie voor uw toepassing</span><span class="sxs-lookup"><span data-stu-id="127af-151">Choose a name and location for your application</span></span>
        - <span data-ttu-id="127af-152">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="127af-152">Select **Create**</span></span>

    - <span data-ttu-id="127af-153">Controleer het project</span><span class="sxs-lookup"><span data-stu-id="127af-153">Inspect the project</span></span>

        <span data-ttu-id="127af-154">U ziet dat er twee bestanden zijn gemaakt: `Driver.cs`, de C#-hosttoepassing. en `Operation.qs`, een Q#-programma dat een eenvoudige bewerking definieert om een bericht naar de console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="127af-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="127af-155">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="127af-155">Run the application</span></span>

        - <span data-ttu-id="127af-156">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**</span><span class="sxs-lookup"><span data-stu-id="127af-156">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="127af-157">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="127af-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="127af-158">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="127af-158">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-vs-code"></a><span data-ttu-id="127af-159">Ontwikkelen met C#, met behulp van VS Code</span><span class="sxs-lookup"><span data-stu-id="127af-159">Develop with C#, using VS Code</span></span>

1. <span data-ttu-id="127af-160">Vereisten</span><span class="sxs-lookup"><span data-stu-id="127af-160">Pre-requisites</span></span>

   - [<span data-ttu-id="127af-161">VS-code</span><span class="sxs-lookup"><span data-stu-id="127af-161">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="127af-162">.NET Core SDK 2.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="127af-162">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="127af-163">Installeer de Quantum VS Code-extensie</span><span class="sxs-lookup"><span data-stu-id="127af-163">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="127af-164">Installeer de [VS Code-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span><span class="sxs-lookup"><span data-stu-id="127af-164">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="127af-165">Installeer de Quantum-projectsjablonen:</span><span class="sxs-lookup"><span data-stu-id="127af-165">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="127af-166">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="127af-166">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="127af-167">Selecteer **Q#: Projectsjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="127af-167">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="127af-168">De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="127af-168">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="127af-169">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="127af-169">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="127af-170">Maak een nieuw project:</span><span class="sxs-lookup"><span data-stu-id="127af-170">Create a new project:</span></span>

        - <span data-ttu-id="127af-171">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="127af-171">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="127af-172">Selecteer **Q#: Nieuw project maken**</span><span class="sxs-lookup"><span data-stu-id="127af-172">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="127af-173">Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken</span><span class="sxs-lookup"><span data-stu-id="127af-173">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="127af-174">Klik op de knop **Nieuw project openen...** zodra het project is gemaakt</span><span class="sxs-lookup"><span data-stu-id="127af-174">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="127af-175">Voer de toepassing uit:</span><span class="sxs-lookup"><span data-stu-id="127af-175">Run the application:</span></span>

        - <span data-ttu-id="127af-176">Ga naar **Fouten opsporen** -> **Starten zonder foutopsporing**</span><span class="sxs-lookup"><span data-stu-id="127af-176">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="127af-177">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="127af-177">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="127af-178">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie.</span><span class="sxs-lookup"><span data-stu-id="127af-178">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="127af-179">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="127af-179">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="127af-180">Ontwikkelen met C#, met behulp van het opdrachtregelprogramma `dotnet`</span><span class="sxs-lookup"><span data-stu-id="127af-180">Develop with C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="127af-181">Vereisten</span><span class="sxs-lookup"><span data-stu-id="127af-181">Pre-requisites</span></span>

    - [<span data-ttu-id="127af-182">.NET Core SDK 2.1 of hoger</span><span class="sxs-lookup"><span data-stu-id="127af-182">.NET Core SDK 2.1 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="127af-183">Installeer de Quantum-projectsjablonen voor .NET</span><span class="sxs-lookup"><span data-stu-id="127af-183">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="127af-184">De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="127af-184">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="127af-185">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="127af-185">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="127af-186">Een nieuwe toepassing maken</span><span class="sxs-lookup"><span data-stu-id="127af-186">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="127af-187">Navigeer naar de nieuwe toepassingsmap</span><span class="sxs-lookup"><span data-stu-id="127af-187">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="127af-188">U ziet dat er twee bestanden zijn gemaakt, samen met de projectbestanden van de toepassing: een Q#-bestand (`Operation.qs`) en een C#-hostbestand (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="127af-188">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="127af-189">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="127af-189">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="127af-190">U ziet de volgende uitvoer: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="127af-190">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="127af-191">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="127af-191">What's next?</span></span>

<span data-ttu-id="127af-192">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="127af-192">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
