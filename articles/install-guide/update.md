---
title: De Quantum Development Kit (QDK) bijwerken
description: 'Hierin wordt beschreven hoe u uw Q #-projecten en de Microsoft Quantum Development Kit bijwerkt naar de huidige versie.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 3245f587493ce12cfec15c8f932fd092d85f688e
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327562"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="74257-103">Het Microsoft Quantum Development Kit bijwerken (QDK)</span><span class="sxs-lookup"><span data-stu-id="74257-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="74257-104">Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.</span><span class="sxs-lookup"><span data-stu-id="74257-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="74257-105">In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="74257-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="74257-106">Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="74257-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="74257-107">We raden u aan om de nieuwste versie van QDK up-to-date te houden.</span><span class="sxs-lookup"><span data-stu-id="74257-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="74257-108">Volg deze update handleiding om een upgrade uit te voeren naar de meest recente versie van QDK.</span><span class="sxs-lookup"><span data-stu-id="74257-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="74257-109">Het proces bestaat uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="74257-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="74257-110">Het bijwerken van uw bestaande Q #-bestanden en-projecten om uw code uit te lijnen met een bijgewerkte syntaxis.</span><span class="sxs-lookup"><span data-stu-id="74257-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="74257-111">De QDK voor uw gekozen ontwikkel omgeving bijwerken.</span><span class="sxs-lookup"><span data-stu-id="74257-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="74257-112">Q #-projecten bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-112">Updating Q# Projects</span></span> 

