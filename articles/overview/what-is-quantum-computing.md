---
title: Wat is kwantumcomputing?
description: Ontdek wat kwantumcomputing is en wat een kwantumcomputer kan doen
author: natke
ms.author: nakersha
ms.date: 10/22/2019
ms.topic: article
uid: microsoft.quantum.overview.what
ms.openlocfilehash: 2f3b64b00a0a9552e52e34cb1e3652810b266eab
ms.sourcegitcommit: edcf15044d7bdf4f8b21fb8f6af4bde475eb13a0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2019
ms.locfileid: "73529936"
---
# <a name="what-is-quantum-computing"></a>Wat is kwantumcomputing?

Er zijn bepaalde problemen die zo moeilijk zijn, zo gigantisch van omvang, dat zelfs als alle supercomputers in de wereld tegelijk aan een oplossing van het probleem zouden werken, het nog langer dan de levensduur van het universum zou duren voordat die gevonden zou zijn.

Kwantumcomputers lijken de oplossing te kunnen bieden voor een aantal van de grootste uitdagingen op onze planeet, bijvoorbeeld op het gebied van milieu, landbouw, gezondheid, energie, klimaat, materiaalwetenschappen en gebieden waarvan we nog geen voorstelling hebben. De impact van kwantumcomputers zal ingrijpend zijn en zal net zo'n invloed hebben als de uitvinding van de transistor in 1947, die de basis heeft gelegd voor de digitale economie van vandaag.

Kwantumcomputing maakt gebruik van het unieke gedrag van kwantumfysica om een nieuw en krachtig computingmodel te bieden. De theorie van de kwantumfysica stelt dat materie, op kwantumniveau, zich in superpositie van meerdere klassieke toestanden kan bevinden. En deze verschillende toestanden verstoren elkaar zoals golven in een getijdepoel.  De toestand van materie valt na een meting uiteen in een van de klassieke toestanden. 

Als daarna dezelfde meting wordt herhaald, levert die hetzelfde klassieke resultaat op.  Kwantumverstrengeling treedt op wanneer de interactie van deeltjes zodanig is dat de kwantumtoestand van elk deeltje niet los van de andere deeltjes kan worden beschreven, zelfs niet als de deeltjes fysiek gescheiden zijn.  

Bij kwantumcomputing worden gegevens opgeslagen in kwantumtoestanden van materie en wordt de kwantumaard van superpositie en verstrengeling gebruikt om kwantumbewerkingen uit te voeren die berekeningen toepassen op gegevens, om zo gebruik te maken van kwantuminterferentie en deze te programmeren.

Kwantumcomputing klinkt misschien erg spannend, maar met de juiste middelen kunt u vandaag nog uw eerste kwantumtoepassingen bouwen.

## <a name="the-qubit"></a>De qubit

Met kwantumcomputing worden computingconcepten gedefinieerd die het kwantumgedrag weerspiegelen.  Kwantumcomputing begint met het principe van een qubit.  In kwantumcomputing is een kwantumbit (meestal een **qubit** genoemd) een eenheid van kwantumgegevens, te vergelijken met een klassieke bit. Waar klassieke bits één binaire waarde bevatten, zoals een 0 of een 1, kan de toestand van een qubit in een **superpositie** zijn van gelijktijdig 0 en 1.  

Als er een meting wordt toegepast op een qubit, verandert de toestand van de qubit. De qubit gaat dan over van de toestand van superpositie naar een van de klassieke toestanden.  

Meerdere qubits kunnen ook **verstrengeld** zijn. Wanneer we een meting uitvoeren van één verstrengelde qubit, wordt onze kennis van de toestand van de andere qubit(s) ook bijgewerkt.

## <a name="quantum-algorithms"></a>Kwantumalgoritmen

Kwantumalgoritmen worden ontworpen om gebruik te maken van de aard en het gedrag van kwantummechanica om klassieke algoritmen te versnellen of om volledig nieuwe manieren te bieden voor de modellering van fysieke systemen.  Deze algoritmen maken gebruik van de manier waarop qubits gegevens versleutelen en van de parallelle aard van interactie met meerdere verstrengelde qubits in superpositie.  

Klassieke computers coderen gegevens in bits, waarbij elke bit 0 mogelijke waarden codeert, 0 of 1.  Eén qubit codeert twee waarden tegelijk, 0 en 1.  Twee klassieke bits coderen een van vier mogelijke waarden, (00, 01, 10, 11) terwijl twee qubits een willekeurige superpositie van die vier waarden tegelijk coderen, hoewel we door te meten slechts een van deze waarden kunnen verkrijgen. Vier qubits coderen elke superpositie van 16 waarden tegelijk, enzovoort, op een exponentiële manier.  100 qubits kunnen meer informatie coderen dan vandaag de dag beschikbaar is in de grootste computersystemen.  

