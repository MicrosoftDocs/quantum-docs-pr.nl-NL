---
title: De Quantum Development Kit (QDK) bijwerken
description: 'Hierin wordt beschreven hoe u uw Q #-projecten en de Microsoft Quantum Development Kit bijwerkt naar de huidige versie.'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.update
ms.openlocfilehash: 89db1a671767b0cc083a251918bbeeed2b39b883
ms.sourcegitcommit: c8ebc5d7d8581444754f5d7bfaca2f25601f1b14
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84578178"
---
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Het Microsoft Quantum Development Kit bijwerken (QDK)

Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.

In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd. Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).

We raden u aan om de nieuwste versie van QDK up-to-date te houden. Volg deze update handleiding om een upgrade uit te voeren naar de meest recente versie van QDK. Het proces bestaat uit twee delen:
1. Het bijwerken van uw bestaande Q #-bestanden en-projecten om uw code uit te lijnen met een bijgewerkte syntaxis.
2. De QDK voor uw gekozen ontwikkel omgeving bijwerken.

## <a name="updating-q-projects"></a>Q #-projecten bijwerken 

Ongeacht of u C# of python gebruikt om Q #-bewerkingen te hosten, volgt u deze instructies om uw Q #-projecten bij te werken.

1. Controleer eerst of u de meest recente versie van de [.NET Core SDK 3,1](https://dotnet.microsoft.com/download)hebt. Voer de volgende opdracht uit in de opdracht prompt:

    ```dotnetcli
    dotnet --version
    ```

    Controleer of de uitvoer is `3.1.100` of hoger. Als dat niet het geval is, installeert u de [nieuwste versie](https://dotnet.microsoft.com/download) en controleert u opnieuw. Volg de onderstaande instructies, afhankelijk van uw installatie (Visual Studio, Visual Studio code of rechtstreeks de opdracht regel).

### <a name="update-q-projects-in-visual-studio"></a>Update Q #-projecten in Visual Studio
 
1. Update naar de nieuwste versie van Visual Studio 2019. Zie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) voor instructies.
2. Open uw oplossing in Visual Studio.
3. Selecteer in het menu een **Build**  ->  **schone oplossing**bouwen.
4. Werk in elk van uw. csproj-bestanden het doel raamwerk bij naar `netcoreapp3.1` (of `netstandard2.1` als het een bibliotheek project is).
    Dat wil zeggen, regels van het formulier bewerken:

    ```xml
    <TargetFramework>netcoreapp3.1</TargetFramework>
    ```

    [Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.

5. Stel in elk van de. csproj-bestanden de SDK in op `Microsoft.Quantum.Sdk` , zoals aangegeven in de onderstaande regel. Het versie nummer moet het meest recent beschik bare zijn, en u kunt dit vaststellen door de [release opmerkingen](https://docs.microsoft.com/quantum/relnotes/)te bekijken.

    ```xml
    <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
    ```

6. Sla alle bestanden in uw oplossing op en sluit deze.

7. Selecteer **extra**  ->  **opdracht regel**opdracht  ->  **prompt**. U kunt ook de pakket beheer console in Visual Studio gebruiken.

8. Voer voor elk project in de oplossing de volgende opdracht uit om dit pakket te **verwijderen** :

    ```dotnetcli
    dotnet remove [project_name].csproj package Microsoft.Quantum.Development.Kit
    ```

   Als uw projecten gebruikmaken van andere micro soft. Quantum-of micro soft. Azure. Quantum pakketten (bijvoorbeeld micro soft. Quantum. NUMERIC), voert u de opdracht toevoegen voor deze **toepassingen** uit om de gebruikte versie bij te werken.

    ```dotnetcli
    dotnet add [project_name].csproj package [package_name]
    ```

9. Sluit de opdracht prompt en selecteer **Build**  ->  **Build Solution** (Selecteer *geen* oplossing voor opnieuw samen stellen).

U kunt nu door gaan om [uw Visual Studio QDK-extensie](#update-visual-studio-qdk-extension)bij te werken.


### <a name="update-q-projects-in-visual-studio-code"></a>Update Q #-projecten in Visual Studio code

1. Open in Visual Studio code de map met het project dat moet worden bijgewerkt.
2. Selecteer **Terminal**  ->  **New Terminal**.
3. Volg de instructies voor het bijwerken met behulp van de opdracht regel (direct hieronder).

### <a name="update-q-projects-using-the-command-line"></a>Q #-projecten bijwerken met behulp van de opdracht regel

1. Navigeer naar de map met het hoofd project bestand.

2. Voer de volgende opdracht uit:

    ```dotnetcli
    dotnet clean [project_name].csproj
    ```

3. Bepaal de huidige versie van de QDK. U kunt het vinden door de [release opmerkingen](https://docs.microsoft.com/quantum/relnotes/)te bekijken. De versie heeft een indeling die vergelijkbaar is met `0.11.2006.207` .

4. In elk van uw `.csproj` bestanden gaat u als volgt te werk:

    - Werk het doel raamwerk bij naar `netcoreapp3.1` (of `netstandard2.1` als het een bibliotheek project is). Dat wil zeggen, regels van het formulier bewerken:

        ```xml
        <TargetFramework>netcoreapp3.1</TargetFramework>
        ```

        [Hier](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks)vindt u meer informatie over het opgeven van doel raamwerken.

    - De verwijzing naar de SDK in de project definitie vervangen. Zorg ervoor dat het versie nummer overeenkomt met de waarde die u in **stap 3**hebt bepaald.

        ```xml
        <Project Sdk="Microsoft.Quantum.Sdk/0.11.2006.207">
        ```

    - Verwijder de verwijzing naar het pakket `Microsoft.Quantum.Development.Kit` indien aanwezig, dat wordt opgegeven in de volgende vermelding:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Development.Kit" Version="0.10.1910.3107" />
        ```

    - Werk de versie van de micro soft Quantum-pakketten bij naar de meest recente versie van de QDK (bepaald in **stap 3**). Deze pakketten worden benoemd met de volgende patronen:

        ```
        Microsoft.Quantum.*
        Microsoft.Azure.Quantum.*
        ```
    
        Verwijzingen naar pakketten hebben de volgende indeling:

        ```xml
        <PackageReference Include="Microsoft.Quantum.Compiler" Version="0.11.2006.207" />
        ```

    - Sla het bijgewerkte bestand op.

    - Herstel de afhankelijkheden van het project door het volgende te doen:

        ```dotnetcli
        dotnet restore [project_name].csproj
        ```

4. Ga terug naar de map met het hoofd project en voer het volgende uit:

    ```dotnetcli
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

1. De `iqsharp` kernel bijwerken 

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Controleer de `iqsharp` versie

    ```dotnetcli
    dotnet iqsharp --version
    ```

    In dat geval moet de volgende uitvoer worden weergegeven:

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    U hoeft zich geen zorgen te maken als uw `iqsharp` versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).

3. Het `qsharp` pakket bijwerken

    ```
    pip install qsharp --upgrade
    ```

4. Controleer de `qsharp` versie

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

5. Voer de volgende opdracht uit vanaf de locatie van uw `.qs` bestanden

    ```
    python -c "import qsharp; qsharp.reload()"
    ```

6. U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.

### <a name="update-iq-for-jupyter-notebooks"></a>Update IQ # voor Jupyter-notebooks

1. De `iqsharp` kernel bijwerken

    ```dotnetcli
    dotnet tool update -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

2. Controleer de `iqsharp` versie

    ```dotnetcli
    dotnet iqsharp --version
    ```

    De uitvoer moet er ongeveer als volgt uitzien:

    ```
    iqsharp: 0.10.1912.501
    Jupyter Core: 1.2.20112.0
    ```

    U hoeft zich geen zorgen te maken als uw `iqsharp` versie hoger is. deze moet overeenkomen met de [nieuwste versie](xref:microsoft.quantum.relnotes).

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

   - Ga naar **View**het  ->  **opdracht palet** weer geven
   - Selecteer **Q #: Project sjablonen installeren**
   - Na een paar seconden krijgt u een pop-up te zien waarin wordt bevestigd dat ' Project sjablonen zijn geïnstalleerd '

### <a name="c-using-the-dotnet-command-line-tool"></a>C# met behulp van het `dotnet` opdracht regel programma

1. De Quantum project sjablonen voor .NET bijwerken

    ```dotnetcli
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```
