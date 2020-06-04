---
title: 'Meer informatie over het maken van een Q #-project met de Quantum Development Kit (QDK)'
description: 'Initialiseer een project voor de Quantum ontwikkeling met de QDK en Q # in de ontwikkel omgeving van uw keuze'
author: natke
ms.author: nakersha
ms.date: 10/19/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.howto.createproject
ms.openlocfilehash: 8019b32a3290e2d45124ebb1eb75395f6cb758db
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327523"
---
# <a name="create-a-q-project-in-your-development-environment"></a>Een Q #-project maken in uw ontwikkel omgeving

Meer informatie over het maken van een Q #-project met de QDK.

Een Q #-project bevat Q # bestanden met een Quantum code en een hostprogramma voor het uitvoeren van het Quantum programma. U kunt het host-programma schrijven in .NET-talen zoals C#, of in python. U kunt ook Q #-code in een Jupyter Notebook uitvoeren met behulp van de IQ # kernel.

Kies uw ontwikkel omgeving en taal in de volgende secties:

* [Python](#create-a-python-project)
* [Q# Jupyter Notebooks](#create-a-q-jupyter-notebook-project)
* [C# met Visual Studio](#create-a-c-project-on-windows-using-visual-studio)
* [C# met VS code](#create-a-c-project-using-vs-code)
* [C# met de opdracht regel](#create-a-c-project-using-the-dotnet-command-line-tool)

## <a name="create-a-python-project"></a>Een python-project maken

1. Vereisten

     * De [Quantum Development Kit voor python](xref:microsoft.quantum.install.python) installeren

1. Maak een map voor uw project en navigeer naar die map

1. Maak een Q #-bestand `Operation.qs` met de naam en voeg hieraan uw Q #-code toe. Bijvoorbeeld:

    ```qsharp
    namespace HelloWorld {
        open Microsoft.Quantum.Intrinsic;
        open Microsoft.Quantum.Canon;

        operation SayHello() : Result {
            Message("Hello from quantum world!");
            return Zero;
        }
    }
    ```

1. Maak een python-bestand `host.py` met de naam om uw Q #-bewerking aan te roepen. Bijvoorbeeld:

    ```python
    import qsharp

    from HelloWorld import SayHello

    SayHello.simulate()
    ```

1. Voer het programma uit:

    ```bash
    python host.py
    ```

1. Controleer de uitvoer. Met het programma worden de volgende regels uitgevoerd:

    ```bash
    Hello from quantum world!
    0
    ```

U kunt nu door gaan met het ontwikkelen van uw Quantum programma.

## <a name="create-a-q-jupyter-notebook-project"></a>Een Q # Jupyter Notebook-project maken

1. Vereisten

    * De [Quantum Development Kit voor Jupyter-notebooks](xref:microsoft.quantum.install.jupyter) installeren

1. Voer de volgende opdracht uit om de Notebook-server te starten:

    ```bash
    jupyter notebook
    ```

1. Blader naar de URL die wordt weergegeven op de opdrachtregel. Bijvoorbeeld: [http://localhost:8888/?token=c790a52ba54f0cf77465c3c8983d776348285b0280d91b85]

1. Er wordt een Jupyter-pagina weer gegeven in de browser. Op het tabblad **bestanden** selecteert u **Nieuw**  >  **Q #** om een Jupyter notebook met een Q #-kernel te maken. Voeg de volgende code toe aan de eerste notebook-cel:

    ```qsharp
    operation SayHello() : Unit {
        Message("Hello from quantum world!");
    }
    ```

1. Selecteer **Cell**  >  **cellen uitvoeren** om het notitie blok uit te voeren. `SayHello`wordt binnenkort weer gegeven in de cel-uitvoer:

    ![Jupyter Notebook cel met Q # code](~/media/install-guide-jupyter.png)

    Bij het uitvoeren van Jupyter-notebooks wordt de Q #-code gecompileerd en de notitie blok voert de naam van de bewerkte (en) bewerkingen uit die worden gevonden.

1. Simuleer in een nieuwe cel de uitvoering in een kwantumcomputer van de bewerking die u zojuist hebt gemaakt met behulp van de `%simulate`-magic:

    ![Jupyter Notebook cel met% simulatie Magic](~/media/install-guide-jupyter-simulate.png)

    Het bericht wordt nu op het scherm weergegeven, samen met het resultaat van de bewerking die u hebt aangeroepen (in dit geval leeg).

U kunt nu andere Q #-bewerkingen toevoegen om uw Quantum ontwikkeling voort te zetten.

## <a name="create-a-c-project-on-windows-using-visual-studio"></a>Een C#-project maken in Windows met behulp van Visual Studio

1. Vereisten

    * De [Quantum Development Kit-extensie voor Visual Studio](xref:microsoft.quantum.install.cs) installeren

1. Maak een nieuwe Q#-toepassing

    * Ga naar het **bestand**  ->  **Nieuw**  ->  **project**
    * Typ `Q#` in het zoekvak
    * Selecteer **Q#-toepassing**
    * Selecteer **volgende**
    * Kies een naam en een locatie voor uw toepassing
    * Selecteer **Maken**

1. Controleer het project

    U ziet dat er twee bestanden zijn gemaakt: `Driver.cs`, de C#-hosttoepassing. en `Operation.qs`, een Q#-programma dat een eenvoudige bewerking definieert om een bericht naar de console af te drukken.

1. De toepassing uitvoeren

    * Selecteer **fouten opsporen**  ->  **starten zonder fout opsporing**
    * Als het goed is, wordt de tekst `Hello quantum world!` afgedrukt naar een consolevenster.

U kunt nu door gaan met het ontwikkelen van uw Quantum met Visual Studio

> [!NOTE]
> * Als u meerdere projecten in één Visual Studio-oplossing hebt, moeten alle projecten in de oplossing zich in dezelfde map bevinden als de oplossing, of in een van de submappen.  

## <a name="create-a-c-project-using-vs-code"></a>Een C#-project maken met behulp van VS code

1. Vereisten

    * De [Quantum Development Kit-uitbrei ding voor VS code](xref:microsoft.quantum.install.cs) installeren

1. Maak een nieuw project:

    * Ga naar **View**het  ->  **opdracht palet** weer geven
    * Selecteer **Q #: nieuw project maken**
    * **Zelfstandige console toepassing** selecteren
    * Ga naar de locatie in het bestandssysteem waar u de toepassing wilt maken
    * Klik op de knop **Nieuw project openen...** zodra het project is gemaakt

1. Voer de toepassing uit:

    * Ga naar **Terminal**  ->  **New Terminal**
    * Voer `dotnet run` in
    * Als het goed is, ziet u de volgende tekst in het uitvoervenster: `Hello quantum world!`

U kunt nu door gaan met het ontwikkelen van uw Quantum met Visual Studio code.

> [!NOTE]
> * Werkruimten met meerdere hoofdmappen worden momenteel niet ondersteund door de Visual Studio Code-extensie. Als u meerdere projecten in één VS Code-werkruimte hebt, moeten alle projecten zich in dezelfde hoofdmap bevinden.

## <a name="create-a-c-project-using-the-dotnet-command-line-tool"></a>Een C#-project maken met behulp van het `dotnet` opdracht regel programma

1. Vereisten

    * De [Quantum Development Kit installeren voor de opdracht regel](xref:microsoft.quantum.install.standalone)

1. Een nieuwe toepassing maken

    ```dotnetcli
    dotnet new console -lang Q# -o <project name>
    ```

1. Navigeer naar de nieuwe toepassingsmap

    ```bash
    cd <project name>
    ```

    U ziet dat er twee bestanden zijn gemaakt, samen met de projectbestanden van de toepassing: een Q#-bestand (`Operation.qs`) en een C#-hostbestand (`Driver.cs`).

1. De toepassing uitvoeren

    ```dotnetcli
    dotnet run
    ```

    U ziet de volgende uitvoer: `Hello quantum world!`

U kunt nu door gaan met de Quantum ontwikkeling met behulp van opdracht regel Programma's.

## <a name="next-steps"></a>Volgende stappen

Nu u een project in uw voorkeurs omgeving hebt gemaakt, kunt u uw Quantum ontwikkeling voortzetten.
