---
title: Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ed2a90749bbe245dde97424fc3191682f995d85b
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76819736"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="b187b-102">Het Microsoft Quantum Development Kit bijwerken (QDK)</span><span class="sxs-lookup"><span data-stu-id="b187b-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="b187b-103">Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.</span><span class="sxs-lookup"><span data-stu-id="b187b-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="b187b-104">In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="b187b-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="b187b-105">Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="b187b-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="b187b-106">We raden u aan om de nieuwste versie van QDK up-to-date te houden.</span><span class="sxs-lookup"><span data-stu-id="b187b-106">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="b187b-107">Volg deze update handleiding om een upgrade uit te voeren naar de meest recente versie van QDK.</span><span class="sxs-lookup"><span data-stu-id="b187b-107">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="b187b-108">Het proces bestaat uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="b187b-108">The process consists of two parts:</span></span>
1. <span data-ttu-id="b187b-109">uw bestaande Q #-bestanden en-projecten bijwerken om uw code uit te lijnen met een bijgewerkte syntaxis</span><span class="sxs-lookup"><span data-stu-id="b187b-109">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="b187b-110">de QDK voor uw gekozen ontwikkel omgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-110">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="b187b-111">Q #-projecten bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-111">Updating Q# Projects</span></span> 

<span data-ttu-id="b187b-112">Ongeacht of u of python gebruikt C# om q #-bewerkingen te hosten, volgt u deze instructies om uw q #-projecten bij te werken.</span><span class="sxs-lookup"><span data-stu-id="b187b-112">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="b187b-113">Controleer eerst of u de meest recente versie van de [.NET Core SDK 3,1](https://dotnet.microsoft.com/download)hebt.</span><span class="sxs-lookup"><span data-stu-id="b187b-113">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="b187b-114">Voer de volgende opdracht uit in de opdracht prompt:</span><span class="sxs-lookup"><span data-stu-id="b187b-114">Run the following command in the command prompt:</span></span>
    ```bash
    dotnet --version
    ```
