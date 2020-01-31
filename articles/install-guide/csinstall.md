---
title: 'Ontwikkelen met Q # +C#'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 1fd829c684502092bb7491b0f46b5f690320c941
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76831015"
---
# <a name="develop-with-q--c"></a>Ontwikkelen met Q # +C#

Installeer de QDK voor het C# ontwikkelen van host-Program Ma's om Q #-bewerkingen aan te roepen.

Q # is gebouwd om goed te kunnen spelen met .NET-talen C#, met name. U kunt in verschillende ontwikkel omgevingen met deze koppeling werken:

- [Q # + C# met Visual Studio (Windows)](#VS)
- [Q # + C# met Visual Studio code (Windows, Linux en Mac)](#VSC)
- [Q # + C# met behulp van het `dotnet` opdracht regel programma](#command)

## Ontwikkelen met Q # + C# met Visual Studio<a name="VS"></a>

Visual Studio biedt een uitgebreide omgeving voor het ontwikkelen van Q #-Program ma's. De Q # Visual Studio-extensie bevat sjablonen voor Q # bestanden en projecten, evenals syntaxis markeringen, het volt ooien van code en IntelliSense-ondersteuning.


1. Vereisten

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld

1. Installeer de Q# Visual Studio-extensie

    - Down load en installeer de [Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Maak een nieuwe Q#-toepassing

        - Ga naar **Bestand** -> **Nieuw** -> **Project**
        - Typ `Q#` in het zoekvak
        - Selecteer **Q#-toepassing**
        - Selecteer **Volgende**
        - Kies een naam en een locatie voor uw toepassing
        - Selecteer **Maken**

    - Controleer het project

        U ziet dat er twee bestanden zijn gemaakt: `Driver.cs`, de C#-hosttoepassing. en `Operation.qs`, een Q#-programma dat een eenvoudige bewerking definieert om een bericht naar de console af te drukken.

    - De toepassing uitvoeren

        - Selecteer **Fouten opsporen** -> **Starten zonder foutopsporing**
        - Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.

> [!NOTE]
> * Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.  

## Ontwikkelen met Q # + C# met Visual Studio code<a name="VSC"></a>

Visual Studio code (VS code) biedt een uitgebreide omgeving voor het ontwikkelen van Q #-Program ma's in Windows, Linux en Mac.  De code-uitbrei ding Q # versus bevat ondersteuning voor Q #-syntaxis markering, code voltooiing en Q #-code fragmenten.

1. Vereisten

   - [VS-code](https://code.visualstudio.com/download)
   - [.NET Core SDK 3,1 of hoger](https://www.microsoft.com/net/download)

1. Installeer de Quantum VS Code-extensie

    - Installeer de [VS Code-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)

1. Installeer de Quantum-projectsjablonen:

   - Ga naar **Weergave** -> **Opdrachtpalet**
   - Selecteer **Q #: Project sjablonen installeren**

    De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Maak een nieuw project:

        - Ga naar **Weergave** -> **Opdrachtpalet**
        - Selecteer **Q #: nieuw project maken**
        - **Zelfstandige console toepassing** selecteren
        - Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken
        - Klik op de knop **Nieuw project openen...** zodra het project is gemaakt

    - Als u de C# uitbrei ding voor VS-code nog niet hebt geïnstalleerd, wordt er een pop-upvenster weer gegeven. Installeer de extensie. 

    - Voer de toepassing uit:

        - Ga naar **terminal** -> **nieuwe terminal**
        - Voer `dotnet run` in
        - Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`


> [!NOTE]
> * Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie. Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.

## Ontwikkelen met Q # + C# met behulp van het opdracht regel programma `dotnet`<a name="command"></a>

Natuurlijk kunt u ook Q#-programma's schrijven en uitvoeren vanaf de opdrachtregel. U hoeft hiervoor alleen de .NET Core SDK en de QDK-projectsjablonen te installeren. 

1. Vereisten

    - [.NET Core SDK 3,1 of hoger](https://www.microsoft.com/net/download)

1. Installeer de Quantum-projectsjablonen voor .NET

    ```bash
    dotnet new -i Microsoft.Quantum.ProjectTemplates
    ```

    De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Een nieuwe toepassing maken

       ```bash
       dotnet new console -lang Q# -o runSayHello
       ```

    - Navigeer naar de nieuwe toepassingsmap

       ```bash
       cd runSayHello
       ```

    U ziet dat er twee bestanden zijn gemaakt, samen met de projectbestanden van de toepassing: een Q#-bestand (`Operation.qs`) en een C#-hostbestand (`Driver.cs`).

    - De toepassing uitvoeren

        ```bash
        dotnet run
        ```

        U ziet de volgende uitvoer: `Hello quantum world!`

    
## <a name="whats-next"></a>En verder?

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.
