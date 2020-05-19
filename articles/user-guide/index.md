---
title: De Q#-gebruikershandleiding
description: Overzicht van het doel en de inhoud van de gebruikershandleiding
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 03/05/2020
ms.topic: article
uid: microsoft.quantum.guide
ms.openlocfilehash: f535aaedbe6ce181375d48f7023409ad8212c702
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2020
ms.locfileid: "83430608"
---
# <a name="the-q-user-guide"></a>De Q#-gebruikershandleiding

Welkom bij de Q#-gebruikershandleiding! 

Hier beschrijven de belangrijkste concepten van de Q#-taal en gevenwe alle informatie die u nodig hebt om kwantumprogramma's te schrijven.

## <a name="user-guide-contents"></a>Inhoud van de gebruikershandleiding

- [Q#-basis](xref:microsoft.quantum.guide.basics): een kennismakend overzicht van het doel en de functionaliteit van de Q#-programmeertaal. 

### <a name="q-language"></a>Q#-taal

- [Typen in Q#](xref:microsoft.quantum.guide.types): hierin wordt het Q#-typemodel gegeven en een beschrijving van de syntaxis om de typen op te geven en ermee te werken.

- [Type-expressies](xref:microsoft.quantum.guide.expressions): details over hoe u waarden opgeeft, ernaar verwijst, combineert en ermee werkt voor elk type in Q#. 

### <a name="using-q"></a>Q# gebruiken

- [Q#-bestandsstructuur](xref:microsoft.quantum.guide.filestructure): hierin worden de structuur en syntaxis van een `*.qs` Q#-bestand beschreven.

- [Bewerkingen en functies](xref:microsoft.quantum.guide.operationsfunctions) beschrijven de twee aanroepbare typen Q#-taal: *bewerkingen*, waaronder acties voor qubit-registers en *functies*, die alleen werken met klassieke informatie. 
    Hier ziet u hoe ze worden gedefinieerd en aangeroepen, inclusief de beheerde versies van kwantumbewerkingen.

- [Variabelen](xref:microsoft.quantum.guide.variables): hiermee wordt de rol van variabelen binnen Q#-programma's beschreven en hoe u er effectief gebruik van maakt. 
    U kunt bijvoorbeeld informatie vinden over bindingsbereiken, evenals de verschillen tussen onveranderlijke en veranderlijke variabelen en hoe u deze toewijst/opnieuw toewijst.

- [Werken met qubits](xref:microsoft.quantum.guide.qubits): hierin worden de functies van Q# uitgelegd die u kunt gebruiken om te werken met afzonderlijke qubits en systemen van qubits. 
    In het bijzonder de functies omtrent hun toewijzing, bewerkingen en uiteindelijk hun metingen. 

- [Controlestroom](xref:microsoft.quantum.guide.controlflow): details van de programmeerstroompatronen die beschikbaar zijn in Q#. Deze omvatten veel standaardtechnieken (voorwaardelijke uitvoering, voor lussen, tijdens lussen, enzovoort) en het patroon voor de kwantumspecifieke herhalingsbewerking.

- [Testen en fouten opsporen](xref:microsoft.quantum.guide.testingdebugging): hierin wordt een aantal technieken uitgelegd om ervoor te zorgen dat uw code doet wat die moet doen. 
    Als gevolg van de algemene matheid van kwantuminformatie, kunnen er voor het opsporen van fouten in een kwantumprogramma gespecialiseerde technieken nodig zijn. 
    Gelukkig ondersteunt Q# veel van de klassieke foutopsporingstechnieken waarmee programmeurs bekend zijn, evenals technieken die specifiek zijn voor kwantum. Deze omvatting het maken/uitvoeren van eenheidstests in Q#, het insluiten van *asserties* voor waarden en waarschijnlijkheden in uw code en de `Dump`-functies die de status van de doelmachine uitvoeren. 
    De laatste kunnen worden gebruikt in onze volledige simulator om fouten in bepaalde berekeningen op te sporen door kwantumlimieten te introduceren (bijvoorbeeld de "no-cloning theorem").

### <a name="quantum-simulators-and-resource-estimators"></a>Kwantumsimulators en resourceschattingen

- [Kwantumsimulators en hosttoepassingen](xref:microsoft.quantum.machines): een overzicht van de verschillende beschikbare simulators, evenals het algemene uitvoeringsmodel tussen het hostprogramma en de doelmachines.

- [Volledige statussimulator](xref:microsoft.quantum.machines.full-state-simulator): de doelcomputer die de volledige kwantumstatus simuleert. Handig voor het volledig uitvoeren of debuggen van kleinere programma's (minder dan een paar dozijn qubits)

- [Resoureschattingen](xref:microsoft.quantum.machines.resources-estimator): maakt een schatting van het aantal benodigde resources om een bepaald exemplaar uit te voeren van een Q#-bewerking in een kwantumcomputer.

- [Traceersimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro): voert een kwantumprogramma uit zonder de toestand van een kwantumcomputer daadwerkelijk te simuleren en kan daarom kwantumprogramma's simuleren die duizenden qubits gebruiken. Handig om klassieke code binnen een kwantumprogramma te debuggen en om in te schatten hoeveel resources zijn vereist.

- [Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator): een kwantumsimulator voor speciale doeleinden die kan worden gebruikt met miljoenen qubits, maar alleen voor programma's met een beperkte set kwantumbewerkingen (met name X, CNOT en multi-controlled X).

### <a name="quick-reference-pages"></a>Snelzoekpagina's

- [IQ# Magic-opdrachten](xref:microsoft.quantum.guide.quickref.iqsharp): Snelzoekpagina's voor IQ# Magic-opdrachten binnen Q# Jupyter Notebooks.
