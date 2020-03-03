---
title: Kwantumontwikkelingstechnieken
description: Leer de basisbeginselen van Q#-programmeren, leer werken met bewerkingen, functies, variabelen en qubits en maak een eenvoudig kwantumprogramma.
keywords: Voeg geen sleutelwoorden toe en bewerk ze niet zonder overleg met uw SEO-expert.
author: QuantumWriter
ms.author: MSFT-alias-person-or-DL
ms.date: 9/20/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.techniques.intro
ms.openlocfilehash: e5b7fbde18afbc0333d89f70c5e4596848e30f4f
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77907712"
---
# <a name="quantum-development-techniques"></a>Kwantumontwikkelingstechnieken

In dit gedeelte van de documentatie vindt u meer informatie over de basisconcepten voor het maken van kwantumprogramma's in Q# en voor interactie met deze programma's vanuit klassieke toepassingen.
We gaan uit van *basiskennis* van concepten van kwantumcomputing, zoals die zijn beschreven in [Concepten van kwantumcomputing](xref:microsoft.quantum.concepts.intro), maar u hoeft geen expert in kwantumcomputing te zijn om informatie uit deze gedeelten te halen.

De inhoud is als volgt.

- [Q#-programmaoverzicht](xref:microsoft.quantum.techniques.file-structure) biedt een overzicht van het doel en de functionaliteit van de Q#-programmeertaal. 
    In het bijzonder wordt uitgelegd hoe Q# *geen* taal is om alleen maar kwantummechanica uit te leggen, hoewel die functionaliteit natuurlijk wel wordt aangeboden door onze volledige simulator. 
    'In plaats daarvan is Q# ontworpen met het oog op de toekomst en in de programma's wordt beschreven hoe een klassieke controlecomputer *communiceert* met qubits. 

- [Bewerkingen en functies](xref:microsoft.quantum.techniques.opsandfunctions) beschrijven de twee aanroepbare typen Q#-taal: *bewerkingen*, waaronder acties voor qubits- en kwantumsystemen, en *functies*, die alleen werken met klassieke informatie. 
    Als zowel de klassieke als kwantuminformatie niet tegelijk werken, is kwantumcomputing niet bereikbaar. 
    In dit gedeelte wordt beschreven hoe u deze aanroepen definieert en gebruikt binnen de controlestroom van een Q#-programma.

- [Met lokale variabelen](xref:microsoft.quantum.techniques.local-variables) wordt de rol van variabelen binnen Q#-programma's beschreven en hoe u er effectief gebruik van maakt. 
    In het bijzonder leert u het verschil tussen onveranderlijke en veranderlijke variabelen en hoe u deze toewijst of opnieuw toewijst.

- In [Werken met qubits](xref:microsoft.quantum.techniques.qubits) worden de functies van Q# uitgelegd die u kunt gebruiken om te werken met afzonderlijke qubits en systemen van qubits. 
    In het bijzonder de functies omtrent hun toewijzing, bewerkingen en uiteindelijk hun metingen. 
    Bovendien leert u een aantal nuttige controlestroomtechnieken aan.

- In [Alles samenbrengen](xref:microsoft.quantum.techniques.puttingittogether) maakt u gebruik van de technieken uit de bovenstaande gedeeltes om een programma te maken die **kwantumteleportatie** uitvoer met twee klassieke bits om de volledige status van een qubit naar de ander te 'teleporteren'.

- In [Verder](xref:microsoft.quantum.techniques.going-further) worden geavanceerde technieken geïntroduceerd die mogelijk nuttig zijn wanneer u zich richt op complexere kwantumcomputing. 
    In het bijzonder wordt het gebruik van *geparameteriseerde bewerkingen* en functies op basis van typen in Q# beschreven, waarmee een hogere controlestroom mogelijk is door een agnostische kijk op de specifieke typen invoer/uitvoer, even als het *lenen* van qubits. 
    Het laatste verschilt van de basisqubittoewijzing in dat een Q#-bewerking gebruik kan maken van 'vervuilde' qubits, qubits die niet zijn geïnitialiseerd in een bekende status, om te helpen bij berekeningen.

- In [Testen en fouten opsporen](xref:microsoft.quantum.techniques.testing-and-debugging) wordt een aantal technieken uitgelegd om ervoor te zorgen dat uw code doet wat die moet doen. 
    Als gevolg van de algemene matheid van kwantuminformatie, kunnen er voor het opsporen van fouten in een kwantumprogramma gespecialiseerde technieken nodig zijn. 
    Gelukkig ondersteunt Q# veel van de klassieke foutopsporingstechnieken waarmee programmeurs bekend zijn, evenals technieken die specifiek zijn voor kwantum. Deze omvatting het maken/uitvoeren van eenheidstests in Q#, het insluiten van *asserties* voor waarden en waarschijnlijkheden in uw code en de `Dump`-functies die de status van de doelmachine uitvoeren. 
    De laatste kunnen worden gebruikt in onze volledige simulator om fouten in bepaalde berekeningen op te sporen door kwantumlimieten te introduceren (bijvoorbeeld de "no-cloning theorem").


![Kwantum](~/media/mobius_strip_preview.png)
