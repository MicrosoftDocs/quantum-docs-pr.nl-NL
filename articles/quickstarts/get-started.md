---
uid: microsoft.quantum.welcome
title: Aan de slag met de Quantum Development Kit (QDK)
description: Lees meer over het programmeren van kwantumprojecten in Q# met de Microsoft Quantum Development Kit.
author: bradben
ms.author: v-benbra
ms.date: 5/10/2020
ms.topic: overview
no-loc:
- Q#
- $$v
ms.openlocfilehash: e56b0e0455773481fbff6cfb7f4a6817cfc93d1a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834496"
---
# <a name="get-started-with-the-quantum-development-kit-qdk"></a>Aan de slag met de Quantum Development Kit (QDK)

Welkom bij de Microsoft Quantum Development Kit.  

De Quantum Development Kit bevat alle hulpmiddelen die u nodig hebt om uw eigen kwantumprogramma's en -experimenten te bouwen met Q#, een programmeertaal die speciaal is ontworpen voor de ontwikkeling van kwantumtoepassingen.

Als u meteen aan de slag wilt gaan, begint u met de [QDK-installatiehandleiding](xref:microsoft.quantum.install).
U wordt begeleid bij de installatie van de Quantum Development Kit op Windows-, Linux- of MacOS-computers, zodat u uw eigen kwantumprogramma's kunt schrijven.

Als u geen ervaring hebt met kwantumcomputing, raadpleegt u de sectie [Overzicht](xref:microsoft.quantum.overview.introduction) voor meer informatie over kwantumcomputers en de grond beginselen van kwantumcomputing.

## <a name="get-started-programming"></a>Aan de slag met programmeren

De Quantum Development Kit biedt veel manieren om een kwantumprogramma te leren ontwikkelen met Q#.
Bekijk een van onze zelfstudies als u de kracht van kwanta wilt gebruiken:

