---
title: Inleiding tot kwantumcomputing
description: Lees hier alles over kwantumcomputing, wat kwantumcomputers kunnen doen en hoe u kwantumcomputing kunt leren.
author: bradben
ms.author: bradben
ms.date: 05/05/2020
ms.topic: overview
uid: microsoft.quantum.overview.introduction
no-loc:
- Q#
- $$v
ms.openlocfilehash: 59cb595ac207d6e84358fc6ba742e0e0019c76f9
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87866975"
---
# <a name="introduction-to-quantum-computing-and-the-quantum-development-kit"></a>Inleiding tot kwantumcomputing en de Quantum Development Kit

De Microsoft Quantum Development Kit (QDK) is een set opensource-hulpprogramma's die ontwikkelaars helpen bij het leren van kwantumalgoritmen en het schrijven van kwantumprogramma's. Kwantumcomputing lijkt de oplossing te kunnen bieden voor een aantal van de grootste uitdagingen op onze planeet, bijvoorbeeld op het gebied van milieu, landbouw, gezondheid, energie, klimaat, materiaalwetenschappen en andere gebieden waar we nog mee te maken krijgen.  

Voor sommige problemen zijn zelfs de krachtigste computers niet sterk genoeg. Hoewel de kwantumtechnologie pas net invloed begint te krijgen in de computerwereld, kan deze onze manier van denken over computing ingrijpend veranderen.

## <a name="what-is-quantum-computing"></a>Wat is kwantumcomputing?

In het moderne taalgebruik is een kwantum de kleinste, ondeelbare hoeveelheid van een fysische eigenschap, gewoonlijk met betrekking tot eigenschappen van atomaire of subatomaire deeltjes. Kwantumcomputers gebruiken daadwerkelijk kwantumdeeltjes, kunstmatige atomen of collectieve eigenschappen van kwantumdeeltjes als verwerkingseenheden. Het zijn grote, ingewikkelde en dure apparaten.

Door het unieke gedrag van kwantumfysica te benutten voor computing-toepassingen, worden met kwantumcomputers nieuwe concepten geïntroduceerd in traditionele programmeermethoden, waarbij gebruik wordt gemaakt van kwantumfysica-gedrag, zoals superpositie, verstrengeling en kwantuminterferentie.

## <a name="what-can-a-quantum-computer-do"></a>Wat kan een kwantumcomputer doen?

Een kwantumcomputer is geen supercomputer die alles sneller kan doen, maar er zijn een paar gebieden waarop kwantumcomputers uitzonderlijk goed presteren.

