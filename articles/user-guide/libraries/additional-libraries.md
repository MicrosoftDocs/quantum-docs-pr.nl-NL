---
title: Extra Q# bibliotheken gebruiken
description: Meer informatie over het toevoegen van extra Q# bibliotheken aan uw Quantum toepassingen.
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
no-loc:
- Q#
- $$v
ms.openlocfilehash: ef88ca765a394a7092eb0a60bf6f3615c082ef6a
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869576"
---
# <a name="using-additional-no-locq-libraries"></a>Extra Q# bibliotheken gebruiken

De Quantum Development Kit biedt aanvullende, domein-specifieke functionaliteit via _NuGet-pakketten_ die aan uw projecten kunnen worden toegevoegd Q# .

| Q#Tagbibliotheek  | NuGet-pakket | Opmerkingen |
|---------|---------|--------|
| [Q#standaard bibliotheek](xref:microsoft.quantum.libraries.standard.intro) | [**Micro soft. Quantum. Standard**](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | Standaard opgenomen |
| [Bibliotheek voor kwantumchemie](xref:microsoft.quantum.chemistry.concepts.intro) | [**Microsoft.Quantum.Chemistry**](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [Bibliotheek voor kwantumberekeningen](xref:microsoft.quantum.numerics.intro) | [**Micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [Kwantumbibliotheek voor machine learning](xref:microsoft.quantum.libraries.machine-learning.intro) | [**Microsoft.Quantum.MachineLearning**](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

Zodra u de Quantum Development Kit hebt geïnstalleerd voor gebruik met uw voorkeurs omgeving en de taal van de host, kunt u eenvoudig bibliotheken toevoegen aan afzonderlijke Q# projecten zonder verdere installatie.

> [!NOTE]
> Sommige Q# bibliotheken kunnen goed werken met aanvullende hulp middelen die samen werken met uw Q# Program ma's of die zijn geïntegreerd met uw host-toepassingen.
> Zo wordt in de [installatie-instructies voor chemie](xref:microsoft.quantum.chemistry.concepts.installation) beschreven hoe u het [pakket **micro soft. Quantum. chemie** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) kunt gebruiken samen met het NWChem computing computing-platform, en hoe u de `qdk-chem` opdracht regel Programma's installeert voor het werken met gegevens van quantum chemie.

## <a name="no-locq-command-line-applications-or-net-interopability"></a>[Q#opdracht regel toepassingen of .NET Interop](#tab/tabid-csproj)

**Opdracht regel of Visual Studio code:** Met de opdracht regel zelf of vanuit Visual Studio code kunt u de `dotnet` opdracht gebruiken om een NuGet-pakket verwijzing toe te voegen aan uw project.
Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen, voert u de volgende opdracht uit:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

**Visual Studio:** Als u Visual Studio 2019 of hoger gebruikt, kunt u extra pakketten toevoegen Q# met behulp van de NuGet Package Manager.
Een pakket laden: 
1. Selecteer met het project open in Visual Studio **Manage NuGet packages...** in het menu **project** .

2. Klik op **Bladeren**, selecteer **include Prerelease** en zoek naar de pakket naam ' micro soft. Quantum. numerics '. Hiermee worden de pakketten weer geven die kunnen worden gedownload.

3. Beweeg de muis aanwijzer over **micro soft. Quantum. numerics** en klik op de pijl omlaag naar rechts van het versie nummer om het pakket met de getallen te installeren.

Zie de [gebruikers interface voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-ui)voor meer informatie.

U kunt ook de Package Manager-console gebruiken om de numerieke bibliotheek toe te voegen aan uw project via de opdracht regel interface.

![De Package Manager-console gebruiken vanaf de opdracht regel](~/media/vs2017-nuget-console-menu.png)

Voer de volgende handelingen uit vanuit de Package Manager-console:

```
Install-Package Microsoft.Quantum.Numerics
```

Zie de [console handleiding voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-console)voor meer informatie.

## <a name="ino-locq-notebooks"></a>[I- Q# notebooks](#tab/tabid-notebook)

U kunt extra pakketten beschikbaar maken voor gebruik in een I- Q# notebook met behulp van de [ `%package` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).
Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen voor gebruik in een I Q# -notebook, voert u de volgende opdracht uit in een notebook-cel:

```
%package Microsoft.Quantum.Numerics
```

Als u deze opdracht volgt, is het pakket beschikbaar voor alle cellen in het notitie blok.
Als u het pakket beschikbaar wilt maken op basis van Q# code in de huidige werk ruimte, laadt u de werk ruimte na het toevoegen van het pakket:

```
%workspace reload
```

## <a name="python-interoperability"></a>[Python-interoperabiliteit](#tab/tabid-python)


U kunt extra pakketten beschikbaar maken voor gebruik in een python-hostprogramma met behulp van de- [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) methode.
Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen voor gebruik in een I Q# -notebook, voert u de volgende python-code uit:

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

Als u deze opdracht volgt, wordt het pakket beschikbaar gesteld voor Q# code die wordt gecompileerd met `qsharp.compile` .
Als u het pakket beschikbaar wilt maken op basis van Q# code in de huidige werk ruimte, laadt u de werk ruimte na het toevoegen van het pakket:

```python
qsharp.reload()
```

***
