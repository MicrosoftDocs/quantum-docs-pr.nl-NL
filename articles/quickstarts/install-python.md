---
title: Ontwikkelen met Q# en Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
no-loc:
- Q#
- $$v
ms.openlocfilehash: 01a5c31a7a920a69f4f90701d370f3a772d2c4d2
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866737"
---
# <a name="develop-with-no-locq-and-python"></a>Ontwikkelen met Q# en Python

Installeer de QDK om Python-hostprogramma's te ontwikkelen waarmee Q#-bewerkingen kunnen worden aangeroepen.

## <a name="install-the-qsharp-python-package"></a>Het Python-pakket voor `qsharp` installeren

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

### <a name="install-using-net-cli-and-pip-advanced"></a>[Installeren met behulp van .NET CLI en PIP (geavanceerd)](#tab/tabid-dotnetcli)

1. Vereisten:

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)
    - [.NET Core SDK 3.1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Installeer het `qsharp`-pakket, een Python-pakket dat interoperabiliteit mogelijk maakt tussen Q# en Python.

    ```
    pip install qsharp
    ```

1. Installeer IQ#, een kernel die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en uitvoeren van Q#-bewerkingen.

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

Dat is alles. U beschikt nu over het Python-pakket met `qsharp` en de IQ#-kernel voor Jupyter, die de kernfunctionaliteit biedt voor het compileren en uitvoeren van Q#-bewerkingen vanuit Python, en u in staat stelt Q# Jupyter Notebooks te gebruiken.

## <a name="choose-your-ide"></a>Uw IDE kiezen

Hoewel u Q# met Python in elke IDE kunt gebruiken, raden we u ten zeerste aan om de IDE van Visual Studio Code (VS Code) voor uw Q# + Python-toepassingen te gebruiken. Met de QDK Visual Studio Code-extensie krijgt u toegang tot uitgebreidere functies, zoals waarschuwingen, markeren van syntaxis, projectsjablonen, en meer.

Ga als volgt te werk als u VS Code wilt gebruiken:

- Installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac).
- Installeer de [QDK-extensie voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

Als u een andere editor wilt gebruiken, helpen bovenstaande instructies u om aan de slag te gaan.

## <a name="write-your-first-no-locq-program"></a>Uw eerste Q#-programma schrijven

Nu bent u klaar om de installatie van het Python-pakket voor `qsharp` te controleren door een eenvoudig Q#-programma te schrijven en uit te voeren.

1. Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en de volgende code toe te voegen:

    :::code language="qsharp" source="~/quantum/samples/interoperability/qrng/Qrng.qs" range="3-14":::

1. Maak in dezelfde map als `Operation.qs` een Python-programma met de naam `host.py`, om de Q# `SampleQuantumRandomNumberGenerator()`-bewerking te simuleren:

    ```python
    import qsharp
    from Qrng import SampleQuantumRandomNumberGenerator

    print(SampleQuantumRandomNumberGenerator.simulate())
    ```

1. Voer vanuit de omgeving die u hebt gemaakt tijdens de installatie (dat is de Conda- of Python-omgeving waarin u `qsharp` hebt geïnstalleerd), het volgende programma uit:

    ```
    python host.py
    ```

1. U ziet nu het resultaat van de bewerking die u hebt aangeroepen. In dit geval ziet u `0` of `1` op het scherm, omdat met de bewerking een willekeurig resultaat is gegenereerd. Als u het programma herhaaldelijk uitvoert, ziet u elk resultaat ongeveer de helft van de tijd.

> [!NOTE]
> * De Python-code is een regulier Python-programma. U kunt een willekeurige Python-omgeving gebruiken, inclusief Jupyter Notebooks op basis van Python, om het Python-programma te schrijven en Q#-bewerkingen aan te roepen. Met het Python-programma kunnen Q#-bewerkingen worden geïmporteerd uit elk .qs-bestand dat zich in dezelfde map bevindt als de Python-code.

## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u deze zelfstudie volgen en [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
