---
title: De Quantum Development Kit (QDK) bijwerken
description: Hierin wordt beschreven hoe u uw Q#-projecten en de Microsoft Quantum Development Kit naar de actuele versie kunt bijwerken.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 8d39716c4d4c96ad87862b4b185895aab66cd210
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274045"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="38be3-103">De Microsoft Quantum Development Kit (QDK) bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="38be3-104">Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de meest recente versie.</span><span class="sxs-lookup"><span data-stu-id="38be3-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="38be3-105">In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="38be3-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="38be3-106">Als u de QDK voor de eerste keer installeert, dient u de [installatiehandleiding](xref:microsoft.quantum.install) te raadplegen.</span><span class="sxs-lookup"><span data-stu-id="38be3-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="38be3-107">We raden u aan om de QDK altijd naar de meest recente versie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="38be3-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="38be3-108">Volg deze updatehandleiding om een upgrade uit te voeren naar de meest recente versie van de QDK.</span><span class="sxs-lookup"><span data-stu-id="38be3-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="38be3-109">Het proces bestaat uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="38be3-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="38be3-110">Uw bestaande Q#-bestanden en -projecten bijwerken om de code uit te lijnen met eventueel bijgewerkte syntaxis.</span><span class="sxs-lookup"><span data-stu-id="38be3-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="38be3-111">De QDK zelf bijwerken voor de door u gekozen ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="38be3-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-q-projects"></a><span data-ttu-id="38be3-112">Q#-projecten bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-112">Updating Q# Projects</span></span> 

<span data-ttu-id="38be3-113">U dient deze instructies te volgen om uw Q#-projecten bij te werken, ongeacht of u C# of Python gebruikt om Q#-bewerkingen te hosten.</span><span class="sxs-lookup"><span data-stu-id="38be3-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="38be3-114">Controleer eerst of u de meest recente versie van de [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) hebt.</span><span class="sxs-lookup"><span data-stu-id="38be3-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="38be3-115">Voer de volgende opdracht uit in de opdrachtprompt:</span><span class="sxs-lookup"><span data-stu-id="38be3-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="38be3-116">Controleer of de uitvoer `3.1.100` of hoger is.</span><span class="sxs-lookup"><span data-stu-id="38be3-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="38be3-117">Als dat niet het geval is, installeert u de [meest recente versie](https://dotnet.microsoft.com/download) en controleert u de uitvoer opnieuw.</span><span class="sxs-lookup"><span data-stu-id="38be3-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="38be3-118">Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio Code of rechtstreeks vanaf de opdrachtregel).</span><span class="sxs-lookup"><span data-stu-id="38be3-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-q-projects-in-visual-studio"></a><span data-ttu-id="38be3-119">Q#-projecten in Visual Studio bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="38be3-120">Voer een update uit naar de meest recente versie van Visual Studio 2019. Instructies hiervoor vindt u [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="38be3-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="38be3-121">Open uw oplossing in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38be3-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="38be3-122">Selecteer in het menu de opties **Bouwen** -> **Oplossing opschonen**.</span><span class="sxs-lookup"><span data-stu-id="38be3-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="38be3-123">Werk in elk van uw .csproj-bestanden het doelframework bij naar `netcoreapp3.1` (of naar `netstandard2.1` als het een bibliotheekproject is).</span><span class="sxs-lookup"><span data-stu-id="38be3-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="38be3-124">Dat wil zeggen dat u de regels van het formulier bewerkt:</span><span class="sxs-lookup"><span data-stu-id="38be3-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="38be3-125">U vindt [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) meer informatie over het opgeven van doelframeworks.</span><span class="sxs-lookup"><span data-stu-id="38be3-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="38be3-126">Stel in elk van de .csproj-bestanden de SDK in op `Microsoft.Quantum.Sdk`, zoals aangegeven in de onderstaande regel.</span><span class="sxs-lookup"><span data-stu-id="38be3-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="38be3-127">Het versienummer moet het meest recent beschikbare nummer zijn. U kunt dit controleren door de [releaseopmerkingen](https://docs.microsoft.com/quantum/relnotes/) te bekijken.</span><span class="sxs-lookup"><span data-stu-id="38be3-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. <span data-ttu-id="38be3-128">Sla alle bestanden in uw oplossing op en sluit deze.</span><span class="sxs-lookup"><span data-stu-id="38be3-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="38be3-129">Selecteer **Hulpprogramma's** -> **Opdrachtregel** -> **Opdrachtprompt voor ontwikkelaars**.</span><span class="sxs-lookup"><span data-stu-id="38be3-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="38be3-130">U kunt echter ook de pakketbeheerconsole in Visual Studio gebruiken.</span><span class="sxs-lookup"><span data-stu-id="38be3-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="38be3-131">Voer voor elk project in de oplossing de volgende opdracht uit om dit pakket te **verwijderen**:</span><span class="sxs-lookup"><span data-stu-id="38be3-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="38be3-132">Als uw projecten gebruikmaken van andere Microsoft.Quantum- of Microsoft.Azure.Quantum-pakketten (bijvoorbeeld Microsoft.Quantum.Numerics), voert u de opdracht **Toevoegen** uit om de gebruikte versie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="38be3-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="38be3-133">Sluit de opdrachtprompt en selecteer **Bouwen** -> **Oplossing bouwen** (selecteer *niet* de optie Oplossing opnieuw bouwen).</span><span class="sxs-lookup"><span data-stu-id="38be3-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="38be3-134">U kunt nu doorgaan met het [bijwerken van uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="38be3-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-q-projects-in-visual-studio-code"></a><span data-ttu-id="38be3-135">Q#-projecten in Visual Studio Code bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="38be3-136">Open in Visual Studio Code de map met het project dat moet worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="38be3-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="38be3-137">Klik op **Terminal** -> **Nieuwe terminal**.</span><span class="sxs-lookup"><span data-stu-id="38be3-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="38be3-138">Volg de instructies voor het bijwerken met behulp van de opdrachtregel (direct hieronder).</span><span class="sxs-lookup"><span data-stu-id="38be3-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-q-projects-using-the-command-line"></a><span data-ttu-id="38be3-139">Q#-projecten bijwerken met behulp van de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="38be3-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="38be3-140">Navigeer naar de map met het hoofdprojectbestand.</span><span class="sxs-lookup"><span data-stu-id="38be3-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="38be3-141">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="38be3-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="38be3-142">Stel vast wat de huidige versie van de QDK is.</span><span class="sxs-lookup"><span data-stu-id="38be3-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="38be3-143">Raadpleeg hiervoor de [releaseopmerkingen](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="38be3-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="38be3-144">De versie heeft een indeling die vergelijkbaar is met `0.11.2006.207`.</span><span class="sxs-lookup"><span data-stu-id="38be3-144">The version will be in a format similar to `0.11.2006.207`.</span></span>

