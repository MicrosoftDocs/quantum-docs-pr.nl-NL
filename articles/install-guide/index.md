---
title: Meer informatie over het installeren van de Microsoft Quantum development kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2a098d89f13278d7137bf182a184a74afb9393be
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462867"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="ad362-102">De Microsoft Quantum development kit (QDK) installeren</span><span class="sxs-lookup"><span data-stu-id="ad362-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="ad362-103">Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="ad362-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="ad362-104">De QDK bestaat uit:</span><span class="sxs-lookup"><span data-stu-id="ad362-104">The QDK consists of:</span></span>

- <span data-ttu-id="ad362-105">de programmeertaal Q#</span><span class="sxs-lookup"><span data-stu-id="ad362-105">the Q# programming language</span></span>
- <span data-ttu-id="ad362-106">een set bibliotheken voor abstractie van complexe functionaliteit in Q#</span><span class="sxs-lookup"><span data-stu-id="ad362-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="ad362-107">een hosttoepassing (geschreven in Python of een .NET-taal) voor het uitvoeren van kwantumbewerkingen die zijn geschreven in Q#</span><span class="sxs-lookup"><span data-stu-id="ad362-107">a host application (written in Python or a .NET language) that runs quantum operations written in Q#</span></span>
- <span data-ttu-id="ad362-108">hulpprogramma's om het ontwikkelen te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="ad362-108">tools to facilitate your development</span></span>

<span data-ttu-id="ad362-109">De installatiestappen kunnen verschillen, afhankelijk van de gekozen ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="ad362-109">Depending on your chosen development environment, there are different installation steps.</span></span> <span data-ttu-id="ad362-110">Kies uw omgeving in de secties hieronder.</span><span class="sxs-lookup"><span data-stu-id="ad362-110">Choose your environment from the sections below.</span></span>

## <a name="develop-with-python"></a><span data-ttu-id="ad362-111">Ontwikkelen met Python</span><span class="sxs-lookup"><span data-stu-id="ad362-111">Develop with Python</span></span>

<span data-ttu-id="ad362-112">Met het qsharp-pakket voor Python simuleert u eenvoudig Q#-bewerkingen en -functies vanuit Python.</span><span class="sxs-lookup"><span data-stu-id="ad362-112">The qsharp package for Python makes it easy to simulate Q# operations and functions from within Python.</span></span> <span data-ttu-id="ad362-113">IQ# (spreek uit als 'i-q-sharp') is een extensie die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ad362-113">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python that provides the core functionality for compiling and simulating Q# operations.</span></span>

