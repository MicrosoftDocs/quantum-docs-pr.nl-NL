---
title: Een kwantumgenerator voor willekeurige getallen maken
description: Bouw een Q# project waarin de fundamentele Quantum concepten zoals de superpositie worden gedemonstreerd door een generator voor wille keurige getallen te maken.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8db892091794cb1166e41744572d8938d975abf2
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869763"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a>Zelfstudie: Een kwantumgenerator voor willekeurige getallen implementeren in Q\#

Een eenvoudig voor beeld van een genoteerd Quantum algoritme Q# is een Quantum ring van een wille keurig getal. Dit algoritme maakt gebruik van de aard van kwantummechanismen om een willekeurig getal te produceren.

## <a name="prerequisites"></a>Vereisten

- De Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- Een Q# project maken voor [gebruik via Q# de opdracht regel](xref:microsoft.quantum.install.standalone)of met een python- [hostprogramma](xref:microsoft.quantum.install.python) of een [C#-hostprogramma](xref:microsoft.quantum.install.cs).

## <a name="write-a-no-locq-operation"></a>Een Q# bewerking schrijven

### <a name="no-locq-operation-code"></a>Q#bewerkings code

1. Vervang de inhoud van het bestand Program.qs door de volgende code:

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

Zoals vermeld in het artikel [Inzicht in kwantumcomputing](xref:microsoft.quantum.overview.understanding) is een qubit een eenheid van kwantuminformatie die in superpositie kan zijn. Bij meting kan een qubit alleen 0 of 1 zijn. Tijdens de uitvoering vertegenwoordigt de toestand van de qubit echter de kans dat een meting een 0 of een 1 oplevert. Deze waarschijnlijkheidstoestand staat bekend als superpositie. We kunnen deze waarschijnlijkheid gebruiken voor het genereren van willekeurige getallen.

In onze Q# bewerking introduceren we het `Qubit` Data type, systeem eigen naar Q# . We kunnen een `Qubit` alleen toewijzen met een `using`-instructie. Wanneer een qubit wordt toegewezen, bevindt deze zich altijd in de toestand `Zero`. 

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


## <a name="creating-a-complete-random-number-generator"></a>Een volledige generator van willekeurige getallen maken

Nu we een bewerking hebben Q# die wille keurige bits genereert, kunnen we deze gebruiken om een volledige Quantum-generator voor wille keurige getallen te maken. We kunnen de Q# opdracht regel toepassingen gebruiken of een host-programma gebruiken.



### <a name="no-locq-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[Q#opdracht regel toepassingen met Visual Studio of Visual Studio code](#tab/tabid-qsharp)

Als u de volledige Q# opdracht regel toepassing wilt maken, voegt u het volgende toegangs punt toe aan het Q# programma: 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

Het uitvoerbare bestand voert de bewerking of functie met het kenmerk `@EntryPoint()` uit in een simulator of resourceschatter, afhankelijk van de projectconfiguratie en opdrachtregelopties.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

Druk in Visual Studio op Ctrl + F5 om het script uit te voeren.

Bouw in VS Code Program.qs voor de eerste keer door het onderstaande in de terminal in te voeren:

```dotnetcli
dotnet build
```

Voor nieuwe uitvoeringen is het niet nodig om de build opnieuw te doen. Typ de volgende opdracht en druk op enter om hem uit te voeren:

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python met Visual Studio Code of de opdrachtregel](#tab/tabid-python)

Als u uw nieuwe Q# programma wilt uitvoeren vanuit Python, slaat u de volgende code op als `host.py` :

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

U kunt vervolgens uw Python-hostprogramma uitvoeren vanaf de opdrachtregel:

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[C# met Visual Studio Code of Visual Studio](#tab/tabid-csharp)

Als u uw nieuwe Q# programma vanuit C# wilt uitvoeren, wijzigt `Driver.cs` u de volgende C#-code:

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

U kunt vervolgens uw C#-hostprogramma uitvoeren vanaf de opdrachtregel (in Visual Studio moet u op F5 drukken):

```bash
$ dotnet run
The random number generated is 42
```

***
