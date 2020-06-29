---
title: De Q#-gebruikershandleiding
description: Overzicht van het doel en de inhoud van de gebruikershandleiding
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: c5611f3e2907791f2dfc1644be0a45515d50dfd7
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415358"
---
# <a name="the-q-user-guide"></a><span data-ttu-id="386f0-103">De Q#-gebruikershandleiding</span><span class="sxs-lookup"><span data-stu-id="386f0-103">The Q# User Guide</span></span>

<span data-ttu-id="386f0-104">Welkom bij de Q#-gebruikershandleiding!</span><span class="sxs-lookup"><span data-stu-id="386f0-104">Welcome to the Q# User Guide!</span></span> 

<span data-ttu-id="386f0-105">In de verschillende delen van deze handleiding beschrijven we de belangrijkste concepten van de Q#-taal en geven we alle informatie die u nodig hebt om kwantumprogramma's te schrijven.</span><span class="sxs-lookup"><span data-stu-id="386f0-105">In the different topics of this guide, we detail the core concepts of the Q# language and all the information you need to write quantum programs.</span></span>

## <a name="user-guide-contents"></a><span data-ttu-id="386f0-106">Inhoud van de gebruikershandleiding</span><span class="sxs-lookup"><span data-stu-id="386f0-106">User Guide Contents</span></span>

