---
title: De Microsoft Quantum Development Kit (QDK) instellen
description: Meer informatie over hoe u de Microsoft Quantum Development Kit installeert voor verschillende omgevingen.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834479"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="928a4-103">De Microsoft Quantum Development Kit (QDK) instellen</span><span class="sxs-lookup"><span data-stu-id="928a4-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="928a4-104">Meer informatie over hoe u de Microsoft Quantum Development Kit (QDK) instelt voor uw omgeving, zodat u aan de slag kunt gaan met kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="928a4-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="928a4-105">De QDK bestaat uit:</span><span class="sxs-lookup"><span data-stu-id="928a4-105">The QDK consists of:</span></span>

- <span data-ttu-id="928a4-106">Q#-programmeertaal</span><span class="sxs-lookup"><span data-stu-id="928a4-106">The Q# programming language</span></span>
- <span data-ttu-id="928a4-107">Een set bibliotheken voor abstractie van complexe functionaliteit in Q#</span><span class="sxs-lookup"><span data-stu-id="928a4-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="928a4-108">API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren</span><span class="sxs-lookup"><span data-stu-id="928a4-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="928a4-109">Hulpprogramma's om het ontwikkelen te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="928a4-109">Tools to facilitate your development</span></span>

<span data-ttu-id="928a4-110">Q#-programma's kunnen worden uitgevoerd als zelfstandige toepassingen met Visual Studio Code of Visual Studio, via Jupyter Notebooks met de IQ# Jupyter-kernel of gekoppeld met een hostprogramma dat is geschreven in Python of een .NET-taal (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="928a4-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="928a4-111">U kunt ook Q#-programma's online uitvoeren met [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) of [Docker](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="928a4-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="928a4-112">Opties om de QDK in te stellen</span><span class="sxs-lookup"><span data-stu-id="928a4-112">Options for setting up the QDK</span></span>

<span data-ttu-id="928a4-113">U kunt de QDK op drie manieren gebruiken:</span><span class="sxs-lookup"><span data-stu-id="928a4-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="928a4-114">De QDK lokaal installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="928a4-115">De QDK online gebruiken</span><span class="sxs-lookup"><span data-stu-id="928a4-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="928a4-116">Een QDK Docker-installatiekopie gebruiken</span><span class="sxs-lookup"><span data-stu-id="928a4-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="928a4-117">De QDK lokaal installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-117">Install the QDK locally</span></span>

<span data-ttu-id="928a4-118">U kunt Q#-code ontwikkelen in de meest gebruikte IDE's, evenals Q# integreren met andere talen zoals Python en .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="928a4-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

