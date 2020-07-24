---
title: Ontwikkelen met Q#-Jupyter Notebooks
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: bbd1f58ba7de205e452be7bac72b5fd78e7acd56
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871447"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Ontwikkelen met Q#-Jupyter Notebooks

Installeer de QDK voor het ontwikkelen van Q#-bewerkingen op Q#-Jupyter Notebooks.

Met Jupyter Notebooks kunt u in-place codes uitvoeren naast instructies, notities en andere inhoud. Deze omgeving is ideaal voor het schrijven van Q#-codes met ingesloten uitleg of interactieve zelfstudies over kwantumcomputing. Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.

> [!NOTE]
> * In Q#-Jupyter Notebooks kunt u alleen Q#-codes uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe hostprogramma's (zoals Python of C#-bestanden). Deze omgeving is niet geschikt als u een extern, klassiek hostprogramma wilt combineren met het kwantumprogramma.

## <a name="install-the-iq-jupyter-kernel"></a>De IQ # Jupyter-kernel installeren

IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.

### <a name="install-using-conda-recommended"></a>[Installeren met behulp van Conda (aanbevolen)](#tab/tabid-conda)

1. Installeer [Miniconda](https://docs.conda.io/en/latest/miniconda.html) of [Anaconda](https://www.anaconda.com/products/individual#Downloads). **Opmerking:** 64-bits installatie vereist.

1. Open een Anaconda-prompt.

   - Of, als u liever PowerShell of pwsh gebruikt: open een shell, voer `conda init powershell` uit, sluit de shell en open deze vervolgens opnieuw.

1. Maak en activeer een nieuwe Conda-omgeving met de naam `qsharp-env` met de vereiste pakketten (inclusief Jupyter Notebook en IQ#) door de volgende opdrachten uit te voeren:

    ```
    conda create -n qsharp-env -c quantum-engineering qsharp notebook

    conda activate qsharp-env
    ```

1. Voer `python -c "import qsharp"` uit via dezelfde terminal om de installatie te controleren, en vul de lokale pakketcache met alle vereiste QDK-onderdelen.

### <a name="install-using-net-cli-advanced"></a>[Installeren met behulp van .NET CLI (geavanceerd)](#tab/tabid-dotnetcli)

1. Vereisten:

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Installeer het `Microsoft.Quantum.IQSharp`-pakket.

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
    
***

Dat is alles. U beschikt nu over de IQ#-kernel voor Jupyter, die de kernfunctionaliteit biedt voor het compileren en uitvoeren van Q#-bewerkingen vanuit Q# Jupyter Notebooks.

## <a name="create-your-first-q-notebook"></a>Uw eerste Q#-notebook maken

Nu bent u klaar om de installatie van uw Q# Jupyter Notebook te controleren door een eenvoudige Q#-bewerking te schrijven en uit te voeren.

1. Voer vanuit de omgeving die u hebt gemaakt tijdens de installatie (dat is de Conda-omgeving die u hebt gemaakt, of de Python-omgeving waarin u Jupyter hebt geïnstalleerd), het volgende programma uit om de Jupyter Notebook-server te starten:

    ```
    jupyter notebook
    ```

    - Als Jupyter Notebook niet automatisch wordt geopend in de browser, kopieert en plakt u de URL die u van de opdrachtregel hebt ontvangen, in de browser.

1. Kies Nieuw → Q# om een Jupyter Notebook met een Q#-kernel te maken, en voeg de volgende code toe aan de eerste notebook-cel:

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="6-13":::

1. Voer deze cel van het Notebook uit:

    ![Cel met Q#-code in een Jupyter Notebook](~/media/install-guide-jupyter.png)

    U ziet `SampleQuantumRandomNumberGenerator` in de uitvoer van de cel. Als u de Q#-code uitvoert in een Jupyter Notebook, wordt de Q#-code gecompileerd en zijn de namen van alle gevonden bewerkingen te zien in de uitvoer van de cel.

1. Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de opdracht `%simulate`:

    ![Cel met %simulate magic in een Jupyter Notebook](~/media/install-guide-jupyter-simulate.png)

    U ziet nu het resultaat van de bewerking die u hebt aangeroepen. In dit geval ziet u `Zero` of `One` op het scherm, omdat met de bewerking een willekeurig resultaat is gegenereerd. Als u de cel herhaaldelijk uitvoert, ziet u elk resultaat ongeveer de helft van de tijd.

## <a name="next-steps"></a>Volgende stappen

Nu u de QDK voor Q#-Jupyter Notebooks hebt geïnstalleerd, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren door Q#-code rechtstreeks in de Jupyter Notebook-omgeving te schrijven.

Ga voor meer voorbeelden van wat u kunt doen met Q#-Jupyter Notebooks naar:

- [Inleiding tot Q# en Jupyter Notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Hier vindt u een Q#-Jupyter Notebook dat meer details biedt over hoe u Q# kunt gebruiken in de Jupyter-omgeving.
- [Quantum Katas](xref:microsoft.quantum.overview.katas), een open-source verzameling van zelfstudies die u in uw eigen tempo kunt uitvoeren, evenals programmeeroefeningen in de vorm van Q#-Jupyter Notebooks. De [Quantum Katas-notebooks voor zelfstudie](https://github.com/microsoft/QuantumKatas#tutorial-topics) zijn een goed beginpunt. In de Quantum Katas leert u meer over de verschillende elementen van kwantumcomputing en Q#-programmering. Ze zijn een uitstekend voorbeeld van wat voor soort inhoud u kunt maken met Q#-Jupyter Notebooks.
