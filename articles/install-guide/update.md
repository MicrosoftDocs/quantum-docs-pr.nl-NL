---
title: Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: ebf1f15d65a12c921cd3f04e4111d463d1060f8e
ms.sourcegitcommit: c93fea5980d1d46fbda1e7c7153831b9337134bf
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2019
ms.locfileid: "73463279"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="618a1-102">Het Microsoft Quantum Development Kit bijwerken (QDK)</span><span class="sxs-lookup"><span data-stu-id="618a1-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="618a1-103">Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.</span><span class="sxs-lookup"><span data-stu-id="618a1-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="618a1-104">In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="618a1-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="618a1-105">Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="618a1-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>


## <a name="updating-q-projects"></a><span data-ttu-id="618a1-106">Q #-projecten bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-106">Updating Q# Projects</span></span> 

1. <span data-ttu-id="618a1-107">Installeer eerst de nieuwste versie van de [.NET Core SDK 3,0](https://dotnet.microsoft.com/download) en voer de volgende opdracht uit in de opdracht prompt:</span><span class="sxs-lookup"><span data-stu-id="618a1-107">First, install the latest version of the [.NET Core SDK 3.0](https://dotnet.microsoft.com/download) and run the following command in the command prompt:</span></span>
```bash
dotnet --version
```
 <span data-ttu-id="618a1-108">Controleer of de uitvoer 3.0.100 of hoger is en volg de onderstaande instructies, afhankelijk van uw instellingen.</span><span class="sxs-lookup"><span data-stu-id="618a1-108">Verify the output is 3.0.100 or higher, then follow the instructions below depending on your setup.</span></span>

### <a name="in-visual-studio"></a><span data-ttu-id="618a1-109">In Visual Studio</span><span class="sxs-lookup"><span data-stu-id="618a1-109">In Visual Studio</span></span>
 
 1. <span data-ttu-id="618a1-110">Update naar de nieuwste versie van Visual Studio 2019. Zie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) voor instructies</span><span class="sxs-lookup"><span data-stu-id="618a1-110">Update to the latest version of Visual Studio 2019, see [here](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) for instructions</span></span>
 2. <span data-ttu-id="618a1-111">Open uw oplossing in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="618a1-111">Open your solution in Visual Studio</span></span>
 3. <span data-ttu-id="618a1-112">Selecteer in het menu de optie bouwen > nieuwe oplossing</span><span class="sxs-lookup"><span data-stu-id="618a1-112">From the menu, select Build > Clean Solution</span></span> 
 4. <span data-ttu-id="618a1-113">[Werk het doel raamwerk](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in elk van uw. csproj-bestanden bij naar netcoreapp 3.0 (of netstandard 2.1 als het een bibliotheek project is)</span><span class="sxs-lookup"><span data-stu-id="618a1-113">[Update the target framework](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
 5. <span data-ttu-id="618a1-114">Sla alle bestanden in uw oplossing op en sluit deze af</span><span class="sxs-lookup"><span data-stu-id="618a1-114">Save and close all files in your solution</span></span>
 6. <span data-ttu-id="618a1-115">Selecteer Extra > opdracht regel > opdracht prompt voor ontwikkel aars</span><span class="sxs-lookup"><span data-stu-id="618a1-115">Select Tools > Command Line > Developer Command Prompt</span></span>
 7. <span data-ttu-id="618a1-116">Voer voor elk project in de oplossing de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="618a1-116">For each project in the solution, run the following command:</span></span>
 ```bash
 dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
 ```
<span data-ttu-id="618a1-117">Als uw projecten andere micro soft. Quantum-pakketten gebruiken, voert u de opdracht ook uit.</span><span class="sxs-lookup"><span data-stu-id="618a1-117">If your projects use any other Microsoft.Quantum packages, run the command for these too.</span></span> 
 8. <span data-ttu-id="618a1-118">Sluit de opdracht prompt en selecteer Build > build-oplossing (Selecteer *geen* oplossing voor opnieuw samen stellen.</span><span class="sxs-lookup"><span data-stu-id="618a1-118">Close the command prompt and select Build > Build Solution (do *not* select Rebuild Solution, as rebuilding will initially fail)</span></span>

### <a name="in-visual-studio-code"></a><span data-ttu-id="618a1-119">In Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="618a1-119">In Visual Studio Code</span></span>

1. <span data-ttu-id="618a1-120">Open in Visual Studio code de map met het project dat moet worden bijgewerkt</span><span class="sxs-lookup"><span data-stu-id="618a1-120">In Visual Studio Code, open the folder containing the project to update</span></span>
1. <span data-ttu-id="618a1-121">Terminal > nieuwe terminal selecteren</span><span class="sxs-lookup"><span data-stu-id="618a1-121">Select Terminal > New Terminal</span></span>
1. <span data-ttu-id="618a1-122">Volg de instructies voor het bijwerken met behulp van de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="618a1-122">Follow the instructions for updating using the command line</span></span>

### <a name="using-the-command-line"></a><span data-ttu-id="618a1-123">Via de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="618a1-123">Using the command line</span></span>

1. <span data-ttu-id="618a1-124">Ga naar de map die het project bestand bevat</span><span class="sxs-lookup"><span data-stu-id="618a1-124">Navigate to the folder containing your project file</span></span>
2. <span data-ttu-id="618a1-125">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="618a1-125">Run the following command:</span></span>
```bash
dotnet clean [project_name].csproj
```

3. <span data-ttu-id="618a1-126">[Werk het doel raamwerk](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in elk van uw. csproj-bestanden bij naar netcoreapp 3.0 (of netstandard 2.1 als het een bibliotheek project is)</span><span class="sxs-lookup"><span data-stu-id="618a1-126">[Update the target framework](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in each of your .csproj files to netcoreapp3.0 (or netstandard2.1 if it is a library project)</span></span>
4. <span data-ttu-id="618a1-127">Voer de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="618a1-127">Run the following command:</span></span>
```bash
dotnet add package Microsoft.Quantum.Development.Kit
```
<span data-ttu-id="618a1-128">Als uw project gebruikmaakt van andere micro soft. Quantum-pakketten, voert u de opdracht ook uit.</span><span class="sxs-lookup"><span data-stu-id="618a1-128">if your project uses any other Microsoft.Quantum packages, run the command for these too.</span></span>

5. <span data-ttu-id="618a1-129">Alle bestanden opslaan en sluiten</span><span class="sxs-lookup"><span data-stu-id="618a1-129">Save and close all files</span></span>
6. <span data-ttu-id="618a1-130">Herhaal 1-4 voor elke project afhankelijkheid en ga vervolgens terug naar de map met het hoofd project en voer het volgende uit:</span><span class="sxs-lookup"><span data-stu-id="618a1-130">Repeat 1-4 for each project dependency, then navigate back to the folder containing your main project and run:</span></span>
```bash
dotnet build [project_name].csproj
```

## <a name="update-iq-for-python"></a><span data-ttu-id="618a1-131">Update IQ # voor python</span><span class="sxs-lookup"><span data-stu-id="618a1-131">Update IQ# for Python</span></span>

1. <span data-ttu-id="618a1-132">De `iqsharp`-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-132">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="618a1-133">De `iqsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="618a1-133">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="618a1-134">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="618a1-134">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```

1. <span data-ttu-id="618a1-135">Het `qsharp`-pakket bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-135">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="618a1-136">De `qsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="618a1-136">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="618a1-137">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="618a1-137">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.10.1911.307
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
1. <span data-ttu-id="618a1-138">Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden</span><span class="sxs-lookup"><span data-stu-id="618a1-138">Run the following command from the location of your `.qs` files</span></span>
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

1. <span data-ttu-id="618a1-139">U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="618a1-139">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="update-iq-for-jupyter-notebooks"></a><span data-ttu-id="618a1-140">Update IQ # voor Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="618a1-140">Update IQ# for Jupyter notebooks</span></span>

1. <span data-ttu-id="618a1-141">De `iqsharp`-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-141">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="618a1-142">De `iqsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="618a1-142">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="618a1-143">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="618a1-143">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```
1. <span data-ttu-id="618a1-144">Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:</span><span class="sxs-lookup"><span data-stu-id="618a1-144">Run the following command from a cell in your Jupyter Notebook:</span></span>
    ```
    %workspace reload
    ```

1. <span data-ttu-id="618a1-145">U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.</span><span class="sxs-lookup"><span data-stu-id="618a1-145">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="update-visual-studio-qdk-extension"></a><span data-ttu-id="618a1-146">De QDK-extensie van Visual Studio bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-146">Update Visual Studio QDK extension</span></span>

1. <span data-ttu-id="618a1-147">De Q # Visual Studio-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-147">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="618a1-148">Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="618a1-148">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="618a1-149">De update accepteren</span><span class="sxs-lookup"><span data-stu-id="618a1-149">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="618a1-150">De Project sjablonen worden bijgewerkt met de uitbrei ding.</span><span class="sxs-lookup"><span data-stu-id="618a1-150">The project templates are updated with the extension.</span></span> <span data-ttu-id="618a1-151">De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten.</span><span class="sxs-lookup"><span data-stu-id="618a1-151">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="618a1-152">De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="618a1-152">The code for your existing projects is not updated when the extension is updated.</span></span>

## <a name="update-vs-code-qdk-extension"></a><span data-ttu-id="618a1-153">QDK-extensie voor bijwerken versus code</span><span class="sxs-lookup"><span data-stu-id="618a1-153">Update VS Code QDK extension</span></span>

1. <span data-ttu-id="618a1-154">De Quantum versus code-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-154">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="618a1-155">Opnieuw opstarten VS code</span><span class="sxs-lookup"><span data-stu-id="618a1-155">Restart VS Code</span></span>
    - <span data-ttu-id="618a1-156">Ga naar het tabblad **extensies**</span><span class="sxs-lookup"><span data-stu-id="618a1-156">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="618a1-157">Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension</span><span class="sxs-lookup"><span data-stu-id="618a1-157">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="618a1-158">De uitbrei ding opnieuw laden</span><span class="sxs-lookup"><span data-stu-id="618a1-158">Reload the extension</span></span>

1. <span data-ttu-id="618a1-159">De Quantum project sjablonen bijwerken:</span><span class="sxs-lookup"><span data-stu-id="618a1-159">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="618a1-160">Ga naar **Weergave** -> **Opdrachtpalet**</span><span class="sxs-lookup"><span data-stu-id="618a1-160">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="618a1-161">Selecteer **Q #: Project sjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="618a1-161">Select **Q#: Install project templates**</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="618a1-162">C#, met behulp van het opdracht regel programma `dotnet`</span><span class="sxs-lookup"><span data-stu-id="618a1-162">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="618a1-163">De Quantum project sjablonen voor .NET bijwerken</span><span class="sxs-lookup"><span data-stu-id="618a1-163">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a><span data-ttu-id="618a1-164">En verder?</span><span class="sxs-lookup"><span data-stu-id="618a1-164">What's next?</span></span>

<span data-ttu-id="618a1-165">Nu u de Quantum Development Kit hebt bijgewerkt in uw voorkeurs omgeving, kunt u uw Quantum Programma's blijven ontwikkelen en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="618a1-165">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="618a1-166">Als u nog geen programma hebt geschreven, kunt u aan de slag met [uw eerste Quantum programma](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="618a1-166">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
