---
title: 'Ontwikkelen met Q # Jupyter-notebooks'
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.jupyter
ms.openlocfilehash: 3302a9bd0652b2dea86b844058bf8303ee7a4a7f
ms.sourcegitcommit: c85c1b439807ac576d3a11aadca307d57b059673
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "83551036"
---
# <a name="develop-with-q-jupyter-notebooks"></a>Ontwikkelen met Q # Jupyter-notebooks

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

    ```bash
    dotnet tool install -g Microsoft.Quantum.IQSharp
    dotnet iqsharp install
    ```

1. Controleer de installatie door een `Hello World`-toepassing te maken

    - Voer de volgende opdracht uit om de Notebook-server te starten:

        ```bash
        jupyter notebook
        ```

    - Als u het Jupyter-notebook wilt openen en de URL wilt plakken die u hebt ontvangen van de opdracht regel in uw browser.

    - Maak een Jupyter Notebook met een Q#-kernel en voeg de volgende code toe aan de eerste Notebook-cel:

        ```qsharp
        operation SayHello () : Unit {
            Message("Hello from quantum world!");
        }
        ```

    - Voer deze cel van het Notebook uit:

        ![Cel met Q#-code in een Jupyter-notebook](~/media/install-guide-jupyter.png)

        U ziet `SayHello` in de uitvoer van de cel. Wanneer u werkt met Jupyter Notebook, wordt de Q#-code gecompileerd en wordt de naam van de gevonden bewerking(en) geretourneerd in de uitvoer.


    - Voer in een nieuwe cel de bewerking uit die u zojuist hebt gemaakt (in een simulator) met behulp van de `%simulate` opdracht:

        ![Cel met %simulate magic in een Jupyter-notebook](~/media/install-guide-jupyter-simulate.png)

        Het bericht wordt afgedrukt op het scherm samen met het resultaat van de bewerking die u hebt aangeroepen (hier zien we de lege tuple omdat de `()` bewerking alleen een `Unit` type retourneert).

## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum development kit hebt geïnstalleerd in de omgeving van uw voorkeur, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
