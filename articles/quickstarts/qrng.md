---
title: Een kwantumgenerator voor willekeurige getallen maken
description: U gaat een Q#-project bouwen waarin fundamentele kwantumconcepten, zoals superpositie, worden gedemonstreerd door een kwantumgenerator voor willekeurige getallen te maken.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: b9c8592b1296a7de1b9ad5d0538ad1972ec25e31
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2020
ms.locfileid: "77906981"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a>Quickstart: Een kwantumgenerator voor willekeurige getallen implementeren in Q#
Een eenvoudig voorbeeld van een kwantumalgoritme dat is geschreven in Q# is een kwantumgenerator voor willekeurige getallen. Dit algoritme maakt gebruik van de aard van kwantummechanismen om een willekeurig getal te produceren. 

## <a name="prerequisites"></a>Vereisten

- De Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- [Een Q#-project maken](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a>Een Q#-bewerking schrijven

### <a name="q-operation-code"></a>Q#-bewerkingscode

1. Vervang de inhoud van het bestand Operation.qs door de volgende code:

 :::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-14":::

Zoals vermeld in het artikel [Wat is kwantumcomputing?](xref:microsoft.quantum.overview.what) is een qubit een eenheid van kwantumgegevens die in superpositie kan zijn. Bij meting kan een qubit alleen 0 of 1 zijn. Tijdens de uitvoering vertegenwoordigt de toestand van de qubit echter de kans dat een meting een 0 of een 1 oplevert. Deze waarschijnlijkheidstoestand staat bekend als superpositie. We kunnen deze waarschijnlijkheid gebruiken voor het genereren van willekeurige getallen.

In onze Q#-bewerking introduceren we het gegevenstype `Qubit`, dat alleen wordt ondersteund in Q#. We kunnen een `Qubit` alleen toewijzen met een `using`-instructie. Wanneer een qubit wordt toegewezen, bevindt deze zich altijd in de toestand `Zero`. 

Met behulp van de bewerking `H` kunnen we onze `Qubit` in superpositie plaatsen. Als u een qubit wilt meten en de waarde ervan wilt lezen, gebruikt u de intrinsieke bewerking `M`.

Door onze `Qubit` in superpositie te plaatsen en vervolgens te meten, levert elke aanroep van de code een andere waarde op. 

Wanneer de toewijzing van een `Qubit` ongedaan wordt gemaakt, moet deze expliciet weer worden ingesteld op de toestand `Zero`, anders rapporteert de simulator een runtime-fout. Dit kan heel eenvoudig door `Reset` aan te roepen.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>De code visualiseren met de Blochbol

In de Blochbol vertegenwoordigt de noordpool de klassieke waarde **0** en de zuidpool de klassieke waarde **1**. Elke superpositie kan worden weergegeven met een punt op de bol (aangeduid met een pijl). Hoe dichter het einde van de pijl bij een pool is, hoe groter de kans is dat de qubit bij meting uiteenvalt in de klassieke waarde die aan die pool is toegewezen. De toestand van de qubit die wordt weergegeven door de rode pijl hieronder heeft bijvoorbeeld een hogere kans om de waarde **0** te retourneren als deze wordt gemeten.

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

We kunnen deze voorstelling gebruiken om te visualiseren wat de code doet:

* We beginnen met een qubit die is geïnitialiseerd in de toestand **0** en passen `H` toe om een superpositie te maken waarin de waarschijnlijkheid van **0** en **1** hetzelfde is.

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">


* Vervolgens meten we de qubit en slaan we de uitvoer op:

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

Aangezien het resultaat van de meting volledig willekeurig is, hebben we een willekeurige bit verkregen. We kunnen deze bewerking meerdere keren aanroepen om gehele getallen te maken. Als we de bewerking bijvoorbeeld drie keer aanroepen om drie willekeurige bits te verkrijgen, kunnen we willekeurige 3-bits getallen maken (dat wil zeggen, een willekeurig getal tussen 0 en 7).

## <a name="creating-a-complete-random-number-generator-using-a-host-program"></a>Een volledige generator van willekeurige getallen maken met een hostprogramma

Nu we een Q#-bewerking hebben die willekeurige bits genereert, kunnen we die gebruiken om een volledige generator van willekeurige getallen te bouwen met een hostprogramma.

 ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python met Visual Studio Code of de opdrachtregel](#tab/tabid-python)
 
 Als u uw nieuwe Q#-programma wilt uitvoeren vanuit Python, slaat u de volgende code op als `host.py`:
 
:::code language="python" source="~/quantum/samples/getting-started/qrng/host.py" range="11-30":::

 U kunt vervolgens uw Python-hostprogramma uitvoeren vanaf de opdrachtregel:
 ```bash
 $ python host.py
 Preparing Q# environment...
 ..The random number generated is 42
 ```
 ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# met Visual Studio Code of de opdrachtregel](#tab/tabid-csharp)
 
 Als u uw nieuwe Q#-programma wilt uitvoeren vanuit C#, wijzigt u `Driver.cs` om de volgende C#-code toe te voegen:
 
 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::
 
 U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdrachtregel:
 
 ```bash
 $ dotnet run
 The random number generated is 42
 ```

 ### <a name="c-with-visual-studio-2019"></a>[C# met Visual Studio 2019](#tab/tabid-vs2019)

 Als u uw nieuwe Q#-programma wilt uitvoeren vanuit C# in Visual Studio, wijzigt u `Driver.cs` om de volgende C#-code toe te voegen:

 :::code language="csharp" source="~/quantum/samples/getting-started/qrng/Host.cs" range="4-39":::

 Druk vervolgens op F5 om het programma uit te voeren. Er wordt nu een nieuw venster weergegeven met het willekeurig gegenereerde getal: 

 ```bash
 $ dotnet run
 The random number generated is 42
 ```
 ***
