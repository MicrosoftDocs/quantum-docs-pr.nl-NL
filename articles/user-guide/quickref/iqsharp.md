---
title: IQ# Magic-opdrachten
description: 'Pagina met Naslag informatie voor IQ # Magic-opdrachten met Q # Jupyter-notebooks'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 0cd1a2289132e2760a21fd9d4f4083696353e271
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83431016"
---
# <a name="iq-magic-commands"></a><span data-ttu-id="1159e-103">IQ# Magic-opdrachten</span><span class="sxs-lookup"><span data-stu-id="1159e-103">IQ# Magic Commands</span></span>

### <a name="general"></a><span data-ttu-id="1159e-104">Algemeen</span><span class="sxs-lookup"><span data-stu-id="1159e-104">General</span></span>

- <span data-ttu-id="1159e-105">`%config`: Hiermee worden de configuratie voorkeuren ingesteld of opgehaald.</span><span class="sxs-lookup"><span data-stu-id="1159e-105">`%config`: Sets or gets configuration preferences.</span></span>
- <span data-ttu-id="1159e-106">`%estimate`: Voert een bepaalde functie of bewerking op de QuantumSimulator doel computer uit.</span><span class="sxs-lookup"><span data-stu-id="1159e-106">`%estimate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="1159e-107">`%lsmagic`: Retourneert een lijst met alle momenteel beschik bare Magic-opdrachten.</span><span class="sxs-lookup"><span data-stu-id="1159e-107">`%lsmagic`: Returns a list of all currently available magic commands.</span></span>
- <span data-ttu-id="1159e-108">`%package`: Biedt de mogelijkheid om een Nuget-pakket te laden.</span><span class="sxs-lookup"><span data-stu-id="1159e-108">`%package`: Provides the ability to load a Nuget package.</span></span>
- <span data-ttu-id="1159e-109">`%performance`: Hiermee worden de huidige prestatie gegevens voor deze kernel gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="1159e-109">`%performance`: Reports current performance metrics for this kernel.</span></span>
- <span data-ttu-id="1159e-110">`%simulate`: Voert een bepaalde functie of bewerking op de QuantumSimulator doel computer uit.</span><span class="sxs-lookup"><span data-stu-id="1159e-110">`%simulate`: Runs a given function or operation on the QuantumSimulator target machine.</span></span>
- <span data-ttu-id="1159e-111">`%toffoli`: Voert een bepaalde functie of bewerking op de doel computer van de ToffoliSimulator Simulator uit.</span><span class="sxs-lookup"><span data-stu-id="1159e-111">`%toffoli`: Runs a given function or operation on the ToffoliSimulator simulator target machine.</span></span>
- <span data-ttu-id="1159e-112">`%who`: Bevat acties die betrekking hebben op de huidige werk ruimte.</span><span class="sxs-lookup"><span data-stu-id="1159e-112">`%who`: Provides actions related to the current workspace.</span></span>
- <span data-ttu-id="1159e-113">`%workspace`: Retourneert een lijst met alle bewerkingen en functies die in de huidige sessie zijn gedefinieerd, interactief of geladen vanuit de huidige werk ruimte.</span><span class="sxs-lookup"><span data-stu-id="1159e-113">`%workspace`: Returns a list of all operations and functions defined in the current session, either interactively or loaded from the current workspace.</span></span>

### <a name="chemistry"></a><span data-ttu-id="1159e-114">Chemische</span><span class="sxs-lookup"><span data-stu-id="1159e-114">Chemistry</span></span>

- <span data-ttu-id="1159e-115">`%chemistry.broombridge`: Laadt en retourneert Broombridge van een gegeven. yaml-bestand.</span><span class="sxs-lookup"><span data-stu-id="1159e-115">`%chemistry.broombridge`: Loads and returns Broombridge electronic structure problem representation from a given .yaml file.</span></span>
- <span data-ttu-id="1159e-116">`%chemistry.encode`: Codeert een fermion-Hamiltonian naar een indeling die kan worden gebruikt door Q #.</span><span class="sxs-lookup"><span data-stu-id="1159e-116">`%chemistry.encode`: Encodes a fermion Hamiltonian to a format consumable by Q#.</span></span>
- <span data-ttu-id="1159e-117">`%chemistry.fh.add_terms`: Hiermee worden voor waarden toegevoegd aan een fermion-Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="1159e-117">`%chemistry.fh.add_terms`: Adds terms to a fermion Hamiltonian.</span></span>
- <span data-ttu-id="1159e-118">`%chemistry.fh.load`: Hiermee wordt de fermion-Hamiltonian voor een probleem met een elektronische structuur geladen.</span><span class="sxs-lookup"><span data-stu-id="1159e-118">`%chemistry.fh.load`: Loads the fermion Hamiltonian for an electronic structure problem.</span></span> <span data-ttu-id="1159e-119">Het probleem wordt geladen vanuit een bestand of doorgevoerd als argument.</span><span class="sxs-lookup"><span data-stu-id="1159e-119">The problem is loaded from a file or passed as an argument.</span></span>
- <span data-ttu-id="1159e-120">`%chemistry.inputstate.load`: Hiermee wordt een Broombridge-probleem met de elektronische structuur geladen en wordt de geselecteerde invoer status geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="1159e-120">`%chemistry.inputstate.load`: Loads Broombridge electronic structure problem and returns selected input state.</span></span>

### <a name="from-microsoftquantumkatas-package"></a><span data-ttu-id="1159e-121">Van het pakket micro soft. Quantum. Katas</span><span class="sxs-lookup"><span data-stu-id="1159e-121">From Microsoft.Quantum.Katas package</span></span>

- <span data-ttu-id="1159e-122">`%kata`: Voert één test uit en meldt of de test is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="1159e-122">`%kata`: Executes a single test, and reports whether the test passed successfully.</span></span>
- <span data-ttu-id="1159e-123">`%check_kata`: Controleert de referentie-implementatie voor de test van één Kata.</span><span class="sxs-lookup"><span data-stu-id="1159e-123">`%check_kata`: Checks the reference implementation for a single kata's test.</span></span>
    <span data-ttu-id="1159e-124">Met name wordt de referentie-implementatie voor één taak in de cel vervangen en wordt gerapporteerd of de test is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="1159e-124">Specifically, it substitutes the reference implementation for a single task into the cell, and reports whether the test passed successfully.</span></span>
