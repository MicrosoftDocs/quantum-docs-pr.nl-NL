---
title: Meer informatie over het installeren van de Microsoft Quantum development kit (QDK)
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: 0e9dd1c74316eeb1fa7bbbf657d2e78231ee4294
ms.sourcegitcommit: 5094c0a60cbafdee669c8728b92df281071259b9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2020
ms.locfileid: "77036505"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="96a16-102">De Microsoft Quantum development kit (QDK) installeren</span><span class="sxs-lookup"><span data-stu-id="96a16-102">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="96a16-103">Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="96a16-103">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="96a16-104">De QDK bestaat uit:</span><span class="sxs-lookup"><span data-stu-id="96a16-104">The QDK consists of:</span></span>

- <span data-ttu-id="96a16-105">de programmeertaal Q#</span><span class="sxs-lookup"><span data-stu-id="96a16-105">the Q# programming language</span></span>
- <span data-ttu-id="96a16-106">een set bibliotheken voor abstractie van complexe functionaliteit in Q#</span><span class="sxs-lookup"><span data-stu-id="96a16-106">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="96a16-107">API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren</span><span class="sxs-lookup"><span data-stu-id="96a16-107">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="96a16-108">hulpprogramma's om het ontwikkelen te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="96a16-108">tools to facilitate your development</span></span>

<span data-ttu-id="96a16-109">Q#-programma's zijn vaak gekoppeld aan een hostprogramma dat is geschreven in een .NET-taal (doorgaans C#) of Python.</span><span class="sxs-lookup"><span data-stu-id="96a16-109">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="96a16-110">Hierdoor kunnen we kwantumbewerkingen aanroepen in een klassiek programma.</span><span class="sxs-lookup"><span data-stu-id="96a16-110">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="96a16-111">Daarnaast biedt de QDK Q#-ondersteuning voor Jupyter Notebooks met het IQ#-Jupter-kernel.</span><span class="sxs-lookup"><span data-stu-id="96a16-111">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="96a16-112">De QDK is beschikbaar voor meerdere ontwikkelomgevingen.</span><span class="sxs-lookup"><span data-stu-id="96a16-112">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="96a16-113">Selecteer uw voorkeursinstellingen in de onderstaande secties:</span><span class="sxs-lookup"><span data-stu-id="96a16-113">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="96a16-114">[Q# installeren voor C#:](xref:microsoft.quantum.install.cs) kies deze omgeving als u C# en Q# wilt combineren om een C#-hostprogramma te maken dat Q#-bewerkingen aanroept.</span><span class="sxs-lookup"><span data-stu-id="96a16-114">[Install Q# for C#:](xref:microsoft.quantum.install.cs) choose this environment if you want to combine C# and Q# to create a C# host program that calls Q# operations.</span></span>
- <span data-ttu-id="96a16-115">[Q# installeren voor Python:](xref:microsoft.quantum.install.python) kies deze omgeving als u Python en Q# wilt combineren om een Python-hostprogramma te maken dat Python-bewerkingen aanroept.</span><span class="sxs-lookup"><span data-stu-id="96a16-115">[Install Q# for Python:](xref:microsoft.quantum.install.python) choose this environment if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="96a16-116">[Q# installeren voor Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) kies deze omgeving als u Q#-code wilt uitvoeren in cellen met ingesloten tekst of om interactieve zelfstudies te maken voor kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="96a16-116">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> <span data-ttu-id="96a16-117">Kies deze omgeving niet als u Q# wilt combineren met een extern klassiek hostprogramma.</span><span class="sxs-lookup"><span data-stu-id="96a16-117">Do not choose this environment if you want to combine Q# with an external classical host program.</span></span>
