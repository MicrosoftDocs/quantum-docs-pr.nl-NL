---
title: Q#-gebruikershandleiding
description: Overzicht van het doel en de inhoud van de gebruikershandleiding
author: gillenhaalb
ms.author: a-gibec
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
no-loc:
- Q#
- $$v
ms.openlocfilehash: 979e468cc743bd9125eaba0b71f794977c914447
ms.sourcegitcommit: b930bb59a1ba8f41d2edc9ed98197109aa8c7f1b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96231754"
---
# <a name="the-no-locq-user-guide"></a><span data-ttu-id="47115-103">Q#-gebruikershandleiding</span><span class="sxs-lookup"><span data-stu-id="47115-103">The Q# User Guide</span></span>

<span data-ttu-id="47115-104">Welkom bij de Q#-gebruikershandleiding.</span><span class="sxs-lookup"><span data-stu-id="47115-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="47115-105">In de verschillende onderwerpen van deze handleiding introduceren we een aantal basisbeginselen voor het ontwikkelen van kwantumprogramma's met Q#.</span><span class="sxs-lookup"><span data-stu-id="47115-105">In the different topics of this guide, we introduce some of the basics for developing quantum programs using Q#.</span></span>

<span data-ttu-id="47115-106">We verwijzen naar de [Q#-taalhandleiding](xref:microsoft.quantum.qsharp.index) voor een volledige specificatie en documentatie van de Q#-kwantumcomputertaal.</span><span class="sxs-lookup"><span data-stu-id="47115-106">We refer to the [Q# language guide](xref:microsoft.quantum.qsharp.index) for a full specification and documentation of the Q# quantum programming language.</span></span> 

## <a name="user-guide-contents"></a><span data-ttu-id="47115-107">Inhoud van de gebruikershandleiding</span><span class="sxs-lookup"><span data-stu-id="47115-107">User Guide Contents</span></span>

- <span data-ttu-id="47115-108">[Q#-programma's](xref:microsoft.quantum.guide.programs): Een korte inleiding tot kwantumprogramma's in Q#.</span><span class="sxs-lookup"><span data-stu-id="47115-108">[Q# programs](xref:microsoft.quantum.guide.programs): An quick introduction to quantum programs in Q#.</span></span> 

- <span data-ttu-id="47115-109">[Manieren om een Q#-programma uit te voeren](xref:microsoft.quantum.guide.host-programs): beschrijft hoe een Q#-programma wordt uitgevoerd, en biedt een overzicht van de verschillende manieren waarop u het programma kunt aanroepen: vanuit de opdrachtregel, in Q# Jupyter Notebooks, of vanuit een klassiek hostprogramma dat in Python of een .NET-taal is geschreven.</span><span class="sxs-lookup"><span data-stu-id="47115-109">[Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs): describes how a Q# program is run, and provides an overview of the various ways you can call the program: from the command line, in Q# Jupyter Notebooks, or from a classical host program written in Python or a .NET language.</span></span>

- <span data-ttu-id="47115-110">[Testen en foutopsporing](xref:microsoft.quantum.guide.testingdebugging): hierin wordt een aantal technieken uitgelegd om ervoor te zorgen dat uw code doet wat die moet doen.</span><span class="sxs-lookup"><span data-stu-id="47115-110">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="47115-111">Als gevolg van de algemene matheid van kwantuminformatie, kunnen er voor het opsporen van fouten in een kwantumprogramma gespecialiseerde technieken nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="47115-111">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="47115-112">Gelukkig ondersteunt Q# veel van de klassieke foutopsporingstechnieken waarmee programmeurs bekend zijn, evenals technieken die kwantumspecifiek zijn.</span><span class="sxs-lookup"><span data-stu-id="47115-112">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="47115-113">Deze omvatten het maken en uitvoeren van eenheidstests in Q#, het insluiten van *asserties* voor waarden en waarschijnlijkheden in uw code en de `Dump`-functies die de statussen van de doelmachines uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="47115-113">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="47115-114">De laatste kunnen worden gebruikt in onze volledige simulator om fouten in bepaalde berekeningen op te sporen door kwantumlimieten te introduceren, bijvoorbeeld de [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span><span class="sxs-lookup"><span data-stu-id="47115-114">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="47115-115">Kwantumsimulators en resourceschattingen</span><span class="sxs-lookup"><span data-stu-id="47115-115">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="47115-116">[Kwantumsimulatoren en hosttoepassingen](xref:microsoft.quantum.machines): Een overzicht van de verschillende beschikbare simulatoren, evenals hoe hostprogramma's en doelmachines samenwerken om Q#-programma's uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="47115-116">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well of how host programs and target machines work together to run Q# programs.</span></span>

- <span data-ttu-id="47115-117">[Volledige statussimulator](xref:microsoft.quantum.machines.full-state-simulator): de doelcomputer die de volledige kwantumstatus simuleert.</span><span class="sxs-lookup"><span data-stu-id="47115-117">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="47115-118">Handig voor het volledig uitvoeren of debuggen van kleinere programma's (minder dan een paar dozijn qubits)</span><span class="sxs-lookup"><span data-stu-id="47115-118">Useful for fully running or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="47115-119">[Resoureschattingen](xref:microsoft.quantum.machines.resources-estimator): maakt een schatting van het aantal benodigde resources om een bepaald exemplaar uit te voeren van een Q#-bewerking in een kwantumcomputer.</span><span class="sxs-lookup"><span data-stu-id="47115-119">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="47115-120">[Traceersimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Voert een kwantumprogramma uit zonder de toestand van een kwantumcomputer daadwerkelijk te simuleren en kan daarom kwantumprogramma's simuleren die duizenden qubits gebruiken.</span><span class="sxs-lookup"><span data-stu-id="47115-120">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Runs a quantum program without actually simulating the state of a quantum computer, and therefore can run quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="47115-121">Handig om klassieke code binnen een kwantumprogramma te debuggen en om in te schatten hoeveel resources zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="47115-121">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="47115-122">[Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator): een kwantumsimulator voor speciale doeleinden die kan worden gebruikt met miljoenen qubits, maar alleen voor programma's met een beperkte set kwantumbewerkingen (X, CNOT en multi-controlled X).</span><span class="sxs-lookup"><span data-stu-id="47115-122">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="47115-123">Snelzoekpagina's</span><span class="sxs-lookup"><span data-stu-id="47115-123">Quick Reference Pages</span></span>

- <span data-ttu-id="47115-124">[IQ# Magic-opdrachten](xref:microsoft.quantum.guide.quickref.iqsharp): Snelzoekpagina voor IQ# Magic-opdrachten binnen Q# Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="47115-124">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
