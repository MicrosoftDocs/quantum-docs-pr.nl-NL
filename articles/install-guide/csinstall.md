---
title: Ontwikkelen met Q# en .NET
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 155367dbb1373f00e2b0bd732a5319b32462c9f9
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426505"
---
# <a name="develop-with-q-and-net"></a>Ontwikkelen met Q# en .NET

Q # is gebouwd om goed te kunnen spelen met .NET-talen zoals C# en F #.
In deze hand leiding wordt uitgelegd hoe u Q # gebruikt met een hostprogramma dat is geschreven in een .NET-taal.

## <a name="prerequisites"></a>Vereisten

- Installeer de Quantum Development Kit [voor gebruik met Q #-opdracht regel projecten](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-q-library-and-a-net-host"></a>Een Q #-bibliotheek en een .NET-host maken

De eerste stap is het maken van projecten voor uw Q #-bibliotheek en voor de .NET-host die de bewerkingen en functies bevat die in uw Q #-bibliotheek zijn gedefinieerd.

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Een nieuwe Q #-bibliotheek maken
  - Ga naar het **bestand**  ->  **Nieuw**  ->  **project**
  - Typ "Q #" in het zoekvak
  - Selecteer **Q # Library**
  - Selecteer **volgende**
  - Een naam en locatie voor uw bibliotheek kiezen
  - Zorg ervoor dat ' project en oplossing in dezelfde directory plaatsen ' is **uitgeschakeld**
  - Selecteer **maken**
- Een nieuw C#-of F #-host-programma maken
  - Ga naar **bestand** → **Nieuw** → **project**
  - Selecteer console-app (.NET core) voor C# of F #
  - Selecteer **volgende**
  - Onder *oplossing*selecteert u ' toevoegen aan oplossing '
  - Kies een naam voor uw hostprogramma
  - Selecteer **maken**

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio code of opdracht regel](#tab/tabid-cmdline)

- Een nieuwe Q #-bibliotheek maken

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Een nieuw C#-of F #-console project maken

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Voeg uw Q #-bibliotheek toe als referentie van uw host-programma

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- Beschrijving Een oplossing maken voor beide projecten

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a>Aanroepen van Q # vanuit .NET

Nadat u uw projecten hebt ingesteld, volgt u de bovenstaande instructies, kunt u aan Q # bellen vanuit uw .NET-console toepassing.
De Q #-compiler maakt .NET-klassen voor elke Q #-bewerking en functie waarmee u uw Quantum Programma's in een Simulator kunt uitvoeren.

Het voor beeld van een [.net-interoperabiliteit](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) omvat bijvoorbeeld het volgende een Q #-bewerking:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

U kunt deze bewerking vanuit .NET aanroepen op een Quantum Simulator door de `Run` methode van de .net-klasse te gebruiken `RunAlgorithm` die is gegenereerd door de Q #-compiler:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a>Volgende stappen

Nu u de Quantum Development Kit hebt ingesteld voor zowel Q # opdracht regel Programma's als voor interoperabiliteit met .NET, kunt u [uw eerste Quantum programma](xref:microsoft.quantum.quickstarts.qrng)schrijven en uitvoeren.
