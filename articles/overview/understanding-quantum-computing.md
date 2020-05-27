---
title: Kwantumcomputing begrijpen
description: Wat zijn kwantumcomputers en hoe maken ze gebruik van de principes van kwantummechanica?
author: bradben
ms.author: bradben
ms.date: 5/5/2020
ms.topic: overview
uid: microsoft.quantum.overview.understanding
ms.openlocfilehash: 65fa85a80021124444fd352f9492d03cbefcb859
ms.sourcegitcommit: a03d79ca3f0774161a9f86a15528d36e1291acce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83433007"
---
# <a name="understanding-quantum-computing"></a>Kwantumcomputing begrijpen

Bij kwantumcomputing worden de principes van kwantummechanica gebruikt voor het verwerken van informatie. Daarom vereist kwantumcomputing een andere benadering dan klassieke computing.  Een verschil, bijvoorbeeld, is de processor die in kwantumcomputers wordt gebruikt.  In klassieke computers worden welbekende siliciumchips gebruikt, terwijl in kwantumcomputers kwantummaterialen zoals atomen, ionen, fotonen of elektronen worden gebruikt.  

Het kwantummateriaal gedraagt zich in overeenstemming met de wetten van kwantummechanica, met behulp van concepten zoals probabilistische computing, superpositie en verstrengeling. Deze concepten vormen de basis voor kwantumalgoritmen, die de kracht van kwantumcomputing benutten voor het oplossen van complexe problemen. In dit artikel worden enkele essentiële concepten van kwantummechanica beschreven waarop kwantumcomputing is gebaseerd.

## <a name="a-birds-eye-view-of-quantum-mechanics"></a>Overzicht van kwantummechanica

Kwantummechanica, ook wel kwantumtheorie genoemd, is een tak van de natuurkunde die zich bezig houdt met deeltjes op atomair en subatomair niveau. Op kwantumniveau zijn echter veel natuurkundige wetten die u voor vanzelfsprekend aanneemt, niet van toepassing. Superpositie, kwantummeting en verstrengeling zijn drie verschijnselen die centraal staan in kwantumcomputing.  

### <a name="superposition-vs-binary-computing"></a>Superpositie versus binaire computing

Stel, u doet lichamelijke oefeningen in uw woonkamer. U draait helemaal naar links en vervolgens helemaal naar rechts. Draai nu tegelijkertijd naar links en rechts. Dat kunt u niet (tenzij u zichzelf in tweeën kunt splitsen).  Natuurlijk kunt u zich niet in twee standen tegelijk bevinden: u kunt niet op hetzelfde moment zowel naar links als naar rechts kijken.

Als u echter een kwantumdeeltje bent, is er een bepaalde kans dat u *naar links* kijkt én een bepaalde kans dat u *naar rechts* kijkt als gevolg van het verschijnsel **superpositie** (ook wel bekend als **coherentie**).

Een kwantumdeeltje, zoals een elektron, heeft zijn eigen eigenschappen voor de naar links of rechts kijkende toestand, zoals een **draaiing**, omhoog of omlaag. Om dit meer te relateren aan klassieke binaire computing, kunnen we die ook 1 of 0 noemen. Wanneer een kwantumdeeltje zich in een toestand van superpositie bevindt, is het een lineaire combinatie van een oneindig aantal toestanden tussen 1 en 0, maar u weet niet welke toestand totdat u deze daadwerkelijk bekijkt. Daarmee komen we toe aan het volgende verschijnsel: **kwantummeting**.

### <a name="quantum-measurement"></a>Kwantummeting

Stel nu dat een vriend(in) langskomt en een foto van u wil nemen terwijl u uw oefeningen doet. Waarschijnlijk krijgt u een wazige afbeelding van uw positie terwijl u zich beweegt van helemaal links naar helemaal rechts of omgekeerd.

Maar als u een kwantumdeeltje bent, gebeurt er iets interessants. Ongeacht in welke positie uw foto wordt genomen, uw toestand wordt altijd weergegeven als helemaal links of helemaal rechts, nooit als iets er tussenin.

Dit komt omdat de toestand van superpositie bij observatie of meting van een kwantumdeeltje **ineenstort** (dit wordt ook wel **decoherentie** genoemd) en het deeltje een klassieke binaire toestand van 1 of 0 heeft.

Deze binaire toestand is nuttig voor ons, omdat we in computing van alles kunnen doen met enen en nullen. Zodra een kwantumdeeltje is gemeten en ineengestort, blijft deze permanent in die toestand (net als uw foto) en is deze altijd 1 of 0. Zoals u later zult zien, zijn er in kwantumcomputing bewerkingen waarmee een deeltje opnieuw kan worden ingesteld op de toestand van superpositie, zodat het opnieuw kan worden gebruikt voor kwantumberekeningen.

