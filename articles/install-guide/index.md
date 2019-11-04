---
title: Meer informatie over het installeren van de Microsoft Quantum development kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 2a098d89f13278d7137bf182a184a74afb9393be
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462867"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>De Microsoft Quantum development kit (QDK) installeren

Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering. De QDK bestaat uit:

- de programmeertaal Q#
- een set bibliotheken voor abstractie van complexe functionaliteit in Q#
- een hosttoepassing (geschreven in Python of een .NET-taal) voor het uitvoeren van kwantumbewerkingen die zijn geschreven in Q#
- hulpprogramma's om het ontwikkelen te vergemakkelijken

De installatiestappen kunnen verschillen, afhankelijk van de gekozen ontwikkelomgeving. Kies uw omgeving in de secties hieronder.

## <a name="develop-with-python"></a>Ontwikkelen met Python

Met het qsharp-pakket voor Python simuleert u eenvoudig Q#-bewerkingen en -functies vanuit Python. IQ# (spreek uit als 'i-q-sharp') is een extensie die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.

1. Vereisten

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)
    - [.NET Core SDK 3.0 of hoger](https://www.microsoft.com/net/download)

1. Installeer het pakket `iqsharp`

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Installeer het pakket `qsharp`

    ```bash
    pip install qsharp
    ```

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en er de volgende code aan toe te voegen:

        ```qsharp
        namespace HelloWorld
        {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Result {
                Message("Hello from quantum world!");
                return Zero;
            }
        }
        ```

    - Maak een Python-programma met de naam `hello_world.py` om de Q#-bewerking `SayHello()` aan te roepen:

        ```python
        import qsharp

        from HelloWorld import SayHello

        SayHello.simulate()
        ```

    - Voer het programma uit:

        ```bash
        python hello_world.py
        ```

    - Controleer de uitvoer. Met het programma worden de volgende regels uitgevoerd:

        ```bash
        Hello from quantum world!
       0
       ```

## <a name="develop-with-jupyter-notebooks"></a>Ontwikkelen met Jupyter-notebooks

Jupyter-notebooks worden veel gebruikt binnen academische instellingen, in wetenschappelijke laboratoria en voor gezamenlijk programmeerprojecten online. Met een Jupyter-notebook kunt u direct code uitvoeren, waaronder nu ook Q#-code, en gebruikmaken van instructies, notities en andere inhoud.  Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.

IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.


1. Vereisten

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.0 of hoger](https://www.microsoft.com/net/download)

1. Installeer het pakket `iqsharp`

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Voer de volgende opdracht uit om de Notebook-server te starten:

        ```bash
        jupyter notebook
        ```

    - Blader naar de URL die wordt weergegeven op de opdrachtregel. Bijvoorbeeld: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85 ]

    - Maak een Jupyter Notebook met een Q#-kernel en voeg de volgende code toe aan de eerste Notebook-cel:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Voer deze cel van het Notebook uit:

        ![Cel met Q#-code in een Jupyter-notebook](~/media/install-guide-jupyter.png)

        U ziet `SayHello` in de uitvoer van de cel. Wanneer u werkt met Jupyter Notebook, wordt de Q#-code gecompileerd en wordt de naam van de gevonden bewerking(en) geretourneerd in de uitvoer.


    - Simuleer in een nieuwe cel de uitvoering in een kwantumcomputer van de bewerking die u zojuist hebt gemaakt met behulp van de `%simulate`-magic:

        ![Cel met %simulate magic in een Jupyter-notebook](~/media/install-guide-jupyter-simulate.png)

        Het bericht wordt nu op het scherm weergegeven, samen met het resultaat van de bewerking die u hebt aangeroepen (in dit geval leeg).


## <a name="develop-with-c-on-windows-using-visual-studio"></a>Ontwikkelen met C# in Windows, met behulp van Visual Studio

Visual Studio biedt een uitgebreide omgeving voor het ontwikkelen van Q#-programma's en beschikt over handige functies die ontwikkelaars helpen bij het bouwen van hun toepassingen, zoals het aanvullen van code en het markeren van de syntaxis.  De Visual Studio-extensie voor Q# bevat sjablonen voor Q#-bestanden en -projecten, evenals syntaxismarkering en IntelliSense-ondersteuning.


1. Vereisten

    - [Visual Studio](https://visualstudio.microsoft.com/downloads/) 16.3, waarbij de workload voor platformoverschrijdende ontwikkeling met .NET Core is ingeschakeld

1. Installeer de Q# Visual Studio-extensie

    - Download de [Visual Studio-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.DevKit)
    - Voeg de extensie toe aan Visual Studio

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

## <a name="develop-with-c-using-visual-studio-code"></a>Ontwikkelen met C# met behulp van Visual Studio Code

Visual Studio Code (VS Code) biedt een uitgebreide omgeving voor het ontwikkelen van Q#-programma's in talloze computeromgevingen, waaronder Windows, Linux en Mac, en beschikt over handige functies die ontwikkelaars helpen bij het bouwen van hun toepassingen, zoals het aanvullen van code en het markeren van de syntaxis.  De VS Code-extensie voor Q# bevat syntaxismarkering en Q#-codefragmenten.

1. Vereisten

   - [VS-code](https://code.visualstudio.com/download)
   - [.NET Core SDK 3.0 of hoger](https://www.microsoft.com/net/download)

1. Installeer de Quantum VS Code-extensie

    - Installeer de [VS Code-extensie](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode)

1. Installeer de Quantum-projectsjablonen:

   - Ga naar **Weergave** -> **Opdrachtpalet**
   - Selecteer **Q#: Projectsjablonen installeren**

    De Quantum development kit is nu geïnstalleerd en klaar voor gebruik in uw eigen toepassingen en bibliotheken.

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Maak een nieuw project:

        - Ga naar **Weergave** -> **Opdrachtpalet**
        - Selecteer **Q#: Nieuw project maken**
        - Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken
        - Klik op de knop **Nieuw project openen...** zodra het project is gemaakt

    - Voer de toepassing uit:

        - Ga naar **Fouten opsporen** -> **Starten zonder foutopsporing**
        - Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`

> [!NOTE]
> * > * Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie. Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.

## <a name="develop-with-c-using-the-dotnet-command-line-tool"></a>Ontwikkelen met C#, met behulp van het opdrachtregelprogramma `dotnet`

Natuurlijk kunt u ook Q#-programma's schrijven en uitvoeren vanaf de opdrachtregel. U hoeft hiervoor alleen de .NET Core SDK en de QDK-projectsjablonen te installeren. 

1. Vereisten

    - [.NET Core SDK 3.0 of hoger](https://www.microsoft.com/net/download)

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

## <a name="whats-next"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.
