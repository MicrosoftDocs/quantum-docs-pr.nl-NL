---
title: 'Q # basis principes'
description: 'Basis concepten van Q #'
author: gillenhaalb
ms.author: a-gibec@microsoft.com
ms.date: 02/28/2020
ms.topic: article
uid: microsoft.quantum.guide.basics
ms.openlocfilehash: e77b52d1a6eb7e2f62ab12dedd75d00ac8fec4be
ms.sourcegitcommit: a35498492044be4018b4d1b3b611d70a20e77ecc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2020
ms.locfileid: "84327319"
---
# <a name="q-basics"></a>Q # basis principes

In deze sectie wordt een korte inleiding tot de basis bouwstenen van Q # weer gegeven.

Voor een snel overzicht van wat Q # is en waar het past in als een fundamenteel onderdeel van de Quantum Development Kit, kunt u zien [wat q #? is](xref:microsoft.quantum.overview.q-sharp). 

## <a name="what-is-a-quantum-program"></a>Wat is een Quantum programma?

Vanuit een technisch perspectief kan een Quantum programma worden gezien als een bepaalde set klassieke subroutines die, wanneer aangeroepen, bepaalde bewerkingen op een Quantum systeem uitvoeren.
Een belang rijk gevolg van deze weer gave is dat een programma dat is geschreven in Q # niet rechtstreeks model qubits is, maar in plaats daarvan beschrijft hoe een klassieke beheer computer communiceert met deze qubits.
Standaard worden met Q # geen Quantum Staten of andere eigenschappen van Quantum mechanismen rechtstreeks gedefinieerd.
Bekijk bijvoorbeeld de status $ \ket{+} = \left (\ket {0} + \ket {1} \right)/\sqrt {2} $ die wordt besproken in de hand leiding over de [quantum computing-concepten](xref:microsoft.quantum.concepts.intro) .
Als u deze status wilt voorbereiden in Q #, gebruiken we de feiten die de qubits zijn geïnitialiseerd in de $ \ket {0} $-status en dat $ \ket{+} = H\ket {0} $, waarbij $H $ de Hadamard-trans formatie is, geïmplementeerd door de [ `H` Operation] (] (XREF: micro soft. Quantum. intrinsiek. H):

```qsharp
using (qubit = Qubit()) {
    // At this point, qubit is in the state |0⟩.
    H(qubit);
    // We've now applied H, such that our qubit is in H|0⟩ = |+⟩, as we wanted.
}
```

## <a name="quantum-states-in-q"></a>Quantum Staten in Q #

Het is belang rijk dat u bij het schrijven van het bovenstaande programma niet expliciet naar de status van Q # verwijst, maar in plaats daarvan hebt aangegeven hoe de status door ons programma is *getransformeerd* .
Op deze manier kunnen we volledig neutraal over wat een Quantum staat, *zelfs op elke* doel computer, die verschillende interpretaties kan hebben, afhankelijk van de computer. 

Een Q #-programma heeft geen mogelijkheid om introspect te gaan in de status van een Qubit.
Een programma kan in plaats daarvan bewerkingen aanroepen zoals [`Measure`](xref:microsoft.quantum.intrinsic.measure) om informatie van een Qubit te leren en om bewerkingen zoals [`X`](xref:microsoft.quantum.intrinsic.x) en [`H`](xref:microsoft.quantum.intrinsic.h) te kunnen aanroepen om te reageren op de status van een Qubit.
Wat deze bewerkingen eigenlijk *doen* , worden alleen concreet gemaakt door de doel computer die we gebruiken om het specifieke Q #-programma uit te voeren.
Als bijvoorbeeld het programma wordt uitgevoerd op onze [volle Simulator](xref:microsoft.quantum.machines.full-state-simulator), voert de Simulator de bijbehorende wiskundige bewerkingen uit op het gesimuleerde Quantum systeem.
Maar in de toekomst kijken, wanneer de doel computer een echte quantum computer is, leidt het aanroepen van dergelijke bewerkingen in Q # ervoor dat de quantum computer de overeenkomstige *real* -bewerkingen op het *echte* Quantum systeem kan uitvoeren (bijvoorbeeld nauw keurig verlopen Laser pulsen).

Een Q #-programma recombineert deze bewerkingen, zoals gedefinieerd door een doel machine, om nieuwe bewerkingen op een hoger niveau te maken voor een snelle Quantum berekening.
Op deze manier maakt Q # het eenvoudig om de logische en hybride Quantum-algoritmen van de logica te expresseren, en is deze ook algemeen wat betreft de structuur van een doel machine of Simulator.

## <a name="q-operations-and-functions"></a>Q # bewerkingen en functies

In concrete zin is een Q #-programma bestaande uit *bewerkingen*, *functies*en eventuele door de gebruiker gedefinieerde typen. 

Bewerkingen worden gebruikt om de trans formaties van Quantum systemen te beschrijven en zijn de meest elementaire bouw stenen van Q #-Program ma's. Elke bewerking die in Q # is gedefinieerd, kan vervolgens een wille keurig aantal andere bewerkingen aanroepen.

