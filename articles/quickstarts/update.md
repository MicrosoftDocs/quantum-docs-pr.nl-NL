---
title: De Quantum Development Kit (QDK) bijwerken
description: Hierin wordt beschreven hoe u uw Q#-projecten en de Microsoft Quantum Development Kit naar de actuele versie kunt bijwerken.
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
no-loc:
- Q#
- $$v
ms.openlocfilehash: dd7360961aa728a6aa63b8d8c4e4840f5bf2afe8
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866754"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="0a0e2-103">De Microsoft Quantum Development Kit (QDK) bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-103">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="0a0e2-104">Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de meest recente versie.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-104">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="0a0e2-105">In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-105">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="0a0e2-106">Als u de QDK voor de eerste keer installeert, dient u de [installatiehandleiding](xref:microsoft.quantum.install) te raadplegen.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-106">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="0a0e2-107">We raden u aan om de QDK altijd naar de meest recente versie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-107">We recommend keeping up to date with the latest QDK release.</span></span> <span data-ttu-id="0a0e2-108">Volg deze updatehandleiding om een upgrade uit te voeren naar de meest recente versie van de QDK.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-108">Follow this update guide to upgrade to the most recent QDK version.</span></span> <span data-ttu-id="0a0e2-109">Het proces bestaat uit twee delen:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-109">The process consists of two parts:</span></span>
1. <span data-ttu-id="0a0e2-110">Uw bestaande Q#-bestanden en -projecten bijwerken om de code in overeenstemming te brengen met eventueel bijgewerkte syntaxis.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-110">Updating your existing Q# files and projects to align your code with any updated syntax.</span></span>
2. <span data-ttu-id="0a0e2-111">De QDK zelf bijwerken voor de door u gekozen ontwikkelomgeving.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-111">Updating the QDK itself for your chosen development environment.</span></span>

## <a name="updating-no-locq-projects"></a><span data-ttu-id="0a0e2-112">Q#-projecten bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-112">Updating Q# Projects</span></span> 

<span data-ttu-id="0a0e2-113">U dient deze instructies te volgen om uw Q#-projecten bij te werken, ongeacht of u C# of Python gebruikt om Q#-bewerkingen te hosten.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-113">Regardless of whether you are using C# or Python to host Q# operations, follow these instructions to update your Q# projects.</span></span>

