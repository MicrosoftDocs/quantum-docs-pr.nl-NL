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
# <a name="update-the-microsoft-quantum-development-kit-qdk"></a>Het Microsoft Quantum Development Kit bijwerken (QDK)

Meer informatie over het bijwerken van de Microsoft Quantum Development Kit (QDK) naar de nieuwste versie.

In dit artikel wordt ervan uitgegaan dat u de QDK al hebt geïnstalleerd. Als u voor de eerste keer installeert, raadpleegt u de [installatie handleiding](xref:microsoft.quantum.install).


## <a name="updating-q-projects"></a>Q #-projecten bijwerken 

1. Installeer eerst de nieuwste versie van de [.NET Core SDK 3,0](https://dotnet.microsoft.com/download) en voer de volgende opdracht uit in de opdracht prompt:
```bash
dotnet --version
```
 Controleer of de uitvoer 3.0.100 of hoger is en volg de onderstaande instructies, afhankelijk van uw instellingen.

### <a name="in-visual-studio"></a>In Visual Studio
 
 1. Update naar de nieuwste versie van Visual Studio 2019. Zie [hier](https://docs.microsoft.com/visualstudio/install/update-visual-studio?view=vs-2019) voor instructies
 2. Open uw oplossing in Visual Studio
 3. Selecteer in het menu de optie bouwen > nieuwe oplossing 
 4. [Werk het doel raamwerk](https://docs.microsoft.com/visualstudio/ide/visual-studio-multi-targeting-overview?view=vs-2019#change-the-target-framework) in elk van uw. csproj-bestanden bij naar netcoreapp 3.0 (of netstandard 2.1 als het een bibliotheek project is)
 5. Sla alle bestanden in uw oplossing op en sluit deze af
 6. Selecteer Extra > opdracht regel > opdracht prompt voor ontwikkel aars
 7. Voer voor elk project in de oplossing de volgende opdracht uit:
 ```bash
 dotnet add [project_name].csproj package Microsoft.Quantum.Development.Kit
 ```
Als uw projecten andere micro soft. Quantum-pakketten gebruiken, voert u de opdracht ook uit. 
 8. Sluit de opdracht prompt en selecteer Build > build-oplossing (Selecteer *geen* oplossing voor opnieuw samen stellen.

### <a name="in-visual-studio-code"></a>In Visual Studio code

1. Open in Visual Studio code de map met het project dat moet worden bijgewerkt
1. Terminal > nieuwe terminal selecteren
1. Volg de instructies voor het bijwerken met behulp van de opdracht regel

### <a name="using-the-command-line"></a>Via de opdracht regel

1. Ga naar de map die het project bestand bevat
2. Voer de volgende opdracht uit:
```bash
dotnet clean [project_name].csproj
```

3. [Werk het doel raamwerk](https://docs.microsoft.com/dotnet/standard/frameworks#how-to-specify-target-frameworks) in elk van uw. csproj-bestanden bij naar netcoreapp 3.0 (of netstandard 2.1 als het een bibliotheek project is)
4. Voer de volgende opdracht uit:
```bash
dotnet add package Microsoft.Quantum.Development.Kit
```
Als uw project gebruikmaakt van andere micro soft. Quantum-pakketten, voert u de opdracht ook uit.

5. Alle bestanden opslaan en sluiten
6. Herhaal 1-4 voor elke project afhankelijkheid en ga vervolgens terug naar de map met het hoofd project en voer het volgende uit:
```bash
dotnet build [project_name].csproj
```

## <a name="update-iq-for-python"></a>Update IQ # voor python

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
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
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
    Version: 0.10.1911.307
    Summary: Python client for Q#, a domain-specific quantum programming language
    ...
    ```
1. Voer de volgende opdracht uit vanaf de locatie van uw `.qs`-bestanden
    ```bash
    python -c "import qsharp; qsharp.reload()"
    ```

1. U kunt nu de bijgewerkte versie van QDK gebruiken om uw bestaande Quantum Program ma's uit te voeren.

## <a name="update-iq-for-jupyter-notebooks"></a>Update IQ # voor Jupyter-notebooks

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
    iqsharp: 0.10.1911.307
    Jupyter Core: 1.2.20112.0
    ```
1. Voer de volgende opdracht uit vanuit een cel in uw Jupyter Notebook:
    ```
    %workspace reload
    ```

1. U kunt nu een bestaand Jupyter-notebook openen en dit uitvoeren met de bijgewerkte QDK.

## <a name="update-visual-studio-qdk-extension"></a>De QDK-extensie van Visual Studio bijwerken

1. De Q # Visual Studio-extensie bijwerken

    - Visual Studio vraagt u updates te accepteren voor de [Quantum Visual Studio-uitbrei ding](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - De update accepteren

    > [!NOTE]
    > De Project sjablonen worden bijgewerkt met de uitbrei ding. De bijgewerkte sjablonen zijn alleen van toepassing op nieuw gemaakte projecten. De code voor uw bestaande projecten wordt niet bijgewerkt wanneer de uitbrei ding wordt bijgewerkt.

## <a name="update-vs-code-qdk-extension"></a>QDK-extensie voor bijwerken versus code

1. De Quantum versus code-extensie bijwerken

    - Opnieuw opstarten VS code
    - Ga naar het tabblad **extensies**
    - Selecteer de **Microsoft Quantum Development Kit voor Visual Studio code** extension
    - De uitbrei ding opnieuw laden

1. De Quantum project sjablonen bijwerken:

   - Ga naar **Weergave** -> **Opdrachtpalet**
   - Selecteer **Q #: Project sjablonen installeren**

## <a name="c-using-the-dotnet-command-line-tool"></a>C#, met behulp van het opdracht regel programma `dotnet`

1. De Quantum project sjablonen voor .NET bijwerken

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

## <a name="whats-next"></a>En verder?

Nu u de Quantum Development Kit hebt bijgewerkt in uw voorkeurs omgeving, kunt u uw Quantum Programma's blijven ontwikkelen en uitvoeren. Als u nog geen programma hebt geschreven, kunt u aan de slag met [uw eerste Quantum programma](xref:microsoft.quantum.write-program).
