---
title: De Quantum Development Kit (QDK) bijwerken
description: 'Hierin wordt beschreven hoe u uw Q #-projecten en de Microsoft Quantum Development Kit bijwerkt naar de huidige versie.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 53f72f1d49ae32a5a8572a1cf68a66a1d9b45e4a
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426908"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="01ebc-103">Het Microsoft Quantum Development Kit bijwerken (QDK)</span><span class="sxs-lookup"><span data-stu-id="01ebc-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="01ebc-104">Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.</span><span class="sxs-lookup"><span data-stu-id="01ebc-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="01ebc-105">In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="01ebc-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="01ebc-106">Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="01ebc-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="01ebc-107">We raden u aan om de nieuwste versie van QDK up-to-date te houden.</span><span class="sxs-lookup"><span data-stu-id="01ebc-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="01ebc-108">Volg deze update handleiding om een upgrade uit te voeren naar de meest recente versie van QDK.</span><span class="sxs-lookup"><span data-stu-id="01ebc-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="01ebc-109">Het proces bestaat uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="01ebc-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="01ebc-110">uw bestaande Q #-bestanden en-projecten bijwerken om uw code uit te lijnen met een bijgewerkte syntaxis</span><span class="sxs-lookup"><span data-stu-id="01ebc-110">updating your existing Q# files and projects to align your code with any updated syntax</span></span>
2. <span data-ttu-id="01ebc-111">de QDK voor uw gekozen ontwikkel omgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-111">updating the QDK itself for your chosen development environment</span></span> 

## <a name="updating-q-projects"></a><span data-ttu-id="01ebc-112">Q #-projecten bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-112">Updating Q# Projects</span></span> 

