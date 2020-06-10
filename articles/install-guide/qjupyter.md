---
title: Ontwikkelen met Q#-Jupyter-notebooks
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: b80d95a160b5f46c1132d3428ba32ad6dcd5656e
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630335"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Ontwikkelen met Q#-Jupyter-notebooks

Installeer de QDK voor het ontwikkelen van Q #-bewerkingen op Q # Jupyter-notebooks.

Met Jupyter-notebooks kunt u uitvoering in-place code uitvoeren naast instructies, notities en andere inhoud. Deze omgeving is ideaal voor het schrijven van Q #-code met Inge sloten zelf studies voor uitleg of Quantum Computing. Hier leest u hoe u aan de slag gaat om uw eigen Q#-notebooks te maken.

IQ# (spreek uit als 'i-q-sharp') is een extensie voor de .NET Core SDK die hoofdzakelijk wordt gebruikt door Jupyter en Python, en die de kernfunctionaliteit biedt voor het compileren en simuleren van Q#-bewerkingen.

> [!NOTE]
> * In Q # Jupyter-notebooks kunt u alleen Q # code uitvoeren en de bewerkingen kunnen niet worden aangeroepen vanuit externe host-Program ma's (zoals python of C#-bestanden). Deze omgeving is niet geschikt als u een extern klassiek host-programma wilt combi neren met het Quantum programma.

1. Vereisten

    - [Python](https://www.python.org/downloads/) 3.6 of hoger
    - [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install.html)
    - [.NET Core SDK 3,1](https://dotnet.microsoft.com/download/dotnet-core/3.1)

1. Installeer het pakket `iqsharp`

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

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Voer de volgende opdracht uit om de Notebook-server te starten:

        ```
        jupyter notebook
        ```

    - Als u de Jupyter Notebook wilt openen, kopieert en plakt u de URL die u hebt ontvangen van de opdracht regel in uw browser.

    - Maak een Jupyter Notebook met een Q #-kernel en voeg de volgende code toe aan de eerste notebook-cel:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Voer deze cel van het Notebook uit:

        ![Jupyter Notebook cel met Q # code](~/media/install-guide-jupyter.png)

        U ziet `SayHello` in de uitvoer van de cel. Wanneer in Jupyter Notebook wordt uitgevoerd, wordt de Q #-code gecompileerd en de notitie blok voert de naam van de bewaarde bewerking (en) uit.


    - Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de `%simulate` opdracht:

        ![Jupyter Notebook cel met% simulatie Magic](~/media/install-guide-jupyter-simulate.png)

        Het bericht wordt afgedrukt op het scherm samen met het resultaat van de bewerking die u hebt aangeroepen (hier zien we de lege tuple omdat de `()` bewerking alleen een `Unit` type retourneert).

## <a name="next-steps"></a>Volgende stappen

Nu u de QDK voor Q # Jupyter-notebooks hebt geïnstalleerd, kunt u [uw eerste Quantum programma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren door uw Q #-code rechtstreeks in de Jupyter notebook omgeving te schrijven.

Voor meer voor beelden van wat u kunt doen met Q # Jupyter-notebooks, gaat u naar:
- [Inleiding tot Q # en Jupyter notebook](https://docs.microsoft.com/samples/microsoft/quantum/intro-to-qsharp-jupyter/). Er wordt een Q #-Jupyter Notebook weer gegeven waarin wordt uitgelegd hoe u Q # in deze omgeving kunt gebruiken.
- [Quantum Katas](xref:microsoft.quantum.overview.katas), een open-source verzameling zelf studies en reeksen programmeer oefeningen in de vorm van Q # Jupyter-notebooks. De [Quantum Katas zelf studie notebooks](https://github.com/microsoft/QuantumKatas#tutorial-topics) zijn een goed uitgangs punt. De Quantum Katas is gericht op het aanwijzen van de elementen van Quantum Computing en Q #-programmering tegelijk. Ze zijn een uitstekend voor beeld van wat voor soort inhoud u kunt maken met Q # Jupyter-notebooks.
