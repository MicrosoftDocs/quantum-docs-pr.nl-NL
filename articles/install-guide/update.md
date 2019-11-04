---
title: Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: fc430a77f88878437e662c5b54507f70f3c6e020
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2019
ms.locfileid: "73185848"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="163b5-102">Het Microsoft Quantum Development Kit bijwerken (QDK)</span><span class="sxs-lookup"><span data-stu-id="163b5-102">Update the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="163b5-103">Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.</span><span class="sxs-lookup"><span data-stu-id="163b5-103">Learn how to update the Microsoft Quantum Development Kit (QDK) to the latest version.</span></span>

<span data-ttu-id="163b5-104">In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="163b5-104">This article assumes that you already have the QDK installed.</span></span> <span data-ttu-id="163b5-105">Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).</span><span class="sxs-lookup"><span data-stu-id="163b5-105">If you are installing for the first time, then please refer to the [installation guide](xref:microsoft.quantum.install).</span></span>

<span data-ttu-id="163b5-106">De update stappen zijn afhankelijk van uw ontwikkel omgeving.</span><span class="sxs-lookup"><span data-stu-id="163b5-106">The update steps depend on your development environment.</span></span> <span data-ttu-id="163b5-107">Kies uw omgeving in de volgende secties.</span><span class="sxs-lookup"><span data-stu-id="163b5-107">Choose your environment from the following sections.</span></span>

## <a name="python"></a><span data-ttu-id="163b5-108">Python</span><span class="sxs-lookup"><span data-stu-id="163b5-108">Python</span></span>

1. <span data-ttu-id="163b5-109">De `iqsharp`-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-109">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="163b5-110">De `iqsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="163b5-110">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="163b5-111">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="163b5-111">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="163b5-112">Het `qsharp`-pakket bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-112">Update the `qsharp` package</span></span>

    ```bash
    pip install qsharp --upgrade
    ```

1. <span data-ttu-id="163b5-113">De `qsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="163b5-113">Verify the `qsharp` version</span></span>

    ```bash
    pip show qsharp
    ```

    <span data-ttu-id="163b5-114">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="163b5-114">You should see the following output:</span></span>

    ```bash
    Name: qsharp
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. <span data-ttu-id="163b5-115">U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="163b5-115">You can now use the updated QDK version to run your existing quantum programs.</span></span>

## <a name="jupyter-notebooks"></a><span data-ttu-id="163b5-116">Jupyter-notebooks</span><span class="sxs-lookup"><span data-stu-id="163b5-116">Jupyter notebooks</span></span>

1. <span data-ttu-id="163b5-117">De `iqsharp`-kernel bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-117">Update the `iqsharp` kernel</span></span>

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. <span data-ttu-id="163b5-118">De `iqsharp` versie controleren</span><span class="sxs-lookup"><span data-stu-id="163b5-118">Verify the `iqsharp` version</span></span>

    ```bash
    dotnet iqsharp --version
    ```

    <span data-ttu-id="163b5-119">In dat geval moet de volgende uitvoer worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="163b5-119">You should see the following output:</span></span>

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. <span data-ttu-id="163b5-120">U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.</span><span class="sxs-lookup"><span data-stu-id="163b5-120">You can now open an existing Jupyter notebook and run it with the updated QDK.</span></span>

## <a name="c-on-windows-using-visual-studio"></a><span data-ttu-id="163b5-121">C#in Windows met Visual Studio</span><span class="sxs-lookup"><span data-stu-id="163b5-121">C# on Windows, using Visual Studio</span></span>

1. <span data-ttu-id="163b5-122">De Q # Visual Studio-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-122">Update the Q# Visual Studio extension</span></span>

    - <span data-ttu-id="163b5-123">Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span><span class="sxs-lookup"><span data-stu-id="163b5-123">Visual Studio prompts you to accept updates to the [Quantum Visual Studio extension](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)</span></span>
    - <span data-ttu-id="163b5-124">De update accepteren</span><span class="sxs-lookup"><span data-stu-id="163b5-124">Accept the update</span></span>

    > [!NOTE]
    > <span data-ttu-id="163b5-125">De Project sjablonen worden bijgewerkt met de uitbrei ding.</span><span class="sxs-lookup"><span data-stu-id="163b5-125">The project templates are updated with the extension.</span></span> <span data-ttu-id="163b5-126">De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten.</span><span class="sxs-lookup"><span data-stu-id="163b5-126">The updated templates apply to newly created projects only.</span></span> <span data-ttu-id="163b5-127">De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="163b5-127">The code for your existing projects is not updated when the extension is updated.</span></span>

1. <span data-ttu-id="163b5-128">De QDK-pakketten bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-128">Update the QDK packages</span></span>

    - <span data-ttu-id="163b5-129">Een bestaande toepassing openen</span><span class="sxs-lookup"><span data-stu-id="163b5-129">Open an existing application</span></span>
    - <span data-ttu-id="163b5-130">**Afhankelijkheden** selecteren in het Solution Explorer</span><span class="sxs-lookup"><span data-stu-id="163b5-130">Select **Dependencies** in the Solution Explorer</span></span>
    - <span data-ttu-id="163b5-131">Selecteer **NuGet-pakketten beheren**</span><span class="sxs-lookup"><span data-stu-id="163b5-131">Select **Manage NuGet Packages**</span></span>
    - <span data-ttu-id="163b5-132">De **micro soft. Quantum** -pakketten bijwerken naar de nieuwste versie</span><span class="sxs-lookup"><span data-stu-id="163b5-132">Update the **Microsoft.Quantum** packages to the latest version</span></span>