<span data-ttu-id="74257-113">Ongeacht of u C# of python gebruikt om Q #-bewerkingen te hosten, volgt u deze instructies om uw Q #-projecten bij te werken.</span><span class="sxs-lookup"><span data-stu-id="74257-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="74257-114">Controleer eerst of u de meest recente versie van de [.NET Core SDK 3,1](https://dotnet.microsoft.com/download)hebt.</span><span class="sxs-lookup"><span data-stu-id="74257-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="74257-115">Voer de volgende opdracht uit in de opdracht prompt:</span><span class="sxs-lookup"><span data-stu-id="74257-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="74257-116">Controleer of de uitvoer is `3.1.100` of hoger.</span><span class="sxs-lookup"><span data-stu-id="74257-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="74257-117">Als dat niet het geval is, installeert u de [nieuwste versie](https://dotnet.microsoft.com/download) en controleert u opnieuw.</span><span class="sxs-lookup"><span data-stu-id="74257-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="74257-118">Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio code of rechtstreeks de opdracht regel).</span><span class="sxs-lookup"><span data-stu-id="74257-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="74257-119">Update Q #-projecten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="74257-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="74257-120">Update naar de nieuwste versie van Visual Studio 2019. Zie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) voor instructies.</span><span class="sxs-lookup"><span data-stu-id="74257-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="74257-121">Open uw oplossing in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="74257-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="74257-122">Selecteer in het menu een **Build**  ->  **schone oplossing**bouwen.</span><span class="sxs-lookup"><span data-stu-id="74257-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="74257-123">Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.1` (of `netstandard2.1` als het een bibliotheek project is).</span><span class="sxs-lookup"><span data-stu-id="74257-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="74257-124">Dat wil zeggen, regels van het formulier bewerken:</span><span class="sxs-lookup"><span data-stu-id="74257-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="74257-125">[Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.</span><span class="sxs-lookup"><span data-stu-id="74257-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="74257-126">Stel in elk van de. csproj-bestanden de SDK in op `Microsoft.Quantum.Sdk` , zoals aangegeven in de onderstaande regel.</span><span class="sxs-lookup"><span data-stu-id="74257-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="74257-127">Het versie nummer moet het meest recent beschik bare zijn, en u kunt dit vaststellen door de [release opmerkingen](https://docs.microsoft.com/quantum/relnotes/)te bekijken.</span><span class="sxs-lookup"><span data-stu-id="74257-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="74257-128">Sla alle bestanden in uw oplossing op en sluit deze.</span><span class="sxs-lookup"><span data-stu-id="74257-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="74257-129">Selecteer **extra**  ->  **opdracht regel**opdracht  ->  **prompt**.</span><span class="sxs-lookup"><span data-stu-id="74257-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="74257-130">U kunt ook de pakket beheer console in Visual Studio gebruiken.</span><span class="sxs-lookup"><span data-stu-id="74257-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="74257-131">Voer voor elk project in de oplossing de volgende opdracht uit om dit pakket te **verwijderen** :</span><span class="sxs-lookup"><span data-stu-id="74257-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="74257-132">Als uw projecten gebruikmaken van andere micro soft. Quantum-of micro soft. Azure. Quantum pakketten (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht toevoegen voor deze **toepassingen** uit om de gebruikte versie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="74257-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="74257-133">Sluit de opdracht prompt en selecteer **Build**  ->  **Build Solution** (Selecteer *geen* oplossing voor opnieuw samen stellen).</span><span class="sxs-lookup"><span data-stu-id="74257-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="74257-134">U kunt nu door gaan om [uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension)bij te werken.</span><span class="sxs-lookup"><span data-stu-id="74257-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="74257-135">Update Q #-projecten in Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="74257-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="74257-136">Open in Visual Studio code de map met het project dat moet worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="74257-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="74257-137">Selecteer **Terminal**  ->  **New Terminal**.</span><span class="sxs-lookup"><span data-stu-id="74257-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="74257-138">Volg de instructies voor het bijwerken met behulp van de opdracht regel (direct hieronder).</span><span class="sxs-lookup"><span data-stu-id="74257-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="74257-139">Q #-projecten bijwerken met behulp van de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="74257-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="74257-140">Navigeer naar de map met het hoofd project bestand.</span><span class="sxs-lookup"><span data-stu-id="74257-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="74257-141">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="74257-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="74257-142">Bepaal de huidige versie van de QDK.</span><span class="sxs-lookup"><span data-stu-id="74257-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="74257-143">U kunt het vinden door de [release opmerkingen](https://docs.microsoft.com/quantum/relnotes/)te bekijken.</span><span class="sxs-lookup"><span data-stu-id="74257-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="74257-144">De versie heeft een indeling die vergelijkbaar is met `0.11.2006.207` .</span><span class="sxs-lookup"><span data-stu-id="74257-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="74257-145">In elk van uw `.csproj` bestanden gaat u als volgt te werk:</span><span class="sxs-lookup"><span data-stu-id="74257-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="74257-146">Werk het doel raamwerk bij naar `netcoreapp3.1` (of `netstandard2.1` als het een bibliotheek project is).</span><span class="sxs-lookup"><span data-stu-id="74257-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="74257-147">Dat wil zeggen, regels van het formulier bewerken:</span><span class="sxs-lookup"><span data-stu-id="74257-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="74257-148">[Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.</span><span class="sxs-lookup"><span data-stu-id="74257-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="74257-149">De verwijzing naar de SDK in de project definitie vervangen.</span><span class="sxs-lookup"><span data-stu-id="74257-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="74257-150">Zorg ervoor dat het versie nummer overeenkomt met de waarde die u in **stap 3**hebt bepaald.</span><span class="sxs-lookup"><span data-stu-id="74257-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="74257-151">Verwijder de verwijzing naar het pakket `Microsoft.Quantum.Development.Kit` indien aanwezig, dat wordt opgegeven in de volgende vermelding:</span><span class="sxs-lookup"><span data-stu-id="74257-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="74257-152">Werk de versie van de micro soft Quantum-pakketten bij naar de meest recente versie van de QDK (bepaald in **stap 3**).</span><span class="sxs-lookup"><span data-stu-id="74257-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="74257-153">Deze pakketten worden benoemd met de volgende patronen:</span><span class="sxs-lookup"><span data-stu-id="74257-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="74257-154">Verwijzingen naar pakketten hebben de volgende indeling:</span><span class="sxs-lookup"><span data-stu-id="74257-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="74257-155">Sla het bijgewerkte bestand op.</span><span class="sxs-lookup"><span data-stu-id="74257-155">Save the updated file.</span></span>

    - <span data-ttu-id="74257-156">Herstel de afhankelijkheden van het project door het volgende te doen:</span><span class="sxs-lookup"><span data-stu-id="74257-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="74257-157">Ga terug naar de map met het hoofd project en voer het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="74257-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="74257-158">Als uw Q #-projecten nu zijn bijgewerkt, volgt u de onderstaande instructies om de QDK zelf bij te werken.</span><span class="sxs-lookup"><span data-stu-id="74257-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="74257-159">De QDK bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-159">Updating the QDK</span></span>