- <span data-ttu-id="386f0-107">[Q#-basis](xref:microsoft.quantum.guide.basics): een kennismakend overzicht van het doel en de functionaliteit van de Q#-programmeertaal.</span><span class="sxs-lookup"><span data-stu-id="386f0-107">[Q# Basics](xref:microsoft.quantum.guide.basics): An introductory overview of the purpose and functionality of the Q# programming language.</span></span> 

### <a name="q-language"></a><span data-ttu-id="386f0-108">Q#-taal</span><span class="sxs-lookup"><span data-stu-id="386f0-108">Q# Language</span></span>

- <span data-ttu-id="386f0-109">[Typen in Q#](xref:microsoft.quantum.guide.types): hierin wordt het Q#-typemodel gegeven en een beschrijving van de syntaxis om de typen op te geven en ermee te werken.</span><span class="sxs-lookup"><span data-stu-id="386f0-109">[Types in Q#](xref:microsoft.quantum.guide.types): Lays out the Q# type model and describes the syntax for specifying and working with types.</span></span>

- <span data-ttu-id="386f0-110">[Type-expressies](xref:microsoft.quantum.guide.expressions): details over hoe u waarden opgeeft, ernaar verwijst, combineert en ermee werkt voor elk type in Q#.</span><span class="sxs-lookup"><span data-stu-id="386f0-110">[Type Expressions](xref:microsoft.quantum.guide.expressions): Details how to specify, reference, combine, and operate on values of each type in Q#.</span></span> 

### <a name="using-q"></a><span data-ttu-id="386f0-111">Q# gebruiken</span><span class="sxs-lookup"><span data-stu-id="386f0-111">Using Q#</span></span>

- <span data-ttu-id="386f0-112">[Q#-bestandsstructuur](xref:microsoft.quantum.guide.filestructure): hierin worden de structuur en syntaxis van een `*.qs` Q#-bestand beschreven.</span><span class="sxs-lookup"><span data-stu-id="386f0-112">[Q# File Structure](xref:microsoft.quantum.guide.filestructure): Describes the structure and syntax of a `*.qs` Q# file.</span></span>

- <span data-ttu-id="386f0-113">[Bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions): beschrijven de twee aanroepbare typen Q#-taal: *bewerkingen*, waaronder acties voor qubit-registers en *functies*, die alleen werken met klassieke informatie.</span><span class="sxs-lookup"><span data-stu-id="386f0-113">[Operations and Functions](xref:microsoft.quantum.guide.operationsfunctions): Details the two callable types of the Q# language: *operations*, which include action on qubit registers, and *functions*, which strictly work with classical information.</span></span> 
    <span data-ttu-id="386f0-114">Hier ziet u hoe ze worden gedefinieerd en aangeroepen, inclusief de beheerde versies van kwantumbewerkingen.</span><span class="sxs-lookup"><span data-stu-id="386f0-114">Here you see how to define and call them, including the adjoint and controlled versions of quantum operations.</span></span>

- <span data-ttu-id="386f0-115">[Variabelen](xref:microsoft.quantum.guide.variables): hiermee wordt de rol van variabelen binnen Q#-programma's beschreven en hoe u er effectief gebruik van maakt.</span><span class="sxs-lookup"><span data-stu-id="386f0-115">[Variables](xref:microsoft.quantum.guide.variables): Describes the role of variables within Q# programs and how to leverage them effectively.</span></span> 
    <span data-ttu-id="386f0-116">U kunt bijvoorbeeld informatie vinden over bindingsbereiken, evenals de verschillen tussen onveranderlijke en veranderlijke variabelen en hoe u deze toewijst of opnieuw toewijst.</span><span class="sxs-lookup"><span data-stu-id="386f0-116">For example, you can find information about binding scopes, as well as the difference between immutable and mutable variables and how to assign or re-assign them.</span></span>

- <span data-ttu-id="386f0-117">[Werken met qubits](xref:microsoft.quantum.guide.qubits): hierin worden de functies van Q# uitgelegd die u kunt gebruiken om te werken met afzonderlijke qubits en systemen van qubits, met name het toewijzen ervan, het uitvoeren van bewerkingen en het meten ervan.</span><span class="sxs-lookup"><span data-stu-id="386f0-117">[Working with qubits](xref:microsoft.quantum.guide.qubits): Describes the features of Q# used to address individual qubits and systems of qubits, specifically, allocating them, performing operations on them, and measuring them.</span></span> 

- <span data-ttu-id="386f0-118">[Controlestroom](xref:microsoft.quantum.guide.controlflow): details van de programmeerstroompatronen die beschikbaar zijn in Q#. Deze omvatten veel standaardtechnieken (zoals voorwaardelijke uitvoering, voor lussen en tijdens lussen) en het patroon voor de kwantumspecifieke herhalingsbewerking.</span><span class="sxs-lookup"><span data-stu-id="386f0-118">[Control Flow](xref:microsoft.quantum.guide.controlflow): Details the programming control flow patterns available in Q#, which includes many standard techniques (such as conditional execution, for loops, while loops) as well as the quantum-specific "Repeat-Until-Success" pattern.</span></span>

- <span data-ttu-id="386f0-119">[Testen en foutopsporing](xref:microsoft.quantum.guide.testingdebugging): hierin wordt een aantal technieken uitgelegd om ervoor te zorgen dat uw code doet wat die moet doen.</span><span class="sxs-lookup"><span data-stu-id="386f0-119">[Testing and debugging](xref:microsoft.quantum.guide.testingdebugging): Details some techniques for making sure your code is doing what it is supposed to do.</span></span> 
    <span data-ttu-id="386f0-120">Als gevolg van de algemene matheid van kwantuminformatie, kunnen er voor het opsporen van fouten in een kwantumprogramma gespecialiseerde technieken nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="386f0-120">Due to the general opacity of quantum information, debugging a quantum program can require specialized techniques.</span></span> 
    <span data-ttu-id="386f0-121">Gelukkig ondersteunt Q# veel van de klassieke foutopsporingstechnieken waarmee programmeurs bekend zijn, evenals technieken die specifiek zijn voor kwantum.</span><span class="sxs-lookup"><span data-stu-id="386f0-121">Fortunately, Q# supports many of the classical debugging techniques programmers are familiar with, as well as those that are quantum-specific.</span></span> <span data-ttu-id="386f0-122">Deze omvatten het maken en uitvoeren van eenheidstests in Q#, het insluiten van *asserties* voor waarden en waarschijnlijkheden in uw code en de `Dump`-functies die de statussen van de doelmachines uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="386f0-122">These include creating and running unit tests in Q#, embedding *assertions* on values and probabilities in your code, and the `Dump` functions which output the states of target machines.</span></span> 
    <span data-ttu-id="386f0-123">De laatste kunnen worden gebruikt in onze volledige simulator om fouten in bepaalde berekeningen op te sporen door kwantumlimieten te introduceren, bijvoorbeeld de [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span><span class="sxs-lookup"><span data-stu-id="386f0-123">The latter can be used alongside our full-state simulator to debug certain parts of computations by skirting some quantum limitations, for example, the [no-cloning theorem](xref:microsoft.quantum.concepts.pauli).</span></span>

### <a name="quantum-simulators-and-resource-estimators"></a><span data-ttu-id="386f0-124">Kwantumsimulators en resourceschattingen</span><span class="sxs-lookup"><span data-stu-id="386f0-124">Quantum Simulators and Resource Estimators</span></span>

- <span data-ttu-id="386f0-125">[Kwantumsimulatoren en hosttoepassingen](xref:microsoft.quantum.machines): een overzicht van de verschillende beschikbare simulators, evenals het algemene uitvoeringsmodel tussen de hostprogramma's en de doelmachines.</span><span class="sxs-lookup"><span data-stu-id="386f0-125">[Quantum simulators and host applications](xref:microsoft.quantum.machines): An overview of the different simulators available, as well as the general execution model between host programs and target machines.</span></span>

- <span data-ttu-id="386f0-126">[Volledige statussimulator](xref:microsoft.quantum.machines.full-state-simulator): de doelcomputer die de volledige kwantumstatus simuleert.</span><span class="sxs-lookup"><span data-stu-id="386f0-126">[Full state simulator](xref:microsoft.quantum.machines.full-state-simulator): The target machine which simulates the full quantum state.</span></span> <span data-ttu-id="386f0-127">Handig voor het volledig uitvoeren of debuggen van kleinere programma's (minder dan een paar dozijn qubits)</span><span class="sxs-lookup"><span data-stu-id="386f0-127">Useful for fully executing or debugging smaller-scale programs (less than a few dozen qubits)</span></span>

- <span data-ttu-id="386f0-128">[Resoureschattingen](xref:microsoft.quantum.machines.resources-estimator): maakt een schatting van het aantal benodigde resources om een bepaald exemplaar uit te voeren van een Q#-bewerking in een kwantumcomputer.</span><span class="sxs-lookup"><span data-stu-id="386f0-128">[Resources estimator](xref:microsoft.quantum.machines.resources-estimator): Estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>

- <span data-ttu-id="386f0-129">[Traceersimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): voert een kwantumprogramma uit zonder de toestand van een kwantumcomputer daadwerkelijk te simuleren en kan daarom kwantumprogramma's simuleren die duizenden qubits gebruiken.</span><span class="sxs-lookup"><span data-stu-id="386f0-129">[Trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): Executes a quantum program without actually simulating the state of a quantum computer, and therefore can execute quantum programs that use thousands of qubits.</span></span> <span data-ttu-id="386f0-130">Handig om klassieke code binnen een kwantumprogramma te debuggen en om in te schatten hoeveel resources zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="386f0-130">Useful for debugging classical code within a quantum program, as well as estimating resources required.</span></span>

- <span data-ttu-id="386f0-131">[Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator): een kwantumsimulator voor speciale doeleinden die kan worden gebruikt met miljoenen qubits, maar alleen voor programma's met een beperkte set kwantumbewerkingen (X, CNOT en multi-controlled X).</span><span class="sxs-lookup"><span data-stu-id="386f0-131">[Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator): A special-purpose quantum simulator that can be used with millions of qubits, but only for programs with a restricted set of quantum operations - X, CNOT, and multi-controlled X.</span></span>

### <a name="quick-reference-pages"></a><span data-ttu-id="386f0-132">Snelzoekpagina's</span><span class="sxs-lookup"><span data-stu-id="386f0-132">Quick Reference Pages</span></span>

- <span data-ttu-id="386f0-133">[IQ# Magic-opdrachten](xref:microsoft.quantum.guide.quickref.iqsharp): Snelzoekpagina's voor IQ# Magic-opdrachten binnen Q# Jupyter Notebooks.</span><span class="sxs-lookup"><span data-stu-id="386f0-133">[IQ# Magic Commands](xref:microsoft.quantum.guide.quickref.iqsharp): Quick reference page for IQ# magic commands within Q# Jupyter Notebooks.</span></span>
