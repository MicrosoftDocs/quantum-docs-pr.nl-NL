---
title: Basis classificatie met de Quantum Machine Learning-bibliotheek
description: 'Meer informatie over het uitvoeren van een Quantum sequentiële classificatie die is geschreven in Q # met de Quantum Machine Learning bibliotheek van de micro soft-QDK.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: 1d2538fd164c4c61c2712978d3b5c57b0eb766e6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275035"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a>Basis classificatie: gegevens classificeren met de QDK

In deze Quick Start leert u hoe u een Quantum sequentiële classificatie kunt uitvoeren die is geschreven in Q # met de Quantum Machine Learning bibliotheek van de QDK. 

In deze hand leiding wordt gebruikgemaakt van de halve maan gegevensset met behulp van een classificatie structuur die is gedefinieerd in Q #.

## <a name="prerequisites"></a>Vereisten

- De Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- Een Q #-project maken voor een [python-hostprogramma](xref:microsoft.quantum.install.python) of een [C#-hostprogramma](xref:microsoft.quantum.install.cs).

## <a name="host-program"></a>Host-programma

Uw hostprogramma bestaat uit drie delen:

- Laad de gegevensset en kies een set start-para meters voor uw model.
- Voer de training uit om de para meters en bias van het model te bepalen.
- Valideer het model om de nauw keurigheid te bepalen

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python met Visual Studio Code of de opdrachtregel](#tab/tabid-python)

    Als u de ' Q #-classificatie van python wilt uitvoeren, slaat u de volgende code op als `host.py` . Houd er rekening mee dat u ook het Q #-bestand nodig hebt `Training.qs` dat verderop in deze zelf studie wordt beschreven.

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    U kunt vervolgens uw Python-hostprogramma uitvoeren vanaf de opdrachtregel:

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# met Visual Studio Code of de opdrachtregel](#tab/tabid-csharp)

    Als u de ' Q #-classificatie van C# wilt uitvoeren, slaat u de volgende code op als `Host.cs` . Houd er rekening mee dat u ook het Q #-bestand nodig hebt `Training.qs` dat verderop in deze zelf studie wordt beschreven.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdrachtregel:

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# met Visual Studio 2019](#tab/tabid-vs2019)

    Als u uw nieuwe Q #-programma van C# in Visual Studio wilt uitvoeren, wijzigt `Host.cs` u de volgende C#-code. Houd er rekening mee dat u ook het Q #-bestand nodig hebt `Training.qs` dat verderop in deze zelf studie wordt beschreven.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Druk vervolgens op F5 om het programma uit te voeren. Er worden nu nieuwe vensters weergegeven met de volgende resultaten: 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a>Q- \# classificeerder code

Nu gaan we kijken hoe de bewerkingen die worden aangeroepen door het hostprogramma worden gedefinieerd in Q #.
We slaan de volgende code op in een bestand met de naam `Training.qs` .

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

De belangrijkste functies en bewerkingen die zijn gedefinieerd in de bovenstaande code zijn:

- `ClassifierStructure() : ControlledRotation[]`: in deze functie hebben we de structuur van ons circuit model ingesteld door de lagen van de beheerde poorten toe te voegen. Deze stap is vergelijkbaar met het declareren van lagen van neurons in een sequentief diep leer model.
- `TrainHalfMoonModel() : (Double[], Double)`: deze bewerking is het belangrijkste deel van de code en definieert de training. Hier laden we de voor beelden uit de gegevensset die in de bibliotheek is opgenomen, stellen we de Hyper-para meters en de eerste para meters voor de training in en de training wordt gestart door de bewerking aan te roepen `TrainSequentialClassifier` die in de bibliotheek is opgenomen. De para meters en de bias die de classificatie bepalen, worden uitgevoerd.
- `ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: met deze bewerking wordt het validatie proces gedefinieerd om het model te evalueren. Hier laden we de voor beelden voor validatie, het aantal metingen per steek proef en de tolerantie. Hiermee wordt het aantal misclassificaties voor de gekozen batch van voor beelden voor validatie uitgevoerd.

## <a name="next-steps"></a>Volgende stappen

Eerst kunt u met de code spelen en een aantal para meters wijzigen om te zien hoe dit van invloed is op de training. Vervolgens kunt u in de volgende zelf studie [uw eigen classificatie ontwerpen](xref:microsoft.quantum.libraries.machine-learning.design). u leert hoe u de structuur van de classificatie definieert.
