---
title: 'Ontwikkelen met Q # + python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 1e40c2dddeaf4fad41693c976493f10fffffa139
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76830998"
---
# <a name="develop-with-q--python"></a>Ontwikkelen met Q # + python

Installeer de QDK om python-hosttoepassingen te ontwikkelen om Q #-bewerkingen aan te roepen.

1. Vereisten

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)
    - [.NET Core SDK 3,1 of hoger](https://www.microsoft.com/net/download)


1. Installeer het `qsharp`-pakket, een python-pakket dat Interop mogelijk maakt tussen Q # en python.

    ```bash
    pip install qsharp
    ```

1. Installeer `iqsharp`, een kernel die wordt gebruikt door Jupyter en python die de kern functionaliteit biedt voor het compileren en uitvoeren van Q #-bewerkingen.

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```
  
1. Hoewel u Q # met python kunt gebruiken in een IDE, raden we u aan om met behulp van de IDE # + python-toepassingen van de Q # code (VS code) te gebruiken. Met Visual Studio code en de Visual Studio code extension van QDK krijgt u toegang tot uitgebreide functionaliteit.

    - [VS-code](https://code.visualstudio.com/download) installeren (Windows, Linux en Mac)
    - Installeer de [QDK-uitbrei ding voor VS code](https://marketplace.visualstudio.com/items?itemName=quantum.quantum-devkit-vscode).

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

        ```bash
        python hello_world.py
        ```

    - Controleer de uitvoer. Met het programma worden de volgende regels uitgevoerd:

        ```bash
        Hello from quantum world!
       ```


> [!NOTE]
> * U kunt ook python Jupyter-notebooks gebruiken om het klassieke python-programma te schrijven en Q #-bewerkingen van de cellen aan te roepen. De python-code is slechts een normaal python-programma.

## <a name="whats-next"></a>En verder?

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.write-program) schrijven en uitvoeren.