- [Kwantumsimulatie](xref:microsoft.quantum.overview.introduction#quantum-simulation)
- [Cryptografie](xref:microsoft.quantum.overview.introduction#cryptography-and-shors-algorithm)
- [Zoeken](xref:microsoft.quantum.overview.introduction#search-and-grovers-algorithm)
- [Optimalisatie](xref:microsoft.quantum.overview.introduction#quantum-inspired-computing-and-optimization)
- [Machine learning](xref:microsoft.quantum.overview.introduction#quantum-machine-learning)

## <a name="quantum-simulation"></a>Kwantumsimulatie

Omdat kwantumcomputers gebruikmaken van kwantumverschijnselen in berekeningen, zijn ze bij uitstek geschikt voor het modelleren van andere kwantumsystemen. Fotosynthese, supergeleiding en complexe moleculaire vormen zijn voorbeelden van kwantummechanismen die met kwantumprogramma's kunnen worden gesimuleerd.

## <a name="cryptography-and-shors-algorithm"></a>Cryptografie en het algoritme van Shor

In 1994 toonde Peter Shor aan dat veelgebruikte versleutelingstechnieken, zoals het RSA-algoritme, kunnen worden gekraakt met een schaalbare kwantumcomputer. Klassieke cryptografie is gebaseerd op de onoplosbaarheid van problemen, zoals ontbinding in priemgetallen of afzonderlijke logaritmen. Veel van die problemen kunnen echter efficiënter kunnen worden opgelost met behulp van kwantumcomputers.

## <a name="search-and-grovers-algorithm"></a>Het zoekalgoritme van Grover

In 1996 ontwikkelde Lov Grover een kwantumalgoritme waarmee ongestructureerde gegevenszoekopdrachten fors sneller en in minder stappen konden worden uitgevoerd dan met welk klassiek algoritme ooit tevoren.

## <a name="quantum-inspired-computing-and-optimization"></a>Door kwantum geïnspireerde computing en optimalisatie

Door kwantum geïnspireerde algoritmen gebruiken kwantumprincipes voor hogere snelheid en verbeterde nauwkeurigheid, maar worden geïmplementeerd op klassieke computersystemen. Met deze aanpak kunnen ontwikkelaars de kracht van nieuwe kwantumtechnieken gebruiken zonder te hoeven wachten op kwantumhardware. Deze industrie is nog in opkomst.

Optimalisatie is het proces van het vinden van de beste oplossing voor een probleem, gegeven de gewenste resultaten en beperkingen. Factoren zoals kosten, kwaliteit of productietijd spelen allemaal een essentiële rol bij het nemen van beslissingen in industrie en wetenschap. Met door kwantum geïnspireerde optimalisatie-algoritmen op klassieke computers van tegenwoordig kunnen oplossingen worden gevonden die tot op heden niet mogelijk waren. Naast het optimaliseren van verkeersstromen om files te verminderen, zijn er kansen voor de toewijzing van gates voor vliegtuigen, pakketbezorging, taakplanning en meer. Met baanbrekende ontwikkelingen in materiaalwetenschappen krijgen we de beschikking over nieuwe vormen van energie, accu's met een grotere capaciteit en lichter en duurzamer materiaal.

> [!NOTE]
> Meer informatie over hoe door kwantum geïnspireerde computing van Microsoft wordt gebruikt op het gebied van [materiaalwetenschappen](https://cloudblogs.microsoft.com/quantum/2020/01/21/oti-lumionics-accelerating-materials-design-microsoft-azure-quantum/), [risicobeheer](https://cloudblogs.microsoft.com/quantum/2019/05/22/microsoft-quantum-collaborates-with-willis-towers-watson-to-transform-risk-management-solutions/) en [medicijnen](https://blogs.microsoft.com/blog/2018/05/18/microsoft-quantum-helps-case-western-reserve-university-advance-mri-research/).

## <a name="quantum-machine-learning"></a>Kwantum-machine learning

Machine learning op klassieke computers brengt een revolutie teweeg in de wereld van de wetenschap en het bedrijfsleven. De hoge rekenkosten voor training van de modellen belemmeren echter de ontwikkeling en het bereik ervan. Op het gebied van kwantum-machine learning wordt verkend hoe we kwantumsoftware kunnen ontwerpen en implementeren om machine learning sneller te kunnen uitvoeren dan op klassieke computers.

De Quantum Development Kit wordt geleverd met de [kwantumbibliotheek voor machine learning](xref:microsoft.quantum.machine-learning.concepts.intro), die u de mogelijkheid biedt om te experimenteren met een hybride combinatie van kwantum-machine learning en klassieke machine learning. De bibliotheek bevat voorbeelden en zelfstudies en voorziet in de nodige hulpprogramma's voor het implementeren van een nieuw hybride kwantum/klassiek algoritme, de circuit-gerichte kwantumclassificatie, om geleide classificatieproblemen op te lossen.

## <a name="no-locq-and-the-microsoft-quantum-development-kit-qdk"></a>Q# en de Microsoft Quantum Development Kit (QDK)

Q# is de opensource-programmeertaal van Microsoft voor het ontwikkelen en uitvoeren van kwantumalgoritmen. Deze maakt deel uit van de [QDK](https://docs.microsoft.com/quantum/), een volledige Development Kit voor Q# die u kunt gebruiken met gangbare hulpprogramma's en talen om kwantumtoepassingen te ontwikkelen die u in verschillende omgevingen kunt uitvoeren, waaronder de ingebouwde kwantumsimulator van de volledige kwantumtoestand.

Er zijn extensies voor Visual Studio en Visual Studio Code, en pakketten voor gebruik met Python en Jupyter Notebook.

De QDK bevat een standaardbibliotheek en gespecialiseerde bibliotheken voor chemie, machine learning en berekeningen.

De documentatie bevat een handleiding voor de taal Q#, zelfstudies en voorbeeldcode waarmee u snel aan de slag kunt gaan, alsmede uitgebreide artikelen om u verder te verdiepen in de concepten van kwantumcomputing.  

## <a name="microsoft-quantum-hardware-partners"></a>Microsoft-partners voor kwantumhardware

Microsoft is een partnerschap aangegaan met kwantumhardwarebedrijven om ontwikkelaars cloudtoegang tot kwantumhardware te bieden. Met het [Azure Quantum](https://azure.microsoft.com/services/quantum/)-platform en de taal Q# kunnen ontwikkelaars kwantumalgoritmen verkennen en hun kwantumprogramma's uitvoeren op verschillende typen kwantumhardware.

[IonQ](https://ionq.com/news/november-4-2019-microsoft-partnership) en [Honeywell](https://www.honeywell.com/en-us/newsroom/news/2019/11/the-future-of-quantum-computing) gebruiken beide processoren met **gevangen ionen**, waarbij gebruik wordt gemaakt van afzonderlijke ionen die gevangen zitten in een elektronisch veld, terwijl [QCI](https://quantumcircuits.com/news-and-publications/quantum-circuits-partners-with-microsoft-on-azure-quantum) gebruik maakt van supergeleidende circuits.

## <a name="next-steps"></a>Volgende stappen

[Belangrijkste concepten voor kwantumcomputing](xref:microsoft.quantum.overview.understanding)
[Quickstarts](xref:microsoft.quantum.welcome)