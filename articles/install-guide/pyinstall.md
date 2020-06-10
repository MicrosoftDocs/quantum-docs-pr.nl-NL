---
title: 'Ontwikkelen met Q # en python'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.python
ms.openlocfilehash: 1ae208e7047cb040fb44945a59c3cc6508a09723
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630290"
---
# <a name="develop-with-q-and-python"></a>Ontwikkelen met Q # en python

Installeer de QDK om python-hosttoepassingen te ontwikkelen om Q #-bewerkingen aan te roepen.

1. Vereisten

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - Python-pakketbeheer voor [PIP](https://pip.pypa.io/en/stable/installing)
    - [.NET Core SDK 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1)


1. Installeer het `qsharp` pakket, een python-pakket dat Interop mogelijk maakt tussen Q # en python.

    ```
    pip install qsharp
    ```

1. Installeer IQ #, een kernel die wordt gebruikt door Jupyter en python die de kern functionaliteit biedt voor het compileren en uitvoeren van Q #-bewerkingen.

    ```dotnetcli
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

    > [!NOTE]
    > Als er tijdens de stap een fout optreedt `dotnet iqsharp install` , opent u een nieuw terminal venster en probeert u het opnieuw.
    > Als dit nog steeds niet werkt, probeert u het geïnstalleerde `dotnet-iqsharp` hulp programma (in Windows) te vinden en uit te `dotnet-iqsharp.exe` voeren:
    > ```
    > /path/to/dotnet-iqsharp install --user --path-to-tool="/path/to/dotnet-iqsharp"
    > ```
    > waar `/path/to/dotnet-iqsharp` moet worden vervangen door het absolute pad naar het `dotnet-iqsharp` hulp programma in het bestands systeem.
    > Normaal gesp roken wordt dit onder `.dotnet/tools` in uw gebruikersprofielmap.
  
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

        ```
        python hello_world.py
        ```

    - Controleer de uitvoer. Met het programma worden de volgende regels uitgevoerd:

        ```
        Hello from quantum world!
        ```


> [!NOTE]
> * U kunt ook python Jupyter-notebooks gebruiken om het klassieke python-programma te schrijven en Q #-bewerkingen van de cellen aan te roepen. De python-code is slechts een normaal python-programma.

## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
