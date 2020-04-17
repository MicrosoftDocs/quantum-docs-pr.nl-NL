---
uid: microsoft.quantum.welcome
title: Aan de slag met de Quantum Development Kit (QDK)
description: Lees meer over het programmeren van kwantumprojecten in Q# met de Microsoft Quantum Development Kit (QDK).
author: natke
ms.author: nakersha
ms.date: 10/23/2019
ms.topic: overview
ms.openlocfilehash: cea39e47ec5e7e2ad97adbbb39ba586274564967
ms.sourcegitcommit: 7d350db4b5e766cd243633aee7d0a839b6274bd6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2020
ms.locfileid: "77907627"
---
# <a name="get-started-with-the-quantum-development-kit-qdk"></a>Aan de slag met de Quantum Development Kit (QDK)

Welkom bij de Microsoft Quantum Development Kit.  
De QDK bevat alle hulpmiddelen die u nodig hebt om uw eigen kwantumprogramma's en -experimenten te bouwen met Q#, een programmeertaal die speciaal is ontworpen voor de ontwikkeling van kwamtumtoepassingen. 

Als u meteen aan de slag wilt gaan, gaat u naar de [QDK-installatiehandleiding](xref:microsoft.quantum.install).
U wordt dan geleid door de installatie van de Quantum Development Kit op Windows-, Linux-of MacOS-computers, zodat u uw eigen kwantumprogramma's kunt schrijven.

Als u het nog niet aandurft gelijk code te gaan schrijven, maar eerst graag meer wilt weten over kwantumcomputing en Q#, raden we u aan dit artikel alsnog te lezen om inzicht te krijgen in de resources die u kunt gebruiken. In de sectie [Vijf vragen over kwantumcomputing](#five-questions-about-quantum-computing) vindt u koppelingen naar precies wat u zoekt.

## <a name="get-started-programming"></a>Aan de slag met programmeren

De Quantum Development Kit biedt veel manieren om een kwantumprogramma te leren ontwikkelen met Q#.
Om zelf de kracht van kwantum te gaan gebruiken, kunt u een van onze *quickstarts* proberen:

