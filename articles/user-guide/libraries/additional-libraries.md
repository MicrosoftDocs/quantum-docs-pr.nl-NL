---
title: 'Extra Q #-bibliotheken gebruiken'
description: 'Meer informatie over het toevoegen van extra Q #-bibliotheken aan uw Quantum toepassingen.'
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
ms.openlocfilehash: b82113b925870d07c8a28aecd50176e009826062
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86872619"
---
# <a name="using-additional-q-libraries"></a>Extra Q #-bibliotheken gebruiken

De Quantum Development Kit biedt aanvullende, domein-specifieke functionaliteit via _NuGet-pakketten_ die aan uw Q #-projecten kunnen worden toegevoegd.

| Q #-bibliotheek  | NuGet-pakket | Opmerkingen |
|---------|---------|--------|
| [Q # standaard bibliotheek](xref:microsoft.quantum.libraries.standard.intro) | [**Micro soft. Quantum. Standard**](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | Standaard opgenomen |
| [Bibliotheek voor kwantumchemie](xref:microsoft.quantum.chemistry.concepts.intro) | [**Microsoft.Quantum.Chemistry**](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [Bibliotheek voor kwantumberekeningen](xref:microsoft.quantum.numerics.intro) | [**Micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [Kwantumbibliotheek voor machine learning](xref:microsoft.quantum.libraries.machine-learning.intro) | [**Microsoft.Quantum.MachineLearning**](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

Zodra u de Quantum Development Kit hebt geïnstalleerd voor gebruik met uw voorkeurs omgeving en de taal van de host, kunt u eenvoudig bibliotheken toevoegen aan afzonderlijke Q #-projecten zonder verdere installatie.

> [!NOTE]
> Sommige Q #-bibliotheken kunnen goed werken met aanvullende hulp middelen die samen werken met uw Q #-Program ma's of die zijn geïntegreerd met uw hosttoepassingen.
> Zo wordt in de [installatie-instructies voor chemie](xref:microsoft.quantum.chemistry.concepts.installation) beschreven hoe u het [pakket **micro soft. Quantum. chemie** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) kunt gebruiken samen met het NWChem computing computing-platform, en hoe u de `qdk-chem` opdracht regel Programma's installeert voor het werken met gegevens van quantum chemie.

## <a name="q-command-line-applications-or-net-interopability"></a>[Q # opdracht regel toepassingen of .NET Interop](#tab/tabid-csproj)

**Opdracht regel of Visual Studio code:** Met de opdracht regel zelf of vanuit Visual Studio code kunt u de `dotnet` opdracht gebruiken om een NuGet-pakket verwijzing toe te voegen aan uw project.
Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen, voert u de volgende opdracht uit:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

**Visual Studio:** Als u Visual Studio 2019 of hoger gebruikt, kunt u extra Q #-pakketten toevoegen met behulp van de NuGet-pakket Manager.
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

## <a name="iq-notebooks"></a>[IQ # notebooks](#tab/tabid-notebook)

U kunt extra pakketten beschikbaar maken voor gebruik in een IQ # notebook met behulp van de [ `%package` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).
Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen voor gebruik in een IQ # notebook, voert u de volgende opdracht uit in een notebook-cel:

```
%package Microsoft.Quantum.Numerics
```

Als u deze opdracht volgt, is het pakket beschikbaar voor alle cellen in het notitie blok.
Als u het pakket beschikbaar wilt maken van Q # code in de huidige werk ruimte, laadt u de werk ruimte na het toevoegen van het pakket:

```
%workspace reload
```

## <a name="python-interoperability"></a>[Python-interoperabiliteit](#tab/tabid-python)


U kunt extra pakketten beschikbaar maken voor gebruik in een python-hostprogramma met behulp van de- [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) methode.
Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen voor gebruik in een IQ # notebook, voert u de volgende python-code uit:

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

De volgende opdracht wordt het pakket beschikbaar gesteld voor alle Q #-code die is gecompileerd met `qsharp.compile` .
Als u het pakket beschikbaar wilt maken van Q # code in de huidige werk ruimte, laadt u de werk ruimte na het toevoegen van het pakket:

```python
qsharp.reload()
```

***
