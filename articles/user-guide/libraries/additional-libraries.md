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
ms.openlocfilehash: 39bf7dc52f4670a6e4536efc437d001c96f9584a
ms.sourcegitcommit: 11bd357baeb6ab53a402882979e75964d0869b57
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/27/2020
ms.locfileid: "88992136"
---
# <a name="using-additional-no-locq-libraries"></a><span data-ttu-id="685e5-103">Extra Q# bibliotheken gebruiken</span><span class="sxs-lookup"><span data-stu-id="685e5-103">Using Additional Q# Libraries</span></span>

<span data-ttu-id="685e5-104">De Quantum Development Kit biedt aanvullende, domein-specifieke functionaliteit via _NuGet-pakketten_ die aan uw projecten kunnen worden toegevoegd Q# .</span><span class="sxs-lookup"><span data-stu-id="685e5-104">The Quantum Development Kit provides additional domain-specific functionality through _NuGet packages_ that can be added to your Q# projects.</span></span>

| <span data-ttu-id="685e5-105">Q# Tagbibliotheek</span><span class="sxs-lookup"><span data-stu-id="685e5-105">Q# Library</span></span>  | <span data-ttu-id="685e5-106">NuGet-pakket</span><span class="sxs-lookup"><span data-stu-id="685e5-106">NuGet package</span></span> | <span data-ttu-id="685e5-107">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="685e5-107">Notes</span></span> |
|---------|---------|--------|
| [<span data-ttu-id="685e5-108">Q# standaard bibliotheek</span><span class="sxs-lookup"><span data-stu-id="685e5-108">Q# standard library</span></span>](xref:microsoft.quantum.libraries.standard.intro) | [<span data-ttu-id="685e5-109">**Micro soft. Quantum. Standard**</span><span class="sxs-lookup"><span data-stu-id="685e5-109">**Microsoft.Quantum.Standard**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | <span data-ttu-id="685e5-110">Standaard opgenomen</span><span class="sxs-lookup"><span data-stu-id="685e5-110">Included by default</span></span> |
| [<span data-ttu-id="685e5-111">Bibliotheek voor kwantumchemie</span><span class="sxs-lookup"><span data-stu-id="685e5-111">Quantum chemistry library</span></span>](xref:microsoft.quantum.chemistry.concepts.intro) | [<span data-ttu-id="685e5-112">**Microsoft.Quantum.Chemistry**</span><span class="sxs-lookup"><span data-stu-id="685e5-112">**Microsoft.Quantum.Chemistry**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [<span data-ttu-id="685e5-113">Bibliotheek voor kwantumberekeningen</span><span class="sxs-lookup"><span data-stu-id="685e5-113">Quantum numerics library</span></span>](xref:microsoft.quantum.numerics.intro) | [<span data-ttu-id="685e5-114">**Micro soft. Quantum. numerics**</span><span class="sxs-lookup"><span data-stu-id="685e5-114">**Microsoft.Quantum.Numerics**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [<span data-ttu-id="685e5-115">Kwantumbibliotheek voor machine learning</span><span class="sxs-lookup"><span data-stu-id="685e5-115">Quantum machine learning library</span></span>](xref:microsoft.quantum.libraries.machine-learning.intro) | [<span data-ttu-id="685e5-116">**Microsoft.Quantum.MachineLearning**</span><span class="sxs-lookup"><span data-stu-id="685e5-116">**Microsoft.Quantum.MachineLearning**</span></span>](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

<span data-ttu-id="685e5-117">Zodra u de Quantum Development Kit hebt geïnstalleerd voor gebruik met uw voorkeurs omgeving en de taal van de host, kunt u eenvoudig bibliotheken toevoegen aan afzonderlijke Q# projecten zonder verdere installatie.</span><span class="sxs-lookup"><span data-stu-id="685e5-117">Once you have installed the Quantum Development Kit for use with your preferred environment and host language, you can easily add libraries to individual Q# projects without any further installation.</span></span>

> [!NOTE]
> <span data-ttu-id="685e5-118">Sommige Q# bibliotheken kunnen goed werken met aanvullende hulp middelen die samen werken met uw Q# Program ma's of die zijn geïntegreerd met uw host-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="685e5-118">Some Q# libraries may work well with additional tools that work alongside your Q# programs, or that integrate with your host applications.</span></span>
> <span data-ttu-id="685e5-119">Zo wordt in de [installatie-instructies voor chemie](xref:microsoft.quantum.chemistry.concepts.installation) beschreven hoe u het [pakket **micro soft. Quantum. chemie** ](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) kunt gebruiken samen met het NWChem computing computing-platform, en hoe u de `qdk-chem` opdracht regel Programma's installeert voor het werken met gegevens van quantum chemie.</span><span class="sxs-lookup"><span data-stu-id="685e5-119">For example, the [chemistry library installation instructions](xref:microsoft.quantum.chemistry.concepts.installation) describe how to use the [**Microsoft.Quantum.Chemistry** package](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) together with the NWChem computational chemistry platform, and how to install the `qdk-chem` command-line tools for working with quantum chemistry data.</span></span>

## <a name="no-locq-applications-or-net-interopability"></a>[<span data-ttu-id="685e5-120">Q# toepassingen of .NET Interop</span><span class="sxs-lookup"><span data-stu-id="685e5-120">Q# applications or .NET interopability</span></span>](#tab/tabid-csproj)

<span data-ttu-id="685e5-121">**Opdracht prompt of Visual Studio code:** Met behulp van de opdracht prompt zelf of vanuit Visual Studio code kunt u de opdracht gebruiken `dotnet` om een NuGet-pakket verwijzing toe te voegen aan uw project.</span><span class="sxs-lookup"><span data-stu-id="685e5-121">**Command prompt or Visual Studio Code:** Using the command prompt on its own or from within Visual Studio Code, you can use the `dotnet` command to add a NuGet package reference to your project.</span></span>
<span data-ttu-id="685e5-122">Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen, voert u de volgende opdracht uit:</span><span class="sxs-lookup"><span data-stu-id="685e5-122">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package, run the following command:</span></span>

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

<span data-ttu-id="685e5-123">**Visual Studio:** Als u Visual Studio 2019 of hoger gebruikt, kunt u extra pakketten toevoegen Q# met behulp van de NuGet Package Manager.</span><span class="sxs-lookup"><span data-stu-id="685e5-123">**Visual Studio:** If you are using Visual Studio 2019 or later, you can add additional Q# packages using the NuGet Package Manager.</span></span>
<span data-ttu-id="685e5-124">Een pakket laden:</span><span class="sxs-lookup"><span data-stu-id="685e5-124">To load a package:</span></span> 
1. <span data-ttu-id="685e5-125">Selecteer met het project open in Visual Studio **Manage NuGet packages...** in het menu **project** .</span><span class="sxs-lookup"><span data-stu-id="685e5-125">With a project open in Visual Studio, select **Manage NuGet Packages...** from the **Project** menu.</span></span>

2. <span data-ttu-id="685e5-126">Klik op **Bladeren**, selecteer **include Prerelease** en zoek naar de pakket naam ' micro soft. Quantum. numerics '.</span><span class="sxs-lookup"><span data-stu-id="685e5-126">Click **Browse**, select **Include prerelease** and search for the package name "Microsoft.Quantum.Numerics".</span></span> <span data-ttu-id="685e5-127">Hiermee worden de pakketten weer geven die kunnen worden gedownload.</span><span class="sxs-lookup"><span data-stu-id="685e5-127">This will list the packages available for download.</span></span>

3. <span data-ttu-id="685e5-128">Beweeg de muis aanwijzer over **micro soft. Quantum. numerics** en klik op de pijl omlaag naar rechts van het versie nummer om het pakket met de getallen te installeren.</span><span class="sxs-lookup"><span data-stu-id="685e5-128">Hover over **Microsoft.Quantum.Numerics** and click the downward-pointing arrow to the right of the version number to install the numerics package.</span></span>

<span data-ttu-id="685e5-129">Zie de [gebruikers interface voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-ui)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="685e5-129">For more details, see the [Package Manager UI guide](https://docs.microsoft.com/nuget/tools/package-manager-ui).</span></span>

<span data-ttu-id="685e5-130">U kunt ook de Package Manager-console gebruiken om de numerieke bibliotheek toe te voegen aan uw project via de opdracht regel interface.</span><span class="sxs-lookup"><span data-stu-id="685e5-130">Alternatively, you can use the Package Manager Console to add the numerics library to your project via the command line interface.</span></span>

![De Package Manager-console gebruiken vanaf de opdracht prompt](~/media/vs2017-nuget-console-menu.png)

<span data-ttu-id="685e5-132">Voer de volgende handelingen uit vanuit de Package Manager-console:</span><span class="sxs-lookup"><span data-stu-id="685e5-132">From the Package Manager Console, run the following:</span></span>

```
Install-Package Microsoft.Quantum.Numerics
```

<span data-ttu-id="685e5-133">Zie de [console handleiding voor pakket beheer](https://docs.microsoft.com/nuget/tools/package-manager-console)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="685e5-133">For more details, see the [Package Manager Console guide](https://docs.microsoft.com/nuget/tools/package-manager-console).</span></span>

## <a name="ino-locq-notebooks"></a>[<span data-ttu-id="685e5-134">I- Q# notebooks</span><span class="sxs-lookup"><span data-stu-id="685e5-134">IQ# Notebooks</span></span>](#tab/tabid-notebook)

<span data-ttu-id="685e5-135">U kunt extra pakketten beschikbaar maken voor gebruik in een I- Q# notebook met behulp van de [ `%package` opdracht Magic](xref:microsoft.quantum.iqsharp.magic-ref.package).</span><span class="sxs-lookup"><span data-stu-id="685e5-135">You can make additional packages available for use in an IQ# Notebook by using the [`%package` magic command](xref:microsoft.quantum.iqsharp.magic-ref.package).</span></span>
<span data-ttu-id="685e5-136">Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen voor gebruik in een I Q# -notebook, voert u de volgende opdracht uit in een notebook-cel:</span><span class="sxs-lookup"><span data-stu-id="685e5-136">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following command in a notebook cell:</span></span>

```
%package Microsoft.Quantum.Numerics
```

<span data-ttu-id="685e5-137">Als u deze opdracht volgt, is het pakket beschikbaar voor alle cellen in het notitie blok.</span><span class="sxs-lookup"><span data-stu-id="685e5-137">Following this command, the package is available to any cells within the notebook.</span></span>
<span data-ttu-id="685e5-138">Als u het pakket beschikbaar wilt maken op basis van Q# code in de huidige werk ruimte, laadt u de werk ruimte na het toevoegen van het pakket:</span><span class="sxs-lookup"><span data-stu-id="685e5-138">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```
%workspace reload
```

## <a name="python-interoperability"></a>[<span data-ttu-id="685e5-139">Python-interoperabiliteit</span><span class="sxs-lookup"><span data-stu-id="685e5-139">Python interoperability</span></span>](#tab/tabid-python)


<span data-ttu-id="685e5-140">U kunt extra pakketten beschikbaar maken voor gebruik in een python-hostprogramma met behulp van de- [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages) methode.</span><span class="sxs-lookup"><span data-stu-id="685e5-140">You can make additional packages available for use in a Python host program by using the [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp-core/qsharp.packages.packages) method.</span></span>
<span data-ttu-id="685e5-141">Als u bijvoorbeeld het pakket [**micro soft. Quantum. numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) wilt toevoegen voor gebruik in een I Q# -notebook, voert u de volgende python-code uit:</span><span class="sxs-lookup"><span data-stu-id="685e5-141">For example, to add the [**Microsoft.Quantum.Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) package for use in an IQ# Notebook, run the following Python code:</span></span>

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

<span data-ttu-id="685e5-142">Als u deze opdracht volgt, wordt het pakket beschikbaar gesteld voor Q# code die wordt gecompileerd met `qsharp.compile` .</span><span class="sxs-lookup"><span data-stu-id="685e5-142">Following this command, the package will be made available to any Q# code compiled using `qsharp.compile`.</span></span>
<span data-ttu-id="685e5-143">Als u het pakket beschikbaar wilt maken op basis van Q# code in de huidige werk ruimte, laadt u de werk ruimte na het toevoegen van het pakket:</span><span class="sxs-lookup"><span data-stu-id="685e5-143">To make the package available from Q# code in the current workspace, reload the workspace after adding your package:</span></span>

```python
qsharp.reload()
```

***