<span data-ttu-id="74257-160">Het proces voor het bijwerken van de QDK varieert, afhankelijk van uw ontwikkelings taal en-omgeving.</span><span class="sxs-lookup"><span data-stu-id="74257-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="74257-161">Selecteer hieronder uw ontwikkel omgeving.</span><span class="sxs-lookup"><span data-stu-id="74257-161">Select your development environment below.</span></span>

* [<span data-ttu-id="74257-162">Python: de extensie # uitbrei ding bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="74257-163">Jupyter-notebooks: de extensie # uitbrei ding bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="74257-164">Visual Studio: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="74257-165">VS code: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="74257-166">Opdracht regel en C#: Project sjablonen bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="74257-167">Update IQ # voor python</span><span class="sxs-lookup"><span data-stu-id="74257-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="74257-168">De `iqsharp` kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="74257-169">Controleer de `iqsharp` versie</span><span class="sxs-lookup"><span data-stu-id="74257-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="74257-170">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="74257-170">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="74257-171">U hoeft zich geen zorgen te maken als uw `iqsharp` versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="74257-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="74257-172">Het `qsharp` pakket bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-172">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="74257-173">Controleer de `qsharp` versie</span><span class="sxs-lookup"><span data-stu-id="74257-173">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="74257-174">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="74257-174">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="74257-175">Voer de volgende opdracht uit vanaf de locatie van uw `.qs` bestanden</span><span class="sxs-lookup"><span data-stu-id="74257-175">Run the following command from the location of your `.qs` files</span></span>

    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="74257-176">U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="74257-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="74257-177">Update IQ # voor Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="74257-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="74257-178">De `iqsharp` kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="74257-179">Controleer de `iqsharp` versie</span><span class="sxs-lookup"><span data-stu-id="74257-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="74257-180">De uitvoer moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="74257-180">Your output should be similar to the following:</span></span>

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="74257-181">U hoeft zich geen zorgen te maken als uw `iqsharp` versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="74257-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="74257-182">Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="74257-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="74257-183">U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.</span><span class="sxs-lookup"><span data-stu-id="74257-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="74257-184">De QDK-extensie van Visual Studio bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="74257-185">De Q # Visual Studio-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="74257-186">Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="74257-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="74257-187">De update accepteren</span><span class="sxs-lookup"><span data-stu-id="74257-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="74257-188">De Project sjablonen worden bijgewerkt met de uitbrei ding.</span><span class="sxs-lookup"><span data-stu-id="74257-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="74257-189">De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten.</span><span class="sxs-lookup"><span data-stu-id="74257-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="74257-190">De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="74257-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="74257-191">QDK-extensie voor bijwerken versus code</span><span class="sxs-lookup"><span data-stu-id="74257-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="74257-192">De Quantum versus code-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="74257-193">Opnieuw opstarten VS code</span><span class="sxs-lookup"><span data-stu-id="74257-193">Restart VS Code</span></span>
    - <span data-ttu-id="74257-194">Ga naar het tabblad **extensies**</span><span class="sxs-lookup"><span data-stu-id="74257-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="74257-195">Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension</span><span class="sxs-lookup"><span data-stu-id="74257-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="74257-196">De uitbrei ding opnieuw laden</span><span class="sxs-lookup"><span data-stu-id="74257-196">Reload the extension</span></span>

2. <span data-ttu-id="74257-197">De Quantum project sjablonen bijwerken:</span><span class="sxs-lookup"><span data-stu-id="74257-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="74257-198">Ga naar **View**het  ->  **opdracht palet** weer geven</span><span class="sxs-lookup"><span data-stu-id="74257-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="74257-199">Selecteer **Q #: Project sjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="74257-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="74257-200">Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat ' Project sjablonen zijn geïnstalleerd '</span><span class="sxs-lookup"><span data-stu-id="74257-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="74257-201">C# met behulp van het `dotnet` opdracht regel programma</span><span class="sxs-lookup"><span data-stu-id="74257-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="74257-202">De Quantum project sjablonen voor .NET bijwerken</span><span class="sxs-lookup"><span data-stu-id="74257-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
