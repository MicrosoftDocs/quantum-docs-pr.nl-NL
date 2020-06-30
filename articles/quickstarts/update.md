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
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>De Microsoft Quantum Development Kit (QDK) bijwerken

Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de meest recente versie.

In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd. Als u de QDK voor de eerste keer installeert, dient u de [installatiehandleiding](xref:microsoft.quantum.install) te raadplegen.

We raden u aan om de QDK altijd naar de meest recente versie bij te werken. Volg deze updatehandleiding om een upgrade uit te voeren naar de meest recente versie van de QDK. Het proces bestaat uit twee delen:
1. Uw bestaande Q#-bestanden en -projecten bijwerken om de code uit te lijnen met eventueel bijgewerkte syntaxis.
2. De QDK zelf bijwerken voor de door u gekozen ontwikkelomgeving.

## <a name="updating-q-projects"></a>Q#-projecten bijwerken 

U dient deze instructies te volgen om uw Q#-projecten bij te werken, ongeacht of u C# of Python gebruikt om Q#-bewerkingen te hosten.

1. Controleer eerst of u de meest recente versie van de [.NET Core SDK 3.1](https://dotnet.microsoft.com/download) hebt. Voer de volgende opdracht uit in de opdrachtprompt:

    ```dotnetcli
    dotnet --version
    ```

    Controleer of de uitvoer `3.1.100` of hoger is. Als dat niet het geval is, installeert u de [meest recente versie](https://dotnet.microsoft.com/download) en controleert u de uitvoer opnieuw. Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio Code of rechtstreeks vanaf de opdrachtregel).

### <a name="update-q-projects-in-visual-studio"></a>Q#-projecten in Visual Studio bijwerken
 
1. Voer een update uit naar de meest recente versie van Visual Studio 2019. Instructies hiervoor vindt u [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019).
2. Open uw oplossing in Visual Studio.
3. Selecteer in het menu de opties **Bouwen** -> **Oplossing opschonen**.
4. Werk in elk van uw .csproj-bestanden het doelframework bij naar `netcoreapp3.1` (of naar `netstandard2.1` als het een bibliotheekproject is).
    Dat wil zeggen dat u de regels van het formulier bewerkt:

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    U vindt [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) meer informatie over het opgeven van doelframeworks.

5. Stel in elk van de .csproj-bestanden de SDK in op `Microsoft.Quantum.Sdk`, zoals aangegeven in de onderstaande regel. Het versienummer moet het meest recent beschikbare nummer zijn. U kunt dit controleren door de [releaseopmerkingen](https://docs.microsoft.com/quantum/relnotes/) te bekijken.

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. Sla alle bestanden in uw oplossing op en sluit deze.

7. Selecteer **Hulpprogramma's** -> **Opdrachtregel** -> **Opdrachtprompt voor ontwikkelaars**. U kunt echter ook de pakketbeheerconsole in Visual Studio gebruiken.

8. Voer voor elk project in de oplossing de volgende opdracht uit om dit pakket te **verwijderen**:

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Als uw projecten gebruikmaken van andere Microsoft.Quantum- of Microsoft.Azure.Quantum-pakketten (bijvoorbeeld Microsoft.Quantum.Numerics), voert u de opdracht **Toevoegen** uit om de gebruikte versie bij te werken.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. Sluit de opdrachtprompt en selecteer **Bouwen** -> **Oplossing bouwen** (selecteer *niet* de optie Oplossing opnieuw bouwen).

U kunt nu doorgaan met het [bijwerken van uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension).


### <a name="update-q-projects-in-visual-studio-code"></a>Q#-projecten in Visual Studio Code bijwerken

1. Open in Visual Studio Code de map met het project dat moet worden bijgewerkt.
2. Klik op **Terminal** -> **Nieuwe terminal**.
3. Volg de instructies voor het bijwerken met behulp van de opdrachtregel (direct hieronder).

### <a name="update-q-projects-using-the-command-line"></a>Q#-projecten bijwerken met behulp van de opdrachtregel

1. Navigeer naar de map met het hoofdprojectbestand.

2. Voer de volgende opdracht uit:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Stel vast wat de huidige versie van de QDK is. Raadpleeg hiervoor de [releaseopmerkingen](https://docs.microsoft.com/quantum/relnotes/). De versie heeft een indeling die vergelijkbaar is met `0.11.2006.207`.

4. Volg voor elk van uw `.csproj`-bestanden de volgende stappen:

    - Werk het doelframework bij naar `netcoreapp3.1` (of naar `netstandard2.1` als het een bibliotheekproject is). Dat wil zeggen dat u de regels van het formulier bewerkt:

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        U vindt [hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) meer informatie over het opgeven van doelframeworks.

    - Vervang de verwijzing naar de SDK in de projectdefinitie. Controleer of het versienummer overeenkomt met de waarde die is vastgesteld in **stap 3**.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - Verwijder de verwijzing naar pakket het `Microsoft.Quantum.Development.Kit`, indien aanwezig, die wordt opgegeven in de volgende vermelding:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - Werk de versie van alle Microsoft Quantum-pakketten bij naar de meest recente versie van de QDK (vastgesteld in **stap 3**). Deze pakketten krijgen een naam volgens de volgende patronen:

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        Verwijzingen naar pakketten hebben de volgende indeling:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - Sla het bijgewerkte bestand op.

    - Herstel de afhankelijkheden van het project op de volgende wijze:

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. Navigeer terug naar de map met uw hoofdproject en voer het volgende uit:

    ```dotnetcli
    dotnet build [project_name].csproj
    ```

Nu uw Q#-projecten zijn bijgewerkt, volgt u de onderstaande instructies om de QDK zelf bij te werken.

## <a name="updating-the-qdk"></a>De QDK bijwerken

Het proces voor het bijwerken van de QDK varieert afhankelijk van uw ontwikkeltaal en-omgeving.
Selecteer uw ontwikkelomgeving hieronder.

* [Python: de IQ#-extensie bijwerken](#update-iq-for-python)
* [Jupyter Notebooks: de IQ#-extensie bijwerken](#update-iq-for-jupyter-notebooks)
* [Visual Studio: de QDK-extensie bijwerken](#update-visual-studio-qdk-extension)
* [VS Code: de QDK-extensie bijwerken](#update-vs-code-qdk-extension)
* [Opdrachtregel en C# : projectsjablonen bijwerken](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a>IQ# voor Python bijwerken

1. Werk de `iqsharp`-kernel bij 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Controleer de `iqsharp`-versie

    ```dotnetcli
    dotnet iqsharp --version
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is; deze moet overeenkomen met de [nieuwste release](xref:microsoft.quantum.relnotes).

3. Werk het `qsharp`-pakket bij

    ```
    pip install qsharp --upgrade
    ```

4. Controleer de `qsharp`-versie

    ```
    pip show qsharp
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```

5. Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. U kunt nu de bijgewerkte versie van de QDK gebruiken om uw bestaande kwantumprogramma's uit te voeren.

### <a name="update-iq-for-jupyter-notebooks"></a>IQ# voor Jupyter Notebooks bijwerken

1. Werk de `iqsharp`-kernel bij

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Controleer de `iqsharp`-versie

    ```dotnetcli
    dotnet iqsharp --version
    ```

    Uw uitvoer moet er als volgt uitzien:

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is; deze moet overeenkomen met de [nieuwste release](xref:microsoft.quantum.relnotes).

3. Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:

    ```
    %workspace reload
    ```

4. U kunt nu een bestaand Jupyter Notebook openen en dit uitvoeren met de bijgewerkte QDK.

### <a name="update-visual-studio-qdk-extension"></a>De Visual Studio QDK-extensie bijwerken

1. Werk de Q# Visual Studio-extensie bij

    - Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Accepteer de update

    > [!NOTE]
    > De projectsjablonen worden bijgewerkt met de extensie. De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten. De code voor uw bestaande projecten wordt niet bijgewerkt als de extensie wordt bijgewerkt.

### <a name="update-vs-code-qdk-extension"></a>De VS Code QDK-extensie bijwerken

1. Werk de Quantum VS Code-extensie bij

    - Start VS Code opnieuw
    - Navigeer naar het tabblad **Extensies**
    - Selecteer de **Microsoft Quantum Development Kit voor de Visual Studio Code**-extensie
    - Laad de extensie opnieuw

2. Werk de Quantum-projectsjablonen bij:

   - Ga naar **Weergave** -> **Opdrachtpalet**
   - Selecteer **Q#: Projectsjablonen installeren**
   - Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat de projectsjablonen zijn geïnstalleerd

### <a name="c-using-the-dotnet-command-line-tool"></a>C#, met behulp van het `dotnet`-opdrachtregelprogramma

1. Werk de Quantum-projectsjablonen voor .NET bij

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