4. <span data-ttu-id="38be3-145">Volg voor elk van uw `.csproj`-bestanden de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="38be3-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="38be3-146">Werk het doelframework bij naar `netcoreapp3.1` (of naar `netstandard2.1` als het een bibliotheekproject is).</span><span class="sxs-lookup"><span data-stu-id="38be3-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="38be3-147">Dat wil zeggen dat u de regels van het formulier bewerkt:</span><span class="sxs-lookup"><span data-stu-id="38be3-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="38be3-148">U vindt [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) meer informatie over het opgeven van doelframeworks.</span><span class="sxs-lookup"><span data-stu-id="38be3-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="38be3-149">Vervang de verwijzing naar de SDK in de projectdefinitie.</span><span class="sxs-lookup"><span data-stu-id="38be3-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="38be3-150">Controleer of het versienummer overeenkomt met de waarde die is vastgesteld in **stap 3**.</span><span class="sxs-lookup"><span data-stu-id="38be3-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - <span data-ttu-id="38be3-151">Verwijder de verwijzing naar pakket het `Microsoft.Quantum.Development.Kit`, indien aanwezig, die wordt opgegeven in de volgende vermelding:</span><span class="sxs-lookup"><span data-stu-id="38be3-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="38be3-152">Werk de versie van alle Microsoft Quantum-pakketten bij naar de meest recente versie van de QDK (vastgesteld in **stap 3**).</span><span class="sxs-lookup"><span data-stu-id="38be3-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="38be3-153">Deze pakketten krijgen een naam volgens de volgende patronen:</span><span class="sxs-lookup"><span data-stu-id="38be3-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="38be3-154">Verwijzingen naar pakketten hebben de volgende indeling:</span><span class="sxs-lookup"><span data-stu-id="38be3-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - <span data-ttu-id="38be3-155">Sla het bijgewerkte bestand op.</span><span class="sxs-lookup"><span data-stu-id="38be3-155">Save the updated file.</span></span>

    - <span data-ttu-id="38be3-156">Herstel de afhankelijkheden van het project op de volgende wijze:</span><span class="sxs-lookup"><span data-stu-id="38be3-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="38be3-157">Navigeer terug naar de map met uw hoofdproject en voer het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="38be3-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="38be3-158">Nu uw Q#-projecten zijn bijgewerkt, volgt u de onderstaande instructies om de QDK zelf bij te werken.</span><span class="sxs-lookup"><span data-stu-id="38be3-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="38be3-159">De QDK bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-159">Updating the QDK</span></span>

<span data-ttu-id="38be3-160">Het proces voor het bijwerken van de QDK varieert afhankelijk van uw ontwikkeltaal en-omgeving.</span><span class="sxs-lookup"><span data-stu-id="38be3-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="38be3-161">Selecteer uw ontwikkelomgeving hieronder.</span><span class="sxs-lookup"><span data-stu-id="38be3-161">Select your development environment below.</span></span>

