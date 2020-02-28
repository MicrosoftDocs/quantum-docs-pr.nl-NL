---
title: Broombridge-Quantum-schei kunde-schema
description: Overzicht van het Broombridge quantum chemie-schema, dat wordt gebruikt om praktijk problemen met de Microsoft Quantum Development Kit te model leren.
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: a746b63055bb1b2c1168b89993a7459ca9597f86
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907814"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Broombridge quantum chemie-schema # 

Met krachtige reken kundige schei kunde-software, zoals [NWChem](http://www.nwchem-sw.org/) , kunt u een breed scala aan praktijk problemen in het leven model leren. Om toegang te krijgen tot NWChem moleculaire modellen met de micro soft quantum chemie-bibliotheek, gebruiken we een op [yaml](https://en.wikipedia.org/wiki/YAML)gebaseerd schema dat we **Broombridge**aanroepen. De naam is gekozen in een verwijzing naar een [oriëntatie](https://en.wikipedia.org/wiki/Broom_Bridge) punt in sommige cirkels celebrated als een Birthplace van Hamiltonians. 

[NWChem](https://github.com/nwchemgit/nwchem) is een open-source project waarvoor een licentie is verkregen onder de ecl-licentie (Conal Community License 2,0). Broombridge is een open-source schema dat [hier](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) wordt opgegeven en dat wordt geleverd met een [definitie](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) volgens [RFC 2119](https://tools.ietf.org/html/rfc2119) en [VALIDATOR script](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) in licentie gegeven onder de MIT-licentie. 

Broombridge is een gestructureerde, door de mens lees bare en YAML bare manier om elektronische structuur problemen aan te duiden. Met name de volgende gegevens kunnen worden weer gegeven: 
- Fermionic Hamiltonians kan worden weer gegeven met een-en tweedelige integraal. 
- U kunt de status van de grond en de opgewonden gebruiken met het maken van reeksen.
- De boven-en ondergrenzen van de energie niveaus kunnen worden opgegeven.

De gegevens indeling kan worden gegenereerd op basis van NWChem met moeiteloos gemak: er is een groot aantal methoden beschikbaar die variëren van een volledige installatie van NWChem om schei kunde uit te voeren, zoals [hier](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) en uitvoer Broombridge als onderdeel van de uitvoering, via een docker-installatie kopie van NWChem die ook kan worden gebruikt voor het genereren van Broombridge van chemie-dekken. Ten slotte wordt een visuele methode gebruikt om snel aan de slag te gaan met berekeningen zonder enige schei kunde te hoeven installeren door de [EMSL-pijlen](https://arrows.emsl.pnnl.gov/api/qsharp_chem) interface naar NWChem. 

Op hoog niveau kunnen de Interplay tussen NWChem en de Microsoft Quantum Development Kit als volgt worden gevisualiseerd: ![chemie stack](~/media/broombridge.png) het blauwe grijze vak het Broombridge-schema vertegenwoordigt, de verschillende grijze gearceerde vakken vertegenwoordigen andere interne gegevens representaties die zijn gekozen voor het weer geven en verwerken van Quantum algoritmen voor reken kundige schei kunde op basis van problemen met de praktijk. 

[Hier](https://github.com/microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML)vindt u meerdere chemische representaties die zijn gedefinieerd met behulp van het Broombridge-schema.
