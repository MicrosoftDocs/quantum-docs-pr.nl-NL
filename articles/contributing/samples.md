---
title: Voor beelden die bijdragen aan de micro soft-QDK
description: Meer informatie over hoe u voorbeeld code bijdraagt aan de Microsoft Quantum Development Kit (QDK).
author: cgranade
ms.author: chgranad
ms.date: 10/12/2018
ms.topic: article
uid: microsoft.quantum.contributing.samples
ms.openlocfilehash: 3bd0de04a448c74eea6c3e8e3a15dcbb19f9d705
ms.sourcegitcommit: d61b388651351e5abd4bfe7a672e88b84a6697f8
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/10/2020
ms.locfileid: "79024148"
---
# <a name="contributing-samples-to-the-quantum-development-kit"></a><span data-ttu-id="2ee9c-103">Voor beelden die bijdragen aan de Quantum Development Kit</span><span class="sxs-lookup"><span data-stu-id="2ee9c-103">Contributing Samples to the Quantum Development Kit</span></span>

<span data-ttu-id="2ee9c-104">Als u geïnteresseerd bent in het verzenden van code naar de [opslag plaats voor beelden](https://github.com/Microsoft/Quantum), hartelijk dank dat u de Quantum Development Community een betere plaats wilt maken.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-104">If you're interested in contributing code to the [samples repository](https://github.com/Microsoft/Quantum), thank you for making the quantum development community a better place!</span></span>

## <a name="the-quantum-development-kit-samples-repository"></a><span data-ttu-id="2ee9c-105">De voor beelden van de Quantum Development Kit-opslag plaats</span><span class="sxs-lookup"><span data-stu-id="2ee9c-105">The Quantum Development Kit Samples Repository</span></span>

<span data-ttu-id="2ee9c-106">Om u te helpen uw bijdrage voor te bereiden om zo veel mogelijk te helpen, is het handig om snel te kijken hoe de voor beelden van de opslag plaats worden opgesteld:</span><span class="sxs-lookup"><span data-stu-id="2ee9c-106">To help you prepare your contribution to help out as much as possible, it's helpful to take a quick look at how the samples repository is laid out:</span></span>

```plaintext
microsoft/Quantum
📁 samples/
  📁 algorithms/
    📁 chsh-game/
      📝 CHSHGame.csproj
      📝 Game.qs
      📝 Host.cs
      📝 host.py
      📝 README.md
     ⋮
  📁 arithmetic/
  📁 characterization/
  📁 chemistry/
   ⋮
```

<span data-ttu-id="2ee9c-107">Dat wil zeggen dat de voor beelden in de [micro soft/Quantum-opslag plaats](https://github.com/microsoft/Quantum) worden onderverdeeld op onderwerpgebied in andere mappen, zoals `algorithms/`, `arithmetic/`of `characterization/`.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-107">That is, the samples in the [microsoft/Quantum repository](https://github.com/microsoft/Quantum) are broken down by subject area into different folders such as `algorithms/`, `arithmetic/`, or `characterization/`.</span></span>
<span data-ttu-id="2ee9c-108">In de map voor elk onderwerp, bestaat elk voor beeld uit één map waarin alles wordt verzameld voor een gebruiker die het voor beeld moet verkennen en gebruiken.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-108">Within the folder for each subject area, each sample consists of a single folder that collects everything a user will need to explore and make use of that sample.</span></span>

## <a name="how-samples-are-structured"></a><span data-ttu-id="2ee9c-109">Hoe steek proeven worden gestructureerd</span><span class="sxs-lookup"><span data-stu-id="2ee9c-109">How Samples are Structured</span></span>

<span data-ttu-id="2ee9c-110">Aan de hand van de bestanden die in elke map zijn gemaakt, gaan we naar het [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) -voor beeld.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-110">Looking at the files that make up each folder, let's dive into the [`algorithms/chsh-game/`](https://github.com/microsoft/Quantum/tree/master/samples/algorithms/chsh-game) sample.</span></span>

| <span data-ttu-id="2ee9c-111">File</span><span class="sxs-lookup"><span data-stu-id="2ee9c-111">File</span></span>              | <span data-ttu-id="2ee9c-112">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2ee9c-112">Description</span></span>                                                |
|-------------------|------------------------------------------------------------|
| `CHSHGame.csproj` | <span data-ttu-id="2ee9c-113">Q #-project gebruikt om het voor beeld samen te stellen met de .NET Core SDK</span><span class="sxs-lookup"><span data-stu-id="2ee9c-113">Q# project used to build the sample with the .NET Core SDK</span></span> |
| `Game.qs`         | <span data-ttu-id="2ee9c-114">Q # bewerkingen en functies voor het voor beeld</span><span class="sxs-lookup"><span data-stu-id="2ee9c-114">Q# operations and functions for the sample</span></span>                 |
| `Host.cs`         | <span data-ttu-id="2ee9c-115">C#hostprogramma dat wordt gebruikt om het voor beeld uit te voeren</span><span class="sxs-lookup"><span data-stu-id="2ee9c-115">C# host program used to run the sample</span></span>                     |
| `host.py`         | <span data-ttu-id="2ee9c-116">Python-hostcluster dat wordt gebruikt om het voor beeld uit te voeren</span><span class="sxs-lookup"><span data-stu-id="2ee9c-116">Python host program used to run the sample</span></span>                 |
| `README.md`       | <span data-ttu-id="2ee9c-117">Documentatie over wat het voor beeld doet en hoe u het kunt gebruiken</span><span class="sxs-lookup"><span data-stu-id="2ee9c-117">Documentation on what the sample does and how to use it</span></span>    |

<span data-ttu-id="2ee9c-118">Niet alle voor beelden hebben exact dezelfde set bestanden (bijvoorbeeld: sommige voor beelden zijn alleen mogelijk, C#andere hebben mogelijk geen python-host, of voor sommige voor beelden zijn mogelijk auxillary-gegevens bestanden vereist).</span><span class="sxs-lookup"><span data-stu-id="2ee9c-118">Not all samples will have the exact same set of files (e.g.: some samples may be C#-only, others may not have a Python host, or some samples may require auxillary data files to work).</span></span>

## <a name="anatomy-of-a-helpful-readme-file"></a><span data-ttu-id="2ee9c-119">Anatomie van een handig Leesmij-bestand</span><span class="sxs-lookup"><span data-stu-id="2ee9c-119">Anatomy of a Helpful README File</span></span>

<span data-ttu-id="2ee9c-120">Een bijzonder belang rijk bestand is, hoewel het `README.md` bestand is, zoals wat gebruikers nodig hebben om aan de slag te gaan met uw voor beeld.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-120">One especially important file, though, is the `README.md` file, as that's what users need to get started with your sample!</span></span>

<span data-ttu-id="2ee9c-121">Elk `README.md` moet beginnen met een aantal meta gegevens waarmee docs.microsoft.com/samples uw bijdrage kan vinden.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-121">Each `README.md` should start with some metadata that helps docs.microsoft.com/samples find your contribution.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="2ee9c-122">Bekijk hoe het chsh-game-voor beeld wordt weer gegeven</span><span class="sxs-lookup"><span data-stu-id="2ee9c-122">See how the chsh-game sample is rendered</span></span>](https://docs.microsoft.com/samples/microsoft/quantum/validating-quantum-mechanics/)

<span data-ttu-id="2ee9c-123">Deze meta gegevens worden weer gegeven als een [yaml-header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) die aangeeft in welke talen uw steek proef betrekking heeft (dit is meestal `qsharp`, `csharp`en `python`) en op welke producten uw voor beeld betrekking heeft (doorgaans `qdk`).</span><span class="sxs-lookup"><span data-stu-id="2ee9c-123">This metadata is provided as a [YAML header](https://dotnet.github.io/docfx/spec/docfx_flavored_markdown.html#yaml-header) that indicates what languages your sample covers (typically, this will be `qsharp`, `csharp`, and `python`), and what products your sample covers (typically, just `qdk`).</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="1-11":::

> [!IMPORTANT]
> <span data-ttu-id="2ee9c-124">De `page_type: sample` sleutel in de header is vereist om het voor beeld weer te geven op docs.microsoft.com/samples.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-124">The `page_type: sample` key in the header is required for your sample to appear at docs.microsoft.com/samples.</span></span>
> <span data-ttu-id="2ee9c-125">Op dezelfde manier zijn de sleutels `product` en `language` essentieel om gebruikers te helpen bij het zoeken en uitvoeren van uw voor beeld.</span><span class="sxs-lookup"><span data-stu-id="2ee9c-125">Similarly, the `product` and `language` keys are critical for helping users to find and run your sample.</span></span>

<span data-ttu-id="2ee9c-126">Daarna is het handig om een korte inleiding te geven die aangeeft wat het nieuwe voor beeld doet:</span><span class="sxs-lookup"><span data-stu-id="2ee9c-126">After that, it's helpful to give a short intro that says what your new sample does:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="13-21":::

<span data-ttu-id="2ee9c-127">Het is ook belang rijk dat gebruikers van uw voor beeld weten wat ze nodig hebben om het uit te voeren (bijvoorbeeld: gebruikers hebben alleen de Quantum Development Kit zelf nodig of hebben ze extra software, zoals node. js?):</span><span class="sxs-lookup"><span data-stu-id="2ee9c-127">Users of your sample will also appreciate knowing what they need to run it (e.g.: do users just need the Quantum Development Kit itself, or do they need additional software such as node.js?):</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="23-25":::

<span data-ttu-id="2ee9c-128">Zo kunt u gebruikers vertellen hoe uw voor beeld moet worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="2ee9c-128">With all that in place, you can tell users how to run your sample:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="27-50":::

<span data-ttu-id="2ee9c-129">Ten slotte is het handig om gebruikers te vertellen wat elk bestand in uw voor beeld doet en waar ze meer informatie kunnen vinden:</span><span class="sxs-lookup"><span data-stu-id="2ee9c-129">Finally, it's helpful to tell users what each file in your sample does, and where they can go for more information:</span></span>

:::code language="markdown" source="~/quantum/samples/algorithms/chsh-game/README.md" range="52-61":::

> [!WARNING]
> <span data-ttu-id="2ee9c-130">Zorg ervoor dat u absolute Url's hier gebruikt, omdat uw voor beeld wordt weer gegeven op een andere URL wanneer het wordt gerenderd op docs.microsoft.com/samples!</span><span class="sxs-lookup"><span data-stu-id="2ee9c-130">Make sure to use absolute URLs here, since your sample will appear at a different URL when rendered at docs.microsoft.com/samples!</span></span>