|&nbsp; | <span data-ttu-id="928a4-119">**VS Code<br>(2019 of hoger)**</span><span class="sxs-lookup"><span data-stu-id="928a4-119">**VS Code<br>(2019 or later)**</span></span>| <span data-ttu-id="928a4-120">**Visual Studio<br>(2019 of hoger)**</span><span class="sxs-lookup"><span data-stu-id="928a4-120">**Visual Studio<br>(2019 or later)**</span></span> | <span data-ttu-id="928a4-121">**Jupyter Notebooks**</span><span class="sxs-lookup"><span data-stu-id="928a4-121">**Jupyter Notebooks**</span></span> | <span data-ttu-id="928a4-122">**Opdrachtregel**</span><span class="sxs-lookup"><span data-stu-id="928a4-122">**Command line**</span></span>|
|:-----|:-----:|:-----:|:-----:|:-----:|
|<span data-ttu-id="928a4-123">**Besturingssysteem**</span><span class="sxs-lookup"><span data-stu-id="928a4-123">**OS**</span></span> |<span data-ttu-id="928a4-124">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="928a4-124">Windows, macOS, Linux</span></span> |<span data-ttu-id="928a4-125">Alleen in Windows</span><span class="sxs-lookup"><span data-stu-id="928a4-125">Windows only</span></span> |<span data-ttu-id="928a4-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="928a4-126">Windows, macOS, Linux</span></span> |<span data-ttu-id="928a4-127">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="928a4-127">Windows, macOS, Linux</span></span> |
|<br><span data-ttu-id="928a4-128">**Q# zelfstandig**</span><span class="sxs-lookup"><span data-stu-id="928a4-128">**Q# standalone**</span></span> |<br>[<span data-ttu-id="928a4-129">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-129">Install</span></span>](xref:microsoft.quantum.install.standalone) |<br> [<span data-ttu-id="928a4-130">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-130">Install</span></span>](xref:microsoft.quantum.install.standalone)  |<br> [<span data-ttu-id="928a4-131">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-131">Install</span></span>](xref:microsoft.quantum.install.jupyter) |<br>[<span data-ttu-id="928a4-132">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-132">Install</span></span>](xref:microsoft.quantum.install.standalone)|
|<span data-ttu-id="928a4-133">**Q# en Python**</span><span class="sxs-lookup"><span data-stu-id="928a4-133">**Q#  and Python**</span></span> |[<span data-ttu-id="928a4-134">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-134">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="928a4-135">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-135">Install</span></span>](xref:microsoft.quantum.install.python) |[<span data-ttu-id="928a4-136">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-136">Install</span></span>](xref:microsoft.quantum.install.jupyter) |[<span data-ttu-id="928a4-137">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-137">Install</span></span>](xref:microsoft.quantum.install.python) |
|<span data-ttu-id="928a4-138">**Q# en .NET (C#, F#)**</span><span class="sxs-lookup"><span data-stu-id="928a4-138">**Q# and .NET (C#, F#)**</span></span>|[<span data-ttu-id="928a4-139">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-139">Install</span></span>](xref:microsoft.quantum.install.cs) |[<span data-ttu-id="928a4-140">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-140">Install</span></span>](xref:microsoft.quantum.install.cs)|<span data-ttu-id="928a4-141">&#10006;</span><span class="sxs-lookup"><span data-stu-id="928a4-141">&#10006;</span></span> |[<span data-ttu-id="928a4-142">Installeren</span><span class="sxs-lookup"><span data-stu-id="928a4-142">Install</span></span>](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a><span data-ttu-id="928a4-143">De QDK online gebruiken</span><span class="sxs-lookup"><span data-stu-id="928a4-143">Use the QDK Online</span></span>

<span data-ttu-id="928a4-144">U kunt ook Q#-code ontwikkelen zonder dat u iets lokaal installeert met de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="928a4-144">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="928a4-145">Resource</span><span class="sxs-lookup"><span data-stu-id="928a4-145">Resource</span></span>|<span data-ttu-id="928a4-146">Voordelen</span><span class="sxs-lookup"><span data-stu-id="928a4-146">Advantages</span></span>|<span data-ttu-id="928a4-147">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="928a4-147">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="928a4-148">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="928a4-148">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="928a4-149">Een rijke online ontwikkelomgeving</span><span class="sxs-lookup"><span data-stu-id="928a4-149">A rich online development environment</span></span>  |<span data-ttu-id="928a4-150">Vereist een Azure-abonnement en -plan</span><span class="sxs-lookup"><span data-stu-id="928a4-150">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="928a4-151">**Binder**</span><span class="sxs-lookup"><span data-stu-id="928a4-151">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="928a4-152">Gratis online notebookervaring</span><span class="sxs-lookup"><span data-stu-id="928a4-152">Free online notebook experience</span></span> |<span data-ttu-id="928a4-153">Geen persistentie</span><span class="sxs-lookup"><span data-stu-id="928a4-153">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="928a4-154">De QDK gebruiken met Docker</span><span class="sxs-lookup"><span data-stu-id="928a4-154">Use the QDK with Docker</span></span>

<span data-ttu-id="928a4-155">U kunt ook onze QDK Docker-installatiekopie gebruiken in uw lokale Docker-installatie of in de cloud via elke service die Docker-installatiekopieën ondersteunt, bijvoorbeeld ACI.</span><span class="sxs-lookup"><span data-stu-id="928a4-155">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="928a4-156">U kunt de IQ# Docker-installatiekopie downloaden via https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span><span class="sxs-lookup"><span data-stu-id="928a4-156">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="928a4-157">U kunt Docker ook gebruiker met een Visual Studio Code Remote Development Container om snel ontwikkelomgevingen te definiëren.</span><span class="sxs-lookup"><span data-stu-id="928a4-157">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="928a4-158">Raadpleeg https://github.com/microsoft/Quantum/tree/master/.devcontainer voor meet informatie over VS Code Development Containers.</span><span class="sxs-lookup"><span data-stu-id="928a4-158">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="928a4-159">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="928a4-159">Next steps</span></span>

<span data-ttu-id="928a4-160">De werkstromen voor elk van deze configuraties worden beschreven en vergeleken in [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="928a4-160">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
