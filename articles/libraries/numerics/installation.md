---
title: Installatie en validatie van de Nummerings bibliotheek | Microsoft Docs
description: Installatie en validatie van de numerieke bibliotheek
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: c41bb73ea484271689eea2ca1b59ce6639dc15a7
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036454"
---
# <a name="numerics-library-installation-and-validation"></a>Installatie en validatie van de numerieke bibliotheek

De Quantum Development Kit biedt ondersteuning voor numerieke functionaliteit via het NuGet-pakket van [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) .

**Visual Studio > = 2019:** Als u Visual Studio 2019 of hoger gebruikt, kunt u het numerieke pakket toevoegen met behulp van de NuGet-pakket Manager.
Selecteer hiervoor ' NuGet-pakketten beheren '. van het menu-item project in Visual Studio.

Zoek op het tabblad Bladeren naar de pakket naam ' micro soft. Quantum. numeric '

> [!NOTE]
> Zorg ervoor dat u ' include Prerelease ' aantikt

Hiermee worden de pakketten weer geven die kunnen worden gedownload.
Als u de muis aanwijzer op ' micro soft. Quantum. numeric ' houdt, wordt er rechts van het versie nummer een pijl naar beneden gericht.
Klik op de pijl om het pakket met de getallen te installeren.

Zie de [gebruikers interface voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-ui)voor meer informatie.

U kunt ook de Package Manager-console gebruiken om de numerieke bibliotheek toe te voegen aan uw project via de opdracht regel interface.

![](../../media/vs2017-nuget-console-menu.png)

Voer de volgende handelingen uit vanuit de Package Manager-console:

```
Install-Package Microsoft.Quantum.Numerics
```

Zie de [console handleiding voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-console)voor meer informatie.

**Opdracht regel of Visual Studio code:** Met de opdracht regel zelf of vanuit Visual Studio code kunt u de `dotnet` opdracht gebruiken om de NuGet-pakket verwijzing toe te voegen aan uw project:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a>De installatie controleren

Net als de rest van de Quantum Development Kit, wordt de bibliotheek met getallen geleverd met voor beelden die u zo snel mogelijk aan de slag kunnen.
Als u de installatie met behulp van deze voor beelden wilt testen, kloont u de [opslag plaats met belangrijkste voor beelden](https://github.com/Microsoft/Quantum) en voert u een van de voor beelden uit

Het [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) -voor beeld uitvoeren:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