* [Kwantumgenerator voor willekeurige nummers](xref:microsoft.quantum.quickstarts.qrng): begin met een Q#-toepassing in 'Hallo wereld'-stijl. Hiermee maakt u kennis met kwamtumconcepten en leert u binnen enkele minuten een kwantumtoepassing te bouwen en uit te voeren.
* [Kennismaken met verstrengeling met Q#](xref:microsoft.quantum.write-program): in deze zelfstudie wordt u begeleid bij het schrijven van een Q#-programma waarin enkele fundamentele concepten van het kwantumprogrammeren worden gedemonstreerd. Als u nog niet zo ver bent om code te gaan schrijven, kunt u de zelfstudie volgen zonder de QDK te installeren om een beeld te krijgen van de Q#-programmeertaal en de basisconcepten van kwantumcomputing.
* [Zoekalgoritme van Grover](xref:microsoft.quantum.quickstarts.search): bekijk dit voorbeeld van een Q#-programma om een idee te krijgen van de kracht van Q# voor het uitdrukken van een kwantumalgoritme op een manier waardoor de kwantumbewerkingen op laag niveau abstract worden gemaakt.
    In deze zelfstudie wordt u begeleid bij het ontwikkelen van het programma als een opdrachtprompttoepassing in Q#, met behulp van Visual Studio of Visual Studio Code.

### <a name="learning-further"></a>Verder leren
* Met de [Microsoft Learn-modules voor kwantumcomputing](https://docs.microsoft.com/learn/browse/?term=quantum) leert u de basisconcepten in uw eigen tempo kennen. De basisbeginselen voor het maken van kwantumprogramma's met de QDK leert u in de [eerste module](https://docs.microsoft.com/learn/modules/qsharp-create-first-quantum-development-kit/).
* Als u meer wilt weten over programmeren in Q#, raadpleegt u de [Quantum Katas](https://github.com/Microsoft/QuantumKatas): een verzameling oefeningen waarmee u op uw eigen tempo kennismaakt met kwantumcomputing aan de hand van programmeeroefeningen in Q#.
    Veel van deze kata's zijn ook beschikbaar als Q#-notebooks. 
* Onze [opslagplaats met voorbeelden](https://github.com/Microsoft/Quantum) laat meerdere voorbeelden zien van hoe u kwantumprogramma's kunt schrijven met behulp van Q#. De meeste van deze voorbeelden zijn geschreven met behulp van onze opensource-[kwantumbibliotheken](https://github.com/Microsoft/QuantumLibraries), waaronder onze [standaard](xref:microsoft.quantum.libraries.standard.intro)- en [chemie](xref:microsoft.quantum.chemistry.concepts.intro)bibliotheken (lees meer hieronder).

## <a name="key-concepts-for-quantum-computing"></a>Belangrijkste concepten voor kwantumcomputing

Als u nog geen ervaring hebt met kwantumontwikkeling, kan dit er allemaal een beetje spannend uitzien. Deze basisconcepten zijn ontworpen om u kennis te laten maken met de kwantumwereld en inzicht te krijgen in hoe kwantumcomputing verschilt van de klassieke wijze van het verwerken van informatie op de computer (computing).

* [Inzicht in kwantumcomputing](xref:microsoft.quantum.overview.understanding)
* [Kwantumcomputers en kwantumsimulators](xref:microsoft.quantum.overview.simulators)
* [Wat wordt verstaan onder de Q#-programmeertaal en de QDK?](xref:microsoft.quantum.overview.q-sharp)
* [Lineaire algebra voor kwantumcomputing](xref:microsoft.quantum.overview.algebra)

## <a name="quantum-development-kit-documentation"></a>Documentatie voor Quantum Development Kit

De huidige documentatie bevat de volgende aanvullende onderwerpen.

### <a name="no-locq-developer-guides"></a>Handleidingen voor ontwikkelaars in Q#

* De [Q#-gebruikershandleiding](xref:microsoft.quantum.guide) beschrijft uitgebreid de concepten voor het maken van kwantumprogramma's in Q#.
* [Kwantumsimulators en hosttoepassingen](xref:microsoft.quantum.machines): bevat informatie over hoe kwantumalgoritmen worden uitgevoerd, welke kwantumcomputers beschikbaar zijn en hoe u een niet-Q#-stuurprogramma schrijft voor uw kwantumprogramma.

### <a name="no-locq-libraries"></a>Q#-bibliotheken

* De [Q#-standaardbibliotheken](xref:microsoft.quantum.libraries.standard.intro) bevatten informatie over de bewerkingen en functies die ondersteuning bieden voor zowel het besturingselement in een klassieke taal als de Q#-kwantumalgoritmen. 
    Besproken onderwerpen omvatten controlestromen, gegevensstructuren, foutcorrectie, testen en foutopsporing. 
* De [Q#-chemiebibliotheek](xref:microsoft.quantum.chemistry.concepts.intro) bevat informatie over de bewerkingen en functies die kwantumsimulaties mogelijk maken voor chemie, een belangrijke toepassing van kwantumcomputing. Onderwerpen zijn onder andere het simuleren van Hamiltoniaanse dynamica en kwantumfaseschatting.
* De [numerieke Q#-bibliotheek](xref:microsoft.quantum.numerics.intro) bevat informatie over de bewerkingen en functies die het uitdrukken van ingewikkelde wiskundige functies mogelijk maken in systeemeigen bewerkingen voor doelcomputers.
* [Naslaginformatie over de Q#-bibliotheek](xref:microsoft.quantum.apiref-intro) bevat naslaginformatie over bibliotheekentiteiten op naamruimte.

### <a name="general-quantum-computing"></a>Algemene kwantumcomputing

* [De concepten van kwantumcomputing](xref:microsoft.quantum.concepts.intro) bieden onder andere informatie over de relevantie van lineaire algebra voor kwantumcomputing, de aard en het gebruik van een qubit, het lezen van een kwantumcircuit en nog veel meer.
* [De woordenlijst voor kwantumcomputing](xref:microsoft.quantum.glossary) is een woordenlijst met een aantal essentiële termen die specifiek zijn voor kwantumcomputing en -programmaontwikkeling.
    Als u nog geen ervaring hebt met dit veld, kan het handig zijn om deze tijdens het lezen van onze documentatie bij de hand te houden.
* [De sectie Meer informatie](xref:microsoft.quantum.more-information) omvat speciaal geselecteerde verwijzingen voor een gedetailleerde verkenning van de onderwerpen rondom kwantumcomputing.

### <a name="additional-info"></a>Aanvullende informatie

* [Opmerkingen bij de release van de Microsoft Quantum Development Kit](xref:microsoft.quantum.relnotes).


## <a name="be-a-part-of-the-no-locq-open-source-community"></a>Deel uitmaken van de opensource-community voor Q#

De Quantum Development Kit is een open-source Development Kit waarmee ontwikkelaars kwantumcomputing toegankelijker maken, zodat we enkele van de meest uitdagende problemen ter wereld kunnen oplossen.  Academische instellingen die opensource-software nodig hebben, kunnen Q# implementeren voor hun kwantumonderwijs- en ontwikkeling. Door de Development Kit opensource te maken, krijgen ontwikkelaars en domeinexperts ook de kans om via hun code verbeteringen en ideeën bij te dragen.

Uw feedback, deelname en bijdragen aan de Quantum Development Kit zijn belangrijk.  Zie [Bijdragen aan de Quantum Development Kit](xref:microsoft.quantum.contributing) voor meer informatie over de Quantum Development Kit-bronnen, om feedback te geven en om informatie te vinden over hoe u deel kunt uitmaken van de beslissingen en bijdragen aan dit groeiende kwantumontwikkelplatform.

Zie [Microsoft Quantum](https://www.microsoft.com/en-us/quantum/) als u meer algemene informatie wilt over het Microsoft-initiatief voor kwantumcomputing.
