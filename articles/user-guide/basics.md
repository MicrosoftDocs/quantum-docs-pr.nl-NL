---
title: Q# Bewerkingen
description: Basis concepten van Q#
author: gillenhaalb
ms.author: a-gibec
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 86f6538cf383f4e7c14255b38cfb1c141c8f991b
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835516"
---
# <a name="no-locq-basics"></a>Q# Bewerkingen

Dit artikel bevat een korte inleiding tot de basis bouwstenen van Q# .

Q#Zie [Wat is Q# ?](xref:microsoft.quantum.overview.q-sharp)voor een overzicht van wat is en waar het past in als een fundamenteel onderdeel van de Quantum Development Kit. 

## <a name="what-is-a-quantum-program"></a>Wat is een Quantum programma?

Vanuit een technisch perspectief is een Quantum programma een bepaalde set klassieke subroutines die, wanneer aangeroepen, bepaalde bewerkingen op een Quantum systeem uitvoeren.
Een belang rijk gevolg van deze weer gave is dat een Q# programma qubits zelf niet rechtstreeks modelt, maar in plaats daarvan wordt beschreven hoe een klassieke, beheerde computer communiceert met die qubits.
Standaard worden door het ontwerp Q# geen Quantum Staten of andere eigenschappen van Quantum mechanismen gedefinieerd.
Bekijk bijvoorbeeld de status $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ die wordt besproken in de hand leiding over de [quantum computing-concepten](xref:microsoft.quantum.concepts.intro) .
Als u deze status wilt voorbereiden in Q# , begint u met de feiten die de qubits hebben geïnitialiseerd in de $ \ket {0} $-status en die $ \ket{+} = H\ket {0} $, waarbij $H $ de [Hadamard-trans formatie](xref:microsoft.quantum.glossary#hadamard)is, geïmplementeerd door de [ `H` bewerking](xref:microsoft.quantum.intrinsic.h). De Basic Q# -code voor het initialiseren en transformeren van een Qubit. dit ziet er als volgt uit:

```qsharp
using (qubit = Qubit()) {
    // At this point, the qubit is in the state |0⟩.
    H(qubit);
    // H is now applied, such that the qubit is in H|0⟩ = |+⟩, as desired.
}
```
Zie [werken met qubits](xref:microsoft.quantum.guide.qubits)voor meer informatie over het initialiseren van, of het *toewijzen*van qubits.

## <a name="quantum-states-in-no-locq"></a>Quantum provincies in Q#

Belang rijk: in het vorige programma wordt niet expliciet naar de status verwezen, Q# maar wordt beschreven hoe ons programma de status heeft *getransformeerd* .
Met deze methode kunt u volledig neutraal over wat een Quantum status *heeft* , zelfs op elke doel computer, die verschillende interpretaties kan hebben, afhankelijk van de computer. 

Een Q# programma kan niet introspect in de status van een Qubit.
Een programma kan in plaats daarvan bewerkingen aanroepen zoals [`Measure`](xref:microsoft.quantum.intrinsic.measure) om informatie van een Qubit te leren en om bewerkingen zoals [`X`](xref:microsoft.quantum.intrinsic.x) en [`H`](xref:microsoft.quantum.intrinsic.h) te kunnen aanroepen om te reageren op de status van een Qubit.
Wat deze bewerkingen eigenlijk *doen* , worden alleen concreet gemaakt door de doel computer die wordt gebruikt om het desbetreffende programma uit te voeren Q# .
Als bijvoorbeeld het programma wordt uitgevoerd op onze [volle Simulator](xref:microsoft.quantum.machines.full-state-simulator), voert de Simulator de bijbehorende wiskundige bewerkingen uit op het gesimuleerde Quantum systeem.
Maar in de toekomst kijken we, wanneer de doel computer een echte quantum computer is, dergelijke bewerkingen aanroepen in Q# de quantum computer om de overeenkomstige *real* -bewerkingen uit te voeren op het *echte* Quantum systeem, bijvoorbeeld nauw keurig verlopen Laser pulsen).

Een Q# programma recombineert deze bewerkingen, zoals gedefinieerd door een doel machine, om nieuwe bewerkingen op een hoger niveau te maken voor een snelle Quantum berekening.
Op deze manier kunt u Q# eenvoudig de logische en hybride Quantum-algoritmen van de logica uitdrukken, maar ook algemeen met betrekking tot de structuur van een doel machine of Simulator.

## <a name="no-locq-operations-and-functions"></a>Q# bewerkingen en functies

In concrete Q# zin bestaat een programma uit *bewerkingen*, *functies*en eventuele door de gebruiker gedefinieerde typen. 

Bewerkingen worden gebruikt om de trans formaties van Quantum systemen te beschrijven en zijn de meest fundamentele bouw stenen voor Q# Program ma's. Elke bewerking die is gedefinieerd in Q# kan vervolgens een wille keurig aantal andere bewerkingen aanroepen.