1. <span data-ttu-id="163b5-133">U kunt nu uw toepassing uitvoeren met de nieuwste QDK.</span><span class="sxs-lookup"><span data-stu-id="163b5-133">You can now run your application with the latest QDK.</span></span>

## <a name="c-using-vs-code"></a><span data-ttu-id="163b5-134">C#, met behulp van VS code</span><span class="sxs-lookup"><span data-stu-id="163b5-134">C#, using VS Code</span></span>

1. <span data-ttu-id="163b5-135">De Quantum versus code-extensie bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-135">Update the Quantum VS Code extension</span></span>

    - <span data-ttu-id="163b5-136">Opnieuw opstarten VS code</span><span class="sxs-lookup"><span data-stu-id="163b5-136">Restart VS Code</span></span>
    - <span data-ttu-id="163b5-137">Ga naar het tabblad **extensies**</span><span class="sxs-lookup"><span data-stu-id="163b5-137">Navigate to the **Extensions** tab</span></span>
    - <span data-ttu-id="163b5-138">Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension</span><span class="sxs-lookup"><span data-stu-id="163b5-138">Select the **Microsoft Quantum Development Kit for Visual Studio Code** extension</span></span>
    - <span data-ttu-id="163b5-139">De uitbrei ding opnieuw laden</span><span class="sxs-lookup"><span data-stu-id="163b5-139">Reload the extension</span></span>

1. <span data-ttu-id="163b5-140">De Quantum project sjablonen bijwerken:</span><span class="sxs-lookup"><span data-stu-id="163b5-140">Update the Quantum project templates:</span></span>

   - <span data-ttu-id="163b5-141">Ga naar **weer gave** -> - **opdracht palet**</span><span class="sxs-lookup"><span data-stu-id="163b5-141">Go to **View** -> **Command Palette**</span></span>
   - <span data-ttu-id="163b5-142">Selecteer **Q #: Project sjablonen installeren**</span><span class="sxs-lookup"><span data-stu-id="163b5-142">Select **Q#: Install project templates**</span></span>

1. <span data-ttu-id="163b5-143">Een bestaande toepassing openen in VS code</span><span class="sxs-lookup"><span data-stu-id="163b5-143">Open an existing application in VS Code</span></span>

   - <span data-ttu-id="163b5-144">Bewerk het. csproj-bestand om de nieuwe pakket versies toe te voegen</span><span class="sxs-lookup"><span data-stu-id="163b5-144">Edit the .csproj file to add the new package versions</span></span>

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    <span data-ttu-id="163b5-145">Als u andere `Microsoft.Quantum`-pakketten gebruikt, werkt u deze ook bij.</span><span class="sxs-lookup"><span data-stu-id="163b5-145">If you use other `Microsoft.Quantum` packages, update these too.</span></span>

1. <span data-ttu-id="163b5-146">U kunt nu uw toepassing uitvoeren met de bijgewerkte QDK</span><span class="sxs-lookup"><span data-stu-id="163b5-146">You can now run your application with the updated QDK</span></span>

## <a name="c-using-the-dotnet-command-line-tool"></a><span data-ttu-id="163b5-147">C#, met behulp van het opdracht regel programma `dotnet`</span><span class="sxs-lookup"><span data-stu-id="163b5-147">C#, using the `dotnet` command-line tool</span></span>

1. <span data-ttu-id="163b5-148">De Quantum project sjablonen voor .NET bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-148">Update the Quantum project templates for .NET</span></span>

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. <span data-ttu-id="163b5-149">Een bestaande toepassing bijwerken en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="163b5-149">Update and run an existing application</span></span>

    - <span data-ttu-id="163b5-150">De versie van het QDK-pakket in uw toepassing bijwerken</span><span class="sxs-lookup"><span data-stu-id="163b5-150">Update the QDK package versions in your application</span></span>

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        <span data-ttu-id="163b5-151">Als uw toepassing andere `Microsoft.Quantum`-pakketten gebruikt, werkt u deze ook bij.</span><span class="sxs-lookup"><span data-stu-id="163b5-151">If your application uses any other `Microsoft.Quantum` packages, update these too.</span></span>

    - <span data-ttu-id="163b5-152">De toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="163b5-152">Run the application</span></span>

        ```bash
        dotnet run
        ```

    - <span data-ttu-id="163b5-153">Uw toepassing wordt uitgevoerd met de nieuwe pakket versies</span><span class="sxs-lookup"><span data-stu-id="163b5-153">Your application will run with the new package versions</span></span>

## <a name="whats-next"></a><span data-ttu-id="163b5-154">En verder?</span><span class="sxs-lookup"><span data-stu-id="163b5-154">What's next?</span></span>

<span data-ttu-id="163b5-155">Nu u de Quantum Development Kit hebt bijgewerkt in uw voorkeurs omgeving, kunt u uw Quantum Programma's blijven ontwikkelen en uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="163b5-155">Now that you have updated the Quantum Development Kit in your preferred environment, you can continue to develop and run your quantum programs.</span></span> <span data-ttu-id="163b5-156">Als u nog geen programma hebt geschreven, kunt u aan de slag met [uw eerste Quantum programma](xref:microsoft.quantum.write-program).</span><span class="sxs-lookup"><span data-stu-id="163b5-156">If you have not written a program yet, you can get started with [your first quantum program](xref:microsoft.quantum.write-program).</span></span>
