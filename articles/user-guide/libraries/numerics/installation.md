---
title: Micro soft Quantum numeriek-bibliotheek-installatie en validatie
description: Meer informatie over hoe u de micro soft Quantum numeriek-bibliotheek kunt toevoegen aan uw installatie van Visual Studio 2019 of hoger.
author: thomashaener
ms.author: thhaner
ms.date: 05/14/2019
ms.topic: article
uid: microsoft.quantum.numerics.installation
ms.openlocfilehash: 60ee91a552fad5becf8eda437406b6e0dfba0eb4
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275189"
---
# <a name="numerics-library-installation-and-validation"></a><span data-ttu-id="d97ef-103">Installatie en validatie van de numerieke bibliotheek</span><span class="sxs-lookup"><span data-stu-id="d97ef-103">Numerics Library Installation and Validation</span></span>

<span data-ttu-id="d97ef-104">De Quantum Development Kit biedt ondersteuning voor numerieke functionaliteit via het [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet-pakket.</span><span class="sxs-lookup"><span data-stu-id="d97ef-104">The Quantum Development Kit provides support for numerics functionality through the [`Microsoft.Quantum.Numerics`](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) NuGet package.</span></span>

<span data-ttu-id="d97ef-105">**Visual Studio >= 2019:** Als u Visual Studio 2019 of hoger gebruikt, kunt u het numerieke pakket toevoegen met behulp van de NuGet-pakket Manager.</span><span class="sxs-lookup"><span data-stu-id="d97ef-105">**Visual Studio >=2019:** If you are using Visual Studio 2019 or later, you can add the numerics package using the NuGet Package Manager.</span></span>
<span data-ttu-id="d97ef-106">Selecteer hiervoor ' NuGet-pakketten beheren '. van het menu-item project in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d97ef-106">To do so, select "Manage NuGet Packages..." from the "Project" menu item in Visual Studio.</span></span>

<span data-ttu-id="d97ef-107">Zoek op het tabblad Bladeren naar de pakket naam ' micro soft. Quantum. numeric '</span><span class="sxs-lookup"><span data-stu-id="d97ef-107">From the Browse tab, search for the package name "Microsoft.Quantum.Numerics"</span></span>

> [!NOTE]
> <span data-ttu-id="d97ef-108">Zorg ervoor dat u ' include Prerelease ' aantikt</span><span class="sxs-lookup"><span data-stu-id="d97ef-108">Make sure to tick "Include prerelease"</span></span>

<span data-ttu-id="d97ef-109">Hiermee worden de pakketten weer geven die kunnen worden gedownload.</span><span class="sxs-lookup"><span data-stu-id="d97ef-109">This will list the packages available for download.</span></span>
<span data-ttu-id="d97ef-110">Als u de muis aanwijzer op ' micro soft. Quantum. numeric ' houdt, wordt er rechts van het versie nummer een pijl naar beneden gericht.</span><span class="sxs-lookup"><span data-stu-id="d97ef-110">Hovering over "Microsoft.Quantum.Numerics" reveals a downward-pointing arrow to the right of the version number.</span></span>
<span data-ttu-id="d97ef-111">Klik op de pijl om het pakket met de getallen te installeren.</span><span class="sxs-lookup"><span data-stu-id="d97ef-111">Click on the arrow in order to install the numerics package.</span></span>

<span data-ttu-id="d97ef-112">Zie de [gebruikers interface voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-ui)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d97ef-112">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="d97ef-113">U kunt ook de Package Manager-console gebruiken om de numerieke bibliotheek toe te voegen aan uw project via de opdracht regel interface.</span><span class="sxs-lookup"><span data-stu-id="d97ef-113">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![De Package Manager-console gebruiken vanaf de opdracht regel](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="d97ef-115">Voer de volgende handelingen uit vanuit de Package Manager-console:</span><span class="sxs-lookup"><span data-stu-id="d97ef-115">From the package manager console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="d97ef-116">Zie de [console handleiding voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-console)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d97ef-116">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

<span data-ttu-id="d97ef-117">**Opdracht regel of Visual Studio code:** Met de opdracht regel zelf of vanuit Visual Studio code kunt u de `dotnet` volgende opdracht gebruiken om een NuGet-pakket verwijzing toe te voegen aan uw project:</span><span class="sxs-lookup"><span data-stu-id="d97ef-117">**Command line or Visual Studio Code:** Using the command line on its own or from within Visual Studio Code, you can use the `dotnet` command to add NuGet package reference to your project:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```


## <a name="verifying-your-installation"></a><span data-ttu-id="d97ef-118">De installatie controleren</span><span class="sxs-lookup"><span data-stu-id="d97ef-118">Verifying your installation</span></span>

<span data-ttu-id="d97ef-119">Net als de rest van de Quantum Development Kit, wordt de bibliotheek met getallen geleverd met voor beelden die u zo snel mogelijk aan de slag kunnen.</span><span class="sxs-lookup"><span data-stu-id="d97ef-119">Like the rest of the Quantum Development Kit, the numerics library comes with samples that help you get started as quickly as possible.</span></span>
<span data-ttu-id="d97ef-120">Als u de installatie met behulp van deze voor beelden wilt testen, kloont u de [opslag plaats met belangrijkste voor beelden](https://github.com/Microsoft/Quantum) en voert u een van de voor beelden uit</span><span class="sxs-lookup"><span data-stu-id="d97ef-120">To test your installation using these samples, clone the [main samples repository](https://github.com/Microsoft/Quantum) and then run one of the samples.</span></span>

<span data-ttu-id="d97ef-121">Het voor [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) beeld uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="d97ef-121">To run the [`CustomModAdd`](https://github.com/microsoft/Quantum/tree/master/samples/numerics/CustomModAdd) sample:</span></span>

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics/CustomModAdd
dotnet run
```