In tegens telling tot bewerkingen worden functies gebruikt om louter *deterministisch* klassiek gedrag te beschrijven en geen effect te hebben naast het uitvoeren van klassieke waarden. Stel bijvoorbeeld dat we de qubits aan het einde van een programma willen meten en de meet resultaten aan een matrix moeten toevoegen.
In dit geval `Measure` is een *bewerking* waarmee de doel computer een meting kan uitvoeren op de (reële of gesimuleerde) qubits, en het klassieke proces van het toevoegen van de geretourneerde resultaten aan een matrix wordt verwerkt door- *functies*.

Bewerkingen en functies worden samen aangeduid als *callables*, en de onderliggende structuur en het gedrag ervan worden geïntroduceerd op de [bewerkingen en functies op de pagina Q #](xref:microsoft.quantum.guide.operationsfunctions) .


## <a name="q-syntax-overview"></a>Q # syntaxis overzicht

De syntaxis van een taal beschrijft de verschillende combi Naties van symbolen die een syntactisch corrigerend programma vormen.
In Q # kunnen we de elementen van de syntaxis in drie verschillende groepen classificeren: typen, expressies en instructies.

### <a name="types"></a>Typen
Q # is een sterk getypeerde taal, zodat het gebruik van typen zorgvuldig kan helpen de compiler sterke garanties te bieden met Q #-Program ma's tijdens het compileren.
Naast de standaard en Quantum specifieke ingebouwde primitieve typen (zoals `Int` ,, `Bool` `Qubit` en `Result` ), biedt Q # ondersteuning voor door de gebruiker gedefinieerde typen.
De verschillende primitieve typen van Q # worden beschreven op de pagina [typen op Q #](xref:microsoft.quantum.guide.types) , samen met details over matrix-en tuple-typen, en het definiëren van nieuwe typen in een Q #-bestand.

### <a name="expressions"></a>Expressies
Een expressie in een programmeer taal is een combi natie van een of meer constanten, variabelen, Opera tors en functies die door de programmeer taal worden geïnterpreteerd en geëvalueerd naar een specifieke waarde.
In de meeste gevallen kunt u voor elk type in een taal *letterlijke* expressies of symbolen van dat type maken die zijn gebonden aan een waarde van dat type.
`5`Is bijvoorbeeld een `Int` letterlijke waarde (ook wel een expressie van `Int` het type), en als het symbool `count` is gebonden aan de integerwaarde `5` , `count` is ook een expressie met gehele getallen.

Daarnaast kan een expressie bestaan uit andere expressies die worden gecombineerd met bepaalde Opera tors.
Een voor beeld van een `Int` expressie die wordt geëvalueerd naar `5` is `2+3` .

De mogelijke expressies van typen in Q # en de compatibele Opera tors die kunnen worden gebruikt om ze te maken, worden beschreven op de pagina [type-expressies in Q #](xref:microsoft.quantum.guide.expressions) . 

### <a name="statements"></a>Instructies 
Een instructie is een syntaxis eenheid van een verplichte programmeer taal die een aantal actie bevat die moet worden uitgevoerd. Met de instructies in deze instructies worden geen resultaten geretourneerd en alleen voor hun neven effecten uitgevoerd, terwijl expressies altijd een resultaat retour neren en vaak geen neven effecten hebben.
Dit onderscheid wordt vaak geconstateerd in de formule: er wordt een expressie geëvalueerd, terwijl een instructie wordt uitgevoerd.

Een eenvoudig voor beeld van een instructie in Q # is het toewijzen van een symbool aan een expressie:
```qsharp
let count = 5;
```

Een iets interessantere voor beeld is de `for` instructie die iteratie ondersteunt en een *instructie blok*bevat.
Stel dat `qubits` het symbool is gebonden aan een REGI ster van qubits (technisch type `Qubit[]` , dat wil zeggen een matrix met `Qubit` typen). Kies
```qsharp
for (qubit in qubits) {
    H(qubit);
}
```
is een instructie waarmee elke qubit in de kassa wordt herhaald, waarbij de `H` bewerking op elk wordt uitgevoerd. Houd er rekening mee dat `H(qubit);` er ook een instructie is.

Een aanroep expressie van het type `Unit` (die callables die geen informatie retour neren) kan ook worden gebruikt als een instructie.
Dit wordt voornamelijk gebruikt wanneer u bewerkingen aanroept voor qubits die resulteren in het `Unit` doel van de instructie om de impliciete Quantum status te wijzigen.
Voor expressie-evaluatie-instructies is een afsluit punt komma vereist.

Bijna elk aspect van een Q #-programma is gebouwd met behulp van instructies, zodat niet alle informatie die betrekking heeft op de pagina kan worden opgenomen.
De lexicale structuur en-opmaak worden echter beschreven op de pagina [q # bestands structuur](xref:microsoft.quantum.guide.filestructure) , de toewijzing van het symbool en het bereik bij [variabelen in q #](xref:microsoft.quantum.guide.variables), en controle stroom lussen zoals `for` bij [controle stroom in q #](xref:microsoft.quantum.guide.controlflow).

## <a name="next-steps"></a>Volgende stappen
In de rest van deze hand leiding wordt uitgelegd hoe u Q # kunt gebruiken om complexe Quantum Programma's te maken met behulp van de basis bouwstenen van bewerkingen, functies en typen.

Om aan de slag te gaan, kunt u beginnen met het leren [van typen in Q #](xref:microsoft.quantum.guide.types).

Als u meer wilt weten over de stichtingen en motivatie achter Q #, Lees [dan waarom hebben we q # nodig?](https://devblogs.microsoft.com/qsharp/why-do-we-need-q/).
