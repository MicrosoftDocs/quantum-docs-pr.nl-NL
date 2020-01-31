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
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Het Microsoft Quantum Development Kit bijwerken (QDK)

Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.

In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd. Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).

We raden u aan om de nieuwste versie van QDK up-to-date te houden. Volg deze update handleiding om een upgrade uit te voeren naar de meest recente versie van QDK. Het proces bestaat uit twee delen:
1. uw bestaande Q #-bestanden en-projecten bijwerken om uw code uit te lijnen met een bijgewerkte syntaxis
2. de QDK voor uw gekozen ontwikkel omgeving bijwerken 

## <a name="updating-q-projects"></a>Q #-projecten bijwerken 

Ongeacht of u of python gebruikt C# om q #-bewerkingen te hosten, volgt u deze instructies om uw q #-projecten bij te werken.

1. Controleer eerst of u de meest recente versie van de [.NET Core SDK 3,1](https://dotnet.microsoft.com/download)hebt. Voer de volgende opdracht uit in de opdracht prompt:
    ```bash
    dotnet --version
    ```
Controleer of de uitvoer `3.1.100` of hoger is. Als dat niet het geval is, installeert u de [nieuwste versie](https://dotnet.microsoft.com/download) en controleert u opnieuw. Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio code of rechtstreeks de opdracht regel).

### <a name="update-q-projects-in-visual-studio"></a>Update Q #-projecten in Visual Studio
 
1. Update naar de nieuwste versie van Visual Studio 2019. Zie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) voor instructies
2. Open uw oplossing in Visual Studio
3. Selecteer in het menu de optie **bouwen** -> **nieuwe oplossing**
4. Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.0` (of `netstandard2.1` als het een bibliotheek project is).
    Dat wil zeggen, regels van het formulier bewerken:
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    [Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.
5. Sla alle bestanden in uw oplossing op en sluit deze af
6. Selecteer **extra** -> **opdracht regel** -> **opdracht prompt voor ontwikkel aars**
7. Voer voor elk project in de oplossing de volgende opdracht uit:
    ```bash
    dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```
    Als uw projecten andere micro soft. Quantum-pakketten gebruiken (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht ook uit.
8. Sluit de opdracht prompt en selecteer **build** -> **Build-oplossing** (Selecteer *geen* oplossing voor opnieuw samen stellen.

U kunt nu door gaan om [uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension)bij te werken.


### <a name="update-q-projects-in-visual-studio-code"></a>Update Q #-projecten in Visual Studio code

1. Open in Visual Studio code de map met het project dat moet worden bijgewerkt
2. **Terminal** -> **nieuwe terminal** selecteren
3. Volg de instructies voor het bijwerken met behulp van de opdracht regel (direct hieronder)

### <a name="update-q-projects-using-the-command-line"></a>Q #-projecten bijwerken met behulp van de opdracht regel

1. Ga naar de map die het project bestand bevat
2. Voer de volgende opdracht uit:
    ```bash
    dotnet clean [project_name].csproj
    ```

3. Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.0` (of `netstandard2.1` als het een bibliotheek project is).
    Dat wil zeggen, regels van het formulier bewerken:
    ```xml
    <TargetFramework>netcoreapp3.0</TargetFramework>
    ```
    [Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.
4. Voer de volgende opdracht uit:
    ```bash
    dotnet add package Microsoft.Quantum.Development.Kit
    ```
    Als uw project gebruikmaakt van andere micro soft. Quantum-pakketten (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht ook uit.
5. Sla alle bestanden op en sluit deze.
6. Herhaal 1-4 voor elke project afhankelijkheid en ga vervolgens terug naar de map met het hoofd project en voer het volgende uit:
    ```bash
    dotnet build [project_name].csproj
    ```

Als uw Q #-projecten nu zijn bijgewerkt, volgt u de onderstaande instructies om de QDK zelf bij te werken.

## <a name="updating-the-qdk"></a>De QDK bijwerken

Het proces voor het bijwerken van de QDK varieert, afhankelijk van uw ontwikkelings taal en-omgeving.
Selecteer hieronder uw ontwikkel omgeving.

* [Python: de extensie # uitbrei ding bijwerken](#update-iq-for-python)
* [Jupyter-notebooks: de extensie # uitbrei ding bijwerken](#update-iq-for-jupyter-notebooks)
* [Visual Studio: de QDK-extensie bijwerken](#update-visual-studio-qdk-extension)
* [VS code: de QDK-extensie bijwerken](#update-vs-code-qdk-extension)
* [Opdracht regel en C#: Project sjablonen bijwerken](#c-using-the-dotnet-command-line-tool)


### <a name="update-iq-for-python"></a>Update IQ # voor python

1. De `iqsharp`-kernel bijwerken 

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. De `iqsharp` versie controleren

    ```bash
    dotnet iqsharp --version
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).

3. Het `qsharp`-pakket bijwerken

    ```bash
    pip install qsharp --upgrade
    ```

4. De `qsharp` versie controleren

    ```bash
    pip show qsharp
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```bash
    Name: qsharp
    Version: 0.10.1912.501
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
5. Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

6. U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.

### <a name="update-iq-for-jupyter-notebooks"></a>Update IQ # voor Jupyter-notebooks

1. De `iqsharp`-kernel bijwerken

    ```bash
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. De `iqsharp` versie controleren

    ```bash
    dotnet iqsharp --version
    ```

    De uitvoer moet er ongeveer als volgt uitzien:

    ```bash
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```
    U hoeft zich geen zorgen te maken als uw `iqsharp`-versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).

3. Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:
    ```
    %workspace reload
    ```

4. U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.

### <a name="update-visual-studio-qdk-extension"></a>De QDK-extensie van Visual Studio bijwerken

1. De Q # Visual Studio-extensie bijwerken

    - Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - De update accepteren

    > [!NOTE]
    > De Project sjablonen worden bijgewerkt met de uitbrei ding. De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten. De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.

### <a name="update-vs-code-qdk-extension"></a>QDK-extensie voor bijwerken versus code

1. De Quantum versus code-extensie bijwerken

    - Opnieuw opstarten VS code
    - Ga naar het tabblad **extensies**
    - Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension
    - De uitbrei ding opnieuw laden

2. De Quantum project sjablonen bijwerken:

   - Ga naar **Weergave** -> **Opdrachtpalet**
   - Selecteer **Q #: Project sjablonen installeren**
   - Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat ' Project sjablonen zijn geïnstalleerd '

### <a name="c-using-the-dotnet-command-line-tool"></a>C#, met behulp van het opdracht regel programma `dotnet`

1. De Quantum project sjablonen voor .NET bijwerken

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a>En verder?

Nu u de Quantum Development Kit hebt bijgewerkt in uw voorkeurs omgeving, kunt u uw Quantum Programma's blijven ontwikkelen en uitvoeren. Als u nog geen programma hebt geschreven, kunt u aan de slag met [uw eerste Quantum programma](xref:microsoft.quantum.write-program).
