---
title: Ontwikkelen met Q# en Python
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 6513acd5b9cdce15ce61ed2c0454f46e6a6d9bd0
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274048"
---
# <a name="develop-with-q-and-python"></a>Ontwikkelen met Q# en Python

Installeer de QDK om Python-hostprogramma's te ontwikkelen waarmee Q#-bewerkingen kunnen worden aangeroepen.

1. Vereisten

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
  
1. Hoewel u Q# met Python in elke IDE kunt gebruiken, raden we u ten zeerste aan om de IDE van Visual Studio Code (VS Code) voor uw Q# + Python-toepassingen te gebruiken. Met Visual Studio Code en de QDK Visual Studio Code-extensie krijgt u toegang tot meer functies.

    - Installeer [VS Code](https://code.visualstudio.com/download) (Windows, Linux en Mac)
    - Installeer de [QDK-extensie voor VS Code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Maak een minimale Q#-bewerking door een bestand met de naam `Operation.qs` te maken en er de volgende code aan toe te voegen:

        ```qsharp
        namespace HelloWorld {
            open Microsoft.Quantum.Intrinsic;
            open Microsoft.Quantum.Canon;

            operation SayHello() : Unit {
                Message("Hello from quantum world!");
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

        ```
        python hello_world.py
        ```

    - Controleer de uitvoer. Met het programma worden de volgende regels uitgevoerd:

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * U kunt Python Jupyter Notebooks ook gebruiken om het klassieke Python-programma te schrijven en Q#-bewerkingen vanuit de cellen aan te roepen. De Python-code is een regulier Python-programma.

## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
