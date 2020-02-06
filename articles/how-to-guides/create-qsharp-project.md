---
title: 'Meer informatie over het maken van een Q #-project met de Quantum Development Kit (QDK)'
description: 'Initialiseer een project voor de Quantum ontwikkeling met de QDK en Q # in de ontwikkel omgeving van uw keuze'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: c093284f1ea33b72d4d264992b0ba6bf6bc72782
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036437"
---
# <a name="create-a-q-project-in-your-development-environment"></a><span data-ttu-id="b156e-103">Een Q #-project maken in uw ontwikkel omgeving</span><span class="sxs-lookup"><span data-stu-id="b156e-103">Create a Q# project in your development environment</span></span>

<span data-ttu-id="b156e-104">Meer informatie over het maken van een Q #-project met de QDK.</span><span class="sxs-lookup"><span data-stu-id="b156e-104">Learn how to create a Q# project with the QDK.</span></span>

<span data-ttu-id="b156e-105">Een Q #-project bevat Q # bestanden met een Quantum code en een hostprogramma voor het uitvoeren van het Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="b156e-105">A Q# project contains Q# files containing quantum code, as well as a host program to run the quantum program.</span></span> <span data-ttu-id="b156e-106">U kunt het host-programma schrijven in .NET C#-talen zoals of in python.</span><span class="sxs-lookup"><span data-stu-id="b156e-106">You can write the host program in .NET languages such as C#, or in Python.</span></span> <span data-ttu-id="b156e-107">U kunt ook Q #-code in een Jupyter-notebook uitvoeren met behulp van de IQ # kernel.</span><span class="sxs-lookup"><span data-stu-id="b156e-107">You can also run Q# code in a Jupyter notebook using the IQ# kernel.</span></span>

<span data-ttu-id="b156e-108">Kies uw ontwikkel omgeving en taal in de volgende secties:</span><span class="sxs-lookup"><span data-stu-id="b156e-108">Choose your development environment and language from the sections below:</span></span>

