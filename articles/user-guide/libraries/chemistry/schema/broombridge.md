---
title: Broombridge quantum chemie-schema
description: Overzicht van het Broombridge quantum chemie-schema, dat wordt gebruikt om praktijk problemen met de Microsoft Quantum Development Kit te model leren.
author: martinro
ms.author: martinro
ms.date: 10/17/2018
ms.topic: article
uid: microsoft.quantum.libraries.chemistry.schema.broombridge
no-loc:
- Q#
- $$v
ms.openlocfilehash: e580fd8267cc7ba30533d557eceb486f8c205be6
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835771"
---
# <a name="broombridge-quantum-chemistry-schema"></a>Broombridge quantum chemie-schema # 

Met krachtige reken kundige schei kunde-software, zoals [NWChem](http://www.nwchem-sw.org/) , kunt u een breed scala aan praktijk problemen in het leven model leren. Als u met de micro soft quantum chemie-bibliotheek toegang wilt krijgen tot NWChem moleculaire modellen, gebruikt u een op [yaml](https://en.wikipedia.org/wiki/YAML)gebaseerd schema met de naam **Broombridge**. De naam is gekozen in een verwijzing naar een [oriëntatie](https://en.wikipedia.org/wiki/Broom_Bridge) punt in sommige cirkels celebrated als een Birthplace van Hamiltonians. 

[NWChem](https://github.com/nwchemgit/nwchem) is een open-source project waarvoor een licentie is verkregen onder de ecl-licentie (Conal Community License 2,0). Het [Broombridge quantum chemie-schema](https://docs.microsoft.com/quantum/libraries/chemistry/schema/spec_v_0_2)) is een open-source schema dat [een definitie](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/broombridge-0.1.schema.json) bevat volgens [RFC 2119](https://tools.ietf.org/html/rfc2119) en een [script voor validatie](https://raw.githubusercontent.com/Microsoft/Quantum/master/Chemistry/Schema/validator.py) van de licentie verlening onder de MIT-licentie. 

Broombridge is een gestructureerde, door de mens lees bare en YAML bare manier om elektronische structuur problemen aan te duiden. Met name de volgende gegevens kunnen worden weer gegeven:
- Fermionic Hamiltonians kan worden weer gegeven met een-en tweedelige integraal.
- U kunt de status van de grond en de opgewonden gebruiken met het maken van reeksen.
- De boven-en ondergrenzen van de energie niveaus kunnen worden opgegeven.

Gegevens kunnen worden gegenereerd van NWChem met behulp van verschillende methoden, zoals het gebruik van een volledige installatie van NWChem voor het uitvoeren van een schei kunde (bijvoorbeeld de [NWChem-bibliotheek](https://github.com/nwchemgit/nwchem/tree/master/QA/chem_library_tests) die Broombridge als onderdeel van de uitvoering), of een docker-installatie kopie van NWChem die ook kan worden gebruikt om Broombridge te genereren op basis van de beschik bare dekken. Om snel aan de slag te gaan met reken kundige schei kunde zonder enige schei kunde te hoeven installeren, kunt u de visuele interface gebruiken om NWChem van [EMSL-pijlen](https://arrows.emsl.pnnl.gov/api/qsharp_chem)te maken.

Op hoog niveau kunnen de Interplay tussen NWChem en de Microsoft Quantum Development Kit als volgt worden gevisualiseerd: ![ schei kunde ](~/media/broombridge.png) in het blauwe grijze vak vertegenwoordigt het Broombridge-schema, de verschillende grijze gearceerde vakken vertegenwoordigen andere interne gegevens representaties die zijn gekozen voor het weer geven en verwerken van Quantum algoritmen voor reken kundige schei kunde op basis van problemen met de praktijk.

De map [integraal/yaml](https://github.com/microsoft/Quantum/tree/master/samples/chemistry/IntegralData/YAML) in de Quantum Development Kit samples-opslag bevat meerdere chemische representaties die zijn gedefinieerd met het Broombridge-schema.