### <a name="entanglement"></a>Verstrengeling

Wellicht het interessantste verschijnsel van kwantummechanica is de mogelijkheid van twee of meer kwantumdeeltjes om met elkaar **verstrengeld** te raken. Wanneer deeltjes verstrengeld raken, vormen ze één systeem waarvan de kwantumtoestand van elk afzonderlijk deeltje niet onafhankelijk kan worden beschreven van de kwantumtoestand van de andere deeltjes. Als u dus een bewerking of proces toepast op een deeltje, is die bewerking of dat proces ook gecorreleerd aan de andere deeltjes.

Naast deze onderlinge afhankelijkheid kan deze verbinding tussen deeltjes behouden blijven, zelfs wanneer de deeltjes van elkaar zijn gescheiden door een ongelooflijk grote afstand, zelfs lichtjaren. De effecten van kwantummeting zijn ook van toepassing op verstrengelde deeltjes. Als een deeltje wordt gemeten en ineenstort, stort ook het andere deeltje in. Omdat er sprake is van een correlatie tussen de verstrengelde qubits, biedt het meten van de toestand van een qubit informatie over de toestand van de andere qubit: deze eigenschap is zeer nuttig bij kwantumcomputing.

### <a name="qubits-and-probability"></a>Qubits en waarschijnlijkheid

Op klassieke computers wordt informatie verwerkt en opgeslagen in bits, die een toestand van 1 of 0 kunnen hebben, maar nooit beide. Het equivalent van een bit in kwantumcomputing is de **qubit**. Qubits geven de toestand van een kwantumdeeltje aan. Vanwege superpositie kan de toestand van qubits 1 of 0 zijn, of iets er tussenin. Afhankelijk van de configuratie van een qubit, heeft deze een bepaalde *kans* ineen te storten tot 1 of 0. De kans dat de qubit ineenstort tot een 1 of 0 wordt bepaald door **kwantuminterferentie**. 

Weet u nog van die vriend(in) die een foto van u nam? Stel dat er een speciaal filter op de camera zat, en wel een *interferentiefilter*. Als we het filter *70/30* selecteren en vervolgens foto's nemen, kijkt u in 70% van de foto's naar links en in 30% van de foto's naar rechts. Het filter heeft de normale toestand van de camera beïnvloed om de kans op het gedrag ervan te beïnvloeden.

Op soortgelijke wijze beïnvloedt kwantuminterferentie de toestand van een qubit om de kans op een bepaalde uitkomst van een meting te beïnvloeden, en deze probabilistische toestand is waarin de kracht van kwantumcomputing uitblinkt.

Zo kunt u bijvoorbeeld met twee bits op een klassieke computer, waarbij elke bit 1 of 0 bevat, vier mogelijke waarden opslaan: **00**, **01**, **10** en **11**, maar slechts één tegelijk. Met twee qubits in superpositie kan elke qubit 1 of 0 of *beide* zijn. Daarmee kunnen dus dezelfde vier waarden tegelijkertijd worden uitgedrukt. Met drie qubits kunnen acht waarden worden uitgedrukt, met vier qubits kunnen zestien waarden worden uitgedrukt, enzovoort.

## <a name="summary"></a>Samenvatting

Deze concepten vormen slechts het topje van de ijsberg van de krachtige mogelijkheden van kwantummechanica, maar zijn belangrijke grondbeginselen die u moet kennen voor kwantumcomputing.

- **Superpositie**: de mogelijkheid van kwantumdeeltjes om een combinatie van alle mogelijke toestanden te vormen.
- **Kwantummeting**: de handeling van het observeren van een kwantumdeeltje in superpositie, hetgeen resulteert in een van de mogelijke toestanden.
- **Verstrengeling**: de mogelijkheid van kwantumdeeltjes om de meetresultaten met elkaar te correleren.
- **Qubit**: de basiseenheid van informatie bij kwantumcomputing. Een qubit vertegenwoordigt een kwantumdeeltje in superpositie van alle mogelijke toestanden.
- **Interferentie**: intrinsiek gedrag van een qubit vanwege superpositie om de kans op ineenstorting tot de ene of andere toestand te beïnvloeden.

## <a name="next-steps"></a>Volgende stappen

> [!div class="nextstepaction"]
> [Kwantumcomputers en kwantumsimulators](xref:microsoft.quantum.overview.simulators)
