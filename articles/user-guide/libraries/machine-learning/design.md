---
title: Uw eigen classificatie ontwerpen met de QDK
description: Leer de basis concepten van het ontwerpen van circuit modellen voor de classificatie van het Quantum circuit Basic.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
ms.openlocfilehash: b304b9d1a15f164f4dfe758aaed31b7b2369b18c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275149"
---
# <a name="design-your-own-classifier"></a>Uw eigen classificatie ontwerpen

In deze hand leiding leert u de basis concepten achter het ontwerp van circuit modellen voor de gecentreerde Quantum-circuit classificatie.

Net als bij klassiek diep leren is er geen algemene regel voor het kiezen van een specifieke architectuur. Afhankelijk van het probleem zullen sommige architecturen beter zijn dan andere. Er zijn echter enkele concepten die nuttig kunnen zijn bij het ontwerpen van het circuit:

- Een groot aantal para meters is een flexibeler model, dat mogelijk geschikt is voor het tekenen van gecompliceerde classificatie grenzen, maar dat ook vatbaarer is voor overmontage.

- Entangling-poorten tussen qubits zijn essentieel voor het vastleggen van de correlaties tussen de Quantum functies.

## <a name="how-to-build-a-classifier-with-q"></a>Een classificatie bouwen met Q\#

Voor het bouwen van een classificatie gaan we parametrized beheerde rotaties in ons circuit model samen voegen. Hiervoor kunnen we het type gebruiken dat is [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) gedefinieerd in de Quantum machine learning-bibliotheek. Dit type accepteert vier argumenten die bepalen: de index van de doel-Qubit, de matrix van de indexen van het besturings element qubits, de rotatieas en de index van de bijbehorende para meter in de matrix met para meters waarmee het model wordt gedefinieerd.

Laten we een voor beeld zien van een classificatie. In het voor [beeld van halve maan](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons)kunnen we de volgende classificatie vinden die in het bestand is gedefinieerd `Training.qs` .

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

Wat we hier definiëren, is een functie die een matrix van `ControlledRotation` elementen retourneert, samen met een matrix met para meters en een bias definieert onze [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel) . Dit type is fundamenteel in de Quantum Machine Learning-bibliotheek en definieert de classificatie. Het circuit dat is gedefinieerd in de bovenstaande functie maakt deel uit van een classificatie waarin elk voor beeld van de gegevensset twee functies bevat. Daarom hebben we slechts twee qubits nodig. De grafische weer gave van het circuit is:

 ![Voor beeld van circuit model](~/media/circuit_model_1.PNG)

## <a name="use-the-library-functions-to-write-layers-of-gates"></a>De functies van de bibliotheek gebruiken om lagen van poorten te schrijven

Stel dat er een gegevensset met 784-functies per exemplaar is, zoals installatie kopieën van 28 × 28 pixels, zoals de MNIST-gegevensset. In dit geval wordt de breedte van het circuit groot genoeg zodat elke afzonderlijke Gate een mogelijke, maar niet-praktische taak wordt. Daarom biedt de Quantum Machine Learning bibliotheek een set hulpprogram ma's waarmee automatisch lagen van parametrized-rotaties kunnen worden gegenereerd. De functie [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) retourneert bijvoorbeeld een matrix met onbeheerde rotaties met één Qubit langs een bepaalde as, met één rotatie voor elke qubit in de kassa, elk parametrized met een andere model parameter. `LocalRotationsLayer(4, X)`Retourneert bijvoorbeeld de volgende set Gates:

 ![Laag lokale draaiingen](~/media/local_rotations_layer.PNG)

We raden u aan de [API-verwijzing van de Quantum machine learning Library](xref:microsoft.quantum.machinelearning) te verkennen om alle hulpprogram ma's te ontdekken die beschikbaar zijn om het circuit ontwerp te stroom lijnen.

## <a name="next-steps"></a>Volgende stappen

 Probeer verschillende structuren in de voor beelden van de voor beelden. Ziet u eventuele wijzigingen in de prestaties van het model? In de volgende zelf studie [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load) leert u hoe u gegevens sets kunt laden om nieuwe architecturen van classificaties te verkennen.