* [<span data-ttu-id="b156e-109">Python</span><span class="sxs-lookup"><span data-stu-id="b156e-109">Python</span></span>](#create-a-python-project)
* [<span data-ttu-id="b156e-110">Q # Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="b156e-110">Q# Jupyter notebooks</span></span>](#create-a-q-jupyter-notebook-project)
* [<span data-ttu-id="b156e-111">C#met Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b156e-111">C# with Visual Studio</span></span>](#create-a-c-project-on-windows-using-visual-studio)
* [<span data-ttu-id="b156e-112">C#met VS code</span><span class="sxs-lookup"><span data-stu-id="b156e-112">C# with VS Code</span></span>](#create-a-c-project-using-vs-code)
* [<span data-ttu-id="b156e-113">C#met de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="b156e-113">C# with the command line</span></span>](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a><span data-ttu-id="b156e-114">Een python-project maken</span><span class="sxs-lookup"><span data-stu-id="b156e-114">Create a Python project</span></span>

1. <span data-ttu-id="b156e-115">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b156e-115">Pre-requisites</span></span>

     * <span data-ttu-id="b156e-116">De [Quantum Development Kit voor python](xref:microsoft.quantum.install.python) installeren</span><span class="sxs-lookup"><span data-stu-id="b156e-116">Install the [Quantum Development Kit for Python](xref:microsoft.quantum.install.python)</span></span>

1. <span data-ttu-id="b156e-117">Maak een map voor uw project en navigeer naar die map</span><span class="sxs-lookup"><span data-stu-id="b156e-117">Create a folder for your project, and navigate to that folder</span></span>

1. <span data-ttu-id="b156e-118">Maak een Q #-bestand met de naam `Operation.qs`en voeg hieraan uw Q #-code toe.</span><span class="sxs-lookup"><span data-stu-id="b156e-118">Create a Q# file called `Operation.qs`, and add your Q# code to it.</span></span> <span data-ttu-id="b156e-119">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="b156e-119">For example:</span></span>

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. <span data-ttu-id="b156e-120">Maak een python-bestand met de naam `host.py` om uw Q #-bewerking aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="b156e-120">Create a python host file called `host.py` to call your Q# operation.</span></span> <span data-ttu-id="b156e-121">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="b156e-121">For example:</span></span>

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. <span data-ttu-id="b156e-122">Voer het programma uit:</span><span class="sxs-lookup"><span data-stu-id="b156e-122">Run the program:</span></span>

    ```bash
    python host.py
    ```

1. <span data-ttu-id="b156e-123">Controleer de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="b156e-123">Verify the output.</span></span> <span data-ttu-id="b156e-124">Met het programma worden de volgende regels uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="b156e-124">Your program should output the following lines:</span></span>

    ```bash
    Hello from quantum world!
    0
    ```

<span data-ttu-id="b156e-125">U kunt nu door gaan met het ontwikkelen van uw Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="b156e-125">You can now continue to develop your quantum program.</span></span>

## <a name="create-a-q-jupyter-notebook-project"></a><span data-ttu-id="b156e-126">Een Q # Jupyter Notebook-project maken</span><span class="sxs-lookup"><span data-stu-id="b156e-126">Create a Q# Jupyter Notebook project</span></span>

1. <span data-ttu-id="b156e-127">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b156e-127">Pre-requisites</span></span>

    * <span data-ttu-id="b156e-128">De [Quantum Development Kit voor Jupyter-notebooks](xref:microsoft.quantum.install.jupyter) installeren</span><span class="sxs-lookup"><span data-stu-id="b156e-128">Install the [Quantum Development Kit for Jupyter notebooks](xref:microsoft.quantum.install.jupyter)</span></span>

1. <span data-ttu-id="b156e-129">Voer de volgende opdracht uit om de Notebook-server te starten:</span><span class="sxs-lookup"><span data-stu-id="b156e-129">Run the following command to start the notebook server:</span></span>

    ```bash
    jupyter notebook
    ```

1. <span data-ttu-id="b156e-130">Blader naar de URL die wordt weergegeven op de opdrachtregel.</span><span class="sxs-lookup"><span data-stu-id="b156e-130">Browse to the URL shown on the command line.</span></span> <span data-ttu-id="b156e-131">Bijvoorbeeld: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span><span class="sxs-lookup"><span data-stu-id="b156e-131">For example: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]</span></span>

1. <span data-ttu-id="b156e-132">Er wordt een Jupyter-pagina weer gegeven in de browser.</span><span class="sxs-lookup"><span data-stu-id="b156e-132">A Jupyter page appears in the browser.</span></span> <span data-ttu-id="b156e-133">Op het tabblad **bestanden** selecteert u **Nieuw** > **Q #** om een Jupyter-notebook met een Q #-kernel te maken.</span><span class="sxs-lookup"><span data-stu-id="b156e-133">On the **Files** tab, select **New** > **Q#** to create a Jupyter notebook with a Q# kernel.</span></span> <span data-ttu-id="b156e-134">Voeg de volgende code toe aan de eerste notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="b156e-134">Add the following code to the first notebook cell:</span></span>

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. <span data-ttu-id="b156e-135">Selecteer **cel** > **Voer cellen uit** om het notitie blok uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b156e-135">Select **Cell** > **Run Cells** to run the notebook.</span></span> <span data-ttu-id="b156e-136">`SayHello` wordt binnenkort weer gegeven in de cel-uitvoer:</span><span class="sxs-lookup"><span data-stu-id="b156e-136">`SayHello` will soon appear in the cell output:</span></span>

    ![Cel met Q#-code in een Jupyter-notebook](~/media/install-guide-jupyter.png)

    <span data-ttu-id="b156e-138">Bij het uitvoeren van Jupyter-notebooks wordt de Q #-code gecompileerd en de notitie blok voert de naam van de bewerkte (en) bewerkingen uit die worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="b156e-138">When running in Jupyter Notebooks, the Q# code is compiled, and the notebook outputs the name of the operation(s) that it finds.</span></span>

1. <span data-ttu-id="b156e-139">Simuleer in een nieuwe cel de uitvoering in een kwantumcomputer van de bewerking die u zojuist hebt gemaakt met behulp van de `%simulate`-magic:</span><span class="sxs-lookup"><span data-stu-id="b156e-139">In a new cell, simulate the execution in a quantum computer of the operation you just created by using the `%simulate` magic:</span></span>

    ![Cel met %simulate magic in een Jupyter-notebook](~/media/install-guide-jupyter-simulate.png)

    <span data-ttu-id="b156e-141">Het bericht wordt nu op het scherm weergegeven, samen met het resultaat van de bewerking die u hebt aangeroepen (in dit geval leeg).</span><span class="sxs-lookup"><span data-stu-id="b156e-141">You should see the message printed on the screen along with the result of the operation you invoked (in this case, empty).</span></span>

<span data-ttu-id="b156e-142">U kunt nu andere Q #-bewerkingen toevoegen om uw Quantum ontwikkeling voort te zetten.</span><span class="sxs-lookup"><span data-stu-id="b156e-142">You can now add other Q# operations to continue your quantum development.</span></span>

## <a name="create-a-c-project-on-windows-using-visual-studio"></a><span data-ttu-id="b156e-143">Een C# project maken in Windows met behulp van Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b156e-143">Create a C# project on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="b156e-144">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b156e-144">Pre-requisites</span></span>

    * <span data-ttu-id="b156e-145">De [Quantum Development Kit-extensie voor Visual Studio](xref:microsoft.quantum.install.cs) installeren</span><span class="sxs-lookup"><span data-stu-id="b156e-145">Install the [Quantum Development Kit extension for Visual Studio](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="b156e-146">Maak een nieuwe Q#-toepassing</span><span class="sxs-lookup"><span data-stu-id="b156e-146">Create a new Q# application</span></span>

    * <span data-ttu-id="b156e-147">Ga naar **Bestand** -> **Nieuw** -> **Project**</span><span class="sxs-lookup"><span data-stu-id="b156e-147">Go to **File** -> **New** -> **Project**</span></span>
    * <span data-ttu-id="b156e-148">Typ `Q#` in het zoekvak</span><span class="sxs-lookup"><span data-stu-id="b156e-148">Type `Q#` in the search box</span></span>
    * <span data-ttu-id="b156e-149">Selecteer **Q#-toepassing**</span><span class="sxs-lookup"><span data-stu-id="b156e-149">Select **Q# Application**</span></span>
    * <span data-ttu-id="b156e-150">Selecteer **Volgende**</span><span class="sxs-lookup"><span data-stu-id="b156e-150">Select **Next**</span></span>
    * <span data-ttu-id="b156e-151">Kies een naam en een locatie voor uw toepassing</span><span class="sxs-lookup"><span data-stu-id="b156e-151">Choose a name and location for your application</span></span>
    * <span data-ttu-id="b156e-152">Selecteer **Maken**</span><span class="sxs-lookup"><span data-stu-id="b156e-152">Select **Create**</span></span>

1. <span data-ttu-id="b156e-153">Controleer het project</span><span class="sxs-lookup"><span data-stu-id="b156e-153">Inspect the project</span></span>

    <span data-ttu-id="b156e-154">U ziet dat er twee bestanden zijn gemaakt: `Driver.cs`, de C#-hosttoepassing. en `Operation.qs`, een Q#-programma dat een eenvoudige bewerking definieert om een bericht naar de console af te drukken.</span><span class="sxs-lookup"><span data-stu-id="b156e-154">You should see that two files have been created: `Driver.cs`, which is the C# host application; and `Operation.qs`, which is a Q# program that defines a simple operation to print a message to the console.</span></span>

1. <span data-ttu-id="b156e-155">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b156e-155">Run the application</span></span>

    * <span data-ttu-id="b156e-156">Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**</span><span class="sxs-lookup"><span data-stu-id="b156e-156">Select **Debug** -> **Start Without Debugging**</span></span>
    * <span data-ttu-id="b156e-157">Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.</span><span class="sxs-lookup"><span data-stu-id="b156e-157">You should see the text `Hello quantum world!` printed to a console window.</span></span>

<span data-ttu-id="b156e-158">U kunt nu door gaan met het ontwikkelen van uw Quantum met Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b156e-158">You can now continue your quantum development using Visual Studio</span></span>

> [!NOTE]
> * <span data-ttu-id="b156e-159">Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.</span><span class="sxs-lookup"><span data-stu-id="b156e-159">If you have multiple projects within one Visual Studio solution, all projects contained in the solution need to be in the same folder as the solution, or in one of its subfolders.</span></span>  

## <a name="create-a-c-project-using-vs-code"></a><span data-ttu-id="b156e-160">Een C# project maken met behulp van VS code</span><span class="sxs-lookup"><span data-stu-id="b156e-160">Create a C# project, using VS Code</span></span>

1. <span data-ttu-id="b156e-161">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b156e-161">Pre-requisites</span></span>

    * <span data-ttu-id="b156e-162">De [Quantum Development Kit-uitbrei ding voor VS code](xref:microsoft.quantum.install.cs) installeren</span><span class="sxs-lookup"><span data-stu-id="b156e-162">Install the [Quantum Development Kit extension for VS Code](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="b156e-163">Maak een nieuw project:</span><span class="sxs-lookup"><span data-stu-id="b156e-163">Create a new project:</span></span>

    * <span data-ttu-id="b156e-164">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="b156e-164">Go to **View** -> **Command Palette**</span></span>
    * <span data-ttu-id="b156e-165">Selecteer **Q #: nieuw project maken**</span><span class="sxs-lookup"><span data-stu-id="b156e-165">Select **Q#: Create New Project**</span></span>
    * <span data-ttu-id="b156e-166">**Zelfstandige console toepassing** selecteren</span><span class="sxs-lookup"><span data-stu-id="b156e-166">Select **Standalone console application**</span></span>
    * <span data-ttu-id="b156e-167">Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken</span><span class="sxs-lookup"><span data-stu-id="b156e-167">Navigate to the location on the file system where you would like to create the application</span></span>
    * <span data-ttu-id="b156e-168">Klik op de knop **Nieuw project openen...** zodra het project is gemaakt</span><span class="sxs-lookup"><span data-stu-id="b156e-168">Click on the **Open new project...** button, once the project has been created</span></span>

1. <span data-ttu-id="b156e-169">Voer de toepassing uit:</span><span class="sxs-lookup"><span data-stu-id="b156e-169">Run the application:</span></span>

    * <span data-ttu-id="b156e-170">Ga naar **terminal** -> **nieuwe terminal**</span><span class="sxs-lookup"><span data-stu-id="b156e-170">Go to **Terminal** -> **New Terminal**</span></span>
    * <span data-ttu-id="b156e-171">Voer `dotnet run` in</span><span class="sxs-lookup"><span data-stu-id="b156e-171">Enter `dotnet run`</span></span>
    * <span data-ttu-id="b156e-172">Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="b156e-172">You should see the following text in the output window `Hello quantum world!`</span></span>

<span data-ttu-id="b156e-173">U kunt nu door gaan met het ontwikkelen van uw Quantum met Visual Studio code.</span><span class="sxs-lookup"><span data-stu-id="b156e-173">You can now continue your quantum development using Visual Studio Code.</span></span>

> [!NOTE]
> * <span data-ttu-id="b156e-174">Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie.</span><span class="sxs-lookup"><span data-stu-id="b156e-174">Workspaces with multiple root folders are not currently supported by the Visual Studio Code extension.</span></span> <span data-ttu-id="b156e-175">Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.</span><span class="sxs-lookup"><span data-stu-id="b156e-175">If you have multiple projects within one VS Code workspace, all projects need to be contained within the same root folder.</span></span>

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a><span data-ttu-id="b156e-176">Een C# project maken met behulp van het opdracht regel programma `dotnet`</span><span class="sxs-lookup"><span data-stu-id="b156e-176">Create a C# project, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="b156e-177">Vereisten</span><span class="sxs-lookup"><span data-stu-id="b156e-177">Pre-requisites</span></span>

    * <span data-ttu-id="b156e-178">De [Quantum Development Kit installeren voor de opdracht regel](xref:microsoft.quantum.install.cs)</span><span class="sxs-lookup"><span data-stu-id="b156e-178">Install the [Quantum Development Kit for the Command Line](xref:microsoft.quantum.install.cs)</span></span>

1. <span data-ttu-id="b156e-179">Een nieuwe toepassing maken</span><span class="sxs-lookup"><span data-stu-id="b156e-179">Create a new application</span></span>

    ```dotnetcli
    dotnet new console -lang Q# -o <project name>
    ```

1. <span data-ttu-id="b156e-180">Navigeer naar de nieuwe toepassingsmap</span><span class="sxs-lookup"><span data-stu-id="b156e-180">Navigate to the new application directory</span></span>

    ```bash
    cd <project name>
    ```

    <span data-ttu-id="b156e-181">U ziet dat er twee bestanden zijn gemaakt, samen met de projectbestanden van de toepassing: een Q#-bestand (`Operation.qs`) en een C#-hostbestand (`Driver.cs`).</span><span class="sxs-lookup"><span data-stu-id="b156e-181">You should see that two files have been created, along with the project files of the application: a Q# file (`Operation.qs`) and a C# host file (`Driver.cs`).</span></span>

1. <span data-ttu-id="b156e-182">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b156e-182">Run the application</span></span>

    ```dotnetcli
    dotnet run
    ```

    <span data-ttu-id="b156e-183">U ziet de volgende uitvoer: `Hello quantum world!`</span><span class="sxs-lookup"><span data-stu-id="b156e-183">You should see the following output: `Hello quantum world!`</span></span>

<span data-ttu-id="b156e-184">U kunt nu door gaan met de Quantum ontwikkeling met behulp van opdracht regel Programma's.</span><span class="sxs-lookup"><span data-stu-id="b156e-184">You now continue your quantum development, using command line tools.</span></span>

## <a name="whats-next"></a><span data-ttu-id="b156e-185">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="b156e-185">What's next?</span></span>

<span data-ttu-id="b156e-186">Nu u een project in uw voorkeurs omgeving hebt gemaakt, kunt u uw Quantum ontwikkeling voortzetten.</span><span class="sxs-lookup"><span data-stu-id="b156e-186">Now that you have created a project in your preferred environment, you can continue your quantum development.</span></span>
