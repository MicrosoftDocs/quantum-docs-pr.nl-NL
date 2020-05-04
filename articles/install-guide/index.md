---
title: Meer informatie over het installeren van de Microsoft Quantum development kit (QDK)
description: Instructies voor het installeren van de Microsoft Quantum Development Kit voor C#-, python- en Jupyter Notebook-omgevingen.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: bca700660094b91f1c0dfa03f9bce1336073ca51
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680197"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a><span data-ttu-id="957b3-103">De Microsoft Quantum development kit (QDK) installeren</span><span class="sxs-lookup"><span data-stu-id="957b3-103">Install the Microsoft Quantum Development Kit (QDK)</span></span>

<span data-ttu-id="957b3-104">Meer informatie over het installeren van de Microsoft Quantum development kit (QDK), zodat u aan de slag kunt gaan met kwantumprogrammering.</span><span class="sxs-lookup"><span data-stu-id="957b3-104">Learn how to install the Microsoft Quantum Development Kit (QDK), so that you can get started with quantum programming.</span></span> <span data-ttu-id="957b3-105">De QDK bestaat uit:</span><span class="sxs-lookup"><span data-stu-id="957b3-105">The QDK consists of:</span></span>

- <span data-ttu-id="957b3-106">de programmeertaal Q#</span><span class="sxs-lookup"><span data-stu-id="957b3-106">the Q# programming language</span></span>
- <span data-ttu-id="957b3-107">een set bibliotheken voor abstractie van complexe functionaliteit in Q#</span><span class="sxs-lookup"><span data-stu-id="957b3-107">a set of libraries that abstract complex functionality in Q#</span></span>
- <span data-ttu-id="957b3-108">API's voor Python en .NET-talen (C#, F# en VB.NET) om kwantumprogramma's in Q# uit te voeren</span><span class="sxs-lookup"><span data-stu-id="957b3-108">APIs for Python and .NET languages (C#, F#, and VB.NET) for running quantum programs written in Q#</span></span>
- <span data-ttu-id="957b3-109">hulpprogramma's om het ontwikkelen te vergemakkelijken</span><span class="sxs-lookup"><span data-stu-id="957b3-109">tools to facilitate your development</span></span>

<span data-ttu-id="957b3-110">Q#-programma's zijn vaak gekoppeld aan een hostprogramma dat is geschreven in een .NET-taal (doorgaans C#) of Python.</span><span class="sxs-lookup"><span data-stu-id="957b3-110">Q# programs are often paired with a host program written in a .NET language (typically C#) or Python.</span></span> <span data-ttu-id="957b3-111">Hierdoor kunnen we kwantumbewerkingen aanroepen in een klassiek programma.</span><span class="sxs-lookup"><span data-stu-id="957b3-111">This allows us to call quantum operations from inside a classical program.</span></span>
<span data-ttu-id="957b3-112">Daarnaast biedt de QDK Q#-ondersteuning voor Jupyter Notebooks met het IQ#-Jupter-kernel.</span><span class="sxs-lookup"><span data-stu-id="957b3-112">In addition, the QDK provides Q# support for Jupyter Notebooks with the IQ# Jupyter kernel.</span></span>

<span data-ttu-id="957b3-113">De QDK is beschikbaar voor meerdere ontwikkelomgevingen.</span><span class="sxs-lookup"><span data-stu-id="957b3-113">The QDK is available for multiple development environments.</span></span> <span data-ttu-id="957b3-114">Selecteer uw voorkeursinstellingen in de onderstaande secties:</span><span class="sxs-lookup"><span data-stu-id="957b3-114">Select your preferred setup from the sections below:</span></span>

- <span data-ttu-id="957b3-115">[Q#-opdrachtregeltoepassing:](xref:microsoft.quantum.install.standalone) kies deze methode als u wilt werken met Q# vanaf de opdrachtregel.</span><span class="sxs-lookup"><span data-stu-id="957b3-115">[Q# command line application:](xref:microsoft.quantum.install.standalone) choose this approach if you want to work with Q# from the command line.</span></span> <span data-ttu-id="957b3-116">Hiervoor is geen stuurprogramma of hostprogramma vereist, zoals voor de onderstaande opties.</span><span class="sxs-lookup"><span data-stu-id="957b3-116">This does not require a driver or a host program like the below options.</span></span>
- <span data-ttu-id="957b3-117">[Q# installeren voor Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) kies deze omgeving als u Q#-code wilt uitvoeren in cellen met ingesloten tekst of om interactieve zelfstudies te maken voor kwantumcomputing.</span><span class="sxs-lookup"><span data-stu-id="957b3-117">[Install Q# for Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) choose this environment to execute Q# code in cells with embedded text or create quantum computing interactive tutorials.</span></span> 
- <span data-ttu-id="957b3-118">[Ontwikkelen met Q# en Python:](xref:microsoft.quantum.install.python) kies deze omgeving als u Python en Q# wilt combineren om een Python-hostprogramma te maken dat Python-bewerkingen aanroept.</span><span class="sxs-lookup"><span data-stu-id="957b3-118">[Develop with Q# and Python:](xref:microsoft.quantum.install.python) if you want to combine Python and Q# to create a Python host program that calls Q# operations.</span></span>
- <span data-ttu-id="957b3-119">[Ontwikkelen met Q# en C# of F#:](xref:microsoft.quantum.install.cs) kies deze optie als u C# of F# en Q# wilt combineren om een .NET-hostprogramma te maken dat Q#-bewerkingen aanroept.</span><span class="sxs-lookup"><span data-stu-id="957b3-119">[Develop with Q# and C# or F#:](xref:microsoft.quantum.install.cs) if you want to combine C# or F# and Q# to create a .NET host program that calls Q# operations.</span></span>