<span data-ttu-id="b187b-115">Controleer of de uitvoer `3.1.100` of hoger is.</span><span class="sxs-lookup"><span data-stu-id="b187b-115">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="b187b-116">Als dat niet het geval is, installeert u de [nieuwste versie](https://dotnet.microsoft.com/download) en controleert u opnieuw.</span><span class="sxs-lookup"><span data-stu-id="b187b-116">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="b187b-117">Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio code of rechtstreeks de opdracht regel).</span><span class="sxs-lookup"><span data-stu-id="b187b-117">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="b187b-118">Update Q #-projecten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b187b-118">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="b187b-119">Update naar de nieuwste versie van Visual Studio 2019. Zie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) voor instructies</span><span class="sxs-lookup"><span data-stu-id="b187b-119">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="b187b-120">Open uw oplossing in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b187b-120">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="b187b-121">Selecteer in het menu de optie **bouwen** -> **nieuwe oplossing**</span><span class="sxs-lookup"><span data-stu-id="b187b-121">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="b187b-122">Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.0` (of `netstandard2.1` als het een bibliotheek project is).</span><span class="sxs-lookup"><span data-stu-id="b187b-122">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="b187b-123">Dat wil zeggen, regels van het formulier bewerken:</span><span class="sxs-lookup"><span data-stu-id="b187b-123">That is, edit lines of the form:</span></span>
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    <span data-ttu-id="b187b-124">[Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.</span><span class="sxs-lookup"><span data-stu-id="b187b-124">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="b187b-125">Sla alle bestanden in uw oplossing op en sluit deze af</span><span class="sxs-lookup"><span data-stu-id="b187b-125">Save and close all files in your solution</span></span>
6. <span data-ttu-id="b187b-126">Selecteer **extra** -> **opdracht regel** -> **opdracht prompt voor ontwikkel aars**</span><span class="sxs-lookup"><span data-stu-id="b187b-126">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="b187b-127">Voer voor elk project in de oplossing de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="b187b-127">For each project in the solution, run the following command:</span></span>
    ```bash
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```
    <span data-ttu-id="b187b-128">Als uw projecten andere micro soft. Quantum-pakketten gebruiken (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht ook uit.</span><span class="sxs-lookup"><span data-stu-id="b187b-128">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="b187b-129">Sluit de opdracht prompt en selecteer **build** -> **Build-oplossing** (Selecteer *geen* oplossing voor opnieuw samen stellen.</span><span class="sxs-lookup"><span data-stu-id="b187b-129">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution, as rebuilding will initially fail)</span></span>

<span data-ttu-id="b187b-130">U kunt nu door gaan om [uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension)bij te werken.</span><span class="sxs-lookup"><span data-stu-id="b187b-130">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="b187b-131">Update Q #-projecten in Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="b187b-131">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="b187b-132">Open in Visual Studio code de map met het project dat moet worden bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="b187b-132">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="b187b-133">**Terminal** -> **nieuwe terminal** selecteren</span><span class="sxs-lookup"><span data-stu-id="b187b-133">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="b187b-134">Volg de instructies voor het bijwerken met behulp van de opdracht regel (direct hieronder)</span><span class="sxs-lookup"><span data-stu-id="b187b-134">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="b187b-135">Q #-projecten bijwerken met behulp van de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="b187b-135">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="b187b-136">Ga naar de map die het project bestand bevat</span><span class="sxs-lookup"><span data-stu-id="b187b-136">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="b187b-137">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="b187b-137">Run the following command:</span></span>
    ```bash
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="b187b-138">Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.0` (of `netstandard2.1` als het een bibliotheek project is).</span><span class="sxs-lookup"><span data-stu-id="b187b-138">In each of your .csproj files, update the target framework to `netcoreapp3.0` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="b187b-139">Dat wil zeggen, regels van het formulier bewerken:</span><span class="sxs-lookup"><span data-stu-id="b187b-139">That is, edit lines of the form:</span></span>
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    <span data-ttu-id="b187b-140">[Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.</span><span class="sxs-lookup"><span data-stu-id="b187b-140">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="b187b-141">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="b187b-141">Run the following command:</span></span>
    ```bash
    dotnet add package Microsoft.Quantum.Development.Kit
    ```
    <span data-ttu-id="b187b-142">Als uw project gebruikmaakt van andere micro soft. Quantum-pakketten (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht ook uit.</span><span class="sxs-lookup"><span data-stu-id="b187b-142">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="b187b-143">Sla alle bestanden op en sluit deze.</span><span class="sxs-lookup"><span data-stu-id="b187b-143">Save and close all files.</span></span>
6. <span data-ttu-id="b187b-144">Herhaal 1-4 voor elke project afhankelijkheid en ga vervolgens terug naar de map met het hoofd project en voer het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="b187b-144">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>
    ```bash
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="b187b-145">Als uw Q #-projecten nu zijn bijgewerkt, volgt u de onderstaande instructies om de QDK zelf bij te werken.</span><span class="sxs-lookup"><span data-stu-id="b187b-145">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="b187b-146">De QDK bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-146">Updating the QDK</span></span>

<span data-ttu-id="b187b-147">Het proces voor het bijwerken van de QDK varieert, afhankelijk van uw ontwikkelings taal en-omgeving.</span><span class="sxs-lookup"><span data-stu-id="b187b-147">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="b187b-148">Selecteer hieronder uw ontwikkel omgeving.</span><span class="sxs-lookup"><span data-stu-id="b187b-148">Select your development environment below.</span></span>

* [<span data-ttu-id="b187b-149">Python: de extensie # uitbrei ding bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-149">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="b187b-150">Jupyter-notebooks: de extensie # uitbrei ding bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-150">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="b187b-151">Visual Studio: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-151">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="b187b-152">VS code: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-152">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="b187b-153">Opdracht regel en C#: Project sjablonen bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-153">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="b187b-154">Update IQ # voor python</span><span class="sxs-lookup"><span data-stu-id="b187b-154">Update IQ# for Python</span></span>

1. <span data-ttu-id="b187b-155">De `iqsharp`-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-155">Update the `iqsharp` kernel</span></span> 

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="b187b-156">De `iqsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="b187b-156">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b187b-157">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="b187b-157">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    <span data-ttu-id="b187b-158">U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="b187b-158">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="b187b-159">Het `qsharp`-pakket bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-159">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="b187b-160">De `qsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="b187b-160">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="b187b-161">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="b187b-161">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
5. <span data-ttu-id="b187b-162">Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden</span><span class="sxs-lookup"><span data-stu-id="b187b-162">Run the following command from the location of your `.qs` files</span></span>
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="b187b-163">U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b187b-163">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="b187b-164">Update IQ # voor Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="b187b-164">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="b187b-165">De `iqsharp`-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-165">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="b187b-166">De `iqsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="b187b-166">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="b187b-167">De uitvoer moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="b187b-167">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    <span data-ttu-id="b187b-168">U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="b187b-168">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="b187b-169">Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="b187b-169">Run the following command from a cell in your Jupyter Notebook:</span></span>
    ```
    %workspace reload
    ```

4. <span data-ttu-id="b187b-170">U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.</span><span class="sxs-lookup"><span data-stu-id="b187b-170">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="b187b-171">De QDK-extensie van Visual Studio bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-171">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="b187b-172">De Q # Visual Studio-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-172">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="b187b-173">Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="b187b-173">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="b187b-174">De update accepteren</span><span class="sxs-lookup"><span data-stu-id="b187b-174">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="b187b-175">De Project sjablonen worden bijgewerkt met de uitbrei ding.</span><span class="sxs-lookup"><span data-stu-id="b187b-175">The project templates are updated with the extension.</span></span> <span data-ttu-id="b187b-176">De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten.</span><span class="sxs-lookup"><span data-stu-id="b187b-176">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="b187b-177">De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b187b-177">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="b187b-178">QDK-extensie voor bijwerken versus code</span><span class="sxs-lookup"><span data-stu-id="b187b-178">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="b187b-179">De Quantum versus code-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-179">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="b187b-180">Opnieuw opstarten VS code</span><span class="sxs-lookup"><span data-stu-id="b187b-180">Restart VS Code</span></span>
    - <span data-ttu-id="b187b-181">Ga naar het tabblad **extensies**</span><span class="sxs-lookup"><span data-stu-id="b187b-181">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="b187b-182">Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension</span><span class="sxs-lookup"><span data-stu-id="b187b-182">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="b187b-183">De uitbrei ding opnieuw laden</span><span class="sxs-lookup"><span data-stu-id="b187b-183">Reload the extension</span></span>

2. <span data-ttu-id="b187b-184">De Quantum project sjablonen bijwerken:</span><span class="sxs-lookup"><span data-stu-id="b187b-184">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="b187b-185">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="b187b-185">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="b187b-186">Selecteer **Q #: Project sjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="b187b-186">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="b187b-187">Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat ' Project sjablonen zijn geïnstalleerd '</span><span class="sxs-lookup"><span data-stu-id="b187b-187">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="b187b-188">C#, met behulp van het opdracht regel programma `dotnet`</span><span class="sxs-lookup"><span data-stu-id="b187b-188">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="b187b-189">De Quantum project sjablonen voor .NET bijwerken</span><span class="sxs-lookup"><span data-stu-id="b187b-189">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="b187b-190">En verder?</span><span class="sxs-lookup"><span data-stu-id="b187b-190">What's next?</span></span>

<span data-ttu-id="b187b-191">Nu u de Quantum Development Kit hebt bijgewerkt in uw voorkeurs omgeving, kunt u uw Quantum Programma's blijven ontwikkelen en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="b187b-191">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="b187b-192">Als u nog geen programma hebt geschreven, kunt u aan de slag met [uw eerste Quantum programma](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="b187b-192">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