1. <span data-ttu-id="0a0e2-114">Controleer eerst of u de meest recente versie van de [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) hebt.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-114">First, check that you have the latest version of the [.NET Core SDK 3.1](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="0a0e2-115">Voer de volgende opdracht uit in de opdrachtprompt:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-115">Run the following command in the command prompt:</span></span>

    ```dotnetcli
    dotnet --version
    ```

    <span data-ttu-id="0a0e2-116">Controleer of de uitvoer `3.1.100` of hoger is.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-116">Verify the output is `3.1.100` or higher.</span></span> <span data-ttu-id="0a0e2-117">Als dat niet het geval is, installeert u de [meest recente versie](https://dotnet.microsoft.com/download) en controleert u de uitvoer opnieuw.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-117">If not, install the [latest version](https://dotnet.microsoft.com/download) and check again.</span></span> <span data-ttu-id="0a0e2-118">Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio Code of rechtstreeks vanaf de opdrachtregel).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-118">Then follow the instructions below depending on your setup (Visual Studio, Visual Studio Code, or directly the command line).</span></span>

### <a name="update-no-locq-projects-in-visual-studio"></a><span data-ttu-id="0a0e2-119">Q#-projecten in Visual Studio bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-119">Update Q# projects in Visual Studio</span></span>
 
1. <span data-ttu-id="0a0e2-120">Voer een update uit naar de meest recente versie van Visual Studio 2019. Instructies hiervoor vindt u [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-120">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions.</span></span>
2. <span data-ttu-id="0a0e2-121">Open uw oplossing in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-121">Open your solution in Visual Studio.</span></span>
3. <span data-ttu-id="0a0e2-122">Selecteer in het menu de opties **Bouwen** -> **Oplossing opschonen**.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-122">From the menu, select **Build** -> **Clean Solution**.</span></span>
4. <span data-ttu-id="0a0e2-123">Werk in elk van uw .csproj-bestanden het doelframework bij naar `netcoreapp3.1` (of naar `netstandard2.1` als het een bibliotheekproject is).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-123">In each of your .csproj files, update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span>
    <span data-ttu-id="0a0e2-124">Dat wil zeggen dat u de regels van het formulier bewerkt:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-124">That is, edit lines of the form:</span></span>

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    <span data-ttu-id="0a0e2-125">U vindt [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) meer informatie over het opgeven van doelframeworks.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-125">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

5. <span data-ttu-id="0a0e2-126">Stel in elk van de .csproj-bestanden de SDK in op `Microsoft.Quantum.Sdk`, zoals aangegeven in de onderstaande regel.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-126">In each of the .csproj files, set the SDK to `Microsoft.Quantum.Sdk`, as indicated in the line below.</span></span> <span data-ttu-id="0a0e2-127">Het versienummer moet het meest recent beschikbare nummer zijn. U kunt dit controleren door de [releaseopmerkingen](https://docs.microsoft.com/quantum/relnotes/) te bekijken.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-127">Please notice that the version number should be the latest available, and you can determine it by reviewing the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span>

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
    ```

6. <span data-ttu-id="0a0e2-128">Sla alle bestanden in uw oplossing op en sluit deze.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-128">Save and close all files in your solution.</span></span>

7. <span data-ttu-id="0a0e2-129">Selecteer **Hulpprogramma's** -> **Opdrachtregel** -> **Opdrachtprompt voor ontwikkelaars**.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-129">Select **Tools** -> **Command Line** -> **Developer Command Prompt**.</span></span> <span data-ttu-id="0a0e2-130">U kunt echter ook de pakketbeheerconsole in Visual Studio gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-130">Alternatively, you can use the package management console in Visual Studio.</span></span>

8. <span data-ttu-id="0a0e2-131">Voer voor elk project in de oplossing de volgende opdracht uit om dit pakket te **verwijderen**:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-131">For each project in the solution, run the following command to **remove** this package:</span></span>

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   <span data-ttu-id="0a0e2-132">Als uw projecten gebruikmaken van andere Microsoft.Quantum- of Microsoft.Azure.Quantum-pakketten (bijvoorbeeld Microsoft.Quantum.Numerics), voert u de opdracht **Toevoegen** uit om de gebruikte versie bij te werken.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-132">If your projects use any other Microsoft.Quantum or Microsoft.Azure.Quantum packages (e.g. Microsoft.Quantum.Numerics), run the **add** command for these to update the version used.</span></span>

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. <span data-ttu-id="0a0e2-133">Sluit de opdrachtprompt en selecteer **Bouwen** -> **Oplossing bouwen** (selecteer *niet* de optie Oplossing opnieuw bouwen).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-133">Close the command prompt and select **Build** -> **Build Solution** (do *not* select Rebuild Solution).</span></span>

<span data-ttu-id="0a0e2-134">U kunt nu doorgaan met het [bijwerken van uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-134">You can now skip ahead to [update your Visual Studio QDK extension](#update-visual-studio-qdk-extension).</span></span>


### <a name="update-no-locq-projects-in-visual-studio-code"></a><span data-ttu-id="0a0e2-135">Q#-projecten in Visual Studio Code bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-135">Update Q# projects in Visual Studio Code</span></span>

1. <span data-ttu-id="0a0e2-136">Open in Visual Studio Code de map met het project dat moet worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-136">In Visual Studio Code, open the folder containing the project to update.</span></span>
2. <span data-ttu-id="0a0e2-137">Klik op **Terminal** -> **Nieuwe terminal**.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-137">Select **Terminal** -> **New Terminal**.</span></span>
3. <span data-ttu-id="0a0e2-138">Volg de instructies voor het bijwerken met behulp van de opdrachtregel (direct hieronder).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-138">Follow the instructions for updating using the command line (directly below).</span></span>

### <a name="update-no-locq-projects-using-the-command-line"></a><span data-ttu-id="0a0e2-139">Q#-projecten bijwerken met behulp van de opdrachtregel</span><span class="sxs-lookup"><span data-stu-id="0a0e2-139">Update Q# projects using the command line</span></span>

1. <span data-ttu-id="0a0e2-140">Navigeer naar de map met het hoofdprojectbestand.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-140">Navigate to the folder containing your main project file.</span></span>

2. <span data-ttu-id="0a0e2-141">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-141">Run the following command:</span></span>

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. <span data-ttu-id="0a0e2-142">Stel vast wat de huidige versie van de QDK is.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-142">Determine the current version of the QDK.</span></span> <span data-ttu-id="0a0e2-143">Raadpleeg hiervoor de [releaseopmerkingen](https://docs.microsoft.com/quantum/relnotes/).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-143">To find it, you can review the [release notes](https://docs.microsoft.com/quantum/relnotes/).</span></span> <span data-ttu-id="0a0e2-144">De versie heeft een indeling die vergelijkbaar is met `0.12.20072031`.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-144">The version will be in a format similar to `0.12.20072031`.</span></span>

4. <span data-ttu-id="0a0e2-145">Volg voor elk van uw `.csproj`-bestanden de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-145">In each of your `.csproj` files, go through the following steps:</span></span>

    - <span data-ttu-id="0a0e2-146">Werk het doelframework bij naar `netcoreapp3.1` (of naar `netstandard2.1` als het een bibliotheekproject is).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-146">Update the target framework to `netcoreapp3.1` (or `netstandard2.1` if it is a library project).</span></span> <span data-ttu-id="0a0e2-147">Dat wil zeggen dat u de regels van het formulier bewerkt:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-147">That is, edit lines of the form:</span></span>

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        <span data-ttu-id="0a0e2-148">U vindt [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) meer informatie over het opgeven van doelframeworks.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-148">You can find more details on specifying target frameworks [here](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks).</span></span>

    - <span data-ttu-id="0a0e2-149">Vervang de verwijzing naar de SDK in de projectdefinitie.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-149">Replace the reference to the SDK in the project definition.</span></span> <span data-ttu-id="0a0e2-150">Controleer of het versienummer overeenkomt met de waarde die is vastgesteld in **stap 3**.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-150">Make sure that the version number corresponds to the value determined in **step 3**.</span></span>

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.12.20072031">
        ```

    - <span data-ttu-id="0a0e2-151">Verwijder de verwijzing naar pakket het `Microsoft.Quantum.Development.Kit`, indien aanwezig, die wordt opgegeven in de volgende vermelding:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-151">Remove the reference to package `Microsoft.Quantum.Development.Kit` if present, which will be specified in the following entry:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - <span data-ttu-id="0a0e2-152">Werk de versie van alle Microsoft Quantum-pakketten bij naar de meest recente versie van de QDK (vastgesteld in **stap 3**).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-152">Update the version of the all the Microsoft Quantum packages to the most recently released version of the QDK (determined in **step 3**).</span></span> <span data-ttu-id="0a0e2-153">Deze pakketten krijgen een naam volgens de volgende patronen:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-153">Those packages are named with the following patterns:</span></span>

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        <span data-ttu-id="0a0e2-154">Verwijzingen naar pakketten hebben de volgende indeling:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-154">References to packages have the following format:</span></span>

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.12.20072031" />
        ```

    - <span data-ttu-id="0a0e2-155">Sla het bijgewerkte bestand op.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-155">Save the updated file.</span></span>

    - <span data-ttu-id="0a0e2-156">Herstel de afhankelijkheden van het project op de volgende wijze:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-156">Restore the dependencies of the project, by doing the following:</span></span>

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. <span data-ttu-id="0a0e2-157">Navigeer terug naar de map met uw hoofdproject en voer het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-157">Navigate back to the folder containing your main project and run:</span></span>

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

<span data-ttu-id="0a0e2-158">Nu uw Q#-projecten zijn bijgewerkt, volgt u de onderstaande instructies om de QDK zelf bij te werken.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-158">With your Q# projects now updated, follow the instructions below to update the QDK itself.</span></span>

## <a name="updating-the-qdk"></a><span data-ttu-id="0a0e2-159">De QDK bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-159">Updating the QDK</span></span>

<span data-ttu-id="0a0e2-160">Het proces voor het bijwerken van de QDK varieert afhankelijk van uw ontwikkeltaal en-omgeving.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-160">The process to update the QDK varies depending on your development language and environment.</span></span>
<span data-ttu-id="0a0e2-161">Selecteer uw ontwikkelomgeving hieronder.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-161">Select your development environment below.</span></span>

* [<span data-ttu-id="0a0e2-162">Python: het `qsharp`-pakket bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-162">Python: update the `qsharp` package</span></span>](#update-the-qsharp-python-package)
* [<span data-ttu-id="0a0e2-163">Jupyter Notebooks: de IQ#-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-163">Jupyter Notebooks: update the IQ# kernel</span></span>](#update-the-iq-jupyter-kernel)
* [<span data-ttu-id="0a0e2-164">Visual Studio: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-164">Visual Studio: update the QDK extension</span></span>](#update-visual-studio-qdk-extension)
* [<span data-ttu-id="0a0e2-165">VS Code: de QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-165">VS Code: update the QDK extension</span></span>](#update-vs-code-qdk-extension)
* [<span data-ttu-id="0a0e2-166">Opdrachtregel en C# : projectsjablonen bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-166">Command-line and C#: update project templates</span></span>](#c-using-the-dotnet-command-line-tool)


### <a name="update-the-qsharp-python-package"></a><span data-ttu-id="0a0e2-167">Het Python-pakket voor `qsharp` bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-167">Update the `qsharp` Python package</span></span>

<span data-ttu-id="0a0e2-168">De updateprocedure is afhankelijk van of u oorspronkelijk hebt geïnstalleerd met behulp van Conda of met behulp van de .NET CLI en PIP.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-168">The update procedure depends on whether you originally installed using conda or using the .NET CLI and pip.</span></span>

#### <a name="update-using-conda-recommended"></a>[<span data-ttu-id="0a0e2-169">Bijwerken met behulp van Conda (aanbevolen)</span><span class="sxs-lookup"><span data-stu-id="0a0e2-169">Update using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="0a0e2-170">Activeer de Conda-omgeving waarin u het `qsharp`-pakket hebt geïnstalleerd, en voer vervolgens deze opdracht uit om het pakket bij te werken:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-170">Activate the conda environment where you installed the `qsharp` package, and then run this command to update it:</span></span>

    ```
    conda update -c quantum-engineering qsharp
    ```

1. <span data-ttu-id="0a0e2-171">Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-171">Run the following command from the location of your `.qs` files:</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="0a0e2-172">Bijwerken met behulp van .NET CLI en PIP (geavanceerd)</span><span class="sxs-lookup"><span data-stu-id="0a0e2-172">Update using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="0a0e2-173">Werk de `iqsharp`-kernel bij</span><span class="sxs-lookup"><span data-stu-id="0a0e2-173">Update the `iqsharp` kernel</span></span> 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="0a0e2-174">Controleer de `iqsharp`-versie</span><span class="sxs-lookup"><span data-stu-id="0a0e2-174">Verify the `iqsharp` version</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="0a0e2-175">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-175">You should see the following output:</span></span>

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    <span data-ttu-id="0a0e2-176">U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-176">Don't worry if your `iqsharp` version is higher.</span></span> <span data-ttu-id="0a0e2-177">Dit komt overeen met de [meest recente release](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-177">It should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

1. <span data-ttu-id="0a0e2-178">Werk het `qsharp`-pakket bij:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-178">Update the `qsharp` package:</span></span>

    ```
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="0a0e2-179">Controleer de `qsharp`-versie:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-179">Verify the `qsharp` version:</span></span>

    ```
    pip show qsharp
    ```

    <span data-ttu-id="0a0e2-180">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-180">You should see the following output:</span></span>

    ```
    Name: qsharp
    Version: 0.12.2007.2031
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. <span data-ttu-id="0a0e2-181">Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-181">Run the following command from the location of your `.qs` files:</span></span>

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

***

<span data-ttu-id="0a0e2-182">U kunt nu het bijgewerkte Python-pakket voor `qsharp` gebruiken om uw bestaande kwantumprogramma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-182">You can now use the updated `qsharp` Python package to run your existing quantum programs.</span></span>

### <a name="update-the-ino-locq-jupyter-kernel"></a><span data-ttu-id="0a0e2-183">De IQ# Jupyter-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-183">Update the IQ# Jupyter kernel</span></span>

<span data-ttu-id="0a0e2-184">De updateprocedure is afhankelijk van of u oorspronkelijk hebt geïnstalleerd met behulp van Conda of met behulp van de .NET CLI en PIP.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-184">The update procedure depends on whether you originally installed using conda or using the .NET CLI and pip.</span></span>

#### <a name="update-using-conda-recommended"></a>[<span data-ttu-id="0a0e2-185">Bijwerken met behulp van Conda (aanbevolen)</span><span class="sxs-lookup"><span data-stu-id="0a0e2-185">Update using conda (recommended)</span></span>](#tab/tabid-conda)

1. <span data-ttu-id="0a0e2-186">Activeer de Conda-omgeving waarin u het `qsharp`-pakket hebt geïnstalleerd, en voer vervolgens deze opdracht uit om het pakket bij te werken:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-186">Activate the conda environment where you installed the `qsharp` package, and then run this command to update it:</span></span>

    ```
    conda update -c quantum-engineering qsharp
    ```

1. <span data-ttu-id="0a0e2-187">Voer de volgende opdracht uit vanuit een cel in al uw bestaande Q# Jupyter Notebooks:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-187">Run the following command from a cell in each of your existing Q# Jupyter Notebooks:</span></span>

    ```
    %workspace reload
    ```

#### <a name="update-using-net-cli-and-pip-advanced"></a>[<span data-ttu-id="0a0e2-188">Bijwerken met behulp van .NET CLI en PIP (geavanceerd)</span><span class="sxs-lookup"><span data-stu-id="0a0e2-188">Update using .NET CLI and pip (advanced)</span></span>](#tab/tabid-dotnetcli)

1. <span data-ttu-id="0a0e2-189">Werk het pakket `Microsoft.Quantum.IQSharp` bij:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-189">Update the `Microsoft.Quantum.IQSharp` package:</span></span>

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="0a0e2-190">Controleer de versie `iqsharp`:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-190">Verify the `iqsharp` version:</span></span>

    ```dotnetcli
    dotnet iqsharp --version
    ```

    <span data-ttu-id="0a0e2-191">Uw uitvoer moet er als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-191">Your output should be similar to the following:</span></span>

    ```
    iqsharp: 0.12.20072031
    Jupyter Core: 1.4.0.0
    ```

    <span data-ttu-id="0a0e2-192">U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-192">Don't worry if your `iqsharp` version is higher.</span></span> <span data-ttu-id="0a0e2-193">Dit komt overeen met de [meest recente release](xref:microsoft.quantum.relnotes).</span><span class="sxs-lookup"><span data-stu-id="0a0e2-193">It should match the [latest release](xref:microsoft.quantum.relnotes).</span></span>

1. <span data-ttu-id="0a0e2-194">Voer de volgende opdracht uit vanuit een cel in al uw bestaande Q# Jupyter Notebooks:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-194">Run the following command from a cell in each of your existing Q# Jupyter Notebooks:</span></span>

    ```
    %workspace reload
    ```

***

<span data-ttu-id="0a0e2-195">U kunt nu de bijgewerkte IQ#-kernel gebruiken om uw bestaande Q# Jupyter Notebooks uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-195">You can now use the updated IQ# kernel to run your existing Q# Jupyter Notebooks.</span></span>

### <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="0a0e2-196">De Visual Studio QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-196">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="0a0e2-197">De Q# Visual Studio-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-197">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="0a0e2-198">Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="0a0e2-198">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="0a0e2-199">Accepteer de update</span><span class="sxs-lookup"><span data-stu-id="0a0e2-199">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a0e2-200">De projectsjablonen worden bijgewerkt met de extensie.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-200">The project templates are updated with the extension.</span></span> <span data-ttu-id="0a0e2-201">De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-201">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="0a0e2-202">De code voor uw bestaande projecten wordt niet bijgewerkt als de extensie wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0a0e2-202">The code for your existing projects is not updated when the extension is updated.</span></span>

### <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="0a0e2-203">De VS Code QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-203">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="0a0e2-204">Werk de Quantum VS Code-extensie bij</span><span class="sxs-lookup"><span data-stu-id="0a0e2-204">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="0a0e2-205">Start VS Code opnieuw</span><span class="sxs-lookup"><span data-stu-id="0a0e2-205">Restart VS Code</span></span>
    - <span data-ttu-id="0a0e2-206">Navigeer naar het tabblad **Extensies**</span><span class="sxs-lookup"><span data-stu-id="0a0e2-206">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="0a0e2-207">Selecteer de **Microsoft Quantum Development Kit voor de Visual Studio Code**-extensie</span><span class="sxs-lookup"><span data-stu-id="0a0e2-207">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="0a0e2-208">Laad de extensie opnieuw</span><span class="sxs-lookup"><span data-stu-id="0a0e2-208">Reload the extension</span></span>

### <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="0a0e2-209">C#, met behulp van het `dotnet`-opdrachtregelprogramma</span><span class="sxs-lookup"><span data-stu-id="0a0e2-209">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="0a0e2-210">Werk de Quantum-projectsjablonen voor .NET bij</span><span class="sxs-lookup"><span data-stu-id="0a0e2-210">Update the Quantum project templates for .NET</span></span>

    <span data-ttu-id="0a0e2-211">Vanaf de opdrachtregel:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-211">From the command line:</span></span>

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

   <span data-ttu-id="0a0e2-212">Als u van plan bent om de opdrachtregelsjablonen te gebruiken en u de VS Code QDK-extensie al hebt geïnstalleerd, kunt u de projectsjablonen ook bijwerken vanuit de extensie zelf:</span><span class="sxs-lookup"><span data-stu-id="0a0e2-212">Alternatively, if you intend to use the command line templates, and already have the VS Code QDK extension installed, you can update the project templates from the extension itself:</span></span>

   - [<span data-ttu-id="0a0e2-213">De QDK-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="0a0e2-213">Update the QDK extension</span></span>](#update-vs-code-qdk-extension)
   - <span data-ttu-id="0a0e2-214">Ga in VS Code naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="0a0e2-214">In VS Code, go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="0a0e2-215">Selecteer **Q#: Projectsjablonen voor opdrachtregel installeren**</span><span class="sxs-lookup"><span data-stu-id="0a0e2-215">Select **Q#: Install command line project templates**</span></span>
   - <span data-ttu-id="0a0e2-216">Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat de projectsjablonen zijn geïnstalleerd</span><span class="sxs-lookup"><span data-stu-id="0a0e2-216">After a few seconds you should get a popup confirming "project templates installed successfully"</span></span>
