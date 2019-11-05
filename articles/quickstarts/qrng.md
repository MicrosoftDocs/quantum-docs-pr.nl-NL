---
title: Een kwantumgenerator voor willekeurige getallen maken
description: U gaat een Q#-project bouwen waarin fundamentele kwantumconcepten, zoals superpositie, worden gedemonstreerd door een kwantumgenerator voor willekeurige getallen te maken.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: a7c077eda3e46430cbe6598cb899adb460451f75
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73443916"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a>Quickstart: Een kwantumgenerator voor willekeurige getallen implementeren in Q#
Een eenvoudig voorbeeld van een kwantumalgoritme dat is geschreven in Q# is een kwantumgenerator voor willekeurige getallen. Dit algoritme maakt gebruik van de aard van kwantummechanismen om een willekeurig getal te produceren. 

## <a name="prerequisites"></a>Vereisten

- De Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- [Een Q#-project maken](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a>Een Q#-bewerking schrijven

### <a name="q-operation-code"></a>Q#-bewerkingscode

1. Vervang de inhoud van het bestand Operation.qs door de volgende code:

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(q = Qubit())  { // Allocate a qubit.
                H(q);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(q);     // Measure the qubit value.
                Reset(q);
                return r;
            }
        }
    }
    ```

Zoals vermeld in het artikel [Wat is kwantumcomputing?](xref:microsoft.quantum.overview.what) is een qubit een eenheid van kwantumgegevens die in superpositie kan zijn. Bij meting kan een qubit alleen 0 of 1 zijn. Tijdens de uitvoering vertegenwoordigt de toestand van de qubit echter de kans dat een meting een 0 of een 1 oplevert. Deze waarschijnlijkheidstoestand staat bekend als superpositie. We kunnen deze waarschijnlijkheid gebruiken voor het genereren van willekeurige getallen.

In onze Q#-bewerking introduceren we het gegevenstype `Qubit`, dat alleen wordt ondersteund in Q#. We kunnen een `Qubit` alleen toewijzen met een `using`-instructie. Wanneer een qubit wordt toegewezen, bevindt deze zich altijd in de toestand `Zero`. 

Met behulp van de bewerking `H` kunnen we onze `Qubit` in superpositie plaatsen. Als u een qubit wilt meten en de waarde ervan wilt lezen, gebruikt u de intrinsieke bewerking `M`.

Door onze `Qubit` in superpositie te plaatsen en vervolgens te meten, levert elke aanroep van de code een andere waarde op. 

Wanneer de toewijzing van een `Qubit` ongedaan wordt gemaakt, moet deze expliciet weer worden ingesteld op de toestand `Zero`, anders rapporteert de simulator een runtime-fout. Dit kan heel eenvoudig door `Reset` aan te roepen.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>De code visualiseren met de Blochbol

In de Blochbol vertegenwoordigt de noordpool de klassieke waarde **0** en de zuidpool de klassieke waarde **1**. Elke superpositie kan worden weergegeven met een punt op de bol (aangeduid met een pijl). Wanneer het einde van de pijl dichter bij een pool is, is de kans groter dat de qubit bij meting uiteenvalt in de klassieke waarde die aan die pool is toegewezen. De toestand van de qubit die wordt weergegeven door de rode pijl hieronder heeft bijvoorbeeld een hogere kans om de waarde **0** te retourneren als deze wordt gemeten.

<img src="./Bloch.svg" width="175">

We kunnen deze voorstelling gebruiken om te visualiseren wat de code doet:

* We beginnen met een qubit die is geïnitialiseerd in de toestand **0** en passen `H` toe om een superpositie te maken waarin de waarschijnlijkheid van **0** en **1** hetzelfde is.

<img src="./H.svg" width="450">

* Vervolgens meten we de qubit en slaan we de uitvoer op:

<img src="./Measurement2.svg" width="450">

Aangezien het resultaat van de meting volledig willekeurig is, hebben we een willekeurige bit verkregen. We kunnen deze functie meerdere keren aanroepen om gehele getallen te maken. Als we de functie bijvoorbeeld drie keer aanroepen om drie willekeurige bits te verkrijgen, kunnen we willekeurige 3-bits getallen maken (dat wil zeggen, een willekeurig getal tussen 0 en 7).