* De [Kwantumgenerator voor willekeurige nummers](xref:microsoft.quantum.quickstarts.qrng) is een Q#-toepassing in 'Hello World'-stijl. Hiermee maakt u kennis met kwamtumconcepten en leert u binnen enkele minuten een kwantumtoepassing bouwen en uitvoeren.
* Handleidingen over de [basisprincipes van kwantumprogramma's in Q#](xref:microsoft.quantum.write-program) begeleiden u bij het schrijven van een Q#-programma dat enkele van de basisconcepten van kwantumprogrammering laat zien. 
    Als u nog niet zo ver bent om code te gaan schrijven, kunt u de zelfstudie volgen zonder de QDK te installeren om een beeld te krijgen van de Q#-programmeertaal en de basisconcepten van kwantumcomputing.
* Het [zoekalgoritme van Grover](xref:microsoft.quantum.quickstarts.search) bevat een voorbeeld van een Q#-programma om een idee te krijgen van de kracht van Q# voor het uitdrukken van een kwantumalgoritme op een manier waardoor de kwantumbewerkingen op laag niveau abstract worden gemaakt. 
    Deze quickstart helpt u bij het ontwikkelen van het programma met behulp van verschillende programmeeromgevingen (met een Python-host of met .NET en Visual Studio of Visual Studio Code).

### <a name="learning-further"></a>Verder leren
* Als u meer wilt weten over programmeren in Q#, raadpleegt u de [Quantum Katas](https://github.com/Microsoft/QuantumKatas): een verzameling oefeningen waarmee u op uw eigen tempo kennismaakt met kwantumcomputing aan de hand van programmeeroefeningen in Q#.
    Veel van deze kata's zijn ook beschikbaar als Q#-notebooks. 
* Onze [opslagplaats met voorbeelden](https://github.com/Microsoft/Quantum) laat meerdere voorbeelden zien van hoe u kwantumprogramma's kunt schrijven met behulp van Q#. De meeste van deze voorbeelden zijn geschreven met behulp van onze opensource [kwantumbibliotheken](https://github.com/Microsoft/QuantumLibraries), waaronder onze [standaard](xref:microsoft.quantum.libraries.standard.intro)- en [chemie](xref:microsoft.quantum.chemistry.concepts.intro)bibliotheken (hierover leest u hieronder meer).

## <a name="five-questions-about-quantum-computing"></a>Vijf vragen over kwantumcomputing

Als u nog geen ervaring hebt met kwantumontwikkeling, kan dit er allemaal een beetje spannend uitzien. We hebben resources verzameld die het makkelijker maken om te leren werken met kwantumcomputing. We weten zeker dat u met de hulp van deze korte artikelen snel aan de slag kunt met programmeren.
* [Wat is kwantumcomputing?](xref:microsoft.quantum.overview.what)
* [Wat kunnen kwantumcomputers doen?](xref:microsoft.quantum.overview.computers)
* [Waarom zou ik kwantumcomputing leren gebruiken?](xref:microsoft.quantum.overview.why)
* [Wat is Q#?](xref:microsoft.quantum.overview.qsharp)
* [Hoe leer ik kwantumcomputing met Q#?](xref:microsoft.quantum.overview.learn)

## <a name="quantum-development-kit-documentation"></a>Documentatie voor Quantum Development Kit

De huidige documentatie bevat de volgende aanvullende onderwerpen.

### <a name="using-q"></a>Q# gebruiken
* [De kwantumontwikkelingstechnieken](xref:microsoft.quantum.techniques.intro) beschrijven de belangrijkste concepten die worden gebruikt voor het maken van kwantumprogrammama's in Q#. Hier komen onder andere onderwerpen aan bod als bestandsstructuren, bewerkingen en functies, werken met qubits en enkele geavanceerde onderwerpen.
* [De naslaginformatie voor de Q#-taal](xref:microsoft.quantum.language.intro) geeft informatie over de Q#-taal, waaronder het type model, expressies, instructies en het gebruik van de compiler.
* [Kwantumsimulators en hosttoepassingen](xref:microsoft.quantum.machines) beschrijft hoe kwantumalgoritmen worden uitgevoerd, welke kwantumcomputers beschikbaar zijn en hoe u een niet-Q#-stuurprogramma schrijft voor uw kwantumprogramma.

### <a name="q-libraries"></a>Q#-bibliotheken
* [Q#-standaardbibliotheken](xref:microsoft.quantum.libraries.standard.intro) beschrijft de bewerkingen en functies die ondersteuning bieden voor zowel het besturingselement in een klassieke taal als de Q#-kwantumalgoritmen. 
    Besproken onderwerpen omvatten controlestromen, gegevensstructuren, foutcorrectie, testen en foutopsporing. 
* [De Q#-chemiebibliotheek](xref:microsoft.quantum.chemistry.concepts.intro) beschrijft de bewerkingen en functies die kwantumsimulaties mogelijk maken voor chemie, een belangrijke toepassing van kwantumcomputing. Onderwerpen zijn onder andere het simuleren van Hamiltoniaanse dynamica en kwantumfaseschatting.
* [De Q#-wiskundebibliotheek](xref:microsoft.quantum.numerics.intro) beschrijft de bewerkingen en functies die het uitdrukken van ingewikkelde wiskundige functies mogelijk maken in systeemeigen bewerkingen voor de doelcomputers.
* [De naslaginformatie voor de Q#-bibliotheek](xref:microsoft.quantum.standardlibsintro) bevat naslaginformatie over bibliotheekentiteiten per naamruimte.

### <a name="general-quantum-computing"></a>Algemene kwantumcomputing
* [De concepten van kwantumcomputing](xref:microsoft.quantum.concepts.intro) bieden onder andere informatie over de relevantie van lineaire algebra voor kwantumcomputing, de aard en het gebruik van een qubit, het lezen van een kwantumcircuit en nog veel meer.
* [De woordenlijst voor kwantumcomputing](xref:microsoft.quantum.glossary) is een woordenlijst met een aantal essentiële termen die specifiek zijn voor kwantumcomputing en -programmaontwikkeling. 
    Als u nog geen ervaring hebt met dit veld, kan het handig zijn om deze tijdens het lezen van onze documentatie bij de hand te houden.
* [De sectie Meer informatie](xref:microsoft.quantum.more-information) omvat speciaal geselecteerde verwijzingen voor een gedetailleerde verkenning van de onderwerpen rondom kwantumcomputing.

### <a name="additional-info"></a>Aanvullende informatie
* [Opmerkingen bij de release van de Microsoft Quantum Development Kit](xref:microsoft.quantum.relnotes).


## <a name="be-a-part-of-the-q-open-source-community"></a>Deel uitmaken van de opensource-community voor Q#
De Quantum Development Kit is een open-source Development Kit waarmee ontwikkelaars kwantumcomputing toegankelijker maken, zodat we enkele van de meest uitdagende problemen ter wereld kunnen oplossen.  Academische instellingen die opensource-software nodig hebben, kunnen Q# implementeren voor hun kwantumonderwijs- en ontwikkeling. Door de Development Kit opensource te maken, krijgen ontwikkelaars en domeinexperts ook de kans om via hun code verbeteringen en ideeën bij te dragen.

Uw feedback, deelname en bijdragen aan de Quantum Development Kit zijn belangrijk.  Zie [Bijdragen aan de Quantum Development Kit](xref:microsoft.quantum.contributing) voor meer informatie over de Quantum Development Kit-bronnen, om feedback te geven en om informatie te vinden over hoe u deel kunt uitmaken van de beslissingen en bijdragen aan dit groeiende kwantumontwikkelplatform.

Zie [Microsoft Quantum](https://www.microsoft.com/en-us/quantum/) als u meer algemene informatie wilt over het Microsoft-initiatief voor kwantumcomputing.
