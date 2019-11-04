---
title: Broombridge-Quantum-schei kunde-schema
author: martinro
ms.author: martinro@microsoft.com
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
ms.openlocfilehash: c2a7636d0b3f07419e3312e04da5d811229ad854
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73185321"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Broombridge quantum chemie-schema # 

Met krachtige reken kundige schei kunde-software, zoals [NWChem](http://www.nwchem-sw.org/) , kunt u een breed scala aan praktijk problemen in het leven model leren. Om toegang te krijgen tot NWChem moleculaire modellen met de micro soft quantum chemie-bibliotheek, gebruiken we een op [yaml](https://en.wikipedia.org/wiki/YAML)gebaseerd schema dat we **Broombridge**aanroepen. De naam is gekozen in een verwijzing naar een [oriëntatie](https://en.wikipedia.org/wiki/Broom_Bridge) punt in sommige cirkels celebrated als een Birthplace van Hamiltonians. 

[NWChem](https://github.com/nwchemgit/nwchem) is een open-source project waarvoor een licentie is verkregen onder de ecl-licentie (Conal Community License 2,0). Broombridge is een open-source schema dat [hier](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) wordt opgegeven en dat wordt geleverd met een [definitie](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) volgens [RFC 2119](https://tools.ietf.org/html/rfc2119) en [VALIDATOR script](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) in licentie gegeven onder de MIT-licentie. 

Broombridge is een gestructureerde, door de mens lees bare en YAML bare manier om elektronische structuur problemen aan te duiden. Met name de volgende gegevens kunnen worden weer gegeven: 
- Fermionic Hamiltonians kan worden weer gegeven met een-en tweedelige integraal. 
- U kunt de status van de grond en de opgewonden gebruiken met het maken van reeksen.
- De boven-en ondergrenzen van de energie niveaus kunnen worden opgegeven.

De gegevens indeling kan worden gegenereerd op basis van NWChem met moeiteloos gemak: er is een groot aantal methoden beschikbaar die variëren van een volledige installatie van NWChem om schei kunde uit te voeren, zoals die [hier](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) en uitvoer Broombridge als onderdeel van de uitvoering, via een docker afbeelding van NWchem, die ook kan worden gebruikt voor het genereren van Broombridge van schei-dekken. Ten slotte wordt een visuele methode gebruikt om snel aan de slag te gaan met berekeningen zonder enige schei kunde te hoeven installeren door de [EMSL-pijlen](https://arrows.emsl.pnnl.gov/api/qsharp_chem) interface naar NWChem. 

Op hoog niveau kunnen de Interplay tussen NWChem en de Microsoft Quantum Development Kit als volgt worden gevisualiseerd: ![chemie stack](~/media/broombridge.png) het blauwe grijze vak het Broombridge-schema vertegenwoordigt, de diverse grijze grijze vakken vertegenwoordigen andere interne gegevens representaties die zijn gekozen voor het weer geven en verwerken van Quantum algoritmen voor reken kundige schei kunde op basis van problemen met de praktijk. 

[Hier](https://github.com/microsoft/Quantum/tree/master/Chemistry/IntegralData/YAML)vindt u meerdere chemische representaties die zijn gedefinieerd met behulp van het Broombridge-schema.