<span data-ttu-id="01ebc-113">Ongeacht of u C# of python gebruikt om Q #-bewerkingen te hosten, volgt u deze instructies om uw Q #-projecten bij te werken.</span><span class="sxs-lookup"><span data-stu-id="01ebc-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="01ebc-114">Controleer eerst of u de meest recente versie van de [.NET Core SDK 3,1](https://dotnet.microsoft.com/download)hebt.</span><span class="sxs-lookup"><span data-stu-id="01ebc-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="01ebc-115">Voer de volgende opdracht uit in de opdracht prompt:</span><span class="sxs-lookup"><span data-stu-id="01ebc-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="01ebc-116">Controleer of de uitvoer is `3.1.100` of hoger.</span><span class="sxs-lookup"><span data-stu-id="01ebc-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="01ebc-117">Als dat niet het geval is, installeert u de [nieuwste versie](https://dotnet.microsoft.com/download) en controleert u opnieuw.</span><span class="sxs-lookup"><span data-stu-id="01ebc-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="01ebc-118">Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio code of rechtstreeks de opdracht regel).</span><span class="sxs-lookup"><span data-stu-id="01ebc-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="01ebc-119">Update Q #-projecten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01ebc-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="01ebc-120">Update naar de nieuwste versie van Visual Studio 2019. Zie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) voor instructies</span><span class="sxs-lookup"><span data-stu-id="01ebc-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
2. <span data-ttu-id="01ebc-121">Open uw oplossing in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01ebc-121">Open your solution in Visual Studio</span></span>
3. <span data-ttu-id="01ebc-122">Selecteer in het menu een **Build**  ->  **schone oplossing** bouwen</span><span class="sxs-lookup"><span data-stu-id="01ebc-122">From the menu, select **Build** -> **Clean Solution**</span></span>
4. <span data-ttu-id="01ebc-123">Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.1` (of `netstandard2.1` als het een bibliotheek project is).</span><span class="sxs-lookup"><span data-stu-id="01ebc-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="01ebc-124">Dat wil zeggen, regels van het formulier bewerken:</span><span class="sxs-lookup"><span data-stu-id="01ebc-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="01ebc-125">[Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.</span><span class="sxs-lookup"><span data-stu-id="01ebc-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
5. <span data-ttu-id="01ebc-126">Sla alle bestanden in uw oplossing op en sluit deze af</span><span class="sxs-lookup"><span data-stu-id="01ebc-126">Save and close all files in your solution</span></span>
6. <span data-ttu-id="01ebc-127">Selecteer **extra**  ->  **opdracht regel**opdracht  ->  **prompt**</span><span class="sxs-lookup"><span data-stu-id="01ebc-127">Select **Tools** -> **Command Line** -> **Developer Command Prompt**</span></span>
7. <span data-ttu-id="01ebc-128">Voer voor elk project in de oplossing de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="01ebc-128">For each project in the solution, run the following command:</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="01ebc-129">Als uw projecten andere micro soft. Quantum-pakketten gebruiken (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht ook uit.</span><span class="sxs-lookup"><span data-stu-id="01ebc-129">If your projects use any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
8. <span data-ttu-id="01ebc-130">Sluit de opdracht prompt en selecteer **Build**  ->  **Build Solution** (Selecteer *geen* oplossing opnieuw maken)</span><span class="sxs-lookup"><span data-stu-id="01ebc-130">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution)</span></span>

<span data-ttu-id="01ebc-131">U kunt nu door gaan om [uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension)bij te werken.</span><span class="sxs-lookup"><span data-stu-id="01ebc-131">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="01ebc-132">Update Q #-projecten in Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="01ebc-132">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="01ebc-133">Open in Visual Studio code de map met het project dat moet worden bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="01ebc-133">In Visual Studio Code, open the folder containing the project to update</span></span>
2. <span data-ttu-id="01ebc-134">**Terminal**  ->  **nieuwe terminal** selecteren</span><span class="sxs-lookup"><span data-stu-id="01ebc-134">Select **Terminal** -> **New Terminal**</span></span>
3. <span data-ttu-id="01ebc-135">Volg de instructies voor het bijwerken met behulp van de opdracht regel (direct hieronder)</span><span class="sxs-lookup"><span data-stu-id="01ebc-135">Follow the instructions for updating using the command line (directly below)</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="01ebc-136">Q #-projecten bijwerken met behulp van de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="01ebc-136">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="01ebc-137">Ga naar de map die het project bestand bevat</span><span class="sxs-lookup"><span data-stu-id="01ebc-137">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="01ebc-138">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="01ebc-138">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="01ebc-139">Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.1` (of `netstandard2.1` als het een bibliotheek project is).</span><span class="sxs-lookup"><span data-stu-id="01ebc-139">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="01ebc-140">Dat wil zeggen, regels van het formulier bewerken:</span><span class="sxs-lookup"><span data-stu-id="01ebc-140">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="01ebc-141">[Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.</span><span class="sxs-lookup"><span data-stu-id="01ebc-141">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>
4. <span data-ttu-id="01ebc-142">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="01ebc-142">Run the following command:</span></span>

    ```dotnetcli
    dotnet add package Microsoft.Quantum.Development.Kit
    ```

    <span data-ttu-id="01ebc-143">Als uw project gebruikmaakt van andere micro soft. Quantum-pakketten (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht ook uit.</span><span class="sxs-lookup"><span data-stu-id="01ebc-143">If your project uses any other Microsoft.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the command for these too.</span></span>
5. <span data-ttu-id="01ebc-144">Sla alle bestanden op en sluit deze.</span><span class="sxs-lookup"><span data-stu-id="01ebc-144">Save and close all files.</span></span>
6. <span data-ttu-id="01ebc-145">Herhaal 1-4 voor elke project afhankelijkheid en ga vervolgens terug naar de map met het hoofd project en voer het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="01ebc-145">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="01ebc-146">Als uw Q #-projecten nu zijn bijgewerkt, volgt u de onderstaande instructies om de QDK zelf bij te werken.</span><span class="sxs-lookup"><span data-stu-id="01ebc-146">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="01ebc-147">De QDK bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-147">Updating the QDK</span></span>

<span data-ttu-id="01ebc-148">Het proces voor het bijwerken van de QDK varieert, afhankelijk van uw ontwikkelings taal en-omgeving.</span><span class="sxs-lookup"><span data-stu-id="01ebc-148">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="01ebc-149">Selecteer hieronder uw ontwikkel omgeving.</span><span class="sxs-lookup"><span data-stu-id="01ebc-149">Select your development environment below.</span></span>

* [<span data-ttu-id="01ebc-150">Python: de extensie # uitbrei ding bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-150">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="01ebc-151">Jupyter-notebooks: de extensie # uitbrei ding bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-151">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="01ebc-152">Visual Studio: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-152">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="01ebc-153">VS code: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-153">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="01ebc-154">Opdracht regel en C#: Project sjablonen bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-154">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="01ebc-155">Update IQ # voor python</span><span class="sxs-lookup"><span data-stu-id="01ebc-155">Update IQ# for Python</span></span>

1. <span data-ttu-id="01ebc-156">De `iqsharp` kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-156">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="01ebc-157">Controleer de `iqsharp` versie</span><span class="sxs-lookup"><span data-stu-id="01ebc-157">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="01ebc-158">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="01ebc-158">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="01ebc-159">U hoeft zich geen zorgen te maken als uw `iqsharp` versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="01ebc-159">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="01ebc-160">Het `qsharp` pakket bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-160">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="01ebc-161">Controleer de `qsharp` versie</span><span class="sxs-lookup"><span data-stu-id="01ebc-161">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="01ebc-162">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="01ebc-162">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="01ebc-163">Voer de volgende opdracht uit vanaf de locatie van uw `.qs` bestanden</span><span class="sxs-lookup"><span data-stu-id="01ebc-163">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="01ebc-164">U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="01ebc-164">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="01ebc-165">Update IQ # voor Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="01ebc-165">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="01ebc-166">De `iqsharp` kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-166">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="01ebc-167">Controleer de `iqsharp` versie</span><span class="sxs-lookup"><span data-stu-id="01ebc-167">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="01ebc-168">De uitvoer moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="01ebc-168">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="01ebc-169">U hoeft zich geen zorgen te maken als uw `iqsharp` versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="01ebc-169">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="01ebc-170">Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="01ebc-170">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="01ebc-171">U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.</span><span class="sxs-lookup"><span data-stu-id="01ebc-171">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="01ebc-172">De QDK-extensie van Visual Studio bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-172">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="01ebc-173">De Q # Visual Studio-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-173">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="01ebc-174">Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="01ebc-174">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="01ebc-175">De update accepteren</span><span class="sxs-lookup"><span data-stu-id="01ebc-175">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="01ebc-176">De Project sjablonen worden bijgewerkt met de uitbrei ding.</span><span class="sxs-lookup"><span data-stu-id="01ebc-176">The project templates are updated with the extension.</span></span> <span data-ttu-id="01ebc-177">De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten.</span><span class="sxs-lookup"><span data-stu-id="01ebc-177">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="01ebc-178">De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="01ebc-178">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="01ebc-179">QDK-extensie voor bijwerken versus code</span><span class="sxs-lookup"><span data-stu-id="01ebc-179">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="01ebc-180">De Quantum versus code-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-180">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="01ebc-181">Opnieuw opstarten VS code</span><span class="sxs-lookup"><span data-stu-id="01ebc-181">Restart VS Code</span></span>
    - <span data-ttu-id="01ebc-182">Ga naar het tabblad **extensies**</span><span class="sxs-lookup"><span data-stu-id="01ebc-182">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="01ebc-183">Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension</span><span class="sxs-lookup"><span data-stu-id="01ebc-183">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="01ebc-184">De uitbrei ding opnieuw laden</span><span class="sxs-lookup"><span data-stu-id="01ebc-184">Reload the extension</span></span>

2. <span data-ttu-id="01ebc-185">De Quantum project sjablonen bijwerken:</span><span class="sxs-lookup"><span data-stu-id="01ebc-185">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="01ebc-186">Ga naar **View**het  ->  **opdracht palet** weer geven</span><span class="sxs-lookup"><span data-stu-id="01ebc-186">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="01ebc-187">Selecteer **Q #: Project sjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="01ebc-187">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="01ebc-188">Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat ' Project sjablonen zijn geïnstalleerd '</span><span class="sxs-lookup"><span data-stu-id="01ebc-188">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="01ebc-189">C# met behulp van het `dotnet` opdracht regel programma</span><span class="sxs-lookup"><span data-stu-id="01ebc-189">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="01ebc-190">De Quantum project sjablonen voor .NET bijwerken</span><span class="sxs-lookup"><span data-stu-id="01ebc-190">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```