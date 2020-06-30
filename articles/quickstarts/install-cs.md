---
title: Ontwikkelen met Q# en .NET
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 2b0b16bdd9fccc3b668036e6df2b20e11b32f8b6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274051"
---
# <a name="develop-with-q-and-net"></a>Ontwikkelen met Q# en .NET

Q# is gebouwd om prettig te kunnen werken met .NET-talen, zoals C# en F#.
In deze handleiding wordt uitgelegd hoe u Q# gebruikt in combinatie met een hostprogramma dat is geschreven in een .NET-taal.

## <a name="prerequisites"></a>Vereisten

- Installeer de Quantum Development Kit [voor Q#-opdrachtregelprojecten](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-q-library-and-a-net-host"></a>Een Q#-bibliotheek en een .NET-host maken

De eerste stap is het maken van projecten voor uw Q#-bibliotheek en voor de .NET-host die de bewerkingen en functies aanroept die in uw Q#-bibliotheek zijn gedefinieerd.

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Maak een nieuwe Q#-bibliotheek
  - Ga naar **Bestand** -> **Nieuw** -> **Project**
  - Typ 'Q#' in het zoekvak
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

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio Code of opdrachtregel](#tab/tabid-cmdline)

- Maak een nieuwe Q#-bibliotheek

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Maak een nieuw C#- or F#-consoleproject

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Voeg uw Q#-bibliotheek toe als referentie van uw hostprogramma

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

***

## <a name="calling-into-q-from-net"></a>Q# aanroepen vanuit .NET

Nadat u uw projecten hebt ingesteld, moet u de bovenstaande instructies volgen om Q# aan te roepen vanuit uw .NET-consoletoepassing.
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

Nu u de Quantum Development Kit hebt ingesteld voor Q#-opdrachtregelprogramma's en interoperabiliteit met .NET, kunt u [uw eerste kwantumprogramma](xref:microsoft.quantum.quickstarts.qrng) schrijven en uitvoeren.
