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
ms.openlocfilehash: c6e128ea8b3845336fb692d2bceefda998b935d9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96228821"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="5850a-103">De Microsoft Quantum Development Kit (QDK) instellen</span><span class="sxs-lookup"><span data-stu-id="5850a-103">Setting up the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="5850a-104">Meer informatie over hoe u de Microsoft Quantum Development Kit (QDK) instelt voor uw omgeving, zodat u aan de slag kunt gaan met kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="5850a-104">Learn how to set up the Microsoft Quantum Development Kit (QDK) for your environment, so that you can get started with quantum programming.</span></span> <span data-ttu-id="5850a-105">De QDK bestaat uit:</span><span class="sxs-lookup"><span data-stu-id="5850a-105">The QDK consists of:</span></span>

- <span data-ttu-id="5850a-106">Q#-programmeertaal</span><span class="sxs-lookup"><span data-stu-id="5850a-106">The Q# programming language</span></span>
- <span data-ttu-id="5850a-107">Een set bibliotheken voor abstractie van complexe functionaliteit in Q#</span><span class="sxs-lookup"><span data-stu-id="5850a-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="5850a-108">API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren</span><span class="sxs-lookup"><span data-stu-id="5850a-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="5850a-109">Hulpprogramma's om het ontwikkelen te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="5850a-109">Tools to facilitate your development</span></span>

<span data-ttu-id="5850a-110">Q#-programma's kunnen worden uitgevoerd als zelfstandige toepassingen met Visual Studio Code of Visual Studio, via Jupyter Notebooks met de IQ# Jupyter-kernel of gekoppeld met een hostprogramma dat is geschreven in Python of een .NET-taal (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="5850a-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, through Jupyter Notebooks with the IQ# Jupyter kernel, or paired with a host program written in Python or a .NET language (C#, F#).</span></span> <span data-ttu-id="5850a-111">U kunt ook Q#-programma's online uitvoeren met [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) of [Docker](#use-the-qdk-with-docker).</span><span class="sxs-lookup"><span data-stu-id="5850a-111">You can also run Q# programs online using [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/), or [Docker](#use-the-qdk-with-docker).</span></span> 

## <a name="options-for-setting-up-the-qdk"></a><span data-ttu-id="5850a-112">Opties om de QDK in te stellen</span><span class="sxs-lookup"><span data-stu-id="5850a-112">Options for setting up the QDK</span></span>

<span data-ttu-id="5850a-113">U kunt de QDK op drie manieren gebruiken:</span><span class="sxs-lookup"><span data-stu-id="5850a-113">You can use the QDK in three ways:</span></span>

