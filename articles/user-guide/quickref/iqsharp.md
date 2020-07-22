---
title: IQ# Magic-opdrachten
description: 'Pagina met Naslag informatie voor IQ # Magic-opdrachten met Q # Jupyter-notebooks'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
uid: microsoft.quantum.guide.quickref.iqsharp
ms.openlocfilehash: 2fb542df8723fa437c82b4a1dfada77e22c1d6e4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870534"
---
# <a name="iq-magic-commands"></a>IQ# Magic-opdrachten

### <a name="general"></a>Algemeen

- [`%config`](xref:microsoft.quantum.iqsharp.magic-ref.config): Hiermee kunnen configuratie opties worden ingesteld of opgevraagd.
- [`%estimate`](xref:microsoft.quantum.iqsharp.magic-ref.estimate): Voert een bepaalde functie of bewerking op de ResourcesEstimator doel computer uit.
- [`%lsmagic`](xref:microsoft.quantum.iqsharp.magic-ref.lsmagic): Retourneert een lijst met alle momenteel beschik bare Magic-opdrachten.
- [`%package`](xref:microsoft.quantum.iqsharp.magic-ref.package): Biedt de mogelijkheid om een NuGet-pakket te laden.
- [`%performance`](xref:microsoft.quantum.iqsharp.magic-ref.performance): Hiermee worden de huidige prestatie gegevens voor deze kernel gerapporteerd.
- [`%simulate`](xref:microsoft.quantum.iqsharp.magic-ref.simulate): Voert een bepaalde functie of bewerking op de QuantumSimulator doel computer uit.
- [`%toffoli`](xref:microsoft.quantum.iqsharp.magic-ref.toffoli): Voert een bepaalde functie of bewerking op de ToffoliSimulator doel computer uit.
- [`%who`](xref:microsoft.quantum.iqsharp.magic-ref.who): Hier worden de Q #-bewerkingen weer gegeven die beschikbaar zijn in de huidige sessie.
- [`%workspace`](xref:microsoft.quantum.iqsharp.magic-ref.workspace): Bevat acties die betrekking hebben op de huidige werk ruimte.

### <a name="azure-quantum-integration"></a>Integratie van Azure Quantum

- [`%azure.connect`](xref:microsoft.quantum.iqsharp.magic-ref.azure.connect): Hiermee maakt u verbinding met een Azure Quantum-werk ruimte of wordt de huidige verbindings status weer gegeven.
- [`%azure.execute`](xref:microsoft.quantum.iqsharp.magic-ref.azure.execute): Voert een taak uit in een Azure Quantum-werk ruimte.
- [`%azure.jobs`](xref:microsoft.quantum.iqsharp.magic-ref.azure.jobs): Hiermee wordt een lijst met taken weer gegeven in de huidige Azure Quantum-werk ruimte.
- [`%azure.output`](xref:microsoft.quantum.iqsharp.magic-ref.azure.output): Hiermee worden de resultaten weer gegeven voor een taak in de huidige Azure Quantum-werk ruimte.
- [`%azure.status`](xref:microsoft.quantum.iqsharp.magic-ref.azure.status): Hiermee wordt de status van een taak in de huidige Azure Quantum-werk ruimte weer gegeven.
- [`%azure.submit`](xref:microsoft.quantum.iqsharp.magic-ref.azure.submit): Hiermee wordt een taak naar een Azure Quantum-werk ruimte verzonden.
- [`%azure.target`](xref:microsoft.quantum.iqsharp.magic-ref.azure.target): Hiermee wordt het actieve uitvoerings doel voor Q # taak inzending ingesteld of weer gegeven in een Azure Quantum-werk ruimte.

### <a name="chemistry-from-microsoftquantumchemistry-package"></a>Schei kunde (van het pakket micro soft. Quantum. chemie)

- [`%chemistry.broombridge`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.broombridge): Laadt en retourneert Broombridge van een gegeven. yaml-bestand.
- [`%chemistry.encode`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.encode): Codeert een fermion-Hamiltonian naar een indeling die kan worden gebruikt door Q #.
- [`%chemistry.fh.add_terms`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.add_terms): Hiermee worden voor waarden toegevoegd aan een fermion-Hamiltonian.
- [`%chemistry.fh.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.fh.load): Hiermee wordt de fermion-Hamiltonian voor een probleem met een elektronische structuur geladen. Het probleem wordt geladen vanuit een bestand of doorgevoerd als argument.
- [`%chemistry.inputstate.load`](xref:microsoft.quantum.iqsharp.magic-ref.chemistry.inputstate.load): Hiermee wordt een Broombridge-probleem met de elektronische structuur geladen en wordt de geselecteerde invoer status geretourneerd.

### <a name="katas-from-microsoftquantumkatas-package"></a>Katas (van het pakket micro soft. Quantum. Katas)

- [`%kata`](xref:microsoft.quantum.iqsharp.magic-ref.kata): Voert één test uit en meldt of de test is geslaagd.
- [`%check_kata`](xref:microsoft.quantum.iqsharp.magic-ref.check_kata): Controleert de referentie-implementatie voor de test van één Kata.
    Met name wordt de referentie-implementatie voor één taak in de cel vervangen en wordt gerapporteerd of de test is geslaagd.