1. <span data-ttu-id="ad362-114">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ad362-114">Pre-requisites</span></span>

    - <span data-ttu-id="ad362-115">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="ad362-115">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - <span data-ttu-id="ad362-116">Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)</span><span class="sxs-lookup"><span data-stu-id="ad362-116">The [PIP](https://pip.pypa.io/en/stable/installing) Python package manager</span></span>
    - [<span data-ttu-id="ad362-117">.NET Core SDK 3.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="ad362-117">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="ad362-118">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="ad362-118">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="ad362-119">Installeer het pakket `qsharp`</span><span class="sxs-lookup"><span data-stu-id="ad362-119">Install the `qsharp` package</span></span>

    ```bash
    pip install qsharp
    ```

1. <span data-ttu-id="ad362-120">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="ad362-120">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ad362-121">Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en er de volgende code aan toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="ad362-121">Create a minimal Q# operation, by creating a file called `Operation.qs`, and adding the following code to it:</span></span>

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

    - <span data-ttu-id="ad362-122">Maak een Python-programma met de naam `hello_world.py` om de Q#-bewerking `SayHello()` aan te roepen:</span><span class="sxs-lookup"><span data-stu-id="ad362-122">Create a Python program called `hello_world.py` to call the Q# `SayHello()` operation:</span></span>

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - <span data-ttu-id="ad362-123">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="ad362-123">Run the program:</span></span>

        ```bash
        python hello_world.py
        ```

    - <span data-ttu-id="ad362-124">Controleer de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ad362-124">Verify the output.</span></span> <span data-ttu-id="ad362-125">Met het programma worden de volgende regels uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="ad362-125">Your program should output the following lines:</span></span>

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a><span data-ttu-id="ad362-126">Ontwikkelen met Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="ad362-126">Develop with Jupyter notebooks</span></span>

<span data-ttu-id="ad362-127">Jupyter-notebooks worden veel gebruikt binnen academische instellingen, in wetenschappelijke laboratoria en voor gezamenlijk programmeerprojecten online. Met een Jupyter-notebook kunt u direct code uitvoeren, waaronder nu ook Q#-code, en gebruikmaken van instructies, notities en andere inhoud.</span><span class="sxs-lookup"><span data-stu-id="ad362-127">A favorite of academic settings, scientific labs, and online-based collaborative programming, Jupyter Notebooks offer in-place code execution—now including Q# code—along with instructions, notes, and other content.</span></span>  <span data-ttu-id="ad362-128">Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.</span><span class="sxs-lookup"><span data-stu-id="ad362-128">Here's what you need to do to start creating your own Q# notebooks.</span></span>

<span data-ttu-id="ad362-129">IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ad362-129">IQ# (pronounced i-q-sharp) is an extension primarily used by Jupyter and Python to the .NET Core SDK that provides the core functionality for compiling and simulating Q# operations.</span></span>


1. <span data-ttu-id="ad362-130">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ad362-130">Pre-requisites</span></span>

    - <span data-ttu-id="ad362-131">[Python](https://www.python.org/downloads/) 3.6 of hoger</span><span class="sxs-lookup"><span data-stu-id="ad362-131">[Python](https://www.python.org/downloads/) 3.6 or later</span></span>
    - [<span data-ttu-id="ad362-132">Jupyter Notebook</span><span class="sxs-lookup"><span data-stu-id="ad362-132">Jupyter Notebook</span></span>](https://jupyter.readthedocs.io/en/latest/install.html)
    - [<span data-ttu-id="ad362-133">.NET Core SDK 3.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="ad362-133">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="ad362-134">Installeer het pakket `iqsharp`</span><span class="sxs-lookup"><span data-stu-id="ad362-134">Install the `iqsharp` package</span></span>

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="ad362-135">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="ad362-135">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ad362-136">Voer de volgende opdracht uit om de Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="ad362-136">Run the following command to start the notebook server:</span></span>

        ```bash
        jupyter notebook
        ```

    - <span data-ttu-id="ad362-137">Blader naar de URL die wordt weergegeven op de opdrachtregel.</span><span class="sxs-lookup"><span data-stu-id="ad362-137">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="ad362-138">Bijvoorbeeld: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]</span><span class="sxs-lookup"><span data-stu-id="ad362-138">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

    - <span data-ttu-id="ad362-139">Maak een Jupyter Notebook met een Q#-kernel en voeg de volgende code toe aan de eerste Notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="ad362-139">Create a Jupyter notebook with a Q# kernel, and add the following code to the first notebook cell:</span></span>

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - <span data-ttu-id="ad362-140">Voer deze cel van het Notebook uit:</span><span class="sxs-lookup"><span data-stu-id="ad362-140">Run this cell of the notebook:</span></span>

        ![Cel met Q#-code in een Jupyter-notebook](~/media/install-guide-jupyter.png)

        <span data-ttu-id="ad362-142">U ziet `SayHello` in de uitvoer van de cel.</span><span class="sxs-lookup"><span data-stu-id="ad362-142">You should see `SayHello` in the output of the cell.</span></span> <span data-ttu-id="ad362-143">Wanneer u werkt met Jupyter Notebook, wordt de Q#-code gecompileerd en wordt de naam van de gevonden bewerking(en) geretourneerd in de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="ad362-143">When running in jupyter notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>


    - <span data-ttu-id="ad362-144">Simuleer in een nieuwe cel de uitvoering in een kwantumcomputer van de bewerking die u zojuist hebt gemaakt met behulp van de `%simulate`-magic:</span><span class="sxs-lookup"><span data-stu-id="ad362-144">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

        ![Cel met %simulate magic in een Jupyter-notebook](~/media/install-guide-jupyter-simulate.png)

        <span data-ttu-id="ad362-146">Het bericht wordt nu op het scherm weergegeven, samen met het resultaat van de bewerking die u hebt aangeroepen (in dit geval leeg).</span><span class="sxs-lookup"><span data-stu-id="ad362-146">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>


## <a name="develop-with-c-on-windows-using-visual-studio"></a><span data-ttu-id="ad362-147">Ontwikkelen met C# in Windows, met behulp van Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ad362-147">Develop with C# on Windows, using Visual Studio</span></span>

<span data-ttu-id="ad362-148">Visual Studio biedt een uitgebreide omgeving voor het ontwikkelen van Q#-programma's en beschikt over handige functies die ontwikkelaars helpen bij het bouwen van hun toepassingen, zoals het aanvullen van code en het markeren van de syntaxis.</span><span class="sxs-lookup"><span data-stu-id="ad362-148">Visual Studio offers a rich environment for developing Q# programs, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="ad362-149">De Visual Studio-extensie voor Q# bevat sjablonen voor Q#-bestanden en -projecten, evenals syntaxismarkering en IntelliSense-ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="ad362-149">The Q# Visual Studio extension contains templates for Q# files and projects as well as syntax highlighting and IntelliSense support.</span></span>


1. <span data-ttu-id="ad362-150">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ad362-150">Pre-requisites</span></span>

    - <span data-ttu-id="ad362-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld</span><span class="sxs-lookup"><span data-stu-id="ad362-151">[Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, with the .NET Core cross-platform development workload enabled</span></span>

1. <span data-ttu-id="ad362-152">Installeer de Q# Visual Studio-extensie</span><span class="sxs-lookup"><span data-stu-id="ad362-152">Install the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="ad362-153">Download de [Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="ad362-153">Download the [Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="ad362-154">Voeg de extensie toe aan Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ad362-154">Add the extension to Visual Studio</span></span>

1. <span data-ttu-id="ad362-155">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="ad362-155">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ad362-156">Maak een nieuwe Q#-toepassing</span><span class="sxs-lookup"><span data-stu-id="ad362-156">Create a new Q# application</span></span>

        - <span data-ttu-id="ad362-157">Ga naar **Bestand** -> **Nieuw** -> **Project**</span><span class="sxs-lookup"><span data-stu-id="ad362-157">Go to **File** -> **New** -> **Project**</span></span>
        - <span data-ttu-id="ad362-158">Typ `Q#` in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="ad362-158">Type `Q#` in the search box</span></span>
        - <span data-ttu-id="ad362-159">Selecteer **Q#-toepassing**</span><span class="sxs-lookup"><span data-stu-id="ad362-159">Select **Q# Application**</span></span>
        - <span data-ttu-id="ad362-160">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="ad362-160">Select **Next**</span></span>
        - <span data-ttu-id="ad362-161">Kies een naam en een locatie voor uw toepassing</span><span class="sxs-lookup"><span data-stu-id="ad362-161">Choose a name and location for your application</span></span>
        - <span data-ttu-id="ad362-162">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="ad362-162">Select **Create**</span></span>

    - <span data-ttu-id="ad362-163">Controleer het project</span><span class="sxs-lookup"><span data-stu-id="ad362-163">Inspect the project</span></span>

        <span data-ttu-id="ad362-164">U ziet dat er twee bestanden zijn gemaakt: `Driver.cs`, de C#-hosttoepassing. en `Operation.qs`, een Q#-programma dat een eenvoudige bewerking definieert om een bericht naar de console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="ad362-164">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

    - <span data-ttu-id="ad362-165">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="ad362-165">Run the application</span></span>

        - <span data-ttu-id="ad362-166">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**</span><span class="sxs-lookup"><span data-stu-id="ad362-166">Select **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="ad362-167">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="ad362-167">You should see the text `Hello quantum world!` printed to a console window.</span></span>

> [!NOTE]
> * <span data-ttu-id="ad362-168">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="ad362-168">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="develop-with-c-using-visual-studio-code"></a><span data-ttu-id="ad362-169">Ontwikkelen met C# met behulp van Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="ad362-169">Develop with C#, using Visual Studio Code</span></span>

<span data-ttu-id="ad362-170">Visual Studio Code (VS Code) biedt een uitgebreide omgeving voor het ontwikkelen van Q#-programma's in talloze computeromgevingen, waaronder Windows, Linux en Mac, en beschikt over handige functies die ontwikkelaars helpen bij het bouwen van hun toepassingen, zoals het aanvullen van code en het markeren van de syntaxis.</span><span class="sxs-lookup"><span data-stu-id="ad362-170">Visual Studio Code (VS Code) offers a rich environment for developing Q# programs across many multiple computer environments, including Windows, Linux and Mac, offering great features like code completion and syntax highlighting that guide the developer in building their applications.</span></span>  <span data-ttu-id="ad362-171">De VS Code-extensie voor Q# bevat syntaxismarkering en Q#-codefragmenten.</span><span class="sxs-lookup"><span data-stu-id="ad362-171">The Q# VS Code extension contains syntax highlighting, and Q# code snippets.</span></span>

1. <span data-ttu-id="ad362-172">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ad362-172">Pre-requisites</span></span>

   - [<span data-ttu-id="ad362-173">VS-code</span><span class="sxs-lookup"><span data-stu-id="ad362-173">VS Code</span></span>](https://code.visualstudio.com/download)
   - [<span data-ttu-id="ad362-174">.NET Core SDK 3.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="ad362-174">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="ad362-175">Installeer de Quantum VS Code-extensie</span><span class="sxs-lookup"><span data-stu-id="ad362-175">Install the Quantum VS Code extension</span></span>

    - <span data-ttu-id="ad362-176">Installeer de [VS Code-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span><span class="sxs-lookup"><span data-stu-id="ad362-176">Install the [VS Code extension](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)</span></span>

1. <span data-ttu-id="ad362-177">Installeer de Quantum-projectsjablonen:</span><span class="sxs-lookup"><span data-stu-id="ad362-177">Install the Quantum project templates:</span></span>

   - <span data-ttu-id="ad362-178">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="ad362-178">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="ad362-179">Selecteer **Q#: Projectsjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="ad362-179">Select **Q#: Install project templates**</span></span>

    <span data-ttu-id="ad362-180">De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ad362-180">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="ad362-181">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="ad362-181">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ad362-182">Maak een nieuw project:</span><span class="sxs-lookup"><span data-stu-id="ad362-182">Create a new project:</span></span>

        - <span data-ttu-id="ad362-183">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="ad362-183">Go to **View** -> **Command Palette**</span></span>
        - <span data-ttu-id="ad362-184">Selecteer **Q#: Nieuw project maken**</span><span class="sxs-lookup"><span data-stu-id="ad362-184">Select **Q#: Create New Project**</span></span>
        - <span data-ttu-id="ad362-185">Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken</span><span class="sxs-lookup"><span data-stu-id="ad362-185">Navigate to the location on the file system where you would like to create the application</span></span>
        - <span data-ttu-id="ad362-186">Klik op de knop **Nieuw project openen...** zodra het project is gemaakt</span><span class="sxs-lookup"><span data-stu-id="ad362-186">Click on the **Open new project...** button, once the project has been created</span></span>

    - <span data-ttu-id="ad362-187">Voer de toepassing uit:</span><span class="sxs-lookup"><span data-stu-id="ad362-187">Run the application:</span></span>

        - <span data-ttu-id="ad362-188">Ga naar **Fouten opsporen** -> **Starten zonder foutopsporing**</span><span class="sxs-lookup"><span data-stu-id="ad362-188">Go to **Debug** -> **Start Without Debugging**</span></span>
        - <span data-ttu-id="ad362-189">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="ad362-189">You should see the following text in the output window `Hello quantum world!`</span></span>

> [!NOTE]
> * > * <span data-ttu-id="ad362-190">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie.</span><span class="sxs-lookup"><span data-stu-id="ad362-190">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="ad362-191">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="ad362-191">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="ad362-192">Ontwikkelen met C#, met behulp van het opdrachtregelprogramma `dotnet`</span><span class="sxs-lookup"><span data-stu-id="ad362-192">Develop with C#, using the `dotnet` command-line tool</span></span>

<span data-ttu-id="ad362-193">Natuurlijk kunt u ook Q#-programma's schrijven en uitvoeren vanaf de opdrachtregel. U hoeft hiervoor alleen de .NET Core SDK en de QDK-projectsjablonen te installeren.</span><span class="sxs-lookup"><span data-stu-id="ad362-193">Of course, you can also build and run Q# programs from the command line by simply installing the .NET Core SDK and the QDK project templates.</span></span> 

1. <span data-ttu-id="ad362-194">Vereisten</span><span class="sxs-lookup"><span data-stu-id="ad362-194">Pre-requisites</span></span>

    - [<span data-ttu-id="ad362-195">.NET Core SDK 3.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="ad362-195">.NET Core SDK 3.0 or later</span></span>](https://www.microsoft.com/net/download)

1. <span data-ttu-id="ad362-196">Installeer de Quantum-projectsjablonen voor .NET</span><span class="sxs-lookup"><span data-stu-id="ad362-196">Install the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    <span data-ttu-id="ad362-197">De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="ad362-197">You now have the Quantum Development Kit installed and ready to use in your own applications and libraries.</span></span>

1. <span data-ttu-id="ad362-198">Controleer de installatie door een `Hello World`-toepassing te maken</span><span class="sxs-lookup"><span data-stu-id="ad362-198">Verify the installation by creating a `Hello World` application</span></span>

    - <span data-ttu-id="ad362-199">Een nieuwe toepassing maken</span><span class="sxs-lookup"><span data-stu-id="ad362-199">Create a new application</span></span>

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - <span data-ttu-id="ad362-200">Navigeer naar de nieuwe toepassingsmap</span><span class="sxs-lookup"><span data-stu-id="ad362-200">Navigate to the new application directory</span></span>

       ```bash
       cd runSayHello
       ```

    <span data-ttu-id="ad362-201">U ziet dat er twee bestanden zijn gemaakt, samen met de projectbestanden van de toepassing: een Q#-bestand (`Operation.qs`) en een C#-hostbestand (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="ad362-201">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

    - <span data-ttu-id="ad362-202">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="ad362-202">Run the application</span></span>

        ```bash
        dotnet run
        ```

        <span data-ttu-id="ad362-203">U ziet de volgende uitvoer: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="ad362-203">You should see the following output: `Hello quantum world!`</span></span>

## <a name="whats-next"></a><span data-ttu-id="ad362-204">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="ad362-204">What's next?</span></span>

<span data-ttu-id="ad362-205">Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ad362-205">Now that you have installed the Quantum Development Kit in your preferred environment, you can write and run [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