- [<span data-ttu-id="5850a-114">De QDK lokaal installeren</span><span class="sxs-lookup"><span data-stu-id="5850a-114">Install the QDK locally</span></span>](#install-the-qdk-locally)
- [<span data-ttu-id="5850a-115">De QDK online gebruiken</span><span class="sxs-lookup"><span data-stu-id="5850a-115">Use the QDK online</span></span>](#use-the-qdk-online)
- [<span data-ttu-id="5850a-116">Een QDK Docker-installatiekopie gebruiken</span><span class="sxs-lookup"><span data-stu-id="5850a-116">Use a QDK Docker image</span></span>](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a><span data-ttu-id="5850a-117">De QDK lokaal installeren</span><span class="sxs-lookup"><span data-stu-id="5850a-117">Install the QDK locally</span></span>

<span data-ttu-id="5850a-118">U kunt Q#-code ontwikkelen in de meest gebruikte IDE's, evenals Q# integreren met andere talen zoals Python en .NET (C#, F#).</span><span class="sxs-lookup"><span data-stu-id="5850a-118">You can develop Q# code in most of your favorites IDEs, as well as integrate Q# with other languages such as Python and .NET (C#, F#).</span></span>

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><span data-ttu-id="5850a-119"><b>VS-code</span><span class="sxs-lookup"><span data-stu-id="5850a-119"><b>VS Code</span></span><br><span data-ttu-id="5850a-120">(2019 of later)</b></span><span class="sxs-lookup"><span data-stu-id="5850a-120">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><span data-ttu-id="5850a-121"><b>Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5850a-121"><b>Visual Studio</span></span><br><span data-ttu-id="5850a-122">(2019 of later)</b></span><span class="sxs-lookup"><span data-stu-id="5850a-122">(2019 or later)</b></span></span></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><span data-ttu-id="5850a-123"><b>Jupyter Notebooks</b></span><span class="sxs-lookup"><span data-stu-id="5850a-123"><b>Jupyter Notebooks</b></span></span></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><span data-ttu-id="5850a-124"><b>Opdrachtregel</b></span><span class="sxs-lookup"><span data-stu-id="5850a-124"><b>Command line</b></span></span></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><span data-ttu-id="5850a-125"><b>Besturingssysteemondersteuning:</b></span><span class="sxs-lookup"><span data-stu-id="5850a-125"><b>OS support:</b></span></span></td>
        <td align="center"><span data-ttu-id="5850a-126">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="5850a-126">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="5850a-127">Alleen in Windows</span><span class="sxs-lookup"><span data-stu-id="5850a-127">Windows only</span></span></td>
        <td align="center"><span data-ttu-id="5850a-128">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="5850a-128">Windows, macOS, Linux</span></span></td>
        <td align="center"><span data-ttu-id="5850a-129">Windows, macOS, Linux</span><span class="sxs-lookup"><span data-stu-id="5850a-129">Windows, macOS, Linux</span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><span data-ttu-id="5850a-130"><b>Q# zelfstandig</b></span><span class="sxs-lookup"><span data-stu-id="5850a-130"><b>Q# standalone</b></span></span></td>
        <td align="center"><span data-ttu-id="5850a-131"><a href="xref:microsoft.quantum.install.standalone">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-131"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-132"><a href="xref:microsoft.quantum.install.standalone">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-132"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-133"><a href="xref:microsoft.quantum.install.jupyter">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-133"><a href="xref:microsoft.quantum.install.jupyter">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-134"><a href="xref:microsoft.quantum.install.standalone">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-134"><a href="xref:microsoft.quantum.install.standalone">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><span data-ttu-id="5850a-135"><b>Q# en Python</b></span><span class="sxs-lookup"><span data-stu-id="5850a-135"><b>Q# and Python</b></span></span></td>
        <td align="center"><span data-ttu-id="5850a-136"><a href="xref:microsoft.quantum.install.python">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-136"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-137"><a href="xref:microsoft.quantum.install.python">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-137"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-138"><a href="xref:microsoft.quantum.install.python">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-138"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-139"><a href="xref:microsoft.quantum.install.python">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-139"><a href="xref:microsoft.quantum.install.python">Install</a></span></span></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><span data-ttu-id="5850a-140"><b>Q# en .NET (C#, F#)</b></span><span class="sxs-lookup"><span data-stu-id="5850a-140"><b>Q# and .NET (C#, F#)</b></span></span></td> 
        <td align="center"><span data-ttu-id="5850a-141"><a href="xref:microsoft.quantum.install.cs">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-141"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-142"><a href="xref:microsoft.quantum.install.cs">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-142"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
        <td align="center"><span data-ttu-id="5850a-143">&#10006;</span><span class="sxs-lookup"><span data-stu-id="5850a-143">&#10006;</span></span></td>
        <td align="center"><span data-ttu-id="5850a-144"><a href="xref:microsoft.quantum.install.cs">Installeren</a></span><span class="sxs-lookup"><span data-stu-id="5850a-144"><a href="xref:microsoft.quantum.install.cs">Install</a></span></span></td>
   </tr>
</table>

## <a name="use-the-qdk-online"></a><span data-ttu-id="5850a-145">De QDK online gebruiken</span><span class="sxs-lookup"><span data-stu-id="5850a-145">Use the QDK Online</span></span>

<span data-ttu-id="5850a-146">U kunt ook Q#-code ontwikkelen zonder dat u iets lokaal installeert met de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="5850a-146">You can also develop Q# code without installing anything locally with these options:</span></span>

|<span data-ttu-id="5850a-147">Resource</span><span class="sxs-lookup"><span data-stu-id="5850a-147">Resource</span></span>|<span data-ttu-id="5850a-148">Voordelen</span><span class="sxs-lookup"><span data-stu-id="5850a-148">Advantages</span></span>|<span data-ttu-id="5850a-149">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="5850a-149">Limitations</span></span>|
|---|---|---|
|[<span data-ttu-id="5850a-150">**Visual Studio Codespaces**</span><span class="sxs-lookup"><span data-stu-id="5850a-150">**Visual Studio Codespaces**</span></span>](xref:microsoft.quantum.install.standalone)|<span data-ttu-id="5850a-151">Een rijke online ontwikkelomgeving</span><span class="sxs-lookup"><span data-stu-id="5850a-151">A rich online development environment</span></span>  |<span data-ttu-id="5850a-152">Vereist een Azure-abonnement en -plan</span><span class="sxs-lookup"><span data-stu-id="5850a-152">Requires an Azure subscription and plan</span></span> |
|[<span data-ttu-id="5850a-153">**Binder**</span><span class="sxs-lookup"><span data-stu-id="5850a-153">**Binder**</span></span>](xref:microsoft.quantum.install.binder) | <span data-ttu-id="5850a-154">Gratis online notebookervaring</span><span class="sxs-lookup"><span data-stu-id="5850a-154">Free online notebook experience</span></span> |<span data-ttu-id="5850a-155">Geen persistentie</span><span class="sxs-lookup"><span data-stu-id="5850a-155">No persistence</span></span> |

## <a name="use-the-qdk-with-docker"></a><span data-ttu-id="5850a-156">De QDK gebruiken met Docker</span><span class="sxs-lookup"><span data-stu-id="5850a-156">Use the QDK with Docker</span></span>

<span data-ttu-id="5850a-157">U kunt ook onze QDK Docker-installatiekopie gebruiken in uw lokale Docker-installatie of in de cloud via elke service die Docker-installatiekopieën ondersteunt, bijvoorbeeld ACI.</span><span class="sxs-lookup"><span data-stu-id="5850a-157">You can use our QDK Docker image in your local Docker installation or in the cloud via any service that supports Docker images, such as ACI.</span></span>

<span data-ttu-id="5850a-158">U kunt de IQ# Docker-installatiekopie downloaden via https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span><span class="sxs-lookup"><span data-stu-id="5850a-158">You can download the IQ# Docker image from https://github.com/microsoft/iqsharp/#using-iq-as-a-container.</span></span> 

<span data-ttu-id="5850a-159">U kunt Docker ook gebruiker met een Visual Studio Code Remote Development Container om snel ontwikkelomgevingen te definiëren.</span><span class="sxs-lookup"><span data-stu-id="5850a-159">You can also use Docker with a Visual Studio Code Remote Development Container to quickly define development environments.</span></span> <span data-ttu-id="5850a-160">Raadpleeg https://github.com/microsoft/Quantum/tree/master/.devcontainer voor meet informatie over VS Code Development Containers.</span><span class="sxs-lookup"><span data-stu-id="5850a-160">For more information about VS Code Development Containers, see https://github.com/microsoft/Quantum/tree/master/.devcontainer.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5850a-161">Volgende stappen</span><span class="sxs-lookup"><span data-stu-id="5850a-161">Next steps</span></span>

<span data-ttu-id="5850a-162">De werkstromen voor elk van deze configuraties worden beschreven en vergeleken in [Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs).</span><span class="sxs-lookup"><span data-stu-id="5850a-162">The workflows for each of these setups are described and compared at [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>
