---
title: Ontwikkelen met Q#-Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 5c613d29c03525d29893307684f13ccd32d4d4eb
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274052"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Ontwikkelen met Q#-Jupyter Notebooks

Installeer de QDK voor het ontwikkelen van Q#-bewerkingen op Q#-Jupyter Notebooks.

Met Jupyter Notebooks kunt u in-place codes uitvoeren naast instructies, notities en andere inhoud. Deze omgeving is ideaal voor het schrijven van Q#-codes met ingesloten uitleg of interactieve zelfstudies over kwantumcomputing. Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.

IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.

> [!NOTE]
> * In Q#-Jupyter Notebooks kunt u alleen Q#-codes uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe hostprogramma's (zoals Python of C#-bestanden). Deze omgeving is niet geschikt als u een extern, klassiek hostprogramma wilt combineren met het kwantumprogramma.

1. Vereisten

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Installeer het pakket `iqsharp`

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Als er tijdens de `dotnet iqsharp install`-stap een fout optreedt, moet u een nieuw terminalvenster openen en het nogmaals proberen.
    > Als het daarna nog steeds niet werkt, zoekt u het geïnstalleerde `dotnet-iqsharp`-hulpprogramma (in Windows, `dotnet-iqsharp.exe`) en voert u dit uit:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > waarbij `/path/to/dotnet-iqsharp` moet worden vervangen door het absolute pad naar het `dotnet-iqsharp`-hulpprogramma in uw bestandssysteem.
    > Dit is meestal bij `.dotnet/tools` in de map van uw gebruikersprofiel.

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Voer de volgende opdracht uit om de Notebook-server te starten:

        ```
        jupyter notebook
        ```

    - Als u de Jupyter Notebook wilt openen, kopieert en plakt u de URL die u van de opdrachtregel hebt ontvangen in uw browser.

    - Maak een Jupyter Notebook met een Q#-kernel en voeg de volgende code toe aan de eerste notebookcel:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Voer deze cel van het Notebook uit:

        ![Cel met Q#-code in een Jupyter Notebook](~/media/install-guide-jupyter.png)

        U ziet `SayHello` in de uitvoer van de cel. Als u de Q#-code uitvoert in een Jupyter Notebook, wordt de Q#-code gecompileerd en wordt de naam van de gevonden bewerking(en) door het notebook uitgevoerd.


    - Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de opdracht `%simulate`:

        ![Cel met %simulate magic in een Jupyter Notebook](~/media/install-guide-jupyter-simulate.png)

        Het bericht wordt nu op het scherm weergegeven, samen met het resultaat van de bewerking die u hebt aangeroepen (in dit geval een lege tuple `()`, omdat onze bewerking een `Unit`-type oplevert).

## <a name="next-steps"></a>Volgende stappen

Nu u de QDK voor Q#-Jupyter Notebooks hebt geïnstalleerd, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren door uw Q#-code rechtstreeks in de Jupyter Notebook-omgeving te schrijven.

Ga voor meer voorbeelden van wat u kunt doen met Q#-Jupyter Notebooks naar:
- [Inleiding tot Q# en Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Daar vindt u een Q#-Jupyter Notebook waarin wordt getoond hoe u Q# in deze omgeving kunt gebruiken.
- [Quantum Katas](xref:microsoft.quantum.overview.katas), een open-source verzameling van zelfstudies die u in uw eigen tempo kunt uitvoeren, evenals programmeeroefeningen in de vorm van Q#-Jupyter Notebooks. De [Quantum Katas-notebooks voor zelfstudie](https://github.com/microsoft/QuantumKatas#tutorial-topics) zijn een goed beginpunt. In de Quantum Katas leert u meer over de verschillende elementen van kwantumcomputing en Q#-programmering. Ze zijn een uitstekend voorbeeld van wat voor soort inhoud u kunt maken met Q#-Jupyter Notebooks.
