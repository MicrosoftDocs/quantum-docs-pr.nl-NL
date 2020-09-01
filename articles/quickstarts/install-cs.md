---
title: Ontwikkelen met Q# en .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: 24318380e0e63957a51961762a33446fe0121b21
ms.sourcegitcommit: 75c4edc7c410cc63dc8352e2a5bef44b433ed188
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/25/2020
ms.locfileid: "88863680"
---
# <a name="develop-with-no-locq-and-net"></a>Ontwikkelen met Q# en .NET

Q# is gebouwd om prettig te kunnen werken met .NET-talen als C# en F#.
In deze handleiding wordt uitgelegd hoe u Q# gebruikt in combinatie met een hostprogramma dat is geschreven in een .NET-taal.

Eerst maken we de Q#-toepassing en .NET-host, en vervolgens laten we zien hoe u Q# aanroept vanaf de host.

## <a name="prerequisites"></a>Vereisten

- Installeer de Quantum Development Kit [voor Q#-projecten](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-no-locq-library-and-a-net-host"></a>Een Q#-bibliotheek en een .NET-host maken

De eerste stap bestaat uit het maken van projecten voor uw Q#-bibliotheek en voor de .NET-host die de bewerkingen en functies aanroept die in de Q#-bibliotheek zijn gedefinieerd.

Volg de instructies op het tabblad dat hoort bij de ontwikkelomgeving.
Als u een andere editor gebruikt dan Visual Studio of VS Code, volgt u gewoon de stappen voor de opdrachtprompt.

### <a name="visual-studio-code-or-command-prompt"></a>[Visual Studio Code of opdrachtprompt](#tab/tabid-cmdline)

- Een nieuwe Q#-bibliotheek maken

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Maak een nieuw C#- or F#-consoleproject

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Voeg vanaf uw hostprogramma de Q#-bibliotheek toe als referentie

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- [Optioneel] Maak een oplossing voor beide projecten

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Een nieuwe Q#-bibliotheek maken
  - Ga naar **Bestand** -> **Nieuw** -> **Project**
  - Typ Q# in het zoekvak
  - Selecteer **Q#-bibliotheek**
  - Selecteer **Volgende**
  - Kies een naam en een locatie voor uw bibliotheek
  - Zorg ervoor dat 'project en oplossing in dezelfde map plaatsen' is **uitgeschakeld**
  - Selecteer **Maken**
- Maak een nieuw C#- of F#-hostprogramma
  - Ga naar **Bestand** → **Nieuw** → **Project**
  - Selecteer 'Consoletoepassing (.NET Core)' voor C# of F#
  - Selecteer **Volgende**
  - Selecteer onder *oplossing* de optie 'aan oplossing toevoegen'
  - Kies een naam voor uw hostprogramma
  - Selecteer **Maken**

***

## <a name="calling-into-no-locq-from-net"></a>Q# aanroepen vanuit .NET

Nadat u de projecten hebt ingesteld, moet u de bovenstaande instructies volgen om Q# aan te roepen vanuit de .NET-consoletoepassing.
De Q#-compiler maakt .NET-klassen voor elke Q#-bewerking en -functie waarmee u uw kwantumprogramma's in een simulator kunt uitvoeren.

Zo bevat het [.NET-interoperabiliteitsvoorbeeld](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) het volgende voorbeeld van een Q#-bewerking:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Als u deze bewerking vanuit .NET wilt aanroepen in een kwantumsimulator, kunt u de `Run`-methode gebruiken van de `RunAlgorithm` .NET-klasse die is gegenereerd door de Q#-compiler:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum Development Kit hebt ingesteld voor Q#-toepassingen en interoperabiliteit met .NET, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