Wanneer meerdere qubits zich bovendien coherent gedragen, kunnen ze meerdere opties tegelijk verwerken. Verstrengelde qubits kunnen gegevens verwerken in een fractie van de tijd die het allersnelste niet-kwantumsysteem nodig zou hebben.

Het benutten van deze kwantumkenmerken is decennia lang het doel geweest van onderzoek naar kwantumalgoritmen en er zijn veel innovatieve technieken die zijn gevonden om problemen op te lossen in een fractie van de tijd die de klassieke aanpak hiervoor nodig heeft.  

Een van de beroemdste kwantumalgoritmen is het _algoritme van Shor_ voor het ontbinden in factoren, waardoor de traditioneel lastige kwestie van het ontbinden van een groot getal in twee priemgetallen snel genoeg kan worden opgelost om zich te meten met traditionele cryptografie.

Een meer opbouwende benadering vinden we in de algoritmen voor veilige distributie van cryptografische sleutels, die mogelijk worden gemaakt door superpositie, kwantumverstrengeling en de eigenschap van qubits dat deze **niet kloonbaar** zijn, wat inhoudt dat qubits niet zonder detectie kunnen worden gekopieerd.

Het _algoritme van Grover_ illustreert een techniek voor kwantumalgoritmen die het mogelijk maakt om ongestructureerde gegevens met een kwadratische factor sneller te doorzoeken.

## <a name="quantum-hardware"></a>Kwantumhardware

In klassieke computers komen bits overeen met spanningsniveaus in schakelingen. Hardware voor kwantumcomputing kan worden geïmplementeerd als een groot aantal verschillende fysieke realisaties van qubits: overlappende ionen, supergeleiding, neutrale atomen, elektronenrotatie, lichtpolarisatie, topologische qubits. Kwantumhardware is een opkomende technologie. Qubits zijn van nature kwetsbaar en worden minder coherent wanneer ze interactie hebben met hun omgeving. Er moet een balans worden gevonden tussen betrouwbaarheid en schaalbaarheid van het systeem. Hoe groter de schaal (het aantal qubits), des te hoger het foutenpercentage.

Microsoft is bezig met de ontwikkeling van een kwantumcomputer op basis van topologische qubits. Wij denken dat een topologische qubit minder zal worden beïnvloed door veranderingen van de omgeving, waardoor de mate van externe foutcorrectie zal afnemen. Topologische qubits zijn stabieler en beter bestand tegen omgevingsruis, wat betekent dat ze makkelijker kunnen worden geschaald en langer betrouwbaar blijven.

## <a name="quantum-computing--a-full-hardware-and-software-stack"></a>Kwantumcomputing: een complete hardware- en software-stack

Het kwantumprogramma van Microsoft is uniek omdat we ons richten op het schalen van elk onderdeel van het systeem om zo echte kwantumimpact te kunnen bieden. Deze uitgebreide aanpak omvat het volgende:

* het bouwen van een kwantumcomputer met behulp van betrouwbare, schaalbare en fouttolerante topologische qubits 
* het ontwerpen van een uniek cryogeen besturingsvlak met een laag stroomverbruik en uitzonderlijke lage warmteafgifte 
* het ontwikkelen van een complete software-stack om programmering van de kwantumcomputer mogelijk te maken evenals het op schaal beheren van het systeem

De open source Quantum Development Kit (QDK) is geïntroduceerd om kwantumprogrammering en de ontwikkeling van algoritmen toegankelijker te maken. Onze high-level programmeertaal, Q#, is bedoeld om de uitdagingen van kwantumprogrammering weg te nemen.  We hebben Q# ontworpen als een high-level, op kwantum gerichte programmeertaal voor het ontwikkelen van algoritmen en toepassingen. De Q#-compiler is geïntegreerd in een software-stack die het mogelijk maakt om een kwantumalgoritme uit te compileren tot de primitieve bewerkingen van een kwantumcomputer.  Tot een bepaalde schaal (aantal qubits) kan kwantumcomputing worden gesimuleerd op een klassieke computer. Met behulp van simulatie kunt u vandaag nog kwantumprogramma's gaan schrijven die morgen beschikbaar zijn voor uitvoering op kwantumhardware.  We hebben Q# ook gekoppeld aan voorbeelden, bibliotheken en praktijkoefeningen om vandaag nog eenvoudig aan de slag te gaan met kwantumprogrammeren. 

## <a name="next-steps"></a>Volgende stappen

* [Wat kunnen kwantumcomputers doen?](xref:microsoft.quantum.overview.computers)
* [Aan de slag met de Microsoft Quantum Development Kit](xref:microsoft.quantum.welcome)
* Lees meer over [de concepten van kwantumcomputing](xref:microsoft.quantum.concepts.intro)