In tegens telling tot bewerkingen worden functies gebruikt om louter *deterministisch* klassiek gedrag te beschrijven en geen effect te hebben naast het uitvoeren van klassieke waarden. Stel bijvoorbeeld dat u de qubits aan het einde van een programma wilt meten en de meet resultaten wilt toevoegen aan een matrix.
In dit geval `Measure` is een *bewerking* waarmee de doel computer een meting kan uitvoeren op de (reële of gesimuleerde) qubits. Terzelfder tijd verwerken *functies* het klassieke proces van het toevoegen van de geretourneerde resultaten aan een matrix.

Samen worden bewerkingen en functies ook wel *callables*genoemd. Hun onderliggende structuur en gedrag worden geïntroduceerd en beschreven in [bewerkingen en functies in Q# ](xref:microsoft.quantum.guide.operationsfunctions).


## <a name="no-locq-syntax-overview"></a>Q# syntaxis overzicht

De syntaxis van een taal beschrijft de verschillende combi Naties van symbolen die een syntactisch corrigerend programma vormen.
In Q# worden syntaxis elementen ingedeeld in drie verschillende groepen: typen, expressies en instructies.

### <a name="types"></a>Typen
Q# is een sterk getypeerde taal, zodat het gebruik van typen zorgvuldig kan bijdragen aan de compiler, waardoor het mogelijk is dat er sterke garanties worden geboden over Q# Program ma's tijdens het compileren.
Naast de standaard en Quantum specifieke ingebouwde primitieve typen, bijvoorbeeld,, `Int` `Bool` `Qubit` en `Result` , Q# biedt ondersteuning voor door de gebruiker gedefinieerde typen.

Q#Zie [typen in Q# ](xref:microsoft.quantum.guide.types)voor beschrijvingen van alle primitieve typen, Details voor matrix-en tuple-typen en stappen voor het definiëren van nieuwe typen in een bestand.

### <a name="expressions"></a>Expressies
Een expressie in een programmeer taal is een combi natie van een of meer constanten, variabelen, Opera tors en functies die door de programmeer taal worden geïnterpreteerd en geëvalueerd naar een specifieke waarde.
In de meeste gevallen kunt u voor elk type in een taal *letterlijke* expressies of symbolen van dat type maken die zijn gebonden aan een waarde van dat type.
`5`Is bijvoorbeeld een `Int` letterlijke waarde (ook wel een expressie van `Int` het type), en als het symbool `count` is gebonden aan de integerwaarde `5` , `count` is ook een expressie met gehele getallen.

Daarnaast kan een expressie bestaan uit andere expressies die worden gecombineerd door bepaalde Opera tors.
Een voor beeld hiervan `Int` is een andere expressie die `5` wordt geëvalueerd naar `2+3` .

Q#Zie [type expressies in Q# ](xref:microsoft.quantum.guide.expressions)voor meer informatie over expressies en compatibele Opera tors in. 

### <a name="statements"></a>Instructies 
Een instructie is een syntaxis eenheid van een verplichte programmeer taal waarin een aantal acties wordt vermeld die moeten worden uitgevoerd. Met de instructies in deze instructies worden geen resultaten geretourneerd en alleen voor hun neven effecten uitgevoerd. Expressies retour neren echter altijd een resultaat en bevatten vaak geen neven effecten. Kortom, Q# instructies worden uitgevoerd, terwijl expressies worden geëvalueerd.

Een eenvoudig voor beeld van een instructie in Q# is het toewijzen van een symbool aan een expressie:
```qsharp
let count = 5;
```

Een interessantere voor beeld is de `for` instructie die iteratie ondersteunt en een *instructie blok*bevat.
Stel dat `qubits` het symbool is gebonden aan een REGI ster van qubits (technisch type `Qubit[]` of een matrix van `Qubit` typen). Kies
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
is een instructie waarmee elke qubit in de kassa wordt herhaald, waarbij de `H` bewerking op elk afzonderlijk wordt uitgevoerd. Houd er rekening mee dat `H(qubit);` er ook een instructie is.

U kunt elke aanroep expressie van het type `Unit` (een `Unit` type geeft geen informatie) als een instructie gebruiken.
Dit type expressie is handig bij het aanroepen van bewerkingen op qubits die worden geretourneerd `Unit` , omdat het doel van de instructie is om de impliciete Quantum status te wijzigen.
Voor expressie-evaluatie-instructies is een afsluit punt komma vereist.

U gebruikt-instructies om bijna elk aspect van een Q# programma te bouwen, en er kan geen enkele pagina alle informatie bevatten.
Zie voor meer informatie over de lexicale structuur en opmaak, [ Q# bestands structuur](xref:microsoft.quantum.guide.filestructure); voor de toewijzing van een symbool binding en het bereik, Zie [variabelen in Q# ](xref:microsoft.quantum.guide.variables); en voor controle stroom lussen zoals `for` , Zie [controle stroom in Q# ](xref:microsoft.quantum.guide.controlflow).

## <a name="next-steps"></a>Volgende stappen

Begin met het leren van [typen in Q# ](xref:microsoft.quantum.guide.types).

Voor meer achtergrond informatie over de stichtingen en motivatie achter Q# , Zie [Waarom zijn we nodig Q# ?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).