* [<span data-ttu-id="38be3-162">Python: de IQ#-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-162">Python: update the IQ# extension</span></span>](#update-iq-for-python)
* [<span data-ttu-id="38be3-163">Jupyter Notebooks: de IQ#-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-163">Jupyter Notebooks: update the IQ# extension</span></span>](#update-iq-for-jupyter-notebooks)
* [<span data-ttu-id="38be3-164">Visual Studio: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="38be3-165">VS Code: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="38be3-166">Opdrachtregel en C# : projectsjablonen bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a><span data-ttu-id="38be3-167">IQ# voor Python bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-167">Update IQ# for Python</span></span>

1. <span data-ttu-id="38be3-168">Werk de `iqsharp`-kernel bij</span><span class="sxs-lookup"><span data-stu-id="38be3-168">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="38be3-169">Controleer de `iqsharp`-versie</span><span class="sxs-lookup"><span data-stu-id="38be3-169">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="38be3-170">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="38be3-170">You should see the following output:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="38be3-171">U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is; deze moet overeenkomen met de [nieuwste release](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="38be3-171">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="38be3-172">Werk het `qsharp`-pakket bij</span><span class="sxs-lookup"><span data-stu-id="38be3-172">Update the `qsharp` package</span></span>

    ```
    pip install qsharp --upgrade
    ```

4. <span data-ttu-id="38be3-173">Controleer de `qsharp`-versie</span><span class="sxs-lookup"><span data-stu-id="38be3-173">Verify the `qsharp` version</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="38be3-174">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="38be3-174">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. <span data-ttu-id="38be3-175">Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden</span><span class="sxs-lookup"><span data-stu-id="38be3-175">Run the following command from the location of your `.qs` files</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. <span data-ttu-id="38be3-176">U kunt nu de bijgewerkte versie van de QDK gebruiken om uw bestaande kwantumprogramma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="38be3-176">You can now use the updated QDK version to run your existing quantum programs.</span></span>

### <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="38be3-177">IQ# voor Jupyter Notebooks bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-177">Update IQ# for Jupyter Notebooks</span></span>

1. <span data-ttu-id="38be3-178">Werk de `iqsharp`-kernel bij</span><span class="sxs-lookup"><span data-stu-id="38be3-178">Update the `iqsharp` kernel</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. <span data-ttu-id="38be3-179">Controleer de `iqsharp`-versie</span><span class="sxs-lookup"><span data-stu-id="38be3-179">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="38be3-180">Uw uitvoer moet er als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="38be3-180">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    <span data-ttu-id="38be3-181">U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is; deze moet overeenkomen met de [nieuwste release](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="38be3-181">Don't worry if your `iqsharp` version is higher, it should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

3. <span data-ttu-id="38be3-182">Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="38be3-182">Run the following command from a cell in your Jupyter Notebook:</span></span>

    ```
    %workspace reload
    ```

4. <span data-ttu-id="38be3-183">U kunt nu een bestaand Jupyter Notebook openen en dit uitvoeren met de bijgewerkte QDK.</span><span class="sxs-lookup"><span data-stu-id="38be3-183">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="38be3-184">De Visual Studio QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-184">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="38be3-185">Werk de Q# Visual Studio-extensie bij</span><span class="sxs-lookup"><span data-stu-id="38be3-185">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="38be3-186">Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="38be3-186">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="38be3-187">Accepteer de update</span><span class="sxs-lookup"><span data-stu-id="38be3-187">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="38be3-188">De projectsjablonen worden bijgewerkt met de extensie.</span><span class="sxs-lookup"><span data-stu-id="38be3-188">The project templates are updated with the extension.</span></span> <span data-ttu-id="38be3-189">De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten.</span><span class="sxs-lookup"><span data-stu-id="38be3-189">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="38be3-190">De code voor uw bestaande projecten wordt niet bijgewerkt als de extensie wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="38be3-190">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="38be3-191">De VS Code QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="38be3-191">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="38be3-192">Werk de Quantum VS Code-extensie bij</span><span class="sxs-lookup"><span data-stu-id="38be3-192">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="38be3-193">Start VS Code opnieuw</span><span class="sxs-lookup"><span data-stu-id="38be3-193">Restart VS Code</span></span>
    - <span data-ttu-id="38be3-194">Navigeer naar het tabblad **Extensies**</span><span class="sxs-lookup"><span data-stu-id="38be3-194">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="38be3-195">Selecteer de **Microsoft Quantum Development Kit voor de Visual Studio Code**-extensie</span><span class="sxs-lookup"><span data-stu-id="38be3-195">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="38be3-196">Laad de extensie opnieuw</span><span class="sxs-lookup"><span data-stu-id="38be3-196">Reload the extension</span></span>

2. <span data-ttu-id="38be3-197">Werk de Quantum-projectsjablonen bij:</span><span class="sxs-lookup"><span data-stu-id="38be3-197">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="38be3-198">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="38be3-198">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="38be3-199">Selecteer **Q#: Projectsjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="38be3-199">Select **Q#: Install project templates**</span></span>
   - <span data-ttu-id="38be3-200">Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat de projectsjablonen zijn geïnstalleerd</span><span class="sxs-lookup"><span data-stu-id="38be3-200">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="38be3-201">C#, met behulp van het `dotnet`-opdrachtregelprogramma</span><span class="sxs-lookup"><span data-stu-id="38be3-201">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="38be3-202">Werk de Quantum-projectsjablonen voor .NET bij</span><span class="sxs-lookup"><span data-stu-id="38be3-202">Update the Quantum project templates for .NET</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
