---
title: De Microsoft Quantum development kit (QDK) installeren
description: De Microsoft Quantum Development Kit installeren voor verschillende omgevingen.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 6a52eb0a9cdf699e8bb37578ffa3d73fe96a990e
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273319"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="ab8f2-103">De Microsoft Quantum development kit (QDK) installeren</span><span class="sxs-lookup"><span data-stu-id="ab8f2-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="ab8f2-104">Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="ab8f2-105">De QDK bestaat uit:</span><span class="sxs-lookup"><span data-stu-id="ab8f2-105">The QDK consists of:</span></span>

- <span data-ttu-id="ab8f2-106">De programmeertaal Q#</span><span class="sxs-lookup"><span data-stu-id="ab8f2-106">The Q# programming language</span></span>
- <span data-ttu-id="ab8f2-107">Een set bibliotheken voor abstractie van complexe functionaliteit in Q#</span><span class="sxs-lookup"><span data-stu-id="ab8f2-107">A set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="ab8f2-108">API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren</span><span class="sxs-lookup"><span data-stu-id="ab8f2-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="ab8f2-109">Hulpprogramma's om het ontwikkelen te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="ab8f2-109">Tools to facilitate your development</span></span>

<span data-ttu-id="ab8f2-110">Q#-programma's kunnen worden uitgevoerd als zelfstandige toepassingen met Visual Studio Code of Visual Studio of via Jupyter Notebooks met de IQ# Jupyter-kernel.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-110">Q# programs can run as standalone applications using Visual Studio Code or Visual Studio, or through Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="ab8f2-111">Ze kunnen ook worden gekoppeld met een hostprogramma dat is geschreven in een .NET-taal (doorgaans C#) of Python, waardoor u kwantumbewerkingen kunt aanroepen vanuit een klassiek programma.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-111">They can also be paired with a host program written in a .NET language (typically C#) or Python, enabling you to call quantum operations from inside a classical program.</span></span>

<span data-ttu-id="ab8f2-112">De QDK is beschikbaar voor meerdere ontwikkelomgevingen.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="ab8f2-113">Selecteer uw voorkeursinstellingen vanuit:</span><span class="sxs-lookup"><span data-stu-id="ab8f2-113">Select your preferred setup from:</span></span>

<span data-ttu-id="ab8f2-114">[Ontwikkelen met Q#-opdrachtregeltoepassing](xref:microsoft.quantum.install.standalone): kies deze methode als u wilt werken met Q# vanaf de opdrachtregel.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-114">[Develop with Q# command line applications](xref:microsoft.quantum.install.standalone) - Choose this approach to work with Q# from the command line.</span></span> <span data-ttu-id="ab8f2-115">Hiervoor is geen stuurprogramma of hostprogramma vereist, zoals voor de onderstaande opties.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-115">This does not require a driver or a host program like the below options.</span></span>

<span data-ttu-id="ab8f2-116">[Ontwikkelen met Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter): kies deze omgeving als u Q#-code wilt uitvoeren in cellen met ingesloten tekst of om interactieve zelfstudies te maken voor kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-116">[Develop with Q# Jupyter Notebooks](xref:microsoft.quantum.install.jupyter) - Select this environment to run Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 

<span data-ttu-id="ab8f2-117">[Ontwikkelen met Q# en Python](xref:microsoft.quantum.install.python): hiermee kunt u Python en Q# combineren om een Python-hostprogramma te maken dat Python-bewerkingen aanroept.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-117">[Develop with Q# and Python](xref:microsoft.quantum.install.python) - Enables you to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>

<span data-ttu-id="ab8f2-118">[Ontwikkelen met Q# en .NET](xref:microsoft.quantum.install.cs): combineer C#, F# of VB.NET met Q# om een .NET-hostprogramma te maken dat Q#-bewerkingen aanroept.</span><span class="sxs-lookup"><span data-stu-id="ab8f2-118">[Develop with Q# and .NET](xref:microsoft.quantum.install.cs) - Combine C#, F#, or VB.NET with Q# to create a .NET host program that calls Q# operations.</span></span>
