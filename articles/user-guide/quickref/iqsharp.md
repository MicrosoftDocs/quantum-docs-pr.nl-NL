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
# <a name="iq-magic-commands"></a>IQ# Magic-opdrachten

### <a name="general"></a>Algemeen

- `%config`: Hiermee worden de configuratie voorkeuren ingesteld of opgehaald.
- `%estimate`: Voert een bepaalde functie of bewerking op de QuantumSimulator doel computer uit.
- `%lsmagic`: Retourneert een lijst met alle momenteel beschik bare Magic-opdrachten.
- `%package`: Biedt de mogelijkheid om een Nuget-pakket te laden.
- `%performance`: Hiermee worden de huidige prestatie gegevens voor deze kernel gerapporteerd.
- `%simulate`: Voert een bepaalde functie of bewerking op de QuantumSimulator doel computer uit.
- `%toffoli`: Voert een bepaalde functie of bewerking op de doel computer van de ToffoliSimulator Simulator uit.
- `%who`: Bevat acties die betrekking hebben op de huidige werk ruimte.
- `%workspace`: Retourneert een lijst met alle bewerkingen en functies die in de huidige sessie zijn gedefinieerd, interactief of geladen vanuit de huidige werk ruimte.

### <a name="chemistry"></a>Chemische

- `%chemistry.broombridge`: Laadt en retourneert Broombridge van een gegeven. yaml-bestand.
- `%chemistry.encode`: Codeert een fermion-Hamiltonian naar een indeling die kan worden gebruikt door Q #.
- `%chemistry.fh.add_terms`: Hiermee worden voor waarden toegevoegd aan een fermion-Hamiltonian.
- `%chemistry.fh.load`: Hiermee wordt de fermion-Hamiltonian voor een probleem met een elektronische structuur geladen. Het probleem wordt geladen vanuit een bestand of doorgevoerd als argument.
- `%chemistry.inputstate.load`: Hiermee wordt een Broombridge-probleem met de elektronische structuur geladen en wordt de geselecteerde invoer status geretourneerd.

### <a name="from-microsoftquantumkatas-package"></a>Van het pakket micro soft. Quantum. Katas

- `%kata`: Voert één test uit en meldt of de test is geslaagd.
- `%check_kata`: Controleert de referentie-implementatie voor de test van één Kata.
    Met name wordt de referentie-implementatie voor één taak in de cel vervangen en wordt gerapporteerd of de test is geslaagd.
