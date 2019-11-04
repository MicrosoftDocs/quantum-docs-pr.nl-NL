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
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Het Microsoft Quantum Development Kit bijwerken (QDK)

Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.

In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd. Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).

De update stappen zijn afhankelijk van uw ontwikkel omgeving. Kies uw omgeving in de volgende secties.

## <a name="python"></a>Python

1. De `iqsharp`-kernel bijwerken

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. De `iqsharp` versie controleren

    ```bash
    dotnet iqsharp --version
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. Het `qsharp`-pakket bijwerken

    ```bash
    pip install qsharp --upgrade
    ```

1. De `qsharp` versie controleren

    ```bash
    pip show qsharp
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```bash
    Name: qsharp
    Version: 0.9.1909.3002
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

1. U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.

## <a name="jupyter-notebooks"></a>Jupyter-notebooks

1. De `iqsharp`-kernel bijwerken

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. De `iqsharp` versie controleren

    ```bash
    dotnet iqsharp --version
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```bash
    iqsharp: 0.9.1909.3002
    Jupyter Core: 1.1.18837.0
    ```

1. U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.

## <a name="c-on-windows-using-visual-studio"></a>C#in Windows met Visual Studio

1. De Q # Visual Studio-extensie bijwerken

    - Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - De update accepteren

    > [!NOTE]
    > De Project sjablonen worden bijgewerkt met de uitbrei ding. De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten. De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.

1. De QDK-pakketten bijwerken

    - Een bestaande toepassing openen
    - **Afhankelijkheden** selecteren in het Solution Explorer
    - Selecteer **NuGet-pakketten beheren**
    - De **micro soft. Quantum** -pakketten bijwerken naar de nieuwste versie

1. U kunt nu uw toepassing uitvoeren met de nieuwste QDK.

## <a name="c-using-vs-code"></a>C#, met behulp van VS code

1. De Quantum versus code-extensie bijwerken

    - Opnieuw opstarten VS code
    - Ga naar het tabblad **extensies**
    - Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension
    - De uitbrei ding opnieuw laden

1. De Quantum project sjablonen bijwerken:

   - Ga naar **weer gave** -> - **opdracht palet**
   - Selecteer **Q #: Project sjablonen installeren**

1. Een bestaande toepassing openen in VS code

   - Bewerk het. csproj-bestand om de nieuwe pakket versies toe te voegen

    ```xml
    <ItemGroup>
        <PackageReference Include="Microsoft.Quantum.Standard" Version="0.9.1909.3002" />
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.9.1909.3002" />
    </ItemGroup>
    ```

    Als u andere `Microsoft.Quantum`-pakketten gebruikt, werkt u deze ook bij.

1. U kunt nu uw toepassing uitvoeren met de bijgewerkte QDK

## <a name="c-using-the-dotnet-command-line-tool"></a>C#, met behulp van het opdracht regel programma `dotnet`

1. De Quantum project sjablonen voor .NET bijwerken

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

1. Een bestaande toepassing bijwerken en uitvoeren

    - De versie van het QDK-pakket in uw toepassing bijwerken

        ```bash
        dotnet add package Microsoft.Quantum.Development.Kit
        dotnet add package Microsoft.Quantum.Standard
        ```

        Als uw toepassing andere `Microsoft.Quantum`-pakketten gebruikt, werkt u deze ook bij.

    - De toepassing uitvoeren

        ```bash
        dotnet run
        ```

    - Uw toepassing wordt uitgevoerd met de nieuwe pakket versies

## <a name="whats-next"></a>En verder?

Nu u de Quantum Development Kit hebt bijgewerkt in uw voorkeurs omgeving, kunt u uw Quantum Programma's blijven ontwikkelen en uitvoeren. Als u nog geen programma hebt geschreven, kunt u aan de slag met [uw eerste Quantum programma](xref:microsoft.quantum.write-program).